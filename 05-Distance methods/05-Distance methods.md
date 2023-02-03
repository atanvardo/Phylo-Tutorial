# Distance-based phylogenetic methods

## UPGMA

This method, developed by Sokal and Michener in 1958, was the first phylogenetic algorithm. It is very straightforward: it reconstructs the tree hierachically from a simple distance matrix.

These distances can be calculated using different indices. One of the simpler and most well-known is Jaccard index, which divides the number of different positions between two sequences by the total number of positions:

$$
J(A,B) = \frac{|A \bigcap B|}{|A \bigcup B|}
$$

The algorithm starts taking the two taxa with the least distance, draw them in the tree, and replace them in the matrix by a mixed new taxon. The process is repeated until all the taxa are drawn in the tree. A detailed explanation, step by step, can be found in http://www.southampton.ac.uk/~re1u06/teaching/upgma/

