# dockerfiles-centos-user-adderable
Nginx install

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t lafin716/nginx .
	docker run -d --name n1 -p 8888:80 lafin716/nginx
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        lafin716/nginx      "/bin/bash"         7 seconds ago       Up 6 seconds                            n1
```

To test, ("lafin716" is username. )
```
	open 127.0.0.1:8888
```
To Rollback
```
    docker rm n1 -f
    docker rmi lafin716/nginx
```
