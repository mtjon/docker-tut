# Docker-compose
Using compose, we can configure an entire docker-setup and start/ stop it from the CLI with a single command.

# Exercise
We built a redis-enabled notebook in the previous exercise, in this exercise we will extend it to include a redis database. It should be accessible by the notebook.

## instructions
- use `docker-compose` version 2.0 or greater
- create two services:
    - a jupyter notebook: use the previous redis-enabled notebook
    - a redis database, an [official docker image][redis-image] is availble on the Docker hub:
        - read the instructions on docker hub
- create a data-volume for the redis data:
    - [docker-volume docs][docker-volume-docs]
    - check the [official docker repo][redis-image] for instructions
- bonus: use a `.env`-file for configuring values:
    - can be accessed in `docker-compose.yml` through `${VAR}`


[redis-image]: https://hub.docker.com/_/redis/
[docker-volume-docs]: https://docs.docker.com/compose/compose-file/#volumes