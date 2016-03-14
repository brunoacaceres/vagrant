FROM ubuntu
MAINTAINER Bruno Caceres <brunocaceres@hotmail.com>
RUN cp -f /usr/share/zoneinfo/America/Campo_Grande /etc/localtime
RUN apt-get update
RUN apt-get install -y nginx
ADD default /etc/nginx/sites-enabled/default
RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/srderr /var/log/nginx/error.log
EXPOSE 8080
CMD ["nginx", "-g", "daemon off;"]
