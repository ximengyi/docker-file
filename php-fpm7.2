FROM php:7.2.32-fpm-alpine

RUN sed -i "s/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g" /etc/apk/repositories

RUN set -ex \
    && apk add --no-cache $PHPIZE_DEPS \
    && apk update \
    && apk add --no-cache libstdc++ libzip-dev  \
        wget \
      #  git \
        vim \
    && apk add --no-cache \
       # librdkafka-dev \
        tzdata \
        bash \
        freetype \
        libpng\
        freetype-dev\
        libjpeg-turbo \
        libjpeg-turbo-dev \
        libmcrypt-dev \
        libpng-dev \
        libwebp-dev \
        libxpm-dev \
        libzip-dev \
        libxml2-dev \
        zip \
        unzip \
    # 安装gd库
    && docker-php-ext-configure  gd \
    --with-freetype-dir=/usr/include/freetype2/ \
    --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd \
    # 安装zip
    && docker-php-ext-install -j$(nproc) zip \
    && docker-php-ext-install -j$(nproc) \
        bcmath \
        pcntl \
        mysqli \
        pdo_mysql \
        opcache \
        sockets \
        soap \
    # 安装pecl扩展
    && pecl install \
    http://pecl.php.net/get/redis-6.0.2.tgz \
    http://pecl.php.net/get/mcrypt-1.0.7.tgz \
    http://pecl.php.net/get/mongodb-1.16.2.tgz \
    http://pecl.php.net/get/swoole-4.8.13.tgz \
       # rdkafka \
    && rm -rf /tmp/pear/download/* \
    && docker-php-ext-enable \
        redis \
        mcrypt \
        mongodb \
        swoole\
    && docker-php-source delete \
    # && pecl clear-cache \
    && rm -rf /var/lib/apt/lists/* \
    && rm -rf /var/cache/apk/* \
    # 安装composer
    # && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    # && php composer-setup.php --install-dir=/bin --filename=composer \
    # && php -r "unlink('composer-setup.php');"
    # 修改 php 配置文件
    && mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini" \
    && rm -rf "$PHP_INI_DIR/../php-fpm.d/*.conf" \
    # 修改时区
    && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo 'Asia/Shanghai' >/etc/timezone \
    # 修改 vim 配置
    && echo "set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936" >> /etc/vim/vimrc \
    && echo "set termencoding=utf-8" >> /etc/vim/vimrc \
    && echo "set encoding=utf-8" >> /etc/vim/vimrc \
    && echo "set paste" >> /etc/vim/vimrc 