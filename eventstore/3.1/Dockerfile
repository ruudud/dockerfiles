# EventStore (geteventstore.com)

FROM debian
MAINTAINER Pål Ruud <ruudud@gmail.com>

ENV ES_VERSION 3.1.0

RUN apt-get update \
        && apt-get install -y curl \
        && rm -rf /var/lib/apt/lists/*

RUN curl -L http://download.geteventstore.com/binaries/EventStore-OSS-Ubuntu-v$ES_VERSION.tar.gz | tar xz -C /opt

VOLUME /data/db
VOLUME /data/logs

EXPOSE 2113
EXPOSE 1113

WORKDIR /opt/EventStore-OSS-Ubuntu-v$ES_VERSION

CMD ./run-node.sh --ext-ip=0.0.0.0 \
    --db /data/db --log /data/logs --run-projections=all
