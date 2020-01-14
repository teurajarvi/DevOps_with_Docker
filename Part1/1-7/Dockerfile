FROM ubuntu:16.04

WORKDIR /mydir
RUN apt-get update && apt-get install -y curl
COPY echo_website.sh .

CMD ["./echo_website.sh"]
