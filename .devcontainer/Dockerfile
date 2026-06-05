FROM mcr.microsoft.com/devcontainers/java:1-17-bullseye

# Install MySQL-compatible command-line client from Debian bullseye
RUN rm -f /etc/apt/sources.list.d/yarn.list /etc/apt/sources.list.d/yarn.list.save || true \
  && sed -i '/dl.yarnpkg.com/d' /etc/apt/sources.list /etc/apt/sources.list.d/* 2>/dev/null || true \
  && apt-get update \
  && apt-get install -y gnupg lsb-release inetutils-tools default-mysql-client
