FROM bruno/ubuntu1404:0.1

#Instalando Nginx
#RUN apt-get update && apt-get install -y nginx && rm -rf /var/lib/apt/lists/* && echo "daemon off;" >> /etc/nginx/nginx.conf
RUN apt-get update && apt-get install -y nginx php5-fpm php-config php5-mysql && rm -rf /var/lib/apt/lists/* && echo "daemon off;" >> /etc/nginx/nginx.conf
# Define working directory.
#WORKDIR /etc/nginx

# Define default command.
#CMD ["nginx"]

# Add custom content
ADD nginx/default /etc/nginx/sites-available/default
#ADD nginx/index.html /var/www/
CMD /etc/init.d/nginx start && php5-fpm -F

# Expose ports.
#EXPOSE 80
