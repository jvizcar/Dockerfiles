# From an official PyTorch image
FROM pytorch/pytorch:0.4.1-cuda9-cudnn7-runtime

# update packages
RUN apt-get update

# install libvips
RUN apt-get install libvips -y

# install Python packages
# RUN apt-get update
# RUN pip install pyvips==2.1.2
RUN conda install -y jupyter=1.0.0 matplotlib=2.2.2
RUN conda install -y tqdm=4.23.4
RUN conda install -y pandas=0.23.0
RUN conda install -y scikit-learn=0.19.1
RUN pip install pyvips==2.1.2

################ ---------------- Set up for starting notebook --------------------------#############
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
