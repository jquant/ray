ARG GPU
FROM jquant/ray-base-deps:6c93cb0bf"$GPU"
#https://s3-us-west-2.amazonaws.com/ray-wheels/latest/ray-1.2.0.dev0-cp38-cp38-manylinux2014_x86_64.whl
ARG WHEEL_PATH=./ray-1.2.0.dev0-cp38-cp38-manylinux2014_x86_64.whl
# For Click
ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8
COPY $WHEEL_PATH .

RUN sudo apt-get update && sudo apt-get install -y \
    cmake \
    build-essential \
    zlib1g-dev

#RUN $HOME/anaconda3/bin/pip --no-cache-dir install `basename $WHEEL_PATH`[all]
RUN $HOME/anaconda3/bin/pip --no-cache-dir install ray==1.1.0
