# Example 3 - Using docker .env files

[docker docs - Declare default environment variables in file](https://docs.docker.com/compose/env-file/)

Using `.env` files to override environment variables.

Defined in [Dockerfile](Dockerfile) are two environment variables with default values.

```Dockerfile
ENV GREETING=Hello
ENV NAME=World
```

## Using `.env` file inside docker Compose file

[docker docs - env_file](https://docs.docker.com/compose/compose-file/#env_file)

Defined in [.env](.env) are two overriding environment variables.

```yml
GREETING=Goodbye
NAME=John
```

Defined in [docker-compose.yml](docker-compose.yml) is a pointer to the [.env](.env) environment file.

```yml
env_file: .env
```

`$ docker-compose up --build`

```
Goodbye, John!
```

## Using `.env` file with `run` command

FILL MEEE