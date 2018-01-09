# Docker-Cassandra

__A container-based multi-node Cassandra cluster__


docker-cassandra| .
:-------        |---------------------------------:
Author          | [M. Massenzio](http://codetrips.com)
Version         | 0.1.0
Updated         | 2017-06-03

## Overview

Originally based on [this blog entry](http://abiasforaction.net/apache-cassandra-cluster-docker/), modified and updated to fix a few nits and networks issues.

### Usage

Use with [Docker Compose](https://docs.docker.com/compose/compose-file/):

    $ docker-compose up -d

To install `Compose`, use:

    $ pip install -U docker-compose

### Connecting to the Cluster

The `seed node` (`DC1N1`) exposes ports `9042, 9160` so you can connect from your development host using a recent download of Cassandra:

    $ cqlsh 127.0.0.1 9042 --cqlversion 3.4.4

both arguments **are required**.

