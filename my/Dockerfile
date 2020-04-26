FROM registry.access.redhat.com/ubi8/ubi:8.0
RUN yum install -y iputils
USER 1001
RUN ping dns -c 10
RUN ping $dns -c 10

