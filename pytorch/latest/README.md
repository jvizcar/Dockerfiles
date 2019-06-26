### tag: latest
*26 June 2019*

This version is built from Pytorch Docker version with 0.4.1 PyTorch version and cuda 9.0. This is an older version as of day of creation but works with Ubuntu 18.04 and tested on two GPU models: Titan V and GTX 2070.

Also contains jupyter notebook and pyvips for working with virtual images (i.e. .svs, .ndpi, etc).

To run a jupyter notebook run in interactive mode (starts on /mnt directory, this is where you should mount your files) and type jupyter notebook. Password for notebook is dGutmanLa8!. Jupyter notebook runs on port 8888 by default.<br>
* To change password to custom, run this before jupyter notebook: ```$ jupyter notebook password```
