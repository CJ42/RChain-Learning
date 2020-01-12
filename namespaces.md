# Namespaces

Namespaces are **collections of communication channels with their own associated rules**.

- virtual groups of RNodes within the networks (can be customized for specific parameters)
- virtual channels on the network, independently and concurrently processing transactions.

Namespaces limit the scope of transaction validations. In fact, validators are only required to achieve consensus related to a particular transaction within its specific namespace. Therefore, network communications only needs to happen between a limited set of validators (those that record transaction in the same namespace). This applies only to relevant transactions, rather than every transaction in the global network.

You can think of namespaces as [*shards*](https://github.com/ethereum/wiki/wiki/Sharding-FAQ), that divides the network into optimized pieces.

Every namespace, process and transaction is inspected and formally verified before executing
Built-in privacy tools

Current systems are constrained by the single chain problem :
Sequential computing inevitably limits scalability and speed + increases transaction costs.
