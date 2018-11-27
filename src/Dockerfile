FROM node:9.11.1-alpine

MAINTAINER Jean-Luc Geering <jeanluc.geering@ufirstgroup.com>

# install bash, su-exec and tini

RUN apk update && apk upgrade && apk add \
  build-base \
  alpine-sdk \
  autoconf \
  automake \
  git \
  nasm \
  libjpeg-turbo \
  libjpeg-turbo-dev \
  libpng \
  libpng-dev \
  libtool \
  libwebp \
  libwebp-dev \
  zlib \
  zlib-dev  

USER root

WORKDIR "/workdir"

ENV WORKDIR "/workdir"
ENV HOMEDIR "/homedir"

VOLUME ["/workdir", "/homedir"]

COPY entrypoint.sh /

ENTRYPOINT ["/sbin/tini", "--", "/entrypoint.sh"]
CMD ["node"]
