FROM tensorflow/tensorflow:1.14.0-gpu-py3

RUN apt-get update && apt-get install -y git && pip install --upgrade pip

RUN apt-get install -y libsm6 libxext6 libxrender-dev \
&& pip install opencv-python && apt-get update && apt-get install -y vim

RUN git clone https://github.com/gontxomde/tf-pose-estimation.git \
&& cd tf-pose-estimation \
&& pip install Cython \
&& pip install -e .

#RUN python /tf-pose-estimation/run.py