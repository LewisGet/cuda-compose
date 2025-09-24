FROM nvidia/cuda:12.0.0-cudnn8-runtime-ubuntu20.04

ENV LANG C.UTF-8
ENV TZ="Asia/Taipei"

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get install -y python3
RUN apt-get install -y python3-pip

RUN python3 -m pip install notebook  --break-system-packages
RUN python3 -m pip install --upgrade jupyter_core jupyter_client --break-system-packages

RUN python3 -m pip install --upgrade jupyter_core jupyter_client

RUN python3 -m pip install jupyterlab --break-system-packages

RUN apt-get install -y git
RUN apt-get install -y git-lfs
RUN apt-get install -y zip
RUN apt-get install -y unzip

RUN apt-get install -y libsndfile1
RUN apt-get install -y ffmpeg libsm6 libxext6

RUN python3 -m pip install torch torchaudio numpy transformers --break-system-packages

EXPOSE 8888

CMD ["python3", "-m", "jupyterlab", "--allow-root", "--port=8888", "--ip=0.0.0.0"]
