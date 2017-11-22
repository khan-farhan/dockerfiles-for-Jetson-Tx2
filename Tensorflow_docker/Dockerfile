FROM arm64v8/ubuntu:16.04

ENV LD_LIBRARY_PATH=/usr/lib/aarch64-linux-gnu/tegra:/usr/local/cuda/lib64

# Set CUDA_ROOT
ENV CUDA_ROOT /usr/local/cuda/bin

RUN apt-get update && apt-get install -y \
   build-essential \
   python3-numpy \
   python3-scipy \
   python3-pip \
   python3-dev 


RUN cp /usr/bin/python3 /usr/bin/python

COPY ./tensorflow-1.3.0-cp35-cp35m-linux_aarch64.whl /

RUN pip3 install /tensorflow-1.3.0-cp35-cp35m-linux_aarch64.whl
