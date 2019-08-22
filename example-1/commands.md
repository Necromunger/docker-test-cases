# Example 1

Default environment variables and passing environment variables through run command.

## Giving only one environment variable through `run` command

### Command:

```
docker run example1
```

### Output:

```
Hello, World!
```

## Giving only one environment variable through `run` command

### Command:

```
docker run -e GREETING=Goodbye example1
```

### Output:

```
Goodbye, World!
```

## Giving multiple environment variables through `run` command

### Command:

```
docker run -e GREETING=Goodbye -e NAME=John example1
```

### Output:

```
Goodbye, John!
```
