FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    build-essential \
    gcc-arm-linux-gnueabi \
    libncurses5-dev \
    git \
    make \
    wget \
    cpio \
    unzip \
    rsync \
    bc \
    python3 \
    python3-dev \
    swig \
    zlib1g-dev \
    libssl-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    apt-get update && apt-get install -y bison flex \
    apt-get update && apt-get install -y python2 \
    apt-get update && apt-get install -y python2-dev

# set up workspace default
WORKDIR /workspace

# run bash shell default
CMD ["/bin/bash"]