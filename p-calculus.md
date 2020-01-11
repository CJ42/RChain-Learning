# About Rho-calculus

## Introduction to mobile process calculus

This was taken here : https://blog.coinfund.io/rchain-series-introduction-985a05804ab

A mobile process calculus is a formal way to model an environment that consists of a number of concurrent processes that engage in communication with each other. Examples of such environments can be found everywhere, both in nature and in computer science. For example, we can look at every car and driver on the road as an independent process, with communication established through speed, turn-signals, and horns. Reducing the scale, we notice that every part of the car is also a concurrent process, where each mechanical part communicates with certain others by applying pressure and each electrical part communicates by producing electrical signal and current. The human body is also made up of a vast number of concurrent processes, cells, which communicate through a complex medley of chemical, electrical and mechanical signals. We can continue these illustrations, but the picture is clear: once you look at the world as a combination of concurrently proceeding processes, you see them everywhere.

Moreover, configuration of the network and coordination between processes may itself be seen as a process, which is changing over time. In mobile process calculus therefore, we see a mechanism that describes and accounts for such fluidity.

Mobile processes calculi are elegant models for programming both real-worl systems and digital environments (such as blockchains and smart contracts).

## Applicability of the mobile process model to blockchain

A blockchain platform operates by running a vast number processes. These processes operate concurrently, in several different contexts. Let's illustrate :

### Each nodes on the network is a process. 

Each node has threads that receive, resend and analyze transactions as they happen.

### A smart-contract environment is inherently a mobile process environment.

Each party to the interaction encoded in the smart contract is itself a process. These processes are of a special kind, because they do not operate continuously, but rather interact with the network as-needed.

*Let's see an example:*

A **multi-signature cryptocurrenct wallet** (Multi-Sig Wallet) is a process which receives signed messages and occasionally performs a funds transfer to the destination address. Each of the parties to such contract sends signed messages to the wallet. From the perspective of the wallet, people that interact with it look like other processes.

## About Rho-Calculus

Greg Meredith has spent many years developing a variation of a mobile process calculus called ρ-calculus (pronounced Rho-calculus).
It solves several issues encountered in more traditional frameworks like π-calculus.

ρ-calculus has additional features compared to π-calculus :

### Reflexivity

Rho = *Reflective High Order*

ρ-calculus supports process referring to themselves + the code that comprises them. This is an important feature for blockchain programming for several reasons :

- Allows a high level of automated analysis of smart contract code (confirm that it adheres to specification and respects constraints set upon by its creators)
- Makes the concept of *namespaces* available (= collection of communication channels with associated rules)

Namespaces + Automated Analysis = verify that certain features of a smart contract are appropriately restricted.

Hence, it prevents security bugs, [like the one recently discovered in the Parity multi-signature wallet.](http://hackingdistributed.com/2017/07/22/deep-dive-parity-bug/)

