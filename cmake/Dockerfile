FROM ubuntu:22.04
RUN apt update \
&& apt-get upgrade -y \
&& apt install -y \
git \
cmake \
python3 \
gcc \
g++
WORKDIR /home/work
RUN git clone https://gitlab.com/nsnam/ns-3-allinone.git
WORKDIR ns-3-allinone
RUN python3 download.py -n ns-3.41
WORKDIR ns-3.41
RUN ./ns3 configure --build-profile=optimized --enable-examples --enable-tests --out=build/debug \
&& ./ns3 configure --build-profile=debug --out=build/debug \
&& ./ns3 build
