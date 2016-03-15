FROM ubuntu
MAINTAINER Bruno Caceres <brunocaceres@hotmail.com>
ENV DEBIAN_FRONTEND noninteractive	 
RUN cp -f /usr/share/zoneinfo/America/Campo_Grande /etc/localtime
RUN apt-get update -qq && apt-get install -y mysql-server-5.5
ADD my.cnf /etc/mysql/conf.d/my.cnf
RUN chmod 664 /etc/mysql/conf.d/my.cnf
ADD run /usr/local/bin/run
VOLUME ["/var/lib/mysql"]
EXPOSE 3006
CMD ["/usr/local/bin/run"]
