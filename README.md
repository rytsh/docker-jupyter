# JupyterLab Docker Image

Just required and minimal features installed. Get on docker hub `ryts/jupyter`

Main password is `secretpass`.

You can edit after open terminal on jupyter and run this command.

```shell
jupyter notebook password
```

Get with build

```shell
docker build -t ryts/jupyterlab:v1.0 -f jupyterlab/Dockerfile jupyterlab
```

Run, don't forget to change base folder `~/jupyter`

```shell
sudo docker run -d --restart always -v ~/jupyter:/jupyter -h jupyter ryts/jupyterlab:v1.0
```
