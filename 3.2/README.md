# dockerfiles-for-Jetson-Tx2(JetPack3.2)

With JetPack3.2, Nvidia has provided support to docker and it can easily be installed. Follow these instructions to install docker:


1. Set up the docker repository
```sh
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo add-apt-repository "deb [arch=arm64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
``` 

2. Install Docker CE
```sh
$ sudo apt-get update
$ sudo apt-get install docker-ce
```

3. Verify installation
```sh
$ sudo docker ps
```

# Running docker images

All the docker images uses Docker.base as the base image which provides all the drivers and CUDA and CUDNN files needed for utilizing the GPU of Nvidia Jetson.

Use the following command for executing the docker images:

```sh
$ sudo docker run -it --rm --privileged DockerImageName
```
PS: Download Tensorflow 1.9 wheel file from this link https://nvidia.box.com/v/TF190rc0-py35-wTRT

 