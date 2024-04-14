# Use the Arch Linux base image
FROM archlinux:base

# Update package repositories and install required packages
RUN pacman -Sy --noconfirm && \
    pacman -S ansible --noconfirm && \
    pacman -S python --noconfirm && \
    pacman -S openssh --noconfirm && \
    pacman -S sudo --noconfirm && \
    pacman -S which --noconfirm && \
    pacman -S git --noconfirm && \
    pacman -S vim --noconfirm && \
    pacman -S python-pip --noconfirm && \
    rm -rf /var/cache/pacman/pkg/*

# Set environment variables if needed
ENV SOME_ENV_VAR=value

# Create a user and group if needed (replace with your user/group names and IDs)
RUN groupadd -g 1000 mlem&& \
    useradd -m -u 1000 -g mlem mlem

# Set the working directory
WORKDIR /home/mlem

# Copy your Ansible playbook and files into the container
COPY . .

# Default command to run when the container starts
CMD ["/bin/bash"]
