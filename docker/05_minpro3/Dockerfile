FROM quay.io/centos/centos:stream9

RUN dnf -y install httpd mod_wsgi && yum clean all

VOLUME /var/www/html /var/log/httpd

COPY vhost.conf /etc/httpd/conf.d
COPY myapp.wsgi /var/www/html/myapp.wsgi

EXPOSE 80/tcp

ENTRYPOINT ["/usr/sbin/httpd", "-D FOREGROUND"]


