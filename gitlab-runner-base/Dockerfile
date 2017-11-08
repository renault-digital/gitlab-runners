FROM alpine:3.6

RUN apk -Uuv add python git openssh curl jq bash wget ca-certificates make groff less py-pip && \
    pip install awscli && \
    rm /var/cache/apk/*


