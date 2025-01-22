FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

# Avoid prompts from apt
ENV DEBIAN_FRONTEND=noninteractive

# Update and install required packages
RUN apt-get update && apt-get install -y \
    racket \
    git \
    curl \
    wget \
    xvfb \
    x11-utils \
    && rm -rf /var/lib/apt/lists/*

# Install Racket packages
RUN raco pkg install --auto --batch --scope installation \
    rackunit \
    rackunit-lib \
    rackunit-doc \
    racket-langserver \
    fmt