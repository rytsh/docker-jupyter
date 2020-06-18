# JupyterLab Docker Image

Just required and minimal features installed.

Get with build

```shell
docker build -t ryts/jupyterlab:1.0 -f jupyterlab/Dockerfile jupyterlab
```

Run

```shell
docker run -d --restart always --network host --user $(id -u):$(id -g) -v ~/jupyter:/jupyter ryts/jupterlab:1.0
```
