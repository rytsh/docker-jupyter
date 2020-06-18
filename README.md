# JupyterLab Docker Image

Just required and minimal features installed.

Main password is `secretpass`.

You can edit after open terminal on jupyter and run this command.

```shell
jupyter notebook password
```

Get with build

```shell
docker build -t ryts/jupyterlab:1.0 -f jupyterlab/Dockerfile jupyterlab
```

Run

```shell
sudo docker run -d --restart always --network host --user $(id -u):$(id -g) -w /jupyter -v ~/jupyter:/jupyter ryts/jupyterlab:1.0
```
