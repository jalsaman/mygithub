FROM python:3.9-slim
WORKDIR /app

# Copy requirements first for better layer caching
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application
COPY . .

# Flask default port is 5000, change if your app uses 8000
EXPOSE 8000

# For testing, this is fine
CMD ["python", "app.py"]