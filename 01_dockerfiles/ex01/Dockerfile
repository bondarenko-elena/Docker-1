FROM debian
MAINTAINER Olena Bondarenko <olbondar@student.unit.ua>

EXPOSE 9987/udp 30033 10011

RUN apt-get update \
	&& apt-get install wget bzip2 wget ca-certificates -y

WORKDIR /home/teamspeak

RUN wget http://dl.4players.de/ts/releases/3.0.11.1/teamspeak3-server_linux-amd64-3.0.11.1.tar.gz \
	&& tar -xzvf *.tar.gz && rm *.tar.gz

WORKDIR teamspeak3-server_linux-amd64

CMD ["sh", "ts3server_minimal_runscript.sh"]

# docker build --tag=teamspeak .
# docker run -it --rm -p=9987:9987/udp  -p=10011:10011 -p=30033:30033 teamspeak