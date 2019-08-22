# Example 1

Default environment variables and passing environment variables through run command.

Defined in Dockerfile are two environment variables with default values.

```Dockerfile
ENV GREETING=Hello
ENV NAME=World
```

## Passing no variables with `run` command

### Command:

```bash
docker run example1
```

### Output:

```
Hello, World!
```

## Passing one environment variables with `run` command

### Command:

```bash
docker run -e GREETING=Goodbye example1
```

### Output:

```
Goodbye, World!
```

## Passing multiple environment variables through `run` command

### Command:

```bash
docker run -e GREETING=Goodbye -e NAME=John example1
```

### Output:

```
Goodbye, John!
```
