# Use the official Visual Studio Code development container image
FROM mcr.microsoft.com/vscode/devcontainers/universal:linux

# Set non-interactive mode for package installation
ENV DEBIAN_FRONTEND=noninteractive

# Install necessary tools and dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    gdb \
    valgrind \
    wireshark \
    && rm -rf /var/lib/apt/lists/*

# [Optional] Add any custom tools or configurations you need here.

# Create a non-root user to use in the Codespace
RUN useradd -m vscode

# Switch to the non-root user
USER vscode

# Set the working directory
WORKDIR /workspace

# Default shell for Codespace
ENV SHELL /bin/bash
