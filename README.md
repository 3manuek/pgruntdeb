# pgrunt[ime]deb[ugging]

[WIP]



## Build

```earthly
earthly --interactive --no-satellite +build-all
earthly --no-satellite --disable-remote-registry-proxy --interactive ./postgres+build-w-patch
```

About `--disable-remote-registry-proxy`, see [Earthly issue 3736](https://github.com/earthly/earthly/issues/3736#issuecomment-1906786044).

## Connecting 

```bash
docker compose exec -it postgres psql -U postgres
```

## Applying patches

Inside the `patches` folder, name your patch and pass its name through the `PATCH` 
argument.

