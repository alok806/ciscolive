FROM ubuntu:14.04

MAINTAINER alwadhwa@cisco.com

RUN apt-get update \
 && apt-get -y install pkg-config python python-pip \
 && apt-get clean
WORKDIR /root
COPY . .
RUN easy_install -Z http://10.29.204.37/acicobra-4.1_1j-py2.7.egg \
 && easy_install -Z http://10.29.204.37/acimodel-4.1_1j-py2.7.egg
RUN mkdir -p /root/input \
 && mkdir -p /root/output
VOLUME /root/input /root/output

