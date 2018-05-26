FROM debian
MAINTAINER Olena Bondarenko <olbondar@student.unit.ua>

RUN apt-get -y update \
	&& apt-get -y install \
	git \
	golang \
	sqlite3

ENV USER=root GOPATH=/

WORKDIR src/github.com/gogits
RUN git clone --depth=1 -b develop https://github.com/gogits/gogs \
	&& go get -u -tags sqlite github.com/gogits/gogs

WORKDIR gogs
RUN go build -tags sqlite
EXPOSE 3000
ENTRYPOINT ["./gogs", "web"]

# docker build --tag=gogit .
# docker run -it --rm gogit