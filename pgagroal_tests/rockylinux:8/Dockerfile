FROM rockylinux/rockylinux:8

RUN dnf -y update && dnf -y install gcc-toolset-11

RUN dnf -y install git cmake make libev libev-devel openssl openssl-devel systemd systemd-devel python3-docutils libatomic

# Install cJson
RUN git clone https://github.com/DaveGamble/cJSON.git /tmp/cJSON

RUN cd /tmp/cJSON && make && make install && ldconfig && rm -rf /tmp/cJSON

CMD ["/bin/sh"]