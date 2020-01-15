FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl vim
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

EXPOSE 8000
WORKDIR /mydir
COPY ./backend-example-docker-master .
