FROM quay.io/centos/centos:stream9
RUN yum -y update && yum -y install vsftpd && yum clean all



COPY vsftpd.conf.centos9.template /etc/vsftpd/vsftpd.conf

VOLUME /var/ftp/pub

COPY WelcomeToMyFTPServer.txt /var/ftp/pub/WelcomeToMyFTPServer.txt 



EXPOSE 20 21

ENTRYPOINT ["/usr/sbin/vsftpd"]