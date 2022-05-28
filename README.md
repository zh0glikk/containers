# Cosmos Docker Convienence Images


![build](https://github.com/faddat/archlinux-docker/workflows/build/badge.svg)

Standardized Cosmos ecosystem Docker images supporting the omnibus branch of tm-db

Please note that if you are using the omnibus branch of tm-db, YOU SHOULD NOT USE IT ON A VALIDATOR.

These images are designed to boost RPC and relay capacity througout the cosmos ecosystem.


### Note
They won't work with rocksdb in the master tm-db branch.


### Use case

These images contain genesis.json located at /genesis.json

Where I could find it I have also included an address book.  Make a docker swarm on a machine with an nvme 1.4+ pcie4.0+ SSD.  Then simply:

```bash
docker service create --publish published=25557,target=26657 --publish published=1317,target=1317 --publish published=9090,target=9090 --publish published=8545,target=8545 --publish published=8546,target=8546--replicas 5 --name evmos ghcr.io/faddat/evmos
```


### More info

This repo doesn't deal with atomation.  For automation, including build of binaries, head to 

https://github.com/notional-labs/cosmosia



