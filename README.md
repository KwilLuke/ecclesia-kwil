# Ecclesia Network

Ecclesia is is a decentralized social network that guarantees the right to free speech on the internet. It is built using [Kwil](<https://docs.kwil.com>), a framework for building decentralized storage networks.

![banner](./assets/logo.png)

## Getting Started

### Installation

To get started with development, you will need to install:

- [Go 1.23+](<https://go.dev/doc/install>)
- [Docker](<https://docs.docker.com/engine/install/>)

### Running Locally

To run a private node locally, run a Postgres instance configured for the Kwil protocol and the main application in this repo:

_Running Postgres:_
```shell
docker run -d -p 5432:5432 --name kwil-postgres -e "POSTGRES_HOST_AUTH_METHOD=trust" \
    kwildb/postgres:latest
```

_Running ecclesia-kwil:_
```shell
go run cmd --autogen
```

## Build From Source

To build a Ecclesia node from source, use the `scripts/binary.sh` script:

```shell
./scripts/binary.sh
```