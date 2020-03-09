FROM ubuntu:18.04

MAINTAINER Thien Nguyen

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y wget default-jdk
RUN mkdir minecraft

WORKDIR minecraft

RUN wget https://launcher.mojang.com/v1/objects/bb2b6b1aefcd70dfd1892149ac3a215f6c636b07/server.jar

RUN echo "eula=true" > eula.txt

EXPOSE 25565

ENTRYPOINT java -Xmx1024M -Xms1024M -jar server.jar nogui
