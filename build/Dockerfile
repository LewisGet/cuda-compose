FROM nvidia/cuda:12.0.0-cudnn8-runtime-ubuntu20.04

ENV LANG C.UTF-8
ENV TZ="Asiz/Taipei"

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get install -y python3
RUN apt-get install -y python3-pip
RUN apt-get install -y python3-notebook

RUN python3 -m pip install --upgrade jupyter_core jupyter_client

RUN apt-get install -y git
RUN apt-get install -y zip
RUN apt-get install -y unzip

EXPOSE 8888

CMD ["python3", "-m", "notebook", "--allow-root", "--port=8888", "--ip=0.0.0.0"]
