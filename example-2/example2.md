# Example 2 - Using docker Compose files

[docker docs - environment](https://docs.docker.com/compose/compose-file/#environment)

Using docker Compose files to override environment variables.

Defined in [Dockerfile](Dockerfile) are two environment variables with default values.

```Dockerfile
ENV GREETING=Hello
ENV NAME=World
```

## Using a docker Compose file

Defined in [`docker-compose.yml`](docker-compose.yml) are two overriding environment variables.

```yml
environment:
    GREETING: Goodbye
    NAME: John
```

`$ docker-compose up --build`

```
Goodbye, John!
```

## Using multiple docker Compose files

[docker docs - Share Compose configurations between files and projects](https://docs.docker.com/compose/extends/)

Use multiple docker Compose files to partially override options of a previous docker compose file.

Defined in [docker-compose.test.yml](docker-compose.test.yml) are two overriding environment variables.

```yml
environment:
    GREETING: Hey
    NAME: Alex
```

`$ docker-compose -f docker-compose.yml -f docker-compose.test.yml up --build`

```
Hey, Alex!
```

## Using multiple docker Compose files then overriding their environment variables with `run` command 

`$ docker run -e GREETING=Greetings -e NAME=Humans example2`

```
Greetings, Humans!
```