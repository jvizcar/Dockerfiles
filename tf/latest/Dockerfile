# Pull latest Tensorflow image that allows GPU usage and comes with Python 3 and Jupyter notebook
FROM tensorflow/tensorflow:1.12.0-gpu-py3


# Add Pyvips requirements (this updates a lot so may have caused performance issues with the image not yet identified)
RUN apt-get update
RUN apt-get install libvips -y


# Add a password to Jupyter notebooks
RUN mkdir -p /.jupyter 
RUN echo c.NotebookApp.ip = \"0.0.0.0\" > /.jupyter/jupyter_notebook_config.py
RUN echo "{\"NotebookApp\": \
    { \"password\": \"sha1:afaafe9194f3:fefec7110ad1f95bcc2fe0bf85c6cb3e2c811924\" } } \
    " >> /.jupyter/jupyter_notebook_config.json


# Install more Python packages
RUN pip install --upgrade pip
RUN pip install pandas==0.24.2
RUN pip install pyvips==2.1.8
RUN pip install tqdm==4.36.1
RUN pip install scikit-learn==0.21.3
RUN pip install scikit-image==0.15.0
RUN pip install seaborn==0.9.0
RUN pip install opencv-python==4.1.1.26
RUN pip install girder_client==3.0.3
RUN pip install histomicstk --find-links https://manthey.github.io/large_image_wheels