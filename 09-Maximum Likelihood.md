# Maximum Likelihood

## The theory

Maximum Likelihood is a statistical method, based on the calculation of probabilities. Namely, it calculates the probability of getting the data matrix ( $D$ ) given a determinate hypothesis ( $H$: the tree and the nucleotide substitution model). In other words: which is the probability of, having obtained a determinate tree, this will be the result of analysing our data? In mathematical language: $P(D|H)$.

We must be aware that the likelihood is not the probability of that our tree will be absolutely correct, but that it corresponds to our data.

## Likelihood calculation

Let’s see it with an example. Let’s suppose that we want to calculate the likelihood of that the sequence CCAT mutates to the sequence CCGT. The parameters of our model are:

$$
P_{i} = 
\begin{bmatrix}
  0.976 & 0.010 & 0.007 & 0.007 \\
  0.002 & 0.983 & 0.005 & 0.010 \\
  0.003 & 0.010 & 0.979 & 0.007 \\
  0.002 & 0.013 & 0.005 & 0.979 \\
\end{bmatrix}
$$

$$
f = 
\begin{bmatrix}
  0.1 & 0.4 & 0.2 & 0.3 \\
\end{bmatrix}
$$

We go position by position, calculating the probability of that the original nucleotide has changed to the corresponding nucleotide in the final sequence. In the first position, the change is from C to C. The probability will be the frequency of C, multiplied by the probability of change from C to C. We calculate this for every position, multiply all the values, and as a result we get the likelihood value:

