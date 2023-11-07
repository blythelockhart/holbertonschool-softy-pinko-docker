# Use an official Python runtime as a parent image
FROM python:3

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install Python3 and Python3-pip
RUN apt-get install -y python3 python3-pip

# Upgrade Python3 
RUN apt-get update -y python3 python3-pip

# Install Flask using pip3
RUN pip3 install Flask

# Copy the Python script into the container
COPY api.py /app/api.py

# Make port 5252 available to the world outside this container
EXPOSE 5252

# Run api.py when the container launches
CMD ["python3", "api.py"]
