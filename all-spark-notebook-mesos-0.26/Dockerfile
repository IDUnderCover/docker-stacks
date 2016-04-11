FROM jupyter/all-spark-notebook

USER root

WORKDIR /
RUN wget http://192.168.1.88:8000/mesos_0.26.0-0.2.145.ubuntu1404_amd64.deb  && \
    wget http://192.168.1.88:8000/sources.list && \
    mv /sources.list /etc/apt/sources.list && \
    apt-get -y update && \
   apt-get -y --force-yes install libsasl2-modules  && \
   apt-get clean && \
   dpkg -i /mesos_0.26.0-0.2.145.ubuntu1404_amd64.deb && \
   rm -f /mesos_0.26.0-0.2.145.ubuntu1404_amd64.deb && \
   rm -rf /var/lib/apt/lists/* 

USER jovyan
WORKDIR /home/jovyan/work
