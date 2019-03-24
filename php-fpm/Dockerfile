FROM php:7-fpm-alpine
RUN apk update \
	&& apk add --no-cache \
	  coreutils \
	  freetype-dev \
	  libjpeg-turbo-dev \
	  libltdl \
	  libmcrypt-dev \
	  libpng-dev \
	&& docker-php-ext-install mysqli \
	&& docker-php-ext-configure gd --with-jpeg-dir=/usr/include/ \
	&& docker-php-ext-install gd \
	&& rm -rf /var/cache/apk/*