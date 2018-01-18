# dockerfiles-for-Jetson-Tx2
==========================

This repo has dockerfiles which are meant to be used for testing different deep learning frameworks on Nvidia's Jetson Tx2. The docker images can be found on docker hub at (https://hub.docker.com/r/khanfarhan/). All the images are build on Ubuntu arm64v8(16.04) and are provided with python 3.5.2

Before using these docker images ensure the JetPack used to flash your Jetson and use the corresponding docker image. Docker files provided here are for JetPack 3.1 and JetPack3.2 Developer preview. 

If you are on JetPack3.1 you have to build a custom kernel which can support docker the instructions of which are given in README of 3.1. 

After JetPack3.2 Nvidia has provided support for docker and Docker can be installed easily.