# RChain-Learning
Learning group for the RChain platform

## Overview

- Symbol: [RHOC](https://coinmarketcap.com/currencies/rchain/)
- Exchange: [KuCoin](https://www.kucoin.com/#/trade/RHOC-ETH)

RChain is a new Blockchain platform that focuses on concurrency :
- operate in parallel
- Single thread using exclusively no-blocking operations.

**Multithreading = several single-threaded operations in parallel to avoid the bottleneck of a single thread.**
**Concurrency = Not having the bottleneck at all.**

To understand concurrency, here is an example :

*Imagine that you have a road. Without concurrency you can have only one lane. You can increase the speed at which the vehicles run, but still each vehicle is going to be behind the previous one. With concurrency you can have multiple lanes, meaning that the vehicles don’t need to be one behind the other in a serial order.*

RChain is also based on a formal mathematical framework: *p-calculus*

## RChain developers and members

* Greg Meredith : Co-op's President and RChain's architect, Mathematician and Computer Scientist
* **[Vlad Zamfir](https://medium.com/rchain-cooperative/vlad-zamfir-joins-the-rchain-cooperative-a05f8e32c110)** : Ethereum Foundation Researcher, developed 1) Casper CBC (Correct-By-Construction), one of the two implementation of the future PoS consensus algorithm, and 2) Sharding for Ethereum

## Comparison with other Blockchains



<table>
  <thead>
    <tr>
      <th>&nbspp;</th>
      <th>Bitcoin</th>
      <th>Ethereum</th>
      <th>Polkadot</th>
      <th>RChain</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Model</th>
      <td></td>
      <td>Single threaded operations</td>
      <td>Multithreaded operations</td>
      <td>Nonblocking operations (concurrency)</td>
    </tr>
    <tr>
      <th>Block composition</th>
      <td>&nbsp;</td>
      <td>smart contracts, ledgers</td>
      <td>&nbsp;</td>
      <td>storage, smart contracts, ledgers</td>
    </tr>
    <tr>
      <th>Computing</th>
      <td colspan="3"></td>
    </tr>
    <tr>
      <th>Concurrent VM</th>
      <td>No VM, just a Stack Machine (like Forth language)</td>
      <td>No</td>
      <td>&nbsp;</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>Concurrent CS Language</th>
      <td>&nbsp;</td>
      <td>No</td>
      <td>&nbsp;</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>Turing Complete</th>
      <td>No (No Loop)</td>
      <td>Yes</td>
      <td>&nbsp;</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>Consensus</th>
      <th>Hashcash + Nakamoto Consensus</th>
      <th>Current: Ethash<br>Future: Eth Casper</th>
      <th>GRANDPA + BABE</th>
      <th>RChain Casper</th>
    </tr>
    <tr>
        <th>Algorithm</th>
        <td>PoW</td>
        <td>Current: PoW<br>Future: PoS (betting on block)</td>
        <td>Hybrid</td>
        <td>PoS (betting on logical propositions)</td>
    </tr>
    <tr>
      <th>Minimum bar to validate</th>
      <td>&nbsp;</td>
      <td>moderate</td>
      <td>&nbsp;</td>
      <td>very low</td>
    </tr>
    <tr>
      <th>Efficiency</th>
      <td>Low</td>
      <td>High</td>
      <td>&nbsp;</td>
      <td>High</td>
    </tr>
    <tr>
      <th>Transactions / second</th>
      <td>7</td>
      <td>100</td>
      <td>&nbsp;</td>
      <td>40,000+ on chain (per namespace)</td>
    </tr>
  </tbody>
</table>

**References**

- [Analysis and comparison between BTC, ETH and RChain](http://rchain-architecture.readthedocs.io/en/latest/introduction/comparison-of-blockchains.html)

## Blockchain model

The *resource-economics model* (also called [*meta-resource model*](https://blog.coinfund.io/blockchain-as-a-resourcebase-48b7938bca34)) in the RChain architecture defines how RChain accounts carry out blockchain transactions.

<table>
  <thead>
    <tr>
      <th colspan="2">Comparison of Resource-Economic Models in different blockchains</th>
    </tr>
    <tr>
      <th>Ethereum</th>
      <th>RChain</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        Gas is used to pay for the computing power to run a smart contract's functionalities<br>
        Other nodes related expenses (disk storage, memory, network use...) are uncompensated.
      </td>
    </tr>
  </tbody>
</table>

> Imagine when a blockchain grows to multiple petabytes of data (conservative estimate for something truly global). A node desiring to become a validator needs to be able to pay for storage of such significant size. If they don’t get compensated by the network for doing so, they will simply not want to provide this important service. The network will then be left without validators.

## Rho-Lang

Rho-Lang is a smart contract language used in RChain. It is based on Rho Calculus (ρ-calculus) and built on top of the Rho Virtual Machine (Rho-VM). Key features are :

- Contains I/O features (Input/Output)
- Based on Reflective Higher Order Calculus (Rho Calculus)
- Highly concurrent programming language

Rho-Lang makes Rho calculus concepts available to programmers as language constructs

- Supports processes referring to themselves (= reflectivity)
- Automated analysis of smart contracts
- Makes concepts of namespaces available

Concurrency is the primary feature of RhoLang. Therefore, it allows to develop highly parallelizable software, whose speed can be increased by adding computing resources to the network.

RhoLang can also be analyzed by automated tools. **This will eventually become integral part of its compiler framework.** Therefore, the compiler may automatically 1) identify bottlenecks, 2) perform optimizations, and 3) execute certain parts of your code in a vectorized fashion on your GPU(s)

When it comes to the limitations of concurrent programming, RhoLang offers significant guarantees :

- **Race conditions** :

The language can find race conditions ***at compile time*** and ensure that all nodes on the network achieve consensus at the race-point only. This is expected to significantly reduce the amount of information that is required to flow through the blockchain network.

- **Deadlocks: ** Tasks should not suspend and indefinitely wait for each other (*« Anything ever happens at all »*)

- **Safety: **

- **Determinism: **



**NB: ** *Rholang is being developed both as a smart contract language and as a high-performance programming language that will eventually be used to implement the low-level functionality of the blockchain nodes themselves.*

### Namespaces

Namespaces are **collections of communication channels with their own associated rules**.

- virtual groups of RNodes within the networks (can be customized for specific parameters)
- virtual channels on the network, independently and concurrently processing transactions.

Namespaces limit the scope of transaction validations. In fact, validators are only required to achieve consensus related to a particular transaction within its specific namespace. Therefore, network communications only needs to happen between a limited set of validators (those that record transaction in the same namespace). This applies only to relevant transactions, rather than every transaction in the global network.

You can think of namespaces as [*shards*](https://github.com/ethereum/wiki/wiki/Sharding-FAQ), that divides the network into optimized pieces.

Every namespace, process and transaction is inspected and formally verified before executing
Built-in privacy tools

Current systems are constrained by the single chain problem :
Sequential computing inevitably limits scalability and speed + increases transaction costs.

## Rho Virtual Machine

The Rho Virtual Machine is built in Scala and Java.

## Casper PoS (Consensus Algorithm)

In R-Chain, the consensus algorithm is called *Casper*. It is based on Proof of Stake (PoS) and is implemented in RhoLang.

- Complex concurrent program
- Use Correct By Construction Tooling (**What is this ?**)

Validators are only required to achieve consensus related to a particular transaction within its specific namespace.

## Nodes

RChain nodes do not need to download the entire blockchain (compared to Bitcoin and Ethereum).

# References

- [Vlad Zamfir joins the RChain Cooperative](https://medium.com/rchain-cooperative/vlad-zamfir-joins-the-rchain-cooperative-a05f8e32c110)
