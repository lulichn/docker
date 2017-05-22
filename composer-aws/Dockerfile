
# https://github.com/frol/docker-alpine-python3/blob/98ca765c4fb83c24593f4872b02f38a2034baab4/Dockerfile

FROM composer/composer:php5-alpine

RUN apk -v --update --no-cache add \
	zip \
	git \
        python3 \
        groff \
        less \
        mailcap \
        && \
    python3 -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip3 install --upgrade awscli && \
    rm /var/cache/apk/* && \
    rm -r /root/.cache

ENTRYPOINT [""]

