#
# Oranchelo-tools for Fedora and RPM-based
#
FROM fedora:latest
MAINTAINER Miguel Hernandez "michelangelo93@gmail.com"

# Configuring system
RUN dnf update -y
RUN dnf install -y sudo nano wget git gcc curl fedora-packager fedora-review
RUN useradd -m orange
RUN usermod -aG wheel orange
RUN echo "orange:docker" | chpasswd

# Configuring oranchelo-tools
RUN git clone https://github.com/Madh93/oranchelo-tools /home/orange/oranchelo-tools
RUN make -C /home/orange/oranchelo-tools
RUN make install -C /home/orange/oranchelo-tools

WORKDIR /home/orange
