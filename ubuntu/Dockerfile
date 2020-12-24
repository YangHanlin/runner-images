FROM ubuntu:20.04

# Install essential tools
RUN apt-get update && apt-get install -y \
    curl \
    wget \
 && rm -rf /var/lib/apt/lists/*

# Use mirror
COPY ./sources.list /etc/apt/sources.list
