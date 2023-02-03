# Distance-based phylogenetic methods

## UPGMA

This method, developed by Sokal and Michener in 1958, was the first phylogenetic algorithm. It is very straightforward: it reconstructs the tree hierachically from a simple distance matrix.

These distances can be calculated using different indices. One of the simpler and most well-known is Jaccard index, which divides the number of different positions between two sequences by the total number of positions:

$$
J(A,B) = \frac{|A \bigcap B|}{|A \bigcup B|}
$$
