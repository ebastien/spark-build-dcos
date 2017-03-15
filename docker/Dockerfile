FROM mesosphere/spark:1.0.7-2.1.0-hadoop-2.6

RUN apt-get update && \
    apt-get install -y git wget

RUN mkdir -p /tmp/build
WORKDIR /tmp/build
RUN wget https://dl.bintray.com/sbt/native-packages/sbt/0.13.13/sbt-0.13.13.tgz
RUN mkdir -p /opt/sbt
RUN tar xzvf sbt-0.13.13.tgz -C /opt/sbt --strip-components 1
RUN rm -f sbt-0.13.13.tgz
RUN /opt/sbt/bin/sbt -batch
