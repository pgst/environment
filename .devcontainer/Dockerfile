# Rubyのバージョンは3系最新版を指定
ARG VARIANT=3-bullseye
FROM mcr.microsoft.com/vscode/devcontainers/ruby:${VARIANT}

# Node.jsのバージョンは直近のLTSである22を指定
ARG NODE_VERSION="22"
RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && nvm install ${NODE_VERSION} 2>&1"

# Bundlerのバージョンは最新版2.6.2を指定
ARG BUNDLER_VERSION='2.6.2'
RUN gem install bundler -v ${BUNDLER_VERSION}
ENV BUNDLE_PATH='/usr/local/bundle'

# Rails7のバージョンは最新版7.2.2.1を指定
ARG RAILS_VERSIONS='7.2.2.1'
RUN gem install rails -v ${RAILS_VERSIONS}
RUN gem install ruby-lsp