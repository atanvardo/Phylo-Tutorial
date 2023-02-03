# Cladistic methods: Maximum Parsimony

## The theory

The Maximum Parsimony method is based on the philosophical tenet known as *Occam’s Razor* or *lex parsimoniae*, proposed by the English monk William of Ockham in the 14th century, based on his readings of classic Greek philosophers. Its modern formulation is:

```
The simplest explanation is usually the correct one.
```

This principle has been often criticized, especially when applied to biological systems, which stubbornly oppose the laws of logic[^1]), because the correct explanation is not usually the simplest one.

In phylogeny, this principe was adopted as:

```
The shortest tree is usually the correct one.
```

The **length** of a tree is defined as the total number of substitutions that must have occurred along all its branches to generate the original data matrix.

We must be aware that Maximum Parsimony analyses are very sensible to the phenomenon known as **Long Branch Attraction (LBA)**, in which lineages with high substitution rates tend to group together in the tree, even if there is no real relationship between them. Ignoring this issue has led to the publication of some erroneous taxonomic conclusions, including some bizarre phylogenies showing than Guinea pigs are not rodents or that the hedgehog is the ancestral mammal. 

## Calculating the length of a tree

For each position in the matrix, we put in each terminal node its corresponding nucleotide. Then we reconstruct which nucleotide was present in each of the ancestral internal nodes:

-	If we have the same nucleotide in a pair of terminal nodes, then the nucleotide at their ancestral node is the same nucleotide.
-	If both nucleotides are different, we determine which one is the ancestral using one of the diverse parsimony algorithms (Fitch, Wagner, Dollo, Transversion...).

Once the whole tree is reconstructed, we count how many nucleotide changes happened along it.

We repeat the same process for each of the positions of our matrix, and at the end we add all the values to get the total length of the tree.

## Maximum Parsimony algorithm

Ideally, we could create all the possible trees, calculate the total length of each one, and choose the shortest tree.

But this is not feasible. The total number of possible (rooted) trees for a T number of taxa is given by this formula:

$$
N = (2T-3) \prod\limits_{i=3}^T (2i-5)
$$




[^1]: As Ian Malcolm (Jeff Golfblum) said in Jurassic Park, “life finds a way”.
