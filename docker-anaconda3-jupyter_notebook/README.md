# Anaconda3 Jupyter Notebook

Docker Hub: https://hub.docker.com/repository/docker/mtabishk/jupyter-nb-anaconda3

Run the Container:
```

$ docker run -it --name jupyter_test -p 8888:8888 --env="DISPLAY"  -v "$PWD/notebooks:/root/notebooks"  mtabishk/jupyter-nb-anaconda3:latest

```
