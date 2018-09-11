ARG ELK_VERSION

# logstash docker image
FROM docker.elastic.co/logstash/logstash-oss:${ELK_VERSION}

#install beats plugin to read file
RUN logstash-plugin install logstash-input-beats
