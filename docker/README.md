# Introduction

This image deploys the package found in https://github.com/gontxomde/tf-pose-estimation, which is forked from [here](https://github.com/ildoonet/tf-pose-estimation/blob/master/run.py). The target is creating a docker image that will serve as an API to process poses and give body coordinates.

It uses gpu-enabled TF 1.4.

# Requirements

To use this image there is a major requirement that has to be satisfied prior to using the image.

[NVDIA Container Toolkit](https://github.com/NVIDIA/nvidia-docker) has to be installed on the host so that gpu can be used from the inside of the container.

# Usage

To run this image, use:

`docker container run --gpus all --rm -ti --name tf-openpose gontxomde/tf-openpose:latest`