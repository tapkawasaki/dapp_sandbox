FROM ubuntu:22.04

WORKDIR /home

RUN mkdir -p /var/ganache
RUN apt-get update && apt-get upgrade -y
RUN apt-get install build-essential curl less vim sudo -y
RUN curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
RUN sudo apt-get install nodejs -y
RUN npm install -g ganache-cli --unsafe-perm

EXPOSE 8545

ENV DOCKER true
ENV DATADIR /var/ganache
ENV NETWORKID 5777
 
ENTRYPOINT ["sh", "-c", "ganache-cli --db=${DATADIR} --mnemonic=${MNEMONIC} --networkId=${NETWORKID}"]
