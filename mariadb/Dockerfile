FROM mariadb:10.0
MAINTAINER HIGUCHI Daisuke <d-higuchi@creationline.com>

RUN echo 'Asia/Tokyo' > /etc/timezone \
	&& dpkg-reconfigure -f noninteractive tzdata
