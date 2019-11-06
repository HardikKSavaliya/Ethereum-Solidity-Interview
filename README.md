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

# How can you make ethereum network ASIC resisitance?

