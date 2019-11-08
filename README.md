# Solidity-Interview-Question(500+)

# What is an Ethereum?
Ethereum is an open source, public, blockchain-based distributed computing platform.

# What is Smart Contract?
Smart Contract is an small program that runs on ethereum blockchain.

# Describe Ethereum node?
Node is copy of chain data. This means that you can participate in validating transactions and blocks on the Ethereum blockchain. The two most common clients for running nodes are Geth and Parity. 

# what is genesis.json?
The genesis file is json structured file which describes among the other the initial settings needed to initialize the blockchain. It is the initial block for ethereum blockchain
```
{
  "config": {
        "chainId": 0,
        "homesteadBlock": 0,
        "eip155Block": 0,
        "eip158Block": 0
    },
  "alloc"      : {},
  "coinbase"   : "0x0000000000000000000000000000000000000000",
  "difficulty" : "0x20000",
  "extraData"  : "",
  "gasLimit"   : "0x2fefd8",
  "nonce"      : "0x0000000000000042",
  "mixhash"    : "0x0000000000000000000000000000000000000000000000000000000000000000",
  "parentHash" : "0x0000000000000000000000000000000000000000000000000000000000000000",
  "timestamp"  : "0x00"
}
```
# Ethereum node types?
* Light Clients: Requires no validation, requests the current state from the P2P network to verify current state (fine for processing payments and simple contract calls), but your validation is out-sourced to other fullnodes with the necessary information.
* Fast Node (Fast Sync/Warp Sync): Will not validate intermediate states during the initial sync, will validate everything else after that, however. This allows older data to be pruned that likely has nothing to do with your transactions
* Full Node: As described above, validates everything, and will prune old intermediate states from memory, and will keep an archive of future state trie updates.
* Archive Node (Historical Node): Validates and stores all intermediate states, nothing is pruned, all state transitions for accounts are retrievable. Future state trie updates and full intermediate states are stored.

# How can you make ethereum network ASIC resisitance?

# what is mist?

# difference between geth/parity?

# what is dApps?
