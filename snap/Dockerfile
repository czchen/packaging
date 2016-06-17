# https://developer.ubuntu.com/en/snappy/build-apps/

FROM ubuntu:16.04

MAINTAINER ChangZhuo Chen (陳昌倬) <czchen@czchen.org>

RUN apt update \
    && apt install -y \
        git \
        snapcraft \
        vim \
    && apt clean

RUN mkdir -p /home/snap
