FROM debian

MAINTAINER thinguye

ENV TS3SERVER_LICENSE=accept

EXPOSE 9987/udp 10011 30033

WORKDIR /home/teamspeak

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y wget bzip2 && \
	wget https://files.teamspeak-services.com/releases/server/3.10.0/teamspeak3-server_linux_amd64-3.10.0.tar.bz2 && \
	tar xvf *.tar.bz2

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT ./ts3server_minimal_runscript.sh
