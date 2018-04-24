FROM node:8.11.1-alpine

MAINTAINER Jean-Luc Geering <jeanluc.geering@ufirstgroup.com>

# install bash, su-exec and tini

RUN apk update && apk upgrade && apk add \
  bash \
  git \
  su-exec \
  tini

USER root

WORKDIR "/workdir"

ENV WORKDIR "/workdir"
ENV HOMEDIR "/homedir"

VOLUME ["/workdir", "/homedir"]

COPY entrypoint.sh /

ENTRYPOINT ["/sbin/tini", "--", "/entrypoint.sh"]
CMD ["node"]
