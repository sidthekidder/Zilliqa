# Zilliqa (codename _Durian_)
[![Build Status](https://travis-ci.org/Zilliqa/Zilliqa.svg?branch=master)](https://travis-ci.org/Zilliqa/Zilliqa)

## Overview
Zilliqa is a new blockchain platform capable of processing thousands of transactions per second with sharding built into it. With sharding, Zilliqa has the potential to match throughput benchmarks set by traditional payment methods (such as _VISA_ and _MasterCard_). More importantly, Zilliqa’s transaction throughput increases (roughly) linearly with its network size.

## Available Features
The current release has the following features implemented:
* Proof of Work 1 (PoW1) and 2 (PoW2) for joining the network
* Network sharding
* Directory Service
* Consensus for DS block, Sharding structure, Shard Microblock and Final block 
* [EC-Schnorr signature](https://en.wikipedia.org/wiki/Schnorr_signature)
* Data layer and accounts store 
* Looking up nodes to allow new nodes to join 
* Persistent storage for transactions
* [Merkle Patricia tree](https://github.com/ethereum/wiki/wiki/Patricia-Tree)
* Transaction verification

In the coming months, we plan to have the following features:
* View change
* Gossip protocol for network message broadcasting
* Incentive structure
* Smart contract design and implementation
* GPU support for PoW
* Zilliqa Wallet 
* Further unit and integration tests
* Enhancement of existing features
* More operating system support
* And much more ...

## Minimum system requirements
To run Zilliqa, we recommend the following minimum system requirements:
* x64 _Linux_ operating system such as _Ubuntu_
* Recent dual core processor
* 2 GB RAM

## Dependencies
To compile and run the Zilliqa codebase, you will need the following dependencies to be installed on your machine:
* `Boost` 
* `OpenSSL`
* `JsonCpp`
* `LevelDB`
* `CMake`
* `build-essential`
* `json-rpc-cpp`
*  pkg-config 

For a _Debian_-based system, you can use the following command to install the dependencies:  
```bash
sudo apt-get install libboost-all-dev libssl-dev libleveldb-dev libjsoncpp-dev libsnappy-dev cmake libjsonrpccpp-dev build-essential pkg-config
```

For _Ubuntu_ versions less than 15.10, you must install libmicrohttpd and make libjson-rpc-cpp manually using the following steps:
```bash
sudo apt-get install curl libargtable2-dev libhiredis-dev
wget -c http://ftp.gnu.org/gnu/libmicrohttpd/libmicrohttpd-0.9.59.tar.gz
(tar zxf libmicrohttpd-0.9.59.tar.gz; cd libmicrohttpd-0.9.59; ./configure; make; sudo make install; cd ..; rm -fr libmicrohttpd-0.9.59)
wget -O libjson-rpc-cpp-1.1.0.tar.gz https://github.com/cinemast/libjson-rpc-cpp/archive/v1.1.0.tar.gz
(tar xzf libjson-rpc-cpp-1.1.0.tar.gz; cd libjson-rpc-cpp-1.1.0; cmake . && make; sudo make install; sudo ldconfig; cd ..; rm -fr libjson-rpc-cpp-1.1.0)
```

For higher _Ubuntu_ versions, you may install libjson-rpc-cpp directly:
```bash
sudo apt-get install libjsonrpccpp-dev
```

For Mac OS X (experimental), you can use the following command to install the dependencies:  
```bash
brew install pkg-config jsoncpp leveldb libjson-rpc-cpp
```

# Running Zilliqa locally (using 10 shard nodes and DS node locally)  
1. Build Zilliqa from the source.  
` ./build.sh`

2. Run the local testnet script  
`./tests/Node/test_node_simple.sh`  

3. Logs of each node can be found at `./local_run`

4. To terminate Zilliqa,   
`pkill zilliqa` 

## Running a Zilliqa Node on the public testnet 
Coming soon...

## For further enquiries
If you have issues running a node, please feel free to join our [Slack](https://invite.zilliqa.com/) and ask questions. You can also submit your issue at our [Github repository](https://github.com/Zilliqa/zilliqa/issues)

## Licence 
You can view our [licence here](https://github.com/Zilliqa/zilliqa/blob/master/LICENSE).

