# mariadb-connector-c-craftinfo

#### Craftinfo for mulle-sde to build [mariadb-connector-c](https://downloads.mariadb.org/connector-c/)

This is only needed for macOSX if the `<unistd.h>` header is not found.

```
mulle-sde dependency add --c --tag 3.1.12 --address mariadb-connector-c 'https://mirror.wtnet.de/mariadb//connector-c-${MULLE_TAG}/mariadb-connector-c-${MULLE_TAG}-src.tar.gz'
mulle-sde dependency mark mariadb-connector-c singlephase
```

## Prerequisite

You will also need [openssl-craftinfo](//github.com/craftinfo/openssl-craftinfo).
Be sure to move a `openssl` dependency ahead of `mariadb-connector-c` with

```
mulle-sde dependency move mariadb-connector-c bottom
```