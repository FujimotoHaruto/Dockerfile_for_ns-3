FROM ubuntu:20.04

RUN apt update \
&& apt-get upgrade -y \
&& apt install -y \
git \
python \
python3 \
gcc \
g++
WORKDIR /home/work
RUN git clone https://gitlab.com/nsnam/ns-3-allinone.git
WORKDIR ns-3-allinone
RUN python3 download.py -n ns-3.29
WORKDIR ns-3.27
RUN ./waf configure --build-profile=optimized --enable-examples --enable-tests --out=build/debug \
&& ./waf configure --build-profile=debug --out=build/debug \
&& ./waf build
