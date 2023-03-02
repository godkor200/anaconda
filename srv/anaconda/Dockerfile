FROM continuumio/anaconda3

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install net-tools -y
RUN apt-get install git -y
RUN apt-get install vim -y
RUN apt-get install curl -y
RUN apt-get install wget -y
RUN apt-get install nano -y
RUN apt-get install lsof -y

RUN apt-get install g++ -y
RUN apt-get install openjdk-11-jdk -y
RUN apt-get install python3-dev -y
RUN apt-get install python3-pip -y

ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk-am64
ENV PATH=$PATH:$JAVA_HOME/bin

RUN pip install --upgrade pip
RUN pip install konlpy
RUN pip install gensim==3.8.3
RUN pip install jupyter

WORKDIR /root
RUN mkdir data
RUN mkdir code

RUN apt-get -y install gcc && pip install --upgrade setuptools
RUN mkdir -p /root/.jupyter
COPY ./srv/anaconda/conf/jupyter_notebook_config.json /root/.jupyter/jupyter_notebook_config.json

EXPOSE 8888
