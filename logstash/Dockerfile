ARG ELK_VERSION

# logstash docker image
FROM docker.elastic.co/logstash/logstash-oss:${ELK_VERSION}

RUN logstash-plugin install logstash-input-beats
