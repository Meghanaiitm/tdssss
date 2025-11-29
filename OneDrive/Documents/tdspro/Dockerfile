FROM mcr.microsoft.com/playwright/python:v1.44.0-jammy

WORKDIR /app

# Install requirements from nested folder
COPY OneDrive/Documents/tdspro/requirements.txt ./requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy project files from nested folder
COPY OneDrive/Documents/tdspro/ ./

EXPOSE 8000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
