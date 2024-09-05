# Dockerfile for book_catalog microservice
# Use a base Python image
FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Copy the requirements file and install dependencies
COPY book_catalog/requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

# Copy the app files
COPY book_catalog/ ./

# Expose the port the app will run on
EXPOSE 8000

# Run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
