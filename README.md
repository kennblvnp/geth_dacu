
# Geth_DACU

# Tools  
geth https://geth.ethereum.org/downloads/  

# Deploy Genesis Block (node 1) 
`geth --datadir "<project>/<directory>/node1" init genesis_puppeth.json`

> A **genesis block** is the first **block** of a **block** chain. Modern versions of Bitcoin number it as **block** 0, though very early versions counted it as **block** 1. The**genesis block** is almost always hardcoded into the software of the applications that utilize its **block**chain.

# Enable Blockchain RPC (node 1) 
`geth --datadir "<project>/<directory>/node1" --networkid 5432 --rpc --rpcport 5000 --rpcaddr 127.0.0.1 --rpccorsdomain "*" console 2>console.log`


> - Remote Procedure Call (RPC) is a protocol that one program can use to request a service from a program located in another computer on a network without having to understand the network's details. A procedure call is also sometimes known as a function call or a subroutine call.  
>
> - rpccorsdomain - allow your web browser to get access to your local Ethereum node 
> (eg. --rpccorsdomain "*.myetherwallet.com,*.ethereum.org")  

# Deploy Genesis Block (node 2) 
`geth --datadir "<project>/<directory>/node2" init genesis_puppeth.json`  

# Enable Blockchain RPC (node 2) 
`geth --datadir "<project>/<directory>/node2" --port 30304 --networkid 5432 --rpcport 5000 --rpcaddr 127.0.0.1 console 2>console.log`  


## basic console commands
*reference URL: https://github.com/ethereum/go-ethereum/wiki/Command-Line-Options*

**Common commands**
`admin.nodeInfo`
`personal.newAccount()`
`miner.start(1)`
`miner.stop()`
`eth.blockNumber`
`eth.getBlock(eth.blockNumber).miner`
`admin.addPeer("enode:.....<ip_address>:<port>")`
`admin.peers`