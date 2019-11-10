# Solidity-Interview-Question(500+)

# What is an Ethereum?
Ethereum is an open source, public, blockchain-based distributed computing platform.

# What is Smart Contract?
Smart Contract is an small program that runs on ethereum blockchain.

# In which language ethereum is written?
solidity is a language of ethereum. it is same like javascript. also vyper is also developing for next option for write smart contracts.

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

# what is EVM?
EVM stands for ethereum virtual machine. EVM is the runtime environment for smart contracts in Ethereum. It is not only sandboxed but actually completely isolated, which means that code running inside the EVM has no access to network, filesystem or other processes. Smart contracts even have limited access to other smart contracts.

# difference between geth/parity?

# what are dApps?
A decentralized applications called dApps. dApps is a computer application that runs on a distributed computing system. DApps have been mostly popularized by distributed ledger technologies (DLT), namely the Ethereum Blockchain, where DApps are often referred to as smart contracts. some of them are CryptoKitties, gitcoin.co,..


# describe about 'pragma'
The pragma keyword is used to enable certain compiler features or checks. A pragma directive is always local to a source file, so you have to add the pragma to all your files if you want enable it in all of your project. .

# default size of uint?
 it is 256 bits. if you wrote uint16 then it will 16 bits and subsequentially.
 
# size of ```address``` type?
it is 160 bits.

# what is expermental pragma?
it is used when you want to enable feature that are not enable by default.(e.g. ABIEncoder2, SMTChecker,.)

# SMTChecker use for?
it is used for additional safety warnings which are obtained by querying an SMT Solver.

# what is state variables?
state variables are variables whose values are permanently stored in contract storage.
```
pragma solidity >=0.5.0 <0.6.0;

contract SampleContract {
    uint sampleStateVariable; // state variable
    // ...
}
```
# what is function?
functions are the executables unit of code within a contract.
```
pragma solidity >=0.5.0 <0.6.0

contract SampleContract {
 function add() public { // function
  // to-do...
 }
}
```
# what is function modifiers?
function modifiers can be used to amend the semantics of functions in a declarative way.
```
pragma solidity >=0.5.0 <0.7.0

contract SampleContract {

  address public miner;
  
  modifier onlyMiner() {
    requier(
      msg.sender== miner
    );
    _;
  }
  
  function authorization() public view onlyMiner { // modifier usuage
    // to-do
  
  }
}
```

# what is events?
events are convenience interfaces with the EVM logging facilities.
```
pragma solidity >=0.5.0 <0.6.0

contrct SampleContract {
  event TokenRequested(address token, uint amount); // event
  
  function mint() public payable {
    // to-do..
    
    emit tokenMinted(msg.sender,msg.value); // Triggering event
  
  }
}
```

# what is enum types?
enums can be used to create custom types with a finite set of 'contants value'.
```
pragma solidity >=0.5.0 <0.6.0

contract SampleContract {
  enum Status { active, inactive, blocked} //enum
}
```
