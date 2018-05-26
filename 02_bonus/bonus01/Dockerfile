FROM ubuntu
MAINTAINER Olena Bondarenko <olbondar@student.unit.ua>

RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install curl -y
RUN curl -sL https://deb.nodesource.com/setup_7.x | bash -
RUN apt-get install nodejs -y
RUN apt-get install vim -y
RUN apt-get install git -y

CMD /bin/bash

# docker build --tag=nodejs .
# docker run -it --rm nodejs