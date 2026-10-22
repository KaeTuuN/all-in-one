FROM docker.io/library/composer:2@sha256:da624c2c705d54e2f5a9bb77a5dc6c7d091711433ebefd7035672e84c2010fee

ARG APCU_VERSION=5.1.28

SHELL ["/bin/ash", "-o", "pipefail", "-c"]
RUN mkdir -p /usr/src/php/ext/apcu \
 && curl -fsSL --retry 5 "https://github.com/krakjoe/apcu/archive/refs/tags/v$APCU_VERSION.tar.gz" \
  | tar -xz --strip-components=1 -C /usr/src/php/ext/apcu \
 && docker-php-ext-install apcu
