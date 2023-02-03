# Bayesian Inference

## The theory

Bayesian Inference calculates the probability of a hypothesis ( $H$, our tree) given some starting data ( $D$, the matrix). Is the complete opposite of likelihood, and it is calculated using the **Bayes theorem**:

$$
P(H|D) = \frac{P(D|H)P(H)}{P(D)}
$$

It is a **posterior** probability calculation, while likelihood is anterior probability. We can see the difference with this simple example:

-	Anterior probability (Likelihood): We have a box with two green balls and three blue balls. *What is the probability of drawing a blue ball?*
-	Posterior probability (Bayesian): We have a box and we draw a blue ball. *What is the probability of that the box contains two green balls and three blue balls?*

The meaning of the components of the Bayes equation for phylogenetic analyses is:

-	$P(D|H)$: It is simply the tree likelihood. We already know how to calculate it (just using the Maximum Likelihood algorithm).
-	$P(H)$: It is the probability of getting a particular tree randomly from all the possible trees. It is usually considered to be equal to $\frac{1}{N_{trees}}$, but some experts have some doubts about it.
-	$P(D)$: It is the probability of our matrix, i.e. that for each position for each of the taxa we find those particular nucleotide instead of another. This value is absolutely impossible to calculate. In order to be able to carry out this analysis, we should use a smart trick to remove this element from the equation. We will learn how to do it in the next section.
