## Install Docker Compose

Docker Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file 
to configure your application’s services. Then, with a single command, you create and start all the services from your 
configuration.

To install Docker Compose, run this command in your terminal:

```shell
wget https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64 -O /usr/local/bin/docker-compose
```

Make this docker-compose executable
```shell
chmod +x /usr/local/bin/docker-compose
```

Check docker-compose version
```shell
docker-compose --version
```

## Task
- make sure docker-compose is installed on node1
- dont install docker-compose on node2 

