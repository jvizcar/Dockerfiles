# From an official PyTorch image
FROM pytorch/pytorch:1.1.0-cuda10.0-cudnn7.5-runtime

# Install additional Python packages..
RUN conda install -y jupyter=1.0.0 \
					 matplotlib=2.2.2 \
					 tqdm=4.23.4 \
					 pandas=0.23.0

# install pyvips
RUN apt-get update && apt-get install libvips -y
RUN pip install pyvips==2.1.2

# Create a user
RUN useradd -ms /bin/bash docker

# Set-up jupyter notebook start ip
RUN mkdir -p /home/docker/.jupyter \
	&& echo c.NotebookApp.ip = \"0.0.0.0\" > /home/docker/.jupyter/jupyter_notebook_config.py

# Set password to dGutmanLa8!
RUN echo "{\"NotebookApp\": \
    { \"password\": \"sha1:3c3713b8bd6c:3a3a114cfb13d79c721b4682771d6ca098c469dd\" } } \
    " >> /home/docker/.jupyter/jupyter_notebook_config.json

# Open permissions to mnt
RUN chmod 777 -R /mnt
RUN chmod 777 -R /home/docker

# Switch users and workdir
USER docker
WORKDIR /mnt
