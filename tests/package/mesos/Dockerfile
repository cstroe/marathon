FROM marathon-package-test:debian9

COPY zookeeper.service /lib/systemd/system

RUN apt-get -o Acquire::Check-Valid-Until=false update && \
  apt-get install -y curl zookeeper && \
  systemctl enable zookeeper && \
  systemctl enable mesos-master

