FROM registry.access.redhat.com/ubi8:8.0

RUN yum install -y --disableplugin=subscription-manager --nodocs httpd\
  && yum clean all

ADD index.html /var/www/html

RUN touch /run/httpd.pid \
  && chgrp -R 0 /var/log/httpd /run/httpd.pid \
  && chmod -R g+rwx /var/log/httpd /run/httpd.pid
  
EXPOSE 80
USER root

CMD [“/usr/sbin/httpd”,” -D”,” FOREGROUND”]

