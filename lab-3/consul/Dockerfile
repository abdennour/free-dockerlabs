FROM ubuntu:16.04
LABEL maintainer="mail@abdennoor.com"

ENV REFRESHED_AT 2019-02-14

RUN apt-get -qqy update
RUN apt-get -qqy install curl unzip
ADD https://releases.hashicorp.com/consul/0.6.4/consul_0.6.4_linux_amd64.zip /tmp/consul.zip
RUN cd /usr/sbin; unzip /tmp/consul.zip; chmod +x /usr/sbin/consul; rm /tmp/consul.zip
ADD consul.json /config/
EXPOSE 53/udp 8300 8301 8301/udp 8302 8302/udp 8400 8500
VOLUME ["/data"]
ENTRYPOINT [ "/usr/sbin/consul", "agent", "-config-dir=/config" ]
CMD []
