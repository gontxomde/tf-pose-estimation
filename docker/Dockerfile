FROM tensorflow/tensorflow:1.14.0-gpu-py3

RUN apt-get update && apt-get install -y git && pip install --upgrade pip

RUN apt-get install -y libsm6 libxext6 libxrender-dev \
&& pip install opencv-python && apt-get update && apt-get install -y vim

ADD https://showcase.linx.twenty57.net:8081/UnixTime/tounixtimestamp?datetime=now /tmp/bustcache

RUN git clone --depth 1 https://github.com/gontxomde/tf-pose-estimation.git \
&& cd tf-pose-estimation \
&& pip install Cython \
&& pip install -e .

RUN python /tf-pose-estimation/run_initialization.py