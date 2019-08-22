# Example 2

[docker docs - compose environment](https://docs.docker.com/compose/compose-file/#environment)

Use docker compose files to override default environment variables.

Defined in Dockerfile are two environment variables with default values.

```Dockerfile
ENV GREETING=Hello
ENV NAME=World
```

## Using default `docker.compose.yml` with overriding environment varables:

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

## Using default `docker.compose.test.yml` with overriding environment varables:

[docker docs - Share Compose configurations](https://docs.docker.com/compose/extends/)

Use additional docker compose files to partially override options of previous docker compose file.

Defined in `docker.compose.test.yml` are two overriding environment variables.

```yml
environment:
    GREETING: Hey
    NAME: Alex
```

`$ docker-compose -f docker-compose.yml -f docker-compose.test.yml up --build`

```
Hey, Alex!
```