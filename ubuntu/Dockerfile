#
# Oranchelo-tools for Ubuntu and DEB-based
#
FROM ubuntu:latest
MAINTAINER Miguel Hernandez "michelangelo93@gmail.com"

# Configuring system
RUN apt -y update
RUN apt -y install sudo git gcc curl dh-make devscripts dput
RUN useradd -m orange
RUN usermod -aG sudo migue

# Configuring oranchelo-tools
RUN git clone https://github.com/Madh93/oranchelo-tools /home/orange/oranchelo-tools
RUN make -C /home/orange/oranchelo-tools
RUN make install -C /home/orange/oranchelo-tools

WORKDIR /home/orange
