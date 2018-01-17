FROM arm64v8/ubuntu:16.04

RUN apt-get update && apt-get install -y \
  build-essential \
  gfortran \
  git \
  wget \
  liblapack-dev \
  libopenblas-dev \
  python3-dev \
  python3-numpy \
  python3-scipy \
  python3-pip \
  python3-nose \
  libhdf5-dev \
  python3-h5py \
  python3-yaml



RUN pip3 install --upgrade pip
RUN pip3 install --upgrade six
RUN pip3 install --upgrade --no-deps git+git://github.com/Theano/Theano.git


# Clone Keras repo and move into it
RUN cd /root && git clone https://github.com/fchollet/keras.git && cd keras && \
  # Install
  python3 setup.py install


