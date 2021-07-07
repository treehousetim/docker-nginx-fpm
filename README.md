# Generic Docker Website Setup
This is my standard way of spinning up a PHP/NGINX docker environment to develop with.

[TOC]

## Folders
Place your files into `/site`

## Docker

### cli, cli2, cli-profile
These allow for a script to be run on the command line. `./cli` and `./cli2` are identical except for docker container name - it's to allow multiple cli scripts to be run simultaneously.  These are shortcuts to `php cli.php` the entrypoint into the OWNx web app.

### down
Down's the entire docker stack and removes the container using `docker stop` and `docker rm`


### login *containername*
`./login [docker container name]` allows you to log into the container running on a given name.  useful only for debugging weird issues.

### logview
a shortcut to `docker-compose logs -f` - used to view follow log entries coming from the docker containers.

These shortcuts create new migrations according to the predefined OWNx templates in the root phinx directory.

### php
`./php` is a way to run any php command in the docker container for php cli.

### up
Brings the entire docker dev stack up.
