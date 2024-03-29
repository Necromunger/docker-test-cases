# Example 1 - Using `run` command

[docker docs - run ENV (environment variables)](https://docs.docker.com/engine/reference/run/#env-environment-variables)

Using the `run` command and the `-e` flag to override environment variables.

Defined in [Dockerfile](Dockerfile) are two environment variables with default values.

```Dockerfile
ENV GREETING=Hello
ENV NAME=World
```

## Passing no variables: 

`$ docker run example1`

```
Hello, World!
```

## Passing one environment variable: 

`$ docker run -e GREETING=Goodbye example1`

```
Goodbye, World!
```

## Passing multiple environment variables:

`$ docker run -e GREETING=Goodbye -e NAME=John example1`

```
Goodbye, John!
```
