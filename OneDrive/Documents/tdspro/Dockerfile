# Dockerfile
FROM mcr.microsoft.com/playwright/python:v1.44.0-jammy

WORKDIR /app

# Copy requirements first
COPY OneDrive/Documents/tdspro/requirements.txt ./requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy entire project folder
COPY OneDrive/Documents/tdspro/ ./

# Expose port
EXPOSE 8000

# Run the app
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
