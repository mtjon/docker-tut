# Validating your Docker installation
We'll be using Docker for the coming exercises. You should already have it installed, we can easily validate this by running the following commands in your shell (CMD, PowerShell, Bash, Terminal, etc.):

```shell
docker version
```

This will return a `Client` and `Server` version.

You can also run `docker info` to see additional information.

## Management commands
Docker commands are of the form:
```shell
docker <command> <sub-command> (options)
```

Those who have already been using docker for a while might be used to running commands like `docker run ...` or `docker images`. This was of the form:

```shell
docker <command> (options)
```

The managements commands allow for clearer distinction between categories of commands, but the old format is still supported in most (all?) cases, as such:
```shell
docker image ls
```
and
```shell
docker images 
```
should both list you your running containers.
