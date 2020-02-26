FROM registry.access.redhat.com/ubi8:8.0

RUN yum install -y --disableplugin=subscription-manager --nodocs httpd\
  && yum clean all

ADD index.html /var/www/html

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
chmod -R g=u /var/log/httpd /var/run/httpd
  
EXPOSE 8080
USER 1001

CMD usr/sbin/httpd -D FOREGROUND

