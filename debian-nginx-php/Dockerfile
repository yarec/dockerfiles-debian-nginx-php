FROM debian:wheezy
MAINTAINER softidy <rwtest@gmail.com>
RUN apt-get update && apt-get install nginx php5-fpm php5-mysql openssh-server supervisor -y --no-install-recommends
RUN echo 'root:123456' | chpasswd
ADD yii /
ADD nginx.conf /etc/nginx/
ADD supervisord.conf /etc/
VOLUME /var/www
VOLUME /yii
EXPOSE 80 22
CMD ["/usr/bin/supervisord"]
