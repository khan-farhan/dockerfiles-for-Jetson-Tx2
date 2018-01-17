Theano : 1.0
Ubuntu : arm64v8:16.04
Python : 3.5.2

Has GPU support with GpuArray backend. CUDA driver and the GPU device are not visible to the Docker container thus we need to pass some libraries and give access to devices related to GPU.

To run this dockerfile use :

sudo docker run -it --rm --device=/dev/nvhost-ctrl --device=/dev/nvhost-ctrl-gpu --device=/dev/nvhost-prof-gpu --device=/dev/nvmap --device=/dev/nvhost-gpu --device=/dev/nvhost-as-gpu -v /usr/lib/aarch64-linux-gnu/tegra:/usr/lib/aarch64-linux-gnu/tegra -v /usr/local/cuda-8.0:/usr/local/cuda khanfarhan/jetson-theano:latest

