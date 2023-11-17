FROM ubuntu:20.04

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y git python3 python3-pip
RUN apt-get autoremove -y &&\
    apt-get clean &&\
    rm -rf /usr/local/src/*

WORKDIR /home
