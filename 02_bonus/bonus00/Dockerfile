FROM node
MAINTAINER Olena Bondarenko <olbondar@student.unit.ua>

WORKDIR /var/www/app

RUN apt-get update && apt-get install -y apt-transport-https
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && apt-get install yarn

COPY app /var/www/app

RUN yarn

EXPOSE 3000

CMD ["node","index.js"]

# docker build --tag=yarn .
# docker run -it --rm yarn