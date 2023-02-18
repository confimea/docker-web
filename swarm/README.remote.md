## Create `.env`

```shell
cp example.remote.env .env
```

## Create network

```shell
docker network create --driver=overlay traefik
```

## Create stack

```shell
export $(grep -v '^#' .env | xargs) && \
docker stack deploy -c remote.yml web
```
