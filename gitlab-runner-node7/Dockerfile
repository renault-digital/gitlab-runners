FROM renaultdigital/gitlab-runner-base


ENV ALPINE_VERSION 3.6
ENV NODE_VERSION 7.10.1-r0
ENV CHROMIUM_VERSION 61
ENV FREETYPE_VERSION 2.7.1

# Install Node
RUN apk add --update \
    "nodejs-current=${NODE_VERSION}" \
    "nodejs-current-npm=${NODE_VERSION}" \
    --update-cache \
    --repository "http://dl-cdn.alpinelinux.org/alpine/${ALPINE_VERSION}/community"

## Install Chromium

RUN apk add --update \
    "chromium>=${CHROMIUM_VERSION}" \
    "chromium-chromedriver>=${CHROMIUM_VERSION}" \
    "freetype>=${FREETYPE_VERSION}" \
    udev \
    ttf-freefont \
    --update-cache \
    --repository 'http://dl-cdn.alpinelinux.org/alpine/edge/community' \
    --repository 'http://dl-cdn.alpinelinux.org/alpine/edge/main'

# apk add --update "chromium>=${CHROMIUM_VERSION}" "chromium-chromedriver>=${CHROMIUM_VERSION}" --update-cache --repository 'http://dl-cdn.alpinelinux.org/alpine/edge/community' --repository 'http://dl-cdn.alpinelinux.org/alpine/edge/main'

## Install Yarn

RUN npm install -g yarn


