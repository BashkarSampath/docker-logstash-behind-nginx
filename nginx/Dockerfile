FROM nginx:latest

USER root
ENV APP_HOME=/etc/nginx

COPY ./nginx.conf $APP_HOME/nginx.conf
COPY ./404.html $APP_HOME/html/404.html
COPY ./404.html $APP_HOME/html/index.html
COPY ./health.html $APP_HOME/html/health.html

#https://discuss.elastic.co/t/can-you-put-logstash-behind-nginx-proxy/279665/13
RUN mkdir $APP_HOME/streams-enabled
RUN chmod 770 $APP_HOME/

EXPOSE 80 5044
CMD ["nginx", "-g", "daemon off;"]