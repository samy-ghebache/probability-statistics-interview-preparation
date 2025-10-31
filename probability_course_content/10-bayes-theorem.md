# Bayes' Theorem

## Introduction
Bayes' theorem is one of the most useful ideas in probability and statistics. It is a cornerstone of machine learning, inverse problems, and engineering inference problems. Bayes' theorem allows us to update our probability estimates for an event based on new, partial information about another event.

## Conditional Probability Recap
- **Conditional probability**: The probability of event A given event B is:
  $P(A|B) = \frac{P(A \cap B)}{P(B)}$
- **Multiplication law**: The probability of both A and B happening is:
  $P(A \cap B) = P(A|B) \cdot P(B)$

## The Inverse Problem
Often, we want to know the probability of an underlying cause (like having a disease) given an observed effect (like a positive test result). This is called an **inverse problem**. Bayes' theorem allows us to compute this "backwards" probability using information we can actually measure.

## Bayes' Theorem (Basic Form)
$P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}$

- **P(B|A)**: Posterior probability (probability of B given A)
- **P(B)**: Prior probability (probability of B before seeing A)
- **P(A|B)**: Likelihood (probability of A given B)
- **P(A)**: Marginal probability (probability of A)

## Derivation
- From the multiplication law:
  $P(A \cap B) = P(A|B) \cdot P(B) = P(B|A) \cdot P(A)$

- Rearranging gives Bayes' theorem:
  $P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}$

## Law of Total Probability (Expanded Bayes' Theorem)
Sometimes, $P(A)$ is hard to compute directly. We can use the law of total probability:
$P(A) = P(A|B) \cdot P(B) + P(A|B^c) \cdot P(B^c)$

where $B^c$ is the complement of B (not B).

So, Bayes' theorem becomes:

$P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A|B) \cdot P(B) + P(A|B^c) \cdot P(B^c)}$

## Generalization (Multiple Disjoint Events)
If there are multiple disjoint events $B_j$ covering the sample space:

$P(B_j|A) = \frac{P(A|B_j) \cdot P(B_j)}{\sum_{i} P(A|B_i) \cdot P(B_i)}$

## Terminology in Bayesian Inference
- **Posterior**: $P(B|A)$ — updated probability after seeing evidence A
- **Prior**: $P(B)$ — initial probability before seeing evidence
- **Likelihood**: $P(A|B)$ — probability of evidence given the hypothesis
- **Marginal/Normalization**: $P(A)$ — ensures probabilities sum to 1

## Sequential Updating
In Bayesian statistics, you can update your prior with new evidence to get a posterior, which then becomes the new prior for the next round of evidence. This process can be repeated as more data is collected.

## Example: Cancer Screening
- **Test accuracy**: 99% ($P(\text{positive} | \text{disease}) = 0.99$)
- **Disease prevalence**: 0.1% ($P(\text{disease}) = 0.001$)
- **False positive rate**: 1% ($P(\text{positive} | \text{no disease}) = 0.01$)
- **Probability of not having disease**: $P(\text{no disease}) = 0.999$

We want: $P(\text{disease} | \text{positive})$

Plug into Bayes' theorem:
$P(\text{disease} | \text{positive}) = \frac{P(\text{positive} | \text{disease}) \cdot P(\text{disease})}{P(\text{positive} | \text{disease}) \cdot P(\text{disease}) + P(\text{positive} | \text{no disease}) \cdot P(\text{no disease})}$
$= \frac{0.99 \times 0.001}{0.99 \times 0.001 + 0.01 \times 0.999}$$= \frac{0.00099}{0.00099 + 0.00999} = \frac{0.00099}{0.01098} \approx 0.09$

So, even with a 99% accurate test, if the disease is rare, a positive test result only means about a 9% chance of actually having the disease. This highlights the importance of considering base rates and why follow-up tests are often needed.

## Summary of Key Formulas
- **Bayes' Theorem (Basic):**
  $P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}$

- **Bayes' Theorem (Expanded):**
  $P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A|B) \cdot P(B) + P(A|B^c) \cdot P(B^c)}$

- **Generalized Bayes' Theorem:**
  $P(B_j|A) = \frac{P(A|B_j) \cdot P(B_j)}{\sum_{i} P(A|B_i) \cdot P(B_i)}$