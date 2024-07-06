# Pull the official base image for Python 3.10
FROM python:3.10-slim

# Set the working directory
WORKDIR /app

# Install Poetry
RUN pip install poetry

# Copy the dependency files
COPY pyproject.toml .
COPY poetry.lock .

# Install dependencies
RUN poetry install

# Copy the application files
COPY . .

# Run prestart script
RUN chmod +x /app/prestart.sh
CMD ["/bin/bash", "-c", "/app/prestart.sh && uvicorn main:app --host 0.0.0.0 --port 8000"]
    