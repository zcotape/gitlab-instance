# Gitlab Instance

This is a ```docker-compose.yaml``` file for running GitLab instance running in version ```13.6.3-ce```. (Updated at 2020-12-14)

## Prerequisite
* Create a new registry authentication (RA) certificate and key
```bash
$ openssl req -new -newkey rsa:2048 -days 3650 -nodes -x509 -keyout ./registry-auth.key -out ./registry-auth.crt
```
* Copy or move RA files into folder named ```certs```
* Generate ```dhparam.pem``` file
```bash
openssl dhparam -out ./dhparam.pem 2048
```
* Copy or move ```dhparam.pem``` file into ```certs```

## Installation
Ensure your machine are installed ```docker``` and ```docker-compose```. For installing Docker in Ubuntu, please visit [Installing Docker Engine in Ubuntu](https://docs.docker.com/engine/install/ubuntu/) and [Installing Docker Compose in Linux](https://docs.docker.com/compose/install/). Then run

```bash
$ docker-compose up -d
```

If you are looking for each container's log, you can find from this command.

```bash
$ docker-compose logs <container-name> -f
```
