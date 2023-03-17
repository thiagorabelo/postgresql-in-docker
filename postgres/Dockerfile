ARG PG_TAG=14.7

FROM postgres:${PG_TAG}

LABEL version=${PG_TAG}
LABEL maintainer="Thiago <https://github.com/thiagorabelo>"

ENV PAGER "less -S"
ENV LANG "pt_BR.UTF-8"
ENV TZ "America/Fortaleza"

RUN localedef -i pt_BR -c -f UTF-8 -A /usr/share/locale/locale.alias pt_BR.UTF-8 \
    && apt-get update \
    && apt-get install less bzip2 iputils-ping nano -y \
    && apt-get clean \
    && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo $TZ > /etc/timezone \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
