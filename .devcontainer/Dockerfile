FROM golang:1.14.3-buster

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

RUN apt-get update \
  && apt-get install -y zsh less libpcap-dev net-tools

RUN useradd --create-home --user-group --uid 1000 app
RUN mkdir -p /go/src /original
RUN chown -R app /go/src /original

WORKDIR /go/src

USER app

ENV SHELL=/bin/zsh HOME=/home/app
