# RNode

## Overview

P2P communication (node-to-node communication) will use a open-source component such as ZeroMQ or RabbitMQ

RChain nodes do not need to download the entire blockchain (compared to Bitcoin and Ethereum).

Since Rnode 0.2.1, three mode of operations exist :

- REPL mode — Allows users to execute Rholang code at the command line. This is a read, evaluate, and print loop (REPL). The Rholang tutorial — 0.2 will help you get started with Rholang while operating RNode in REPL mode.
- EVAL mode — Allows users to pass in Rholang code stored in a text file with the extension .RHO.
- P2P mode (default) — Allows users to stand up a node that connects to other nodes in the RChain network.

Full details on operating the node in these modes is described in the [documentation](https://github.com/rchain/rchain/blob/master/node/README.md).

## How transactions work in RChain?

All transactions in the world do not need to be placed in sequential order. Just the ones whose order matters to resolving conflicts, such as a double-spend.

The ability to narrow the scope of consensus around a specific transaction allows RChain to do as little work as possible in validating specific transactions. At an extreme low end of the spectrum, this translates to being able to create an equivalent of state channels, which can be seen as transactions between a small number of counterparts, carried out cheaply and efficiently without engaging the consensus protocol of the larger network. Essentially, with RChain you can think of state channels as a feature you get for free, without the need to create additional software layers to support them.

# Reference 

[Foster N. (2018). RNode 0.2.1, RhoLang integration](https://medium.com/rchain-cooperative/rnode-0-2-1-integrates-rholang-to-the-rchain-node-183c0e13b024)
