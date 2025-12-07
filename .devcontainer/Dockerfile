FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    build-essential \        # gcc, g++, make, etc.
    clang \                  # clang, clang++
    clang-tools \            # clang-tidy, clangd, etc.
    llvm \                   # LLVM toolchain (IR tools, etc.)
    lldb \                   # LLVM debugger
    clang-format \           # code formatter
    cmake \
    ninja-build \
    gdb \
    git \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Dev container user for VS Code
RUN useradd -m vscode && \
    usermod -aG sudo vscode && \
    echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER vscode
WORKDIR /workspace
