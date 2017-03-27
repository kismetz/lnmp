From php:5.6-fpm

#安装扩展，gd需要libpng支持
RUN apt-get update \
	&& apt-cache search libpng \
	&& apt-get install -y libpng12-dev \
	&& docker-php-ext-install gd \
	&& docker-php-ext-install pdo_mysql

ADD composer.phar /usr/local/bin/composer
RUN chmod 755 /usr/local/bin/composer
ADD phpunit-6.0.10.phar /usr/local/bin/phpunit
RUN chmod +x /usr/local/bin/phpunit

WORKDIR e:/opt

#权限
#Mac还需加上&& usermod -G staff www-data
RUN usermod -u 1000 www-data

VOLUME ["/opt"]