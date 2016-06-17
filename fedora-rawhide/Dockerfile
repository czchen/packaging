# https://fedoraproject.org/wiki/How_to_create_an_RPM_package

FROM fedora:latest

MAINTAINER ChangZhuo Chen (陳昌倬) <czchen@czchen.org>

RUN dnf update --assumeyes \
    && dnf install --assumeyes \
        @development-tools \
        fedora-packager \
        git \
        rpmdevtools \
        sudo \
        vim \
    && echo 'installed required packages'

ADD makerpm /etc/sudoers.d/makerpm

RUN /usr/sbin/useradd makerpm \
    && usermod -a -G mock makerpm \
    && chmod 0400 /etc/sudoers.d/makerpm \
    && su makerpm -c rpmdev-setuptree \
    && echo 'create account makerpm'

VOLUME ["/host"]
