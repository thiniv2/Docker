FROM ubuntu:18.04

MAINTAINER thinguye

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y wget vim git emacs

WORKDIR /tmp
RUN wget https://dl.google.com/go/go1.11.linux-amd64.tar.gz

RUN tar -xvf go1.11.linux-amd64.tar.gz && mv go /usr/local

WORKDIR /root

RUN sed -i -e '9s/^/tty -s \&\&\ /' .profile
RUN echo "PATH=$PATH:/usr/local/go/bin" >> .profile
RUN echo "PATH=$PATH:/usr/local/go/bin" >> .bashrc
RUN . ~/.profile
