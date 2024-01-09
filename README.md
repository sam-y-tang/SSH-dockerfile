# SSH-dockerfile

This Dockerfile creates an ssh service inside a docker container


![Docker](https://github.com/s1ntaxe770r/SSH-dockerfile/workflows/Docker/badge.svg)

* default user and password is test

[s1ntaxe770r](https://github.com/s1ntaxe770r) wrote about why you'd want to do this here [here](https://dev.to/s1ntaxe770r/how-to-setup-ssh-within-a-docker-container-i5i)

I used it to access ubuntu development environment on another Windows PC which has docker ubuntu container.  ssh and sftp. I don't need.


## Building the image

```
docker build -t IMAGE_NAME .
``` 

## Runing the image 

```dos
docker run --name CONTAINER_NAME --hostname=docker --env=HOME=/root --env=PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin -p 22:22 --volume=E:\temp\data:/data --workdir=/root --restart=no -t -d IMAGE_NAME
```
