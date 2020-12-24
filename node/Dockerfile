FROM hanlinyang/ubuntu:20.04

# Install Node.js 14 LTS and NPM (NodeSource version)
# https://github.com/nodesource/distributions/blob/master/README.md
RUN (curl -sL https://deb.nodesource.com/setup_lts.x | bash -) \
 && apt-get install -y nodejs \
 && rm -rf /var/lib/apt/lists/*

# Install Yarn and CNPM
RUN npm install -g yarn cnpm

# Set up Taobao mirror for NPM and Yarn
RUN npm config set registry https://registry.npm.taobao.org \
 && yarn config set registry https://registry.npm.taobao.org
