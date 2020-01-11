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


## Rho-Lang

Rho-Lang is a smart contract language used in RChain. It is based on Rho Calculus and built on top of the Rho Virtual Machine (Rho-VM). It contains I/O features (Input/Output). Key points are :

- Concurrent computational system
- Intelligent concurrency
- based on Rho-calculus innovation
- Reflective Higher Order Calculus (Rho Calculus)

### Namespaces

- virtual groups of RNodes within the networks (can be customized for specific parameters)
- virtual channels on the network, independently and concurrently processing transactions

Next generation sharding divides the network into optimize pieces = eliminate races conditions

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

# References

- [Vlad Zamfir joins the RChain Cooperative](https://medium.com/rchain-cooperative/vlad-zamfir-joins-the-rchain-cooperative-a05f8e32c110)
