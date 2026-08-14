# Use a minimal base image with Python 3.9 installed
FROM python:3.9-slim

# Set the working directory inside the container to /app
WORKDIR /app

# Copy the saved model and preprocessor
COPY best_random_forest_model.joblib best_random_forest_model.joblib
COPY preprocessor.joblib preprocessor.joblib

# Copy the application code
COPY app.py app.py

# Install Python dependencies listed in requirements.txt
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port that the Flask app will run on
EXPOSE 5000

# Define the command to run the Flask application
CMD ["python", "app.py"]
