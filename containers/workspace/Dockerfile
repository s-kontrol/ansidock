FROM fedora:latest

# Create a non-root user with a specified UID and GID
RUN dnf update -y
RUN dnf install wget git vim curl sudo -y && dnf clean all

RUN useradd -ms /bin/bash ansible
RUN echo "ansible ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/ansible

# Set the user as the default user for the container
USER ansible

CMD ["sleep", "infinity"]
