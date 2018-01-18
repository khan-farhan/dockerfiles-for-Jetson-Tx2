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




 