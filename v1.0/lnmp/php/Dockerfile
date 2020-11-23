FROM centos:centos7
ENV  TIME_ZONE Asia/Shanghai

RUN yum update -y && \
    yum install -y epel-release

RUN yum install -y http://rpms.remirepo.net/enterprise/remi-release-7.rpm && \
    yum install -y yum-utils && \
    yum-config-manager --enable remi-php72 && \
    yum -y update

RUN yum install -y php-fpm php-xml php-cli php-bcmath php-dba php-gd php-intl \
                   php-mbstring php-mysql php-pdo php-soap php-pecl-apcu \
                   php-pecl-imagic php-common php-devel php-mcrypt php-mysqlnd \
                   php-opcache php-pear php-pecl-redis php-pecl-xdebug php-xmlrpc
        

RUN useradd www

RUN yum clean all
RUN mkdir /run/php-fpm && chown -R www. /run/php-fpm

CMD php-fpm
