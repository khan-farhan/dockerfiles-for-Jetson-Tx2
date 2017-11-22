dockerfiles-for-Jetson-Tx2
==========================

This repo has dockerfiles which are meant to be used for testing different deep learning frameworks on Nvidia's Jetson Tx2. The docker images can be found on docker hub at (https://hub.docker.com/r/khanfarhan/) 


Motivation
==========


Challenges
==========




Installing Docker on Jetson TX2 
===============================

Nvidia Jetson Tx2 doesn't have docker support. Thanks to Technica-Corporation (https://github.com/Technica-Corporation/Tegra-Docker) for providing detailed procedure to enable docker support. Follow there procedure to install docker.


Configuring CUDA and CUDNN support
==================================

All docker images require cuda and cudnn support. While flashing Jetson Tx2 with Jetpack 3.1, cuda and cudnn are also installed. In order to provide support to docker some library files are copied into cuda library folder. 

To configure CUDA and CUDNN support run following commands.

```sh

cp /usr/lib/aarch64-linux-gnu/libcudnn.so /usr/local/cuda/lib64
cp /usr/lib/aarch64-linux-gnu/libcudnn.so.6 /usr/local/cuda/lib64
cp /usr/lib/aarch64-linux-gnu/libcudnn.so.6.0.21 /usr/local/cuda/lib64
cp /usr/lib/aarch64-linux-gnu/libcudnn_static.a /usr/local/cuda/lib64
cp /usr/include/cudnn.h /usr/local/cuda/include

```



 