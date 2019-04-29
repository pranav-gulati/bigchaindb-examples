# Tokain Starter Code
This repo contains starter code for the Tokain project. It includes an example application that allows us to post messages to the BigChainDB database as well as an example of how to connect an angular frontend for the application. This models the core code needed to record verified information onto the blockchain and have an updated frontend. 

### Dependencies

The application can be [run via Docker](http://bigchaindb-examples.readthedocs.io/en/latest/install.html#the-docker-way)
(**recommended**), but, if you'd like, you can also [run them locally](http://bigchaindb-examples.readthedocs.io/en/latest/install.html#install-from-source)
with the following system dependencies:

 - OS dependencies: see [setup BigchainDB & RethinkDB](https://bigchaindb.readthedocs.io/en/latest/installing-server.html#install-and-run-rethinkdb-server)
 - python>=3.4
 - node>=5.3 using [nvm](https://github.com/creationix/nvm#installation) (**recommended**), or [manually](https://nodejs.org/en/download/)
 - [npm>=3.3](https://docs.npmjs.com/getting-started/installing-node) (should be installed with node)

## Quick start


### Docker

To run via Docker, set up your docker environment as necessary and:

```bash
$ make
```

**Note**: If using docker-machine, you'll have to run `make` with your docker-machine ip:

```bash
$ DOCKER_MACHINE_IP=$(docker-machine ip) make
```

The app will be available at <http://localhost:33000> (replace ``localhost`` with your
docker-machine ip as necessary).

### Locally

If you'd like to run these examples locally (preferably in a virtualenv), you can do so using
the handy CLI:

```bash
$ bigchaindb-examples --help

# Start everything
$ bigchaindb-examples start --init --all

# Reset everything
$ bigchaindb-examples reset-all
```

The app will be available at <http://localhost:3000>.

This is a simple logging app, modeling the behavior needed for posting campaign donations to BigChainDB, the core functionality of the Tokain application. 

<p align="center">
  <img width="70%" height="70%" src ="./docs/img/tokain-logging" />
</p>

### Use cases

- Immutable logging of data
- Notarization of data, text, emails

### Functionality

#### Create assets
- with arbitrary payload
- and an unlimited amount

#### Retrieve assets
- that you currently own (like UTXO's)
- by searching the asset data/payload
- state indicator (in backlog vs. on bigchain)

#### What this app doesn't provide

- Proper user and key management
- Transfer of assets
