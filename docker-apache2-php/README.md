## Run the apache2 webserver with php:

```
#   docker run -d --name mywebserver -p 8888:80 mtabishk/apache2-php

```
## Proceed to open the following URL on our browser: 

                             http://[IP Address of DockerHost]:8888


## This Docker Images comes with following configuration:
#### 1. Ubuntu:18.04
#### 2. Necessary Tools like: vim wget  net-tools curl
#### 3. apache2 webserver
#### 4. php7

## Document Root: /var/www/html

## Get bash shell of the container
```
#   docker exec -it  mywebserver  /bin/bash
```
