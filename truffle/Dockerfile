FROM ubuntu:22.04

WORKDIR /home

RUN apt-get update && apt-get upgrade -y
RUN apt-get install build-essential curl less vim sudo -y
RUN curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
RUN sudo apt-get install nodejs -y
RUN npm install -g truffle --unsafe-perm
