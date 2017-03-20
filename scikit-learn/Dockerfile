FROM ubuntu:17.04

MAINTAINER prashanth.gedde@gmail.com

# install python
RUN apt-get update && apt-get install -y python \
    python-dev \
    python-pip

# pip-install all python libraries
RUN pip install --no-cache-dir numpy scipy matplotlib pandas scikit-learn jupyter

WORKDIR /workdir

# expose Jupyter port 8888
EXPOSE 8888

# start Jupyter server
ENTRYPOINT ["/bin/sh"]
CMD ["-c", "jupyter notebook --no-browser --port=8888 --ip=0.0.0.0 --notebook-dir=/notebook"]
