# Quality Control and Sampling: The Hypergeometric Distribution

## Destructive Testing in Manufacturing

In quality control, many inspection methods require **destructive testing**—physically testing parts to failure or cutting them open to verify quality. This is common across industries:
- Aircraft composite parts must be tested for structural integrity
- Materials need internal inspection for defects
- Components require testing to failure to verify specifications

While **non-destructive testing (NDT)** exists (using acoustics or other methods to inspect without damage), destructive testing is often still necessary for quality assurance.

## The Sampling Problem

**Setup:**
- **Total items in lot:** $N$
- **Defective items in lot:** $K$ (unknown initially)
- **Sample size:** $R$ items tested
- **Defective in sample:** $M$ items found defective

**Question:** What is the probability that our sample of $R$ items contains exactly $M$ defective items?

## Breaking Down the Sample

### Sample Composition
$R = M \text{ (defective)} + (R - M) \text{ (good)}$

### Lot Composition
$N = K \text{ (defective)} + (N - K) \text{ (good)}$

## Computing the Probability

This is a **sampling without replacement** problem where **order doesn't matter**—we use the "n choose r" combinatorial formula.

### General Probability Formula

$P(\text{M defective in sample}) = \frac{\text{Number of ways to get M defective}}{\text{Total number of possible samples}}$

### Three Key Counts

**Total possible samples of R from N:**
$\binom{N}{R} = \frac{N!}{R!(N-R)!}$

This goes in the denominator.

**Ways to select M defective from K total defective:**
$\binom{K}{M} = \frac{K!}{M!(K-M)!}$

**Ways to select (R - M) good items from (N - K) total good:**
$\binom{N-K}{R-M} = \frac{(N-K)!}{(R-M)!(N-K-R+M)!}$

### Complete Formula

$P(M \text{ defective in sample}) = \frac{\binom{K}{M} \times \binom{N-K}{R-M}}{\binom{N}{R}}$

**Interpretation:**
- Numerator: Ways to get $M$ defective AND $(R-M)$ good items—these are independent events, so we multiply
- Denominator: Total possible random samples

## General Form: hypergeometric Distribution

For a lot with **Good (G)** and **Bad (B)** items, sampling $n$ items with $g$ good and $b$ bad:

$P(g \text{ good}, b \text{ bad}) = \frac{\binom{G}{g} \times \binom{B}{b}}{\binom{G+B}{n}}$

where $n = g + b$ (total sample size).

## Key Assumptions

**Equally likely samples:** All items have equal probability of being selected (truly random sampling).

**Without replacement:** Once an item is sampled, it's removed from the pool—the lot gets smaller.

**Known parameters:** To compute this probability, we assume we know $N$, $K$, $R$, and $M$.

## The Inverse Problem: Statistics

**Critical limitation:** The formula above computes probability when we know everything—including $K$ (total defective in the lot).

**Real-world challenge:** In quality control, $K$ is typically **unknown**. The whole point is to estimate $K$ without destroying the entire lot.

### Statistical Questions

**Given sample data (R items tested, M found defective), we want to know:**
- What is the most likely value of $K$?
- What is the distribution of possible $K$ values?
- How large does $R$ need to be for 99% confidence in our estimate of $K$?
- What statistical statements can we make about lot quality?

This is an **inverse problem**—we have data (the sample) and want to infer parameters (total defect rate). This requires **statistics**, not just probability.

### Tools for the Inverse Problem

**Bayes' Theorem:** Combines prior knowledge with sample data to estimate unknown parameters.

**Hypothesis testing:** Tests claims about defect rates using sample evidence.

**Confidence intervals:** Provides ranges for $K$ with specified confidence levels.

These statistical methods will be covered in later lectures.

## Notes

- The hypergeometric distribution is a discrete probability distribution that models the probability of obtaining a specific number of "successes" in a fixed number of draws from a finite population, where each draw is made without replacement.
