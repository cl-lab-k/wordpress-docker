FROM nginx:1.10
MAINTAINER HIGUCHI Daisuke <d-higuchi@creationline.com>

RUN /bin/rm /etc/nginx/conf.d/default.conf

COPY php-fpm.conf /etc/nginx/conf.d/php-fpm.conf
