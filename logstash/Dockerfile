FROM docker.elastic.co/logstash/logstash:8.6.1

USER root
ENV APP_HOME=/usr/share/logstash

COPY ./docker-entrypoint.sh ./
COPY ./config/default-http-pipeline.conf $APP_HOME/config/default-http-pipeline.conf
COPY ./config/pipelines.yml $APP_HOME/config/pipelines.yml

RUN chmod 770 $APP_HOME/
EXPOSE 5200
ENTRYPOINT [ "/bin/bash", "./docker-entrypoint.sh" ]