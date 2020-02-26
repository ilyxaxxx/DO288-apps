FROM registry.access.redhat.com/ubi8:8.0

RUN yum install -y --disableplugin=subscription-manager --nodocs httpd\
  && yum clean all

ADD index.html /var/www/html

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
chmod -R g=u /var/log/httpd /var/run/httpd
RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf  
EXPOSE 8080
USER 1001

CMD usr/sbin/httpd -D FOREGROUND

