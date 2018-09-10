FROM debian

MAINTAINER jlasne <jlasne@student.42.fr>

RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install curl -y
RUN apt-get install bzip2 -y


EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 10011
EXPOSE 41144

RUN useradd ts3
WORKDIR /home/t3

RUN curl http://dl.4players.de/ts/releases/3.0.13.6/teamspeak3-server_linux_amd64-3.0.13.6.tar.bz2 > teamspeak-server.tar.bz2
RUN tar -xjvf teamspeak-server.tar.bz2
WORKDIR teamspeak3-server_linux_amd64
COPY ts3.ini /home/t3/teamspeak3-server_linux_amd64/ts3.ini
USER ts3


ENTRYPOINT ["sh","ts3server_minimal_runscript.sh", "inifile=ts3.ini"]