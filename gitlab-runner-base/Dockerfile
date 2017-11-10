FROM docker:17.06.2-ce

RUN apk -Uuv add python git openssh curl jq bash wget ca-certificates make groff less py-pip && \
    pip install -U awscli botocore docutils yamllint && \
    rm /var/cache/apk/*


