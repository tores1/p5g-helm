FROM ubuntu:18.04

RUN apt update && apt install software-properties-common -y && add-apt-repository ppa:open5gs/latest \
 && apt update && apt install open5gs iproute2 iptables iputils-ping -y
