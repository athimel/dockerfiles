## Hu ?

Just like anybody, here is the dockerfiles I use

### post-its

#### List running containers

```
docker ps
```

#### Run bash in a running container

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
docker inspect --format '{{ .NetworkSettings.IPAddress }}' <id/name>
```

