FROM mhart/alpine-node:6.9.2

ENV PATH /root/.yarn/bin:$PATH

RUN apk --update --no-cache add --virtual build-dep curl bash binutils tar \
  && rm -rf /var/cache/apk/* \
  && /bin/bash \
  && touch ~/.bashrc \
  && curl -o- -L https://yarnpkg.com/install.sh | bash -s -- --version 0.18.1 \
  && apk del build-dep
