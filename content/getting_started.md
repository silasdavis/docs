## Introduction to the Agreements Network

The Agreements Network is the legal layer for a networked world. Be part of the paradigm shift from legal services to legal products. Join the network, build products and services on top of it or reimagine what law looks like when it’s facilitated through technology. The possibilities are truly endless entering into this new paradigm.

After briefly introducing the technical aspects of the Agreements Network this page provides detailed API documentation for the REST API as well as the Contract API.

### The Agreements Network Architecture

The Agreements Network’s architecture leverages robust interconnected distributed systems.

<img src="images/AN-Cosmos-ETH.png" alt="Agreements Network Architecture" width="600" align="middle">

The Agreements Network is configured to significantly reduce the operational costs to users.By operating a sharded, optimized, zone, the Agreements Network is able to interact with Ethereum smart contracts without being exposed to backlogs or attacks in transactional processing within the Ethereum public blockchain.

### The Agreements Network Protocol

The Agreements Network provides structures that support defining and operating legal products.

<img src="images/workflow-07.png" alt="Agreements Network Protocol" width="600">

**Smart contract factory.** A smart contract factory generates other smart contracts. These factories enable reuse of and management of objects within the Agreements Network.

**Active Agreements.** Active Agreements are the most visible object within the Agreements Network. Active Agreements can be any type of legal artifact or instrument, automated with smart contracts workflows.

**Archetypes.** Archetypes are smart contracts factories. Each Archetype provides a blueprint for an individual Active Agreement.

**Archetype factory.** The Agreements Network Archetype Factory enables creative combinations of legal prose templates, standardized parameters, workflows and events to manufacture Archetypes that serve a particular legal services purpose. These archetypes are reusable and manageable as objects within the Agreements Network.

**Workflows.** A workflow smart contract monitors a specific sequence of events prescribed by an Active Agreement. Separate but related workflows are used during formation and execution of the same Active Agreement. Workflow smart contracts are designed using the Monax Business Process Modeling Engine.
Workflow factories. Workflow factories process a sequence of prescribed events, create a specific process contract and register smart contract that within the network. Active Agreements and Agreement factories use workflow factories to execute logic.

**Attestations.** Attestations are endorsements of fitness of purpose of an Active Agreement made by qualified individual. In return for putting their reputation at stake they are rewarded when a template consumer instantiates an agreement to which they have attested.

## Get started as a Network validator

<img src="images/users_of_AN-for_dev.png" alt="Agreements Network Users" width="500">

Network Validators assure the operational backbone for the network blockchain by bonding tokens and participating in the decentralized consensus mechanism. In return, Validators earn a Maintenance Fee over the lifecycle of each Active Agreement, based upon their positive contributions to the Agreements Network.

### Install Dependencies

The [Go](https://golang.org) programing language is used to build all the necessary tools. Please first install Go.

Second, we need to install [jq](https://stedolan.github.io/jq/download/) which is an `sed` like tool that makes it easy and simple to work with json files.

Lastly, you'll need [Git](https://gist.github.com/derhuerst/1b15ff4652a867391f03) installed on your machine.

### Create your own key and send us the information

Monax keys is a simple tool for generating keys, along with producing and verifying signatures. These features are exposed through the `monax-keys` tool. To install this run the following command:

```
go get github.com/monax/bosmarmot/keys/cmd/monax-keys
```

Run monax-keys server on the machine you intend to run as validator and save the process ID in a variable.

```
monax-keys server &
MONAX_KEYS_PID=$!
```

Next we generate a key with the below command. In the below command we do not give the key a passphrase to encrypt it on disk, but that option is up to you.

```
ADDR=$(monax-keys gen --no-pass)
```

**If and only iff** you wish to give it a passphrase then remove the `--no-pass` flag and manually copy and paste the address outputted into a shell variable in the following manner.

```
monax-keys gen
ADDR="COPY_AND_PASTE_THE_ADDRESS_OUTPUTTED"
```

Next also we will pass the new key's address into the `convert` command to give us the output we need.

```
monax-keys convert --addr $ADDR | jq '{address: .address, pubKey: .pub_key[1]}' > validator_info.json
```

The final step is to send validator_info.json to the [Network Validator Waiting List](mailto:join@agreements.network) and keep a note of the validator key you will need to configure your node. When you send the email, we'd love to learn a bit about your organization and why you'd like to join the validator pool.

### Boot your burrow node and connect into the network

Once we have confirmed that your key has been moved off the waiting list into the active network then you will boot your local node in the following manner.

(**N.B.** if you've stoped your keys server then restart it with the commands above. You'll also need to manually add your address into the `$ADDR` shell variable.)

First you will need [Hyperledger Burrow](https://www.hyperledger.org/projects/hyperledger-burrow) which is the base blockchain node used for the Agreements Network.

```
go get github.com/hyperledger/burrow/cmd/burrow
```

Now that we have `burrow` available on our machine we will set it up to connect to the network. First, we'll need to download the `genesis.json` which sets the beginning of the network along with the `base.toml` that has all the key variables preconfigured. They are both available with a simple curl command.

```
curl -L https://info.t1.agreements.network/genesis.json > genesis.json
curl -L https://info.t1.agreements.network/base.toml > burrow.toml
```

Now we are all set to boot our node and connect into the network. In the below command, you'll change `ORGNAME` to something which clearly identifies your node on the network.

```
burrow serve \
    --genesis genesis.json \
    --config burrow.toml \
    --validator-moniker ORGNAME-t1.agreements.network-validator \
    --validator-address $ADDR
```

### Operational Notes

One point of note is that if you have generated the key using a password you will add the `--validator-passphrase XXXX` flag with your password.

Another point is that if you are running this on a cloud box you may want to run within `tmux` or `screen` so that you can detach from the shell without shutting down the node. At a minimum you'll want to add `&` or `&disown` to the end of the command if you are not running within `tmux` or `screen`.

If you're running burrow in a cluster or via Docker then all the commands listed above can be handled with envirnoment variables (i.e., `BURROW_VALIDATOR_MONIKER`, `BURROW_VALIDATOR_ADDRESS` and `BURROW_VALIDATOR_PASSPHRASE`).

There is a `helm` [chart for burrow](https://github.com/kubernetes/charts/tree/master/stable/burrow) which may be helpful as well.

## Structure of the API documentation

The following sections provide in depth guidance and information on the Agreements Network's REST API and Contracts API.
