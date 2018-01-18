# dockerfiles-for-Jetson-Tx2(JetPack3.1)



Installing Docker on Jetson TX2 
===============================

Nvidia Jetson Tx2 doesn't have docker support. Thanks to Technica-Corporation (https://github.com/Technica-Corporation/Tegra-Docker) for providing detailed procedure to enable docker support. Follow there procedure to install docker.


Configuring CUDA and CUDNN support
==================================

All docker images require cuda and cudnn support. While flashing Jetson Tx2 with Jetpack 3.1, cuda and cudnn are also installed. In order to provide support to docker some library files are copied into cuda library folder. 

To configure CUDA and CUDNN support run following commands:

```sh

cp /usr/lib/aarch64-linux-gnu/libcudnn.so /usr/local/cuda/lib64
cp /usr/lib/aarch64-linux-gnu/libcudnn.so.6 /usr/local/cuda/lib64
cp /usr/lib/aarch64-linux-gnu/libcudnn.so.6.0.21 /usr/local/cuda/lib64
cp /usr/lib/aarch64-linux-gnu/libcudnn_static.a /usr/local/cuda/lib64
cp /usr/include/cudnn.h /usr/local/cuda/include

```

Running docker images
=====================

Running the docker images normally will utilize only CPU of Jetson Tx2 as the docker containers doesn't have any access to the GPU. The access can be given by passing some libraries and giving some device permissions to the container.

To run the images on GPU use following command:

```sh

sudo docker run -it --rm --device=/dev/nvhost-ctrl --device=/dev/nvhost-ctrl-gpu --device=/dev/nvhost-prof-gpu --device=/dev/nvmap --device=/dev/nvhost-gpu --device=/dev/nvhost-as-gpu -v /usr/lib/aarch64-linux-gnu/tegra:/usr/lib/aarch64-linux-gnu/tegra -v /usr/local/cuda-8.0:/usr/local/cuda khanfarhan/dockerimagename

```




 