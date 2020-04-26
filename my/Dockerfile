FROM centos/centos7
RUN yum install -y iputils 
#USER 1001
RUN ping dns -c 10
RUN ping $dns

#RUN while 1; do echo 1; sleep 5; done