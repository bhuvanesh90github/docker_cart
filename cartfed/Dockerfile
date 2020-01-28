# Docker file for cart frontend
#DOCKERCMD command
FROM centos:7
MAINTAINER mohanraz@gmail.com
RUN yum -y update
ADD scripts /opt
RUN chmod +x /opt/*.sh
RUN /opt/installpackages.sh
ADD code /var/www/html
ENV MY_DB_HOST_WRITE=test
EXPOSE 80
CMD ["httpd", "-D", "FOREGROUND"]