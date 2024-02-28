# Curve Trees

This is a fork of [Curve Trees benchmarking implementation](https://github.com/simonkamp/curve-trees). Read there for details.

Currently the only change applied here is to make the universal hash function use static constants, instead of generating the parameters (alpha and beta) randomly, allowing reconstruction of the Tree by more than one participant from the same set. (For context, the UH is used as a transformation applied to each point, such that the point compression tiebreaker (i.e. which y-coord to use for the given serialized x-coord) can be calculated easily inside the circuit.

TODO: may need to look into how null values at the leaf level are initialized into the tree to avoid forgery being possible.

