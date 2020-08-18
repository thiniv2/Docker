FROM ubuntu:18.04

MAINTAINER Thien Nguyen

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y wget default-jdk
RUN mkdir minecraft

WORKDIR minecraft

RUN wget https://launcher.mojang.com/v1/objects/c5f6fb23c3876461d46ec380421e42b289789530/server.jar

RUN echo "eula=true" > eula.txt

EXPOSE 25565

ENTRYPOINT java -Xmx1024M -Xms1024M -jar server.jar nogui
