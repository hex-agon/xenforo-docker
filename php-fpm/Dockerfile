FROM php:7-fpm-alpine
RUN apk update \
	&& apk add --no-cache \
	  autoconf \
	  coreutils \
	  freetype-dev \
	  libjpeg-turbo-dev \
	  libltdl \
	  gmp-dev \
	  imagemagick-dev \
	  libmcrypt-dev \
	  libpng-dev \
	  libzip-dev \ 	
	&& docker-php-ext-install mysqli \
	&& docker-php-ext-configure gd --with-jpeg-dir=/usr/include/ \
	&& pecl install apcu imagick \
	&& docker-php-ext-enable apcu imagick \
	&& docker-php-ext-install gd \
	&& docker-php-ext-install gmp \
	&& docker-php-ext-install zip \
	&& rm -rf /var/cache/apk/*	
