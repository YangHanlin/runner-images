FROM hanlinyang/ubuntu:20.04

# Install Python 3.8 and Pip
RUN apt-get update && apt-get install -y \
    python3.8 \
    python3-pip \
 && rm -rf /var/lib/apt/lists/*

# Set up aliases for python and pip
RUN echo "\n\
alias python=python3\n\
alias pip=pip3\n" \
    >>~/.bashrc

# Set up PyPI mirror
# https://mirrors.tuna.tsinghua.edu.cn/help/pypi/
RUN python3 -m pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
