# RChain Architecture

![RChain architecture](https://architecture-docs.readthedocs.io/_images/architecture-overview.png)

- **LMDB** = Lightning Memory-Mapped Database

High-performance embedded transactional database in the form of a key-value store. [More infos on Wikipedia (deserves a deep-dive)](https://en.wikipedia.org/wiki/Lightning_Memory-Mapped_Database)

- **REPL** = Read, Evaluate, Print Loop

This is a Command Line tool that allow each node to execute Rholang code via the CLI.

- **Node API**

Exposes features via HTTP and JSON RPC.
