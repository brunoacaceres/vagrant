FROM ubuntu
MAINTAINER Bruno Caceres <brunocaceres@hotmail.com>
RUN cp -f /usr/share/zoneinfo/America/Campo_Grande /etc/localtime
RUN apt-get update
RUN apt-get install -y nginx
ADD default /etc/nginx/sites-enabled/default
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
ADD ./ /rails
WORKDIR /rails
EXPOSE 8080
CMD service nginx start
