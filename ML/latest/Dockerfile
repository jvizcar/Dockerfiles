FROM fgiuste/ml:py3

USER root
RUN apt-get update && apt-get install -yq python3-openslide

RUN pip install --upgrade pip
RUN pip install girder_client

RUN apt install -yq git-all

RUN git clone https://github.com/girder/large_image.git
WORKDIR /home/mainuser/large_image
RUN pip install -e .[openslide,memcached]

USER mainuser