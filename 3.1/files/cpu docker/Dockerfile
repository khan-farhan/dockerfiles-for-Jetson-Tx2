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
  python3-nose 



RUN pip3 install --upgrade pip
RUN pip3 install --upgrade six

RUN pip3 install Theano



# Set up .theanorc 
RUN echo "\n[global]\nfloatX=float64\n" > /root/.theanorc
