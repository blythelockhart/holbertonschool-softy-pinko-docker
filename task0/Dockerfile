# Use the latest official Ubuntu as the base image
FROM ubuntu:latest

# Update the APT package repository
RUN apt-get update

# Upgrade currently installed software through APT and automatically answer yes to prompts
RUN apt-get upgrade -y

# Run a command that echoes "Hello, World!" when the container starts
CMD ["/bin/bash", "-c", "echo 'Hello, World!'"]