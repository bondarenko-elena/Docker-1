FROM shawn/ubuntu-precise-i386
MAINTAINER Olena Bondarenko <olbondar@student.unit.ua>

RUN apt-get -qqy update && \
	apt-get -qqy install \
	build-essential \
	valgrind

WORKDIR /app
CMD /bin/bas

# docker build --tag=valgrind .
# docker run -it --rm valgrind