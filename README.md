# Modem: Broadcast

> Dockerized Icecast deployment for broadcasting to Modem listeners

[![Build Status](https://travis-ci.org/radiomodem/broadcast.svg)](https://travis-ci.org/radiomodem/broadcast)

## Deployment

The easiest way to deploy the setup to the production server at https://broadcast.radiomodem.dk is by first adding the server to [Docker Machine]:

```sh
$ docker-machine create -d generic \
    --generic-ip-address direct.broadcast.radiomodem.dk \
    --generic-ssh-user root \
    --generic-ssh-key ./secrets/digitalocean/ssh.enc \
    broadcast.radiomodem.dk
```

Next, connect to the server and boot up the setup using [Docker Compose]:

```sh
$ eval `docker-machine env broadcast.radiomodem.dk`
$ docker-compose up -d
```

That's it!

---

Copyright &copy; 2015-2016 Modem. Licensed under the terms of the [MIT license](LICENSE.md).

[Docker Machine]: https://docs.docker.com/machine/
[Docker Compose]: https://docs.docker.com/compose/
