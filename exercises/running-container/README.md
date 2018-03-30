# Running containers

## Basic NGINX
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

## Mount a volume

Usually, you'll want to use data in your containers. As they ephemeral by nature, you will need to store this externally for it to be persistent. Let's have a look at mounting a local directory:

```shell
docker run --rm -p 80:80 -v $(pwd):/etc/www