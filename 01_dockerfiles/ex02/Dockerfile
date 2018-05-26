FROM ruby
MAINTAINER Olena Bondarenko <olbondar@student.unit.ua>

EXPOSE 3000

RUN apt-get update -y && apt-get upgrade -y && gem install rails && apt-get install nodejs -y

ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install && rails db:migrate && rails db:seed

# docker build --tag=ruby .
# docker run -it --rm ruby