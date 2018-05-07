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


### How to get started on the Agreements Network as Validator or Service Provider?

The Agreements Network serves the multi-sided needs of the legal sector.

<img src="images/users_of_AN-for_dev.png" alt="Agreements Network Users" width="500">

**Network Validators.** Network Validators assure the operational backbone for the network blockchain by bonding tokens and participating in the decentralized consensus mechanism. In return, Validators earn a Maintenance Fee over the lifecycle of each Active Agreement, based upon their positive contributions to the Agreements Network.

**Technical requirements for joining as a Validator**

1. **Install <a href="https://github.com/monax/bosmarmot">Bosmarmot</a>.** This is a monorepo containing condensed and updated versions of the Monax tooling. This repo intends to provide the basic tooling required to interact with a Burrow chain.
2. **Install <a href="https://golang.org/">Go</a>.** programing language 

3. **Create your own key.** Monax Keys is a simple dev-only tool for generating keys, producing and verifying signatures. These features are exposed through Monax tooling.
   **Go get monax-keys <a href="https://github.com/monax/bosmarmot/keys/cmd/monax-keys">here</a>.** Run monax-keys server on the machine you intend to run as validator _(requires the jq tool available on most distributions)_. We generate a key passing its address into the convert command to give us the output we need.

    - monax-keys convert --addr $(monax-keys gen --no-pass) | jq '{address: .address, pubKey: .pub_key[1]}' > validator_info.json

    - Send validator_info.json to **<join@agreements.network>** and keep a note of the validator key you will need to configure your node

4. Email public key and address to **<join@agreements.network>**

5. Boot your burrow node and connect into the network.

    Download genesis.json from **<a href="https://info.t1.agreements.network/genesis.json">** to your local directory

    Create a local config file 

    <code>Burrow -c base.toml configure</code>

    Change the seeds field in the <code>burrow.toml</code> to:

    tcp://1B1ECA9055642DC89C04ADC477FB08C9D09A9570@peers.t1.agreements.network/001:80,tcp://1B1ECA9055642DC89C04ADC477FB08C9D09A9570@peers.t1.agreements.network/002:80,tcp://1B1ECA9055642DC89C04ADC477FB08C9D09A9570@peers.t1.agreements.network/003:80,tcp://1B1ECA9055642DC89C04ADC477FB08C9D09A9570@peers.t1.agreements.network/004:80,tcp://1B1ECA9055642DC89C04ADC477FB08C9D09A9570@peers.t1.agreements.network/005:80,tcp://1B1ECA9055642DC89C04ADC477FB08C9D09A9570@peers.t1.agreements.network/006:80

    Change the moniker field in the <code>burrow.toml</code> to: 

    <code>ORGNAME-t1.agreements.network-validator</code> 

    Start burrow with the local <code>burrow.toml</code> and local <code>genesis.json</code>

6. **Monitoring considerations**
Network 


**Services Providers.** Legal products often entail leveraging point solutions for things like identity, market information, payments, insurance, etc. The Agreements Network’s public blockchain protocol is a stable base on which Service Providers can build solutions linked to the vital commercial data contained within it.


### What is Burrow?

Hyperledger Burrow, commonly referred to as Burrow, is a permissioned Ethereum smart-contract blockchain node. It executes Ethereum smart contract code on a permissioned virtual machine. Burrow provides transaction finality and high transaction throughput on a proof-of-stake Tendermint consensus engine. Burrow is built for a multi-chain universe with application specific optimization in mind. Burrow as a node is constructed out of three main components; the consensus engine, the permissioned Ethereum virtual machine and the rpc gateway.

Burrow has been architected with a longer term vision on security and data privacy from the outset, featuring cryptographically secured consensus,remote signing, secure signing and multi-chain universe.
For all details and to install Burrow click <a href="https://github.com/hyperledger/burrow">here</a>.


### Structure of the API documentation

The following sections provide in depth guidance and information on the Agreements Network's REST API and Contracts API.