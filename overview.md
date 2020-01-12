# Overview

- Operate in parallel
- Single thread using exclusively non-blocking operations.

**Multithreading = several single-threaded operations in parallel to avoid the bottleneck of a single thread.**
**Concurrency = Not having the bottleneck at all.**

To understand concurrency, here is an example :

*Imagine that you have a road. Without concurrency you can have only one lane. You can increase the speed at which the vehicles run, but still each vehicle is going to be behind the previous one. With concurrency you can have multiple lanes, meaning that the vehicles don’t need to be one behind the other in a serial order.*
