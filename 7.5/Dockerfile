FROM solr:7.5
MAINTAINER Phuc Do "dduyphuc@gmail.com"

USER root

RUN apt-get update && \
  apt-get -y install sudo \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

RUN usermod -aG sudo solr \
  && echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER solr

# Custom docker-entrypoint.sh
COPY ./scripts/docker-entrypoint.sh /opt/docker-solr/scripts/docker-entrypoint.sh


