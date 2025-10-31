# Multiplication Law and Law of Total Probability

## Review of Conditional Probability
- **Conditional probability** allows us to update the probability of event A given that event B has happened.
- Formula: 
  $P(A|B) = \frac{P(A \cap B)}{P(B)}$

## Multiplication Law
- The probability of both A and B happening is:
  $P(A \cap B) = P(A|B) \times P(B)$
  
- This is called the **multiplication law**.
- It follows directly from the definition of conditional probability.
- $A \cap B$ means both A and B occur (intersection).
- $P(A|B)$ is the probability of A given B has occurred.

## Law of Total Probability
- Suppose the sample space $\Omega$ is divided into disjoint sets $B_1, B_2, \ldots, B_n$:
  - $\Omega = B_1 \cup B_2 \cup \ldots \cup B_n$
  - Disjoint means $B_i \cap B_j = \emptyset$ for $i \neq j$.
- The **law of total probability** states:
  $P(A) = \sum_{i=1}^n P(A|B_i) \times P(B_i)$
- This means: To find the probability of A, sum over all disjoint subsets $B_i$, multiplying the probability of A given $B_i$ by the probability of $B_i$.

### Example: Cards
- Four suits: Hearts, Diamonds, Clubs, Spades (each is a disjoint set).
- Let A: Card is red (Hearts or Diamonds).
- Compute:
  $P(A) = P(A|\text{Hearts}) \times P(\text{Hearts}) + P(A|\text{Diamonds}) \times P(\text{Diamonds}) + P(A|\text{Clubs}) \times P(\text{Clubs}) + P(A|\text{Spades}) \times P(\text{Spades})$
- $P(A|\text{Hearts}) = 1$, $P(\text{Hearts}) = \frac{1}{4}$
- $P(A|\text{Diamonds}) = 1$, $P(\text{Diamonds}) = \frac{1}{4}$
- $P(A|\text{Clubs}) = 0$, $P(\text{Clubs}) = \frac{1}{4}$
- $P(A|\text{Spades}) = 0$, $P(\text{Spades}) = \frac{1}{4}$
- So:
  $P(A) = 1 \times \frac{1}{4} + 1 \times \frac{1}{4} + 0 \times \frac{1}{4} + 0 \times \frac{1}{4} = \frac{1}{2}$

## Special Case: Two Disjoint Sets
- The sample space can be split into B and its complement $B^c$:
  - $\Omega = B \cup B^c$
- Law of total probability:
  $P(A) = P(A|B) \times P(B) + P(A|B^c) \times P(B^c)$
- This is a very common and useful way to cover the sample space.

## Summary of Key Formulas
- **Multiplication Law**:
  $P(A \cap B) = P(A|B) \times P(B)$
- **Law of Total Probability**:
  $P(A) = \sum_{i=1}^n P(A|B_i) \times P(B_i)$
- **Special Case**:
  $P(A) = P(A|B) \times P(B) + P(A|B^c) \times P(B^c)$
  
***
