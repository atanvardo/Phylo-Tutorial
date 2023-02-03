# Nucleotide substitution models

## The problem

As organisms evolve, their DNA accumulates mutations. This may lead us to think that, if we compare the same DNA marker from two organims and count the number of different nucleotides, we can directly infer how much evolutionary distance is between them.

This is false.

Why? Because the number of differences between two nucleotide sequences is not proportional to their time of divergence. One difference between two sequences does not mean that there was only one change.

For example, if we have an `A` in one sequence and a `C` in the other sequence, this can be the result of:

1. The ancestor had `A`, and there was one mutation in the second sequence: 1 observed difference, 1 change.
2. The ancestor had `C`, and there was one mutation in the first sequence: 1 observed difference, 1 change.
3. The ancestor had `A`, and it changed to `G` and then to `C` in the second sequence: 1 observed difference, **2 changes**.
4. The ancestor had `G`, and it changed to `A` in the first sequence and to `C` in the second: 1 observed difference, **2 changes**.
5. The ancestor had `G`, and then it changed to `T` and later to `A` in the first sequence, and to `C`, then to `G`, and then back to `C` in the second sequence: 1 observed difference, **5changes**.

Additionally, we can have cases in which the same nucleotide in both sequences (**0 observed differences**) come from identical changes from a different ancestral nucleotide (**2 changes**). Or many other different cases...
