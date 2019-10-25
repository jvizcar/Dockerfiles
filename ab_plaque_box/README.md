## AB Plaque Box

Used for PyTorch work on Whole Slide Image data. Includes PyVips Python wrapper as well as a runnable jupyter notebook. Requires nvidia-docker to be installed to use GPU. Includes girder_client Python package. 

Instructions on how to run:<br>
```
$ nvidia-docker run -it --rm --ipc=host -p<local_port>:8888 -v <local_dir>:/mnt/ jvizcar/ab_plaque_box:latest
In interactive mode:
$ jupyter notebook
$ enter password, see Dockerfile for info regarding this

