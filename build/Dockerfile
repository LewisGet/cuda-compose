FROM nvidia/cuda:12.2.0-devel-ubuntu20.04

ENV LANG C.UTF-8
ENV TZ="Asiz/Taipei"

RUN apt-get update
RUN apt-get install -y python3
RUN apt-get install -y python3-pip
RUN python3 -m pip install notebook

EXPOSE 8888

CMD ["python3", "-m", "notebook", "--allow-root", "--port=8888", "--ip=0.0.0.0"]
