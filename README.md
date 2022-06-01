# Solidity-Interview-Question(500+)

# What is an Ethereum?
Ethereum is an open source, public, blockchain-based distributed computing platform.

# What is solidity?
Solidity is an object-oriented, high-level language for implementing smart contracts. Smart contracts are programs which govern the behaviour of accounts within the Ethereum state.

# What is Smart Contract?
Smart Contract is an small program that runs on ethereum blockchain. it have all charecterstics of blockchain.

# In which language ethereum is written?
solidity is a language of ethereum. it is same like javascript. also vyper is also developing for next option for write smart contracts.

# Describe Ethereum node?
Node is copy of chain data. This means that you can participate in validating transactions and blocks on the Ethereum blockchain. The two most common clients for running nodes are Geth and Parity. 

# What is genesis.json?
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

# What is mist?

# GHOST protocol?

# Account State in ethereum?
* nonce: If the account is an externally owned account, this number represents the number of transactions sent from the account’s address. If the account is a contract account, the nonce is the number of contracts created by the account.
* balance: The number of Wei owned by this address. There are 1e+18 Wei per Ether.
* storageRoot: A hash of the root node of a Merkle Patricia tree. This tree encodes the hash of the storage contents of this account, and is empty by default.
* codeHash: The hash of the EVM code of this account. For contract accounts, this is the code that gets hashed and stored as the codeHash. For externally owned accounts, the codeHash field is the hash of the empty string.

# what is EVM?
EVM stands for ethereum virtual machine. EVM is the runtime environment for smart contracts in Ethereum. It is not only sandboxed but actually completely isolated, which means that code running inside the EVM has no access to network, filesystem or other processes. Smart contracts even have limited access to other smart contracts.

# Difference between geth and parity?

# Merkle Patricia Tree?

# what are dApps?
A decentralized applications called dApps. dApps is a computer application that runs on a distributed computing system. DApps have been mostly popularized by distributed ledger technologies (DLT), namely the Ethereum Blockchain, where DApps are often referred to as smart contracts. some of them are CryptoKitties, gitcoin.co,..

# describe about 'pragma'
The pragma keyword is used to enable certain compiler features or checks. A pragma directive is always local to a source file, so you have to add the pragma to all your files if you want enable it in all of your project. .

# default size of uint?
 it is 256 bits. if you wrote uint16 then it will 16 bits and subsequentially.
 
# size of ```address``` type?
it is 160 bits.

# Type of accounts in Ethereum?
* External accounts: controlled by public-private key pairs
* Contract accounts: which are controlled by the code stored together with the account.

# what is expermental pragma?
it is used when you want to enable feature that are not enable by default.(e.g. ABIEncoder2, SMTChecker,.)

# What is payload?


# Difference between ```mint``` and ```send``` functions?
The mint function sends an amount of newly created coins to another address while The send function can be used by anyone (who already has some of these coins) to send coins to anyone else.

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
  
  function 
  
  
  () public payable {
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

# how can you define null value in variable?
In solidity there is no concept of null or undefined.

# how nmany value types exist in solidity?
* boolean(bool)
it can be true else false
* integers(int/unit)
signed and unsigned integers of various sizes.
* fixed point numbers(fixed/ufixed)
signed and unsigned fixed points number of various sizes.
* address(address/ address payable)
* contract
* fixed-size byte arrays
* dynamically-sized byte array
* address literals
* rational and integer literals
* string literals and types
* hexadecimal literals
* enums
* function types


# you can convert address payable to address types?
yes, but vice versa is not allowed.

# Member of addresses?
* balance and transfer
* send
* call,delegatecall and staticcall

# Difference between send and transfer?
send is the low-level counterpart of transfer. if the execution fails due to an whatever reason. the current contract will not stop, but the send will return false.

# Default function is external or internal?
it has internal. you can omit the internal keyword.

# How many data location are exist?
* memory
* storage
* calldata

# What will be default value of enum?
first element of enum is default value for that.

# How many types of visibilities for functions and state variables?
* external
External functions are part of the contract interface, which means they can be called from other contrancts and via transactions
* public
Public functions are part of the contract interface and can be either called internally or via messages. 
* internal
functions and state varialbles can only be accessed internally.
* private
private functions and state variables are only visible for the contract they are defined in and not even derived contracts.


# Where can we use view keyword in functions?
view are used to not modifiy the state of functions. below scenario count to modified state
* Writing to state variables.
* Emitting events.
* Creating other contracts.
* Using selfdestruct.
* Sending Ether via calls.
* Calling any function not marked view or pure.
* Using low-level calls.
* Using inline assembly that contains certain opcodes.

# What is pure functions? 
functions can be declared pure in which case they promise not to read from or modify the state.
below scenario count to read from state
* Reading from state variables.
* Accessing address(this).balance or <address>.balance.
* Accessing any of the members of block, tx, msg (with the exception of msg.sig and msg.data).
* Calling any function not marked pure.
* Using inline assembly that contains certain opcodes.
  
  
# Difference betweeen ERC-20 and ERC-721 tokens?

# Default value of boolean unassigned variable?
it will be false.
