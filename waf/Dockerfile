FROM ubuntu:16.04

RUN apt update && apt install -y\
git\
python\
python3\
gcc\
g++
WORKDIR ~/work
RUN git clone https://gitlab.com/nsnam/ns-3-allinone.git
WORKDIR ns-3-allinone
RUN python3 download.py -n ns-3.27
WORKDIR ns-3.27
RUN ./waf configure --build-profile=optimized --enable-examples --enable-tests --out=build/debug\
&& ./waf build

WORKDIR /root
