# Use the jupyter/scipy-notebook as the base image
FROM jupyter/scipy-notebook:latest

# Switch to root user for installation
USER root

# Install basic dependencies including gnupg
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        sudo \
        wget \
        gnupg \
        apt-utils \
        && rm -rf /var/lib/apt/lists/*

# Install NVIDIA CUDA Toolkit
RUN wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2204/x86_64/cuda-keyring_1.1-1_all.deb
RUN sudo dpkg -i cuda-keyring_1.1-1_all.deb

RUN sudo apt-get update && sudo apt-get install -y nvidia-container-toolkit && sudo apt-get -y install cuda && sudo apt-get -y install nvidia-gds

# Switch back to the jovyan user
USER $NB_UID

# Set the working directory
WORKDIR /home/$NB_USER/work
