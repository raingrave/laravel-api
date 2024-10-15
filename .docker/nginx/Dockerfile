FROM nginx:1.24.0-alpine

RUN apk update && apk upgrade

RUN apk add bash

RUN rm /etc/nginx/conf.d/default.conf
COPY ./sites/* /etc/nginx/conf.d

WORKDIR ./var/www
