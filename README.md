# my-blockchain-notes

Resource:
https://www.youtube.com/watch?v=M576WGiDBdQ&ab_channel=freeCodeCamp.org
# Full-blockchain-solidity-course-py
(search in github for the codes)
-> documentation is very important
-> after 30 minutes, take a break
-> Engage with the community (stackoverflow,stackovereth)

Bitcoin allow to make peer to peer transaction
It is powered by cryptography.
for more look in the whitepaper of the bitcoin

after that ethereum protocol comes to play, which used the same blockchain infrastructure with more features. was released in 2015 

Smart contracts allow for agreements without 3 party companies or goverments.

in 1994 a man called nick szabo developed a technology called smart contracts. 

Smart contracts are self executing sets of instructions, without 3rd parties. They come to live on a blockchain.

Smart contracts are the core thing, that we will work with and develop. They are similar to the normal contracts but instead of creating the contract on paper or on computer, it is all written in code.  

To Sum Up:
Smart contracts are self executing on a decentralized network and written in codes.

The Flow/problem in the blockchain is **the oracle Problem**
means that everything happend in the smart contracts or in the blockchain are isolated from the real world

Blockchain Oracles are devices that bring data into blockchain or execute something on the blockchain. 
The problem here is that in order to get the data from real world to the blockchain, they need a centralized node that do that!!!

Hybrid Smart contracts ?
But we have smart contracts like chainlink that get the data from real world to the blockchain on decentralized node.

DApp = Smart contract = Decentralized App(a combination of serval smart contracts)

Understanding Ethereum means we will understand the majority of these platforms.

Summary: 
- Blockchain was the first one to take blockchain mainstream 
- Bitcoin is like a digital gold
- Ethereum allows for smart contracts
- Smart contracts can access external data/computation outside the blockchain using oracles (devices)
Chainlink a powerfull decentralized oracle network and it allows to build hybrid smart contracts.
- hybrid smart contracts are combine of on-chain and off-chain components

Blockchain / Smart contracts features:
1. **Decentralized**. (No centralized source that can control the blockchain) - Ex: we have banks that control us and they have the power to freeze our money or do anything 
2. **Transparency & Flexibility** means everything happens on blockchain can be seen by everyone  (but it is super anonymous)
3. **Speed and Efficiency**  Transfering money in seconds/minutes unlike banks that may take some days or weeks.
4. **Security & Immutability** Immutability means data can't be changed/tempared/corapted in any shape of forms, which allows us to have a really massive security on our data and on our transaction or anything on the like. It is enough to have only one nodes to make data stay secure (there is a hundreds of thousands node in the worlds), which means if all nodes are down, we lose our data!!!!
Hacking the blockchain is nearly impossible. The Data are locked on the blockchain for ever and all you need to access it, is to have a private key (password).
5. **Remove of countryparty risk** Blockchain allows us to move from brand based agreements to a math based agreements. Like ensuring companies which tries everything to not to pay for its client, because they want to make money, so with blockchains they will not be able to make such stuffs, because everything is done by code, math and numbers. 
6. **Trust Minimized Agreements**

There is no centralized controling body, that influencing every action that we made. All the rules are the same and no body is getting a special treatments

**DAO's**: Decentralized Autonomous Organization. Organizations which live online on the blockchain.


Metamask wallet
etherscan

a wallet has:
- **mnemonic**, which are some words for your wallet as a password (a key for all account on that wallet)
- **private key**, which is a key for one account on that wallet (a key for one account on that wallet)
- **public address**, an address to send/recieve money with it.

There is Test networks (like Rinkeby, Kavan or Ropsten) for testing smart contracts with not with real money.
**Testnets** are free and for testing smart contracts for our apps 
**Mainnet** cost money and are considered "live" 

## Testnets
**Faucet** is an application that gives us free test ethereum(tokens)
-> To get free test Ethereum:
faucet.rinkeby.io
-> To see the made transactions by rinkeby network on the wallet: 
rinkeby.etherscan.io

Etherscan is a **block Explorer**
**block Explorer** is an application that allows us to "view" transactions that happen on a blockchain.

- **Gas** is a unit of computational measure. The more computation a transaction uses the more "gas" you have to pay. 
- Every transaction that happens on-chain pays a "gas free" to node operators (everything to do on blockchain will cost gas)
- Sending 1 ethereum to one address will be cheaper that sending 1 ethereum to 1000 addresses.
- Transaction fee : (eth-converter.com "gwei wei eth")
**Gas**: Measure of computation something use
**Gas Price**: How much it costs (in gwei) per unit of gas
**Gas Limit**: Max account of gas that can be used in a transaction
**Transaction fees**: Gas used x Gas Price
ie: if we make a transaction that costs 21,000 gas
and one gas = one gwei, that means we will pay 21,000 gwei in a transaction fee

we can make a transaction with Gas Price= 1 Gwei and Gas Limit = 21,000 (the max amount fees to pay for this transaction)

why we need something to put the Gas price much more then 1 Gwei ?

The blockchain (blockchain node) can only process/put so many transactions at a time into the block. If there are a lot of people making transactions, the nodes will pick the transaction with high Gas price to process their transaction. This called **ethgasstation**

Gas Price is based off the "demand" of the blockchain.
The more people want to make transactions, the higher the gas price, and therefore the higher the transaction fees.


## Understanding Blockchain
andersbrownworth.com/blockchain/hash

**Block** 
A block is a list of transactions mined together 
A block contains: 
1. Block number
2. Nonce (the value, that makes the hash starts with 0000 and also used to define the transaction number for an address) 
3. Data (ex: transactions)
4.  Hash 
-> In block a hash has to start with 0000, so the Nonce will try from 0 and up to until the hash start with 0000 
**Blockchain**
Has many Blocks 
Block - Nonce - Data - Prev - Hash 
**Genesis Block**: the first block in the blockchain 
If you break a block that blocks after will be broken and not valid, so blockchain is immutable. anything you change one thing you destroy the blocks after and the node will be ignored from the other nodes -> that what makes blockchain very secure. 

if someone is controlling the blockchain, he is able to fix the destroyed blocks but if the blockchain is decentralized, there will be many peers, and all peers has to match up (has the same hash) to make the transaction.
**Tokens**
Block - Nonce - Tx - Prev - Hash 
Tx contains many transactions, so the block contain many transactions.

-> How can we know that **A** send money to **B**? 
because of the private and public key 
**Private key**: is only know to the key holder, and used to "sign" transactions to be sent
**Public key**: is derived by using digital signature algorithm using your private key. public key is used to verify the transaction. Your ethereum address is a piece of your public key

Private key >create> Public Key >create> Address 

**Mining**
It is a process of finding the "solution" to the blockchain "problem". 
In our example, the "problem" was to find a hash that starts with 0000
Nodes get paid for mining blocks. (nodes could be any device running a blockchain software, that is working to find a hash start with 0000 for blocks)


1:12:00
**Consensus** is the mechanism used to agree on the state of a blockchain.
Like: if a peer changes something in the block and the other don't the majority will rule and kick that peer out.

Sybil Resistence: 
has 2 types:
1. Proof Of Work (PoW) who is the block author 
2. Proof Of Stacke 

Nakamoto Consensus 

Block Confirmations

Gas fee (transaction fee), who is getting this money ? 
It is going to the miners or validators
In PoW, they called miners
In PoS, they called validators

1. Proof Of Work: 
In PoW system all the miners nodes are competing each other to find the Nonce value to make the hash starts with 0000. the first node who finds the solution, will get the money (transaction fee + block rewards)
It uses a lot of energy

Sybil Attack: Attacker create a sudo anonymous accounts to try to influence the network.
51% Attack: 
Longest Chain Rule 

2. Proof Of Stack:
Uses much less Energy
Only one Nodes do 

1:25:00

Scalability:

Sharding:

Layer 1: Base Layer blockchain Implementation
Layer 2: Any Application built on top of the layer 2

Rollups:
[1:28:00]

Sum Up:
-> ETH and BTC are Proof of work blockchains
-> ETH 2.0 will be Proof of Stake
-> PoW & PoS are sybil resistance mechanisms 
-> The bigger the blockchain, the more secure
-> Consensus is how blockchains decide what the state of the chain is 
-> Sharding and rollups are solutions for the scalability issues on layer 1
-> Layer 1 is any base blockchain implementation like BTC or ETH
-> Blockchain Scalability problems is that, there is no enough space for the amount of transactions that needed to be done, this leads to very high gas fees 
-> Gas Prices are how much it costs to interact with the blockchian (perform executions on-chain)

Make account on stackoverflow + ethereum.stackexchange + github
1:31:00

remix.ethereum.org 

