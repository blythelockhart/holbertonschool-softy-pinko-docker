# Use an official Python runtime as a parent image
FROM python:3.8

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install and upgrade Python3
RUN apt-get install -y && apt-get upgrade python3

# Install Flask using pip3 and Flask-CORS
RUN pip3 install flask
RUN pip3 install flask-cors

# Copy the Python script into the container
COPY api.py /app/api.py

# Make port 5252 available to the world outside this container
EXPOSE 5252

# Run api.py when the container launches
CMD ["python3", "api.py"]
