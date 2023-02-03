# Bayesian Inference

## The theory

Bayesian Inference calculates the probability of a hypothesis ( $H$, our tree) given some starting data ( $D$, the matrix). Is the complete opposite of likelihood, and it is calculated using the **Bayes theorem**:

$$
P(H|D) = \frac{P(D|H)P(H)}{P(D)}
$$

It is a **posterior** probability calculation, while likelihood is anterior probability. We can see the difference with this simple example:

-	Anterior probability (Likelihood): We have a box with two green balls and three blue balls. *What is the probability of drawing a blue ball?*
-	Posterior probability (Bayesian): We have a box and we draw a blue ball. *What is the probability of that the box contains two green balls and three blue balls?*

