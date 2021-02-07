# Indicio Mediator Training - Lab 1

In this lab, we will be demonstrating mediation using three local agents: Alice, Bob, and a Mediator. We will connect Alice and the Mediator, arrange for mediation, and connect Alice and Bob through the Mediator.

## Setup

### Prerequisites
Before we get started, we will need to download and install the following:
- [Docker](https://docs.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Node JS](https://nodejs.org/en/download/) - Current LTS Release

### Obtain Code

#### Aries Toolbox

```shell
$ git clone https://github.com/hyperledger/aries-toolbox
```

#### Lab Agent Configuration
```shell
$ git clone https://github.com/indicio-tech/mediator-labs
```

### Start up the Toolbox

We will start by installing the Aries Toolbox and its dependencies and starting up an instance.

First, enter the toolbox directory:
```shell
$ cd aries-toolbox
```

Now, install dependencies:
```shell
$ npm install
```

Finally, start the toolbox with:
```shell
$ npm run dev
```

A window like the following should pop up:

![Toolbox Start](images/toolbox-0.png)