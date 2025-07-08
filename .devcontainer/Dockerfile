ARG VARIANT=3.3.5
FROM mcr.microsoft.com/devcontainers/ruby:${VARIANT}

ARG NODE_VERSION=18
ARG BUNDLER_VERSION=2.5.7

RUN su vscode -c ". /usr/local/share/nvm/nvm.sh && nvm install ${NODE_VERSION} && corepack enable"

RUN apt-get update && apt-get install -y \
  libpq-dev \
  libvips \
  build-essential \
 && apt-get clean

RUN gem install bundler -v ${BUNDLER_VERSION}
