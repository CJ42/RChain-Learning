# How transactions work in RChain?

All transactions in the world do not need to be placed in sequential order. Just the ones whose order matters to resolving conflicts, such as a *double-spend*.

The ability to narrow the scope of consensus around a specific transaction allows RChain to do as little work as possible in validating specific transactions. At an extreme low end of the spectrum, this translates to being able to create an equivalent of state channels, which can be seen as transactions between a small number of counterparts, carried out cheaply and efficiently without engaging the consensus protocol of the larger network. Essentially, with RChain you can think of state channels as a feature you get for free, without the need to create additional software layers to support them.
