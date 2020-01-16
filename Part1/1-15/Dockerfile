FROM ubuntu:16.04

RUN apt-get update && apt-get install build-essential manpages-dev -y

WORKDIR /mydir
COPY ./hypotenusa-master .
RUN cc hypotenusa.c -o hypotenusa -lm
CMD ["./hypotenusa"]
