# Set the base image to Ubuntu
FROM ubuntu:18.04

# File Author / Maintainer
MAINTAINER Muhammad Tabish <mtabishkhanday@gmail.com>

#To install without any interactive dialogue
ENV DEBIAN_FRONTEND=noninteractive

# Update and upgrade the repository
RUN apt-get update && apt-get -y upgrade

# Install necessary tools
RUN apt-get install -y vim wget  net-tools curl

# Download and Install Nginx
RUN apt-get install -y apache2 

# Download and Install Php
RUN apt install -y php

# Index Page
RUN rm -rvf /var/www/html/*
COPY index.php /var/www/html/

# Set an Entrypoint to start the apache2 service (Prod Env)
ENTRYPOINT ["/usr/sbin/apachectl"]
CMD ["-D", "FOREGROUND"]

# Expose port
EXPOSE 80
