FROM renaultdigital/gitlab-runner-base


ENV ALPINE_VERSION edge
ENV NODE_VERSION 7.10.1-r0
ENV CHROMIUM_VERSION 61
ENV FREETYPE_VERSION 2.7.1

# Install Node & Chromium
RUN apk add \
    --update \
    "nodejs-current=${NODE_VERSION}" \
    "nodejs-current-npm=${NODE_VERSION}" \
    "chromium>=${CHROMIUM_VERSION}" \
    "chromium-chromedriver>=${CHROMIUM_VERSION}" \
    "freetype>=${FREETYPE_VERSION}" \
    udev \
    ttf-freefont \
    --update-cache \
    --repository "http://dl-cdn.alpinelinux.org/alpine/${ALPINE_VERSION}/community" && \
    rm /var/cache/apk/* && \
    npm install -g yarn


