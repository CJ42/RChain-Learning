# RChain-Learning
Learning group for the RChain platform

## Overview

- Symbol: [RHOC](https://coinmarketcap.com/currencies/rchain/)
- Exchange: [KuCoin](https://www.kucoin.com/#/trade/RHOC-ETH)

RChain is a new Blockchain platform that focuses on concurrency. The platform is based on a formal mathematical framework: *p-calculus*


## Get Started

- [Architecture Overview](architecture.md)
- [RhoLang](rholang.md)
- [Rho Virtual Machine (RhoVM)](RhoVM.md)
- [Namespaces](namespaces.md)
- [Casper Consensus](consensus.md)
- [Rnode](rnode.md)

## RChain developers and members

* Greg Meredith : Co-op's President and RChain's architect, Mathematician and Computer Scientist
* **[Vlad Zamfir](https://medium.com/rchain-cooperative/vlad-zamfir-joins-the-rchain-cooperative-a05f8e32c110)** : Ethereum Foundation Researcher, developed 1) Casper CBC (Correct-By-Construction), one of the two implementation of the future PoS consensus algorithm, and 2) Sharding for Ethereum

## Comparison with other Blockchains



<table>
  <thead>
    <tr>
      <th>&nbsp;</th>
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


# References

- [RChain Platform Architecture (readthedocs.io](https://architecture-docs.readthedocs.io/index.html)
- [Vlad Zamfir joins the RChain Cooperative](https://medium.com/rchain-cooperative/vlad-zamfir-joins-the-rchain-cooperative-a05f8e32c110)
- [RChain series - Introduction (Medium)](https://blog.coinfund.io/rchain-series-introduction-985a05804ab)
