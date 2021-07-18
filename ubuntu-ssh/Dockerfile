FROM ubuntu:latest
LABEL maintainer="Muhammad Tabish" email="mtabishkhanday@gmail.com"
RUN apt update && apt install openssh-server sudo -y
RUN useradd -rm -d /home/devops -s /bin/bash -g root -G sudo -u 1000 devops
RUN  echo 'devops:password' | chpasswd
RUN echo "devops ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
RUN service ssh start
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]
