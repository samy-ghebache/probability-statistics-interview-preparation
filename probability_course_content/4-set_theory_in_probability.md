# Sets, Events, and Axioms of Probability

In this video, probability is formalized with set theory so we can describe events and compute their likelihoods in a general, reusable way.

## Core idea
- Probability measures the likelihood of an event A occurring.
- We describe possible outcomes with a sample space and events as subsets of that space.

## Sample space and events
- Sample space ($\Omega$): the set of all possible outcomes of a random experiment (e.g., 3 coin flips, a hand of poker, number of emails in an hour).
- An outcome ($\omega$): a specific realization in $\Omega$.
- An event ($A$, $B$, ...): a subset of $\Omega$ describing outcomes of interest.

Example: three coin flips
- $\Omega = \{\text{HHH},\, \text{HHT},\, \text{HTH},\, \text{HTT},\, \text{THH},\, \text{THT},\, \text{TTH},\, \text{TTT}\}$.
- Event $A$: “first flip is heads” $= \{\text{HHH},\, \text{HHT},\, \text{HTH},\, \text{HTT}\}$.
- Event $B$: “second flip is tails” $= \{\text{HTH},\, \text{HTT},\, \text{TTH},\, \text{TTT}\}$.

If all outcomes are equally likely, $P(A)$ can be computed by counting: number in $A$ divided by number in $\Omega$.

## Set operations for events
- Union ($A\,\text{or}\,B$, $A\cup B$): all outcomes that are in $A$ or in $B$ (or both).
  - For the coin example, $A\cup B = \{\text{HHH},\,\text{HHT},\,\text{HTH},\,\text{HTT},\,\text{TTH},\,\text{TTT}\}$ (6 elements).
- Intersection ($A\,\text{and}\,B$, $A\cap B$): outcomes in both $A$ and $B$.
  - Here, $A\cap B = \{\text{HTH},\,\text{HTT}\}$ (2 elements).
- Complement ($A^c$): all outcomes in $\Omega$ not in $A$.

These operations are commutative and associative in the usual set-theoretic sense.

## Probability as a measure
Probability $P$ assigns a number between 0 and 1 to each event (subset of $\Omega$). This lets us handle non-uniform cases (e.g., a biased coin) where simple counting is not enough.

- Intuition: in diagrams, think “area of A divided by area of $\Omega$” when outcomes are uniformly likely.

## Axioms (properties) of probability
For events $A, B \subseteq \Omega$:
1. $P(\Omega) = 1$ (something in $\Omega$ must occur).
2. $0 \le P(A)$ (nonnegativity for any event $A$).
3. If $A$ and $B$ are disjoint ($A\cap B=\emptyset$), then $P(A\cup B) = P(A) + P(B)$.

Useful consequences:
- $P(A^c) = 1 - P(A)$.
- $P(\emptyset) = 0$.
- If $A \subseteq B$ then $P(A) \le P(B)$.
- Inclusion–exclusion for two events: $P(A\cup B) = P(A) + P(B) - P(A\cap B)$.

## Visual intuition (Venn-style)
- Union: the combined region of $A$ and $B$.
- Intersection: overlap of $A$ and $B$.
- Complement: everything in $\Omega$ outside $A$.
- With uniform randomness, probabilities correspond to relative areas.

## Why this matters
- These definitions and axioms let us rigorously compute probabilities for complex scenarios (biased coins, dependent events, non-uniform models), not just simple equal-likelihood counting.
- We’ll use this framework repeatedly as problems become more realistic and nuanced.