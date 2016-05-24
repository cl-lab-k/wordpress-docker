FROM wordpress:4.5-fpm
MAINTAINER HIGUCHI Daisuke <d-higuchi@creationline.com>

RUN echo 'Asia/Tokyo' > /etc/timezone \
	&& dpkg-reconfigure -f noninteractive tzdata
