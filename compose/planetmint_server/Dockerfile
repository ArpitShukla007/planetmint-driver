FROM python:3.9

RUN apt-get update && apt-get install -y vim

ARG branch
ARG backend
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

RUN pip install --upgrade pip ipdb ipython

COPY . /usr/src/app/
ENV PLANETMINT_DATABASE_BACKEND "${backend}"
RUN pip install git+https://github.com/planetmint/planetmint.git@"${branch}"#egg=planetmint
