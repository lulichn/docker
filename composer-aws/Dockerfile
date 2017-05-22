

FROM composer/composer:php5-alpine

RUN apk -v --update add \
	zip \
	git \
        python \
        py-pip \
        groff \
        less \
        mailcap \
        && \
    pip install --upgrade pip awscli && \
    apk -v --purge del py-pip && \
    rm /var/cache/apk/*

ENTRYPOINT [""]

