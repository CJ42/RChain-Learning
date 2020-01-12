# RhoLang


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