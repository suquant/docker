FROM ubuntu:trusty

MAINTAINER Georgiy Kutsurua <g.kutsurua@gmail.com>

RUN echo "deb http://get.docker.io/ubuntu docker main" > /etc/apt/sources.list.d/docker.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9
# install builder, docker, and hook dependencies
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -yq git aufs-tools iptables lxc curl lxc-docker make python

# install all i18n locales
RUN ln -s /usr/share/i18n/SUPPORTED /var/lib/locales/supported.d/all && locale-gen