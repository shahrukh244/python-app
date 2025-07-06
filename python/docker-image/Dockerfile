# Use an official Python runtime as a parent image
FROM glb:5000/python:3.9-slim

# Set the working directory in the container
# This is where your Flask application will reside and run from
WORKDIR /app

# Copy requirements.txt from its new location and install dependencies
# We copy it first to leverage Docker's build cache
COPY code/requirements/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire Flask application code into the container's /app directory
# This copies the content of the 'flask-app' directory into /app
COPY code/flask-app/ .

# Expose the port that the Flask application will listen on
EXPOSE 5000

# Define environment variables for Flask (these will be overridden by Kubernetes secrets)
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_RUN_PORT=5000

# Define the command to run the Flask application
CMD ["flask", "run"]

