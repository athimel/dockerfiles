## Hu ?

Just like anybody, here is the dockerfiles I use

### post-its

#### List running containers

```
docker ps
```

#### Run bash

```
docker exec -it <id/name> bash
```

#### Stop container

```
docker stop <id/name>
```

#### Remove container

```
docker rm <id/name>
```

#### Get container IP addresses

```
docker exec -it <id/name> sh -c 'ifconfig  | grep -B 1 "inet addr:"'
```

#### Get container IP addresses (with net-tools install)

```
docker exec -it <id/name> sh -c 'apt-get update && apt-get install -y net-tools && ifconfig  | grep -B 1 "inet addr:"'
```

