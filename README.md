# docker-isis-security-db

A docker container for keeping
[isis-module-security](https://github.com/isisaddons/isis-module-security)'s
RDBMS part in a [MariaDB](http://mariadb.org) server.

### Run as server

The most simple way to run the container is to specify the root password with
`-e`:

```
docker run --name mariadb -e PASSWORD=root -d mcreations/isis-security-db
```

#### Location of data

The data is stored in the `/data` directory
inside the container. You can mount a volume from the host with:

```
docker run -v $HOME/data:/data -e PASSWORD=root -d mcreations/isis-security-db
```

### More Information

For more information please see the README of parent Docker container
[here](https://github.com/m-creations/docker-openwrt-mariadb/blob/master/README.md)
