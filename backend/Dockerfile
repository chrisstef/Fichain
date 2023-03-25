FROM python:3.9-slim-buster

# Install gcc
RUN apt-get update && \
    apt-get install -y gcc

# Set the working directory to /app
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt .

# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the contents of the backend directory into the container
COPY ./backend /app/backend

# Expose port 5000 for the Flask app to listen on
EXPOSE 5000

# Set the command to start the Flask app
CMD ["flask", "run"]
