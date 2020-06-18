# JupyterLab Docker Image

Just required and minimal features installed. Get on docker hub `ryts/jupyter`

Main password is `secretpass`.

Get with build

```shell
docker build -t ryts/jupyter:v1.0 -f jupyterlab/Dockerfile jupyterlab
```

Run, don't forget to change base folder `~/jupyter`

```shell
docker run -d --restart always -p 8888:8888 -v ~/jupyter:/jupyter -h jupyter ryts/jupyter:v1.0
```

## Change Password

Open terminal on jupyter and run this command. After this command restart container.

```shell
# in jupyterlab terminal
jupyter notebook password
```

Restart docker container

```shell
docker restart <ContainerID>
```
