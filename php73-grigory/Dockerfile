FROM php:7.3-fpm-alpine
RUN apk add --no-cache --virtual .build-deps \
    $PHPIZE_DEPS \
    curl-dev \
    libtool \
    libxml2-dev \
    postgresql-dev \
    && apk add --no-cache \
    curl \
    postgresql-libs \
    libintl \
    icu \
    icu-dev \
    libzip-dev \
    && docker-php-ext-install \
    curl \
    iconv \
    mbstring \
    pdo \
    pdo_pgsql \
    pcntl \
    tokenizer \
    xml \
    zip \
    intl \
    opcache \
    && apk del -f .build-deps
WORKDIR /app