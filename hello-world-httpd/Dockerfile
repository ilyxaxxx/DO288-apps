FROM registry.access.redhat.com/ubi8:8.0

RUN yum install -y --disableplugin=subscription-manager --nodocs httpd\
  && yum clean all

ADD index.html /var/www/html

RUN rm -rf /run/httpd && mkdir /run/httpd
  
EXPOSE 80
USER root

CMD usr/sbin/httpd -D FOREGROUND

