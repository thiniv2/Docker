FROM ubuntu:18.04

MAINTAINER thinguye

ENV TERM=xterm

RUN apt-get update && apt-get upgrade -y && apt-get install -y xterm wget openssh-server ca-certificates
RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && \ 
	chmod 777 script.deb.sh && bash script.deb.sh && \
	apt-get install -y gitlab-ce

RUN apt-get install -y tzdata

EXPOSE 22 80 443

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && \
			gitlab-ctl reconfigure && \
			tail -f /dev/null
