# Miniconda Jupyter Notebook

Docker Hub: https://hub.docker.com/repository/docker/mtabishk/miniconda-jupyternb

Run the Container:
```
$ mkdir notebooks/

$ docker run -dit --name jupyter-nb -p 8888:8888 --env="DISPLAY" -v "$PWD/notebooks:/root/notebooks" mtabishk/miniconda-jupyternb:latest

```

Proceed to open the following URL on our browser: http://localhost:8888
Enter "tabish" as the password. 


#### Prepare a hashed password
You can prepare a hashed password manually, using the function notebook.auth.security.passwd():
```
In [1]: from notebook.auth import passwd

In [2]: passwd()

Enter password:
Verify password:

Out[2]: 'sha1:67c9e60bb8b6:9ffede0825894254b2e042ea597d771089e11aed'
```
You can replace this hash with the one given in the Dockerfile.
