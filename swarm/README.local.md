```shell
cp example.local.env .env
```

```shell
docker network create --driver=overlay traefik
```

```shell
export $(grep -v '^#' .env | xargs) && \
docker stack deploy -c local.yml web
```

<http://traefik.localhost:8000>

<http://portainer.localhost:8000>
