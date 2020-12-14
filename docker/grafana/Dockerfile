FROM ubuntu:latest
WORKDIR /usr/share/grafana
ENV PATH=/usr/share/grafana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin GF_PATHS_CONFIG=/etc/grafana/grafana.ini GF_PATHS_DATA=/var/lib/grafana GF_PATHS_HOME=/usr/share/grafana GF_PATHS_LOGS=/var/log/grafana GF_PATHS_PLUGINS=/var/lib/grafana/plugins GF_PATHS_PROVISIONING=/etc/grafana/provisioning
RUN apt update -y && apt upgrade -y && apt install -y gnupg2 curl
RUN curl https://packages.grafana.com/gpg.key | apt-key add -
RUN apt-get install software-properties-common  -y
RUN add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"
RUN apt -y install grafana
RUN apt-get update;apt-get install -y openjdk-8-jdk-headless wget openssh-server tar vim
EXPOSE 22 3000
ENTRYPOINT ["/etc/init.d/grafana-server"]
CMD ["start"]