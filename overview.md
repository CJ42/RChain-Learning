# Overview

- Operate in parallel
- Single thread using exclusively non-blocking operations.

**Multithreading = several single-threaded operations in parallel to avoid the bottleneck of a single thread.**
**Concurrency = Not having the bottleneck at all.**

To understand concurrency, here is an example :

*Imagine that you have a road. Without concurrency you can have only one lane. You can increase the speed at which the vehicles run, but still each vehicle is going to be behind the previous one. With concurrency you can have multiple lanes, meaning that the vehicles don’t need to be one behind the other in a serial order.*

## Blockchain model

> Imagine when a blockchain grows to multiple petabytes of data (conservative estimate for something truly global). A node desiring to become a validator needs to be able to pay for storage of such significant size. If they don’t get compensated by the network for doing so, they will simply not want to provide this important service. The network will then be left without validators.

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
        <strong>Gas</strong> : used to pay for the computing power to run a smart contract's functionalities<br>
        Other nodes related expenses (disk storage, memory, network use...) are uncompensated.
      </td>
      <td>
        <strong>Phlogiston</strong> : multi-dimensional, depends on<br>
        <ul>
          <li>usage of compute (depending on instructions)</li>
          <li>storage (depending on size and duration)</li>
          <li>bandwidth resources (quality-of-service and throughput)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

See [*"Rate Limiting Mechanism"*](https://architecture-docs.readthedocs.io/execution_model/rhovm.html#rate-limiting-mechanism) in RChain docs

