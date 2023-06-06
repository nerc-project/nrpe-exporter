FROM debian:latest

RUN apt update \
  && apt upgrade -y \
  && apt install -y prometheus-node-exporter \
  && apt install -y nagios-nrpe-plugin \
  && apt install -y nagios-plugins-contrib

RUN apt install -y wget make gcc procps

RUN mkdir /opt/build && cd /opt/build \
  && wget https://github.com/nagios-plugins/nagios-plugins/releases/download/release-2.4.5/nagios-plugins-2.4.5.tar.gz \
  && tar xvfz nagios-plugins-2.4.5.tar.gz \
  && cd nagios-plugins-2.4.5 \
  && ./configure && make && make install

COPY docker-entrypoint.sh /docker-entrypoint.sh

ENTRYPOINT ["bash", "/docker-entrypoint.sh"]

CMD ["/usr/bin/prometheus-node-exporter"]
