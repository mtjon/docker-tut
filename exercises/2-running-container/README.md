# Running containers

Let's run some containers. A simple nginx-server provides a fast example:

```shell
docker run -p 80:80 nginx
```

Nothing appears to happen, but try to access the website on `127.0.0.1:80`; notice what happens in the shell.

> NOTE: You can close the interaction with the container using `ctrl` + `c`.

> If you're interested, take a look at the [documenation][docker-docs] for additional options (e.g. `--rm`, `--name`, etc.)

[docker-docs]: https://docs.docker.com/engine/reference/run/

For now, remove the container:

```shell
docker container ls
```

Look for the container you just created, note its name and run:

```shell
docker container rm -f <container_name>
```

## Pulling a specific container
You may have noticed docker downloading some files before the NGINX-container started. If docker does not have an image in its local cache, it will look for it on the Docker hub. You can also pull images manually, try:

```shell
docker pull jupyter/datascience-notebook
```

## Mounting volumes
It is likely that you'll want to use data in your containers. Given the ephemeral nature of containers, we need to find a solution for persistent storage. 
Luckily, we can mount data in our containers with `--volume` or `-v`. These can be **docker volumes** or **local directories**.

This can be done from the CLI with the following command:

```shell
docker run -v <docker volume>:<container mountpoint> <image>
```

