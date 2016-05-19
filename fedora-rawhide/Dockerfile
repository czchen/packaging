# https://fedoraproject.org/wiki/How_to_create_an_RPM_package

FROM fedora:latest

MAINTAINER ChangZhuo Chen (陳昌倬) <czchen@czchen.org>

RUN dnf install --assumeyes \
        @development-tools \
        fedora-packager \
        git \
        rpmdevtools \
    echo 'installed required packages'

RUN /usr/sbin/useradd makerpm && \
    usermod -a -G mock makerpm && \
    su makerpm -c rpmdev-setuptree
