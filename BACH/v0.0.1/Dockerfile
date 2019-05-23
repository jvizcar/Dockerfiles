# using tensorflow-gpu running Python v3 and jupyter as base image
# https://hub.docker.com/r/tensorflow/tensorflow/
FROM tensorflow/tensorflow:1.13.1-gpu-py3-jupyter

# update and add packages for opencv
RUN apt-get update
RUN apt-get install -y libsm6 libxext6 libxrender-dev

# install python packages needed
RUN pip install --upgrade pip && \
	pip install opencv-python && \
	pip install pillow tqdm scikit-learn