FROM ubuntu:20.04

# Install essential tools
RUN apt-get update && apt-get install -y \
    curl \
    wget \
    git \
    p7zip-full \
 && rm -rf /var/lib/apt/lists/*

# Use mirror
COPY ./ubuntu/sources.list /etc/apt/sources.list
