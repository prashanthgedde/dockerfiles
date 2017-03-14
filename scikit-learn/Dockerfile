FROM ubuntu:17.04

MAINTAINER prashanth.gedde@gmail.com

RUN apt-get update && apt-get install -y python \
    python-dev \
    python-pip

RUN pip install --no-cache-dir numpy scipy pandas scikit-learn jupyter 

EXPOSE 8888
ENTRYPOINT ["/bin/sh"]
CMD ["-c", "jupyter notebook --no-browser --port=8888 --ip=0.0.0.0"]
