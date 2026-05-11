# Use Python 3.9 as the base image
FROM python:3.9

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file and install dependencies
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application source code
COPY . /app/

# Initialize the database with pre-defined posts
RUN python init_db.py

# Expose the application port
EXPOSE 3111

# Run the application when the container starts
CMD ["python", "app.py"]
