# Example 2

[docker docs - compose environment](https://docs.docker.com/compose/compose-file/#environment)

Use docker compose files to override default environment variables.

Defined in Dockerfile are two environment variables with default values.

```Dockerfile
ENV GREETING=Hello
ENV NAME=World
```

## Using default `docker.compose.yml` with overriding envrioment varables:

Defined in `docker.compose.yml` are two overriding environment variables.

```yml
environment:
    GREETING: Goodbye
    NAME: John
```

`$ docker-compose up --build`

```
Goodbye, John!
```