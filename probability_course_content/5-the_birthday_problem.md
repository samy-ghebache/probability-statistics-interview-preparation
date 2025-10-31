# The Birthday Problem: Computing Unintuitive Probabilities

## Problem Statement

If there are $n$ people in a room, how large does $n$ need to be for at least a 50% chance that at least two people share a birthday?

**Intuitive guess:** Many people initially guess around $\frac{365}{2}$ (approximately 182-183 people).

**Actual answer:** $n = 23$ people.

This is a surprisingly unintuitive result that demonstrates why clever counting methods are essential in probability.

## Why Direct Counting is Hard

Computing the probability that "at least two people share a birthday" directly is extremely difficult. You would need to enumerate:
- Exactly 2 people sharing a birthday
- Exactly 3 people sharing a birthday
- Exactly 4 people sharing a birthday
- Mixed cases (e.g., 2 people share one date AND 3 people share another date)

This leads to nested, complex sums with many edge cases and potential double-counting issues.

## The Complement Trick

**Key insight:** It's much easier to compute the probability that *nobody* shares a birthday, then use:

$P(\text{at least 2 share}) = 1 - P(\text{no one shares})$

This is an example of using the complement rule: $P(A^c) = 1 - P(A)$.

## Calculating the Probability

### Number of Comparisons

For $n$ people, the number of unique pairwise comparisons is:

$\frac{n(n-1)}{2}$

This is the formula Gauss famously discovered as a child (sum of integers from 1 to $n-1$).

For $n = 20$: $\frac{20 \times 19}{2} = 190$ comparisons, already exceeding $\frac{365}{2}$.

### Probability No One Shares

**Setup:** Assign birthdays to $n$ people sequentially without replacement:

- Person 1: Can have any of 365 days → probability $\frac{365}{365}$
- Person 2: Must avoid Person 1's birthday → probability $\frac{364}{365}$
- Person 3: Must avoid Persons 1 and 2 → probability $\frac{363}{365}$
- Person $n$: Must avoid all previous → probability $\frac{365 - n + 1}{365}$

**Formula:**

$P(\text{no one shares}) = \frac{365}{365} \times \frac{364}{365} \times \frac{363}{365} \times \cdots \times \frac{365-n+1}{365}$

This can be written as:

$P(\text{no one shares}) = \frac{365!}{(365-n)! \times 365^n}$

### Computation Strategy

**Important:** Don't compute $365!$ directly—it's too large for most calculators.

Instead, use an iterative approach in a for loop:
1. Start with probability = 1
2. For each person $k = 1$ to $n$:
   - Multiply probability by $\frac{365 - k + 1}{365}$

This keeps all intermediate values manageable since each factor is close to 1.

## Results

For $n = 20$: $P(\text{no one shares}) \approx 0.589$

Therefore: $P(\text{at least 2 share}) \approx 0.411$ or 41%

For $n = 23$: The probability that no one shares drops below 50%, meaning the probability that at least two people share exceeds 50%.

## Homework Exercise

Write a program to:
1. Compute $P(\text{no one shares})$ for $n = 1, 2, 3, \ldots$
2. Plot both $P(\text{no one shares})$ and $P(\text{at least 2 share})$ versus $n$
3. Find where the probability crosses 50%
4. Calculate the exact probability for specific values like $n = 20$

Use the iterative multiplication method to avoid overflow errors.

## Assumptions Made

**365 days per year:** No leap years; February 29 is excluded.

**Equal probability for all days:** In reality, birth rates vary by season, creating "hot spots" where shared birthdays are more likely.

**Independence:** Each person's birthday is independent of others.

### Critical Thinking Questions

- How would results change with real birth rate data accounting for seasonal variation?
- What if you observed 5 people with the same birthday in a room of 23—would you suspect non-randomness?
- How could you refine the model with actual birth distribution data?

## Key Takeaways

**Complement rule:** When direct calculation is complex, compute the complement and subtract from 1.

**Sampling without replacement:** When each choice reduces the pool of available options, use factorial-based formulas.

**Unintuitive probabilities:** Human intuition often fails with probabilistic reasoning—formal calculation is essential.

This problem demonstrates that probability calculations can yield surprising results that contradict initial intuition, highlighting the importance of rigorous mathematical approaches.
