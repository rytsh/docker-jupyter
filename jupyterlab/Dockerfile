FROM python:3-alpine

LABEL maintainer="Eray Ates <rytsh@devusage.com>"

RUN apk add --no-cache \
    # system requirements
    build-base zeromq-dev \
    # python requirements
    && pip install jupyterlab

# clean image
RUN apk del build-base

RUN install -m 777 -d /.local /.jupyter /.cache

ADD jupyter_notebook_config.json /.jupyter/jupyter_notebook_config.json

WORKDIR /jupyter

CMD [ "jupyter", "lab" ]
