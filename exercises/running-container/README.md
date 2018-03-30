# Running containers

Let's run some containers. A simple nginx-server provides a fast example:

```shell
docker run -p 80:80 nginx
```

Nothing appears to happen, but try to access the website on `127.0.0.1:80`; notice what happens in the shell.

> NOTE: You can close the interaction with the container using `ctrl` + `c`.

