# Data files

When we codify the data that we gathered to reconstruct a phylogenetic tree (usually DNA sequences, but sometimes other kind of data), those are usually codified in one of the standard file format. Choosing one or another file format depends on our data and the program that we are going to use, as not all the programs are compatible with all the formats. The most used file format is NEXUS, due to its versatility.

## PHYLIP format

It was the first standart format to give data to phylogenetic programs. It was developed by Joe Felsenstein in 1980, when he created his phylogenetic package PHYLIP, the first software dedicated for reconstructing phylogenies. Indeed, most of the current phylogenetic programs are based on the PHYLIP source code (which is still being updated), so they can be considered as its "children".

The PHYLIP format is a simple text file. In the first line we indicate the number of taxa and the number of characters. This line is followed by the matrix, in which each line includes the name of the taxon (the strict PHYLIP format uses the first 10 characters of the line for this, so if our name has a length of 6 characters we must add 4 blank spaces afterwards), followed by its corresponding sequence.

```
8    6
Alpha1    AAGAAG
Alpha2    AAGAAG
Beta1     AAGGGG
Beta2     AAGGGG
Gamma1    AGGAAG
Gamma2    AGGAAG
Delta     GGAGGA
Epsilon   GGAAAG
```

The PHYLIP format requires that the sequences have the same length are must be aligned.

Files in PHYLIP format usually have the extension phy.

## FASTA format

