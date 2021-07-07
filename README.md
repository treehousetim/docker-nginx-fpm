# Generic Docker Website Setup
This is my standard way of spinning up a PHP/NGINX docker environment to develop with.

[TOC]

## Folders
Place your files into `/site`

## Configuration

Create a .env file in the root containing values for the following keys:

```
DB_ROOT_PASS
DB_APP_NAME
DB_APP_USER
DB_APP_PASS
```

### cli, cli2
These allow for a script to be run on the command line. `./cli` and `./cli2` are identical except for docker container name - it's to allow multiple cli scripts to be run simultaneously.

### down
Down's the entire docker stack and removes the container using `docker stop` and `docker rm`

### login *containername*
`./login [docker container name]` allows you to log into the container running on a given name.  useful only for debugging weird issues.

### logview
a shortcut to `docker-compose logs -f` - used to view follow log entries coming from the docker containers.

### php
`./php` is a way to run any php command in the docker container for php cli.

### up
Brings the entire docker dev stack up.
