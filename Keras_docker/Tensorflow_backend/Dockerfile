FROM khanfarhan/jetson-tensorflow:latest

RUN apt-get update && apt-get install -y \
  libhdf5-dev \
  python3-h5py \
  python3-yaml


RUN cd /root && git clone https://github.com/fchollet/keras.git && cd keras && \
  # Install
  python3 setup.py install



