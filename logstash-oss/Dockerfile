FROM docker.elastic.co/logstash/logstash-oss:6.2.3
MAINTAINER Sebastian Vetter <seb@roadsi.de>

RUN logstash-plugin install logstash-output-datadog_logs

RUN rm -rf /usr/share/logstash/pipeline/*.conf
ADD ./pipeline/ /usr/share/logstash/pipeline/
ADD ./patterns/ /usr/share/logstash/patterns/

CMD ["logstash"]
