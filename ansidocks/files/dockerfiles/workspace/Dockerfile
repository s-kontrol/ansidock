FROM fedora:latest

# Create a non-root user with a specified UID and GID
RUN dnf update -y && \
    dnf install wget git vim curl sudo -y && \
    dnf clean all

RUN useradd -m ansible
RUN usermod -aG wheel ansible
RUN echo "ansible ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/ansible
# Set the user as the default user for the container
RUN mkdir -p /home/ansible/dev/

USER ansible
CMD ["sleep", "infinity"]
