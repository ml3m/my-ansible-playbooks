# Use an official Ubuntu image as a base
FROM --platform=linux/amd64 ubuntu:20.04

# Set the working directory
WORKDIR /app

# Install necessary packages
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    ansible

# Copy your files into the container
COPY . . 

# Command to run when starting the container
CMD ["bash"]
