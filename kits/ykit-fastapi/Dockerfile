FROM python:3.10-slim

# Install dependencies
RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*

WORKDIR /app

# Copy application
COPY app.py /app/

# Install dependencies
RUN pip install fastapi uvicorn

# Expose port and set command
EXPOSE 8080
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8080"]
