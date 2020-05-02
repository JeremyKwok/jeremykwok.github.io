# Getting Started
On Windows,
Download geth(go-etherneum) from the official website [here](https://geth.ethereum.org/downloads/).
Also, consider installing solidity compiler.

Run the following to sync up to a Rinkeby testnet

```
geth --rinkeby --syncmode "light"
```

In a seperate cmd window, run the following. This will open a console to interact with the net you have launched

```
geth --datadir=C:\Users\User\.rinkeby attach ipc:\\.\pipe\geth.ipc console
```

In the console 

```
personal.newAccount("password")
eth.accounts[0]
eth.getBalance(eth.accounts[0])
```

<details>
  <summary>What are the syncmodes?</summary>
  
  1. Full Sync: 
    Gets the block headers, the block bodies, and validates every element from genesis block.

  2. Fast Sync: 
    Gets the block headers, the block bodies, it processes no transactions until current block - 64(*). Then it gets a snapshot state and goes like a full synchronization.

  3. Light Sync: 
    Gets only the current state. To verify elements, it needs to ask to full (archive) nodes for the corresponding tree leaves.
</details>

<details>
  <summary>testnet?</summary>
  
  <details>
    <summary>What is a testnet?</summary>
  
    A Testnet is an Ethereum blockchain that uses identical technology and software as the “Mainnet” Ethereum blockchain. However, whereas the Mainnet network is used for “actual” transactions with “value”, Testnets are used for testing smart contracts and decentralized applications (“DApps”).
  </details>
  
  <details>
    <summary>Differences with mainnet?</summary>
  
    Blockchains are simply databases created by a network of computers that interact with each other, using purposefully designed software to get the computers on that network to agree (i.e. achieve “consensus”) on what data to add and store on the database. The only difference between Testnets and Mainnet is that they are operated by different networks; i.e. one group of computers has agreed to work with each other and form a Testnet network, while another group of computers has agreed to work together to serve as the Mainnet network.
    In order for a network of computers to agree to “work with each other”, they must agree on two parameters which uniquely identify each network:
    A network ID: 
        a number parameter which acts as an identifier for a network. For example, the Mainnet’s network ID is 1, while the other most commonly used Testnets have network IDs of 3, 4, and 42 for Ropsten, Rinkeby, and Kovan, respectively. So if you want to connect your computer to one of the blockchains, you run the Ethereum software and specify a network ID of 1 to connect it to the Mainnet, or you specify a network ID of 3 for Ropsten. That way, it knows which network of computers to connect to.
    Genesis block: 
        all computers on a network must agree to all the data stored on that blockchain, which of course must begin somewhere: the genesis block. The genesis block is block #1 of a network’s blockchain; it is just arbitrary data that has been designated as the beginning of that blockchain.
  </details>
  Read more from [here](https://medium.com/hummingbot/finance-3-0-wiki-testnet-vs-mainnet-8ab5b78d93)
</details>

