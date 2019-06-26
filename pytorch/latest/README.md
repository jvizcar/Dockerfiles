### tag: latest
*26 June 2019*

This version is built from Pytorch Docker version with 1.1.0 PyTorch version and cuda 10.0. This is the newest version available from Pytorch Docker that is not nightly or devel. Tested on Ubuntu 18.04 and a GTX 2070 GPU (and NVIDIA driver: 410.104). 

Also contains jupyter notebook and pyvips for working with virtual images (i.e. .svs, .ndpi, etc).

To run a jupyter notebook run in interactive mode (starts on /mnt directory, this is where you should mount your files) and type jupyter notebook. Password for notebook is dGutmanLa8!. Jupyter notebook runs on port 8888 by default.<br>
* To change password to custom, run this before jupyter notebook: ```$ jupyter notebook password```
