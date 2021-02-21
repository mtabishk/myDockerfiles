FROM ubuntu:latest

#To install without any interactive dialogue
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update

RUN apt-get install curl wget gnupg -y

# Add the Spotify APT repository to your systems software repository list
RUN echo "deb http://repository.spotify.com stable non-free" | tee /etc/apt/sources.list.d/spotify.list

# Import the repositorys GPG key
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys  D1742AD60D811D58

# Install Spotify
RUN apt-get update &&  apt-get install spotify-client -y


CMD ["spotify"]
