FROM resin/rpi-raspbian:jessie-20161202
# Inspired by the Phusion baseimage
# https://github.com/phusion/baseimage-docker
MAINTAINER Nikolai Schlegel <nikolai.schlegel@gmail.com>

ADD . /bd_build

RUN /bd_build/prepare.sh && \
	/bd_build/system_services.sh && \
	/bd_build/utilities.sh && \
	/bd_build/cleanup.sh

# need to figure out if we really still need this
#RUN	/bd_build/fix_pam_bug.sh

CMD ["/sbin/my_init"]
