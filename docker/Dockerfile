# Sử dụng Ubuntu 22.04 LTS làm nền tảng ổn định
FROM ubuntu:22.04

# Bỏ qua các thông báo tương tác khi cài đặt
ENV DEBIAN_FRONTEND=noninteractive

# Cập nhật hệ thống và cài đặt toolchain cùng các thư viện phụ thuộc
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

# Thiết lập thư mục làm việc mặc định trong container
WORKDIR /workspace

# Khởi chạy Bash shell mặc định
CMD ["/bin/bash"]