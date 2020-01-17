FROM ubuntu:18.04

# Install wget and gnupg to be able to add Atom package
RUN apt-get update && apt-get install -y wget gnupg
RUN wget -qO - https://packagecloud.io/AtomEditor/atom/gpgkey | apt-key add -
RUN sh -c 'echo "deb [arch=amd64] https://packagecloud.io/AtomEditor/atom/any/ any main" > /etc/apt/sources.list.d/atom.list'
RUN apt-get update && apt-get install -y vim atom

# Install Node, git and subversion
RUN apt install -y nodejs git subversion

WORKDIR /home

CMD ["/bin/bash"]
