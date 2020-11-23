FROM centos:centos7

ENV  TIME_ZONE Asia/Shanghai

RUN yum update -y && \
    yum install -y epel-release

RUN yum install -y nginx


RUN yum clean all
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
CMD nginx
