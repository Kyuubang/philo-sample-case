## Using docker command 

Docker containers are built from Docker images. By default, Docker pulls these images from Docker Hub, a Docker registry
managed by Docker, the company behind the Docker project. Anyone can host their Docker images on Docker Hub, so most 
applications and Linux distributions you’ll need will have images hosted there.

1. Run sample container from Docker Hub on all node
```shell
docker run hello-world
```

2. pull image from Docker Ubuntu 20.04 on node 1
```shell
docker pull ubuntu:20.04
```

3. pull image from docker alpine 3.17 on node 2
```shell
docker pull alpine:3.17
```

## Task
- Run sample container from Docker Hub on all node
- make sure ubuntu 20.04 is pulled on node 1
- make sure alpine 3.17 is pulled on node 2

