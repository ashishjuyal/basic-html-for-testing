## Starting webserver using docker

```shell
# run a container mounting the local volume to the HTML directory:

docker run --rm -d \
  -p 8082:80 \
  -v ${PWD}/html:/usr/share/nginx/html \
  --name nginx-selenium \
  nginx:alpine
```

Browse: `http://localhost:8082`

## Cleanup

Cleanup by removing all containers:

```shell
docker rm -f $(docker ps -aq)
```