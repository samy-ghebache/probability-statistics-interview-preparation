# Conditional Probability

## Introduction
Conditional probability is a fundamental concept in probability theory. It allows us to update or refine the probability of an event based on partial information about another event. This concept is crucial for real-world applications, where knowing something about one event can change our estimate for another.

## Basic Definitions
- **Event Space (Omega $\Omega$)**: The set of all possible outcomes.
- **Event A**: A subset of $\Omega$, e.g., "next card is a spade".
- **Event B**: Another subset, e.g., "next card is a three".

## Probability of an Event
- Probability of event A: Count the number of ways A can happen, divided by the total number of possible outcomes in $\Omega$.
- Pictorially: Area of A divided by area of $\Omega$.

## Conditional Probability Notation
- **Probability of A given B**: Denoted as $P(A|B)$.
- This means: "What is the probability of event A happening, if we know for a fact that event B happened?"

## Conditional Probability Formula
If we know event B happened, we restrict ourselves to the subset B. The probability of A given B is:

$
P(A|B) = \frac{P(A \cap B)}{P(B)}
$

- **$P(A \cap B)$**: Probability that both A and B happen (the intersection).
- **$P(B)$**: Probability that B happens.

## Intuitive Explanation
- If B happened, we "zoom in" to the B region.
- The probability of A given B is the area of A and B divided by the area of B.
- Sometimes knowing B changes the probability of A; sometimes it does not.

## Examples
### Example 1: Dice Rolls
- Let A: First die equals 3.
- Let B: Second die equals 5.
- Let C: Sum of dice equals 6.

- **Probability of A given B**: Does knowing the second die is 5 change the probability of the first die being 3? No. These are independent events.
  - $P(A|B) = P(A) = \frac{1}{6}$

- **Probability of A given C**: If the sum is 6, does that change the probability of the first die being 3? (Left as a question for the student to work out.)

### Example 2: Drawing Cards
- Four suits: Hearts, Clubs, Spades, Diamonds.
- Clubs and Spades are black; Diamonds and Hearts are red.

- Let A: Card is a Spade.
- Let B: Card is black.

- $P(A) = \frac{1}{4}$ (one out of four suits)
- $P(B) = \frac{1}{2}$ (two out of four suits are black)
- **Probability of A given B**: If the card is black, only Clubs or Spades are possible. So:
  - $P(A|B) = \frac{1}{2}$

- Let C: Card is red.
- **Probability of A given C**: If the card is red, it cannot be a Spade. So:
  - $P(A|C) = 0$

### Example 3: Disease Screening
- Testing 1,000 people for cancer.
- Two groups: 500 have cancer, 500 do not.
- Of those with cancer: 450 test positive, 50 test negative.
- Of those without cancer: 100 test positive (false positives), 400 test negative.

- **Event B**: Has cancer.
- **Event A**: Tests positive.

- **Probability of A (tests positive)**:
  - Total positives: 450 (with cancer) + 100 (without cancer) = 550
  - $P(A) = \frac{550}{1000} = 0.55$ (55%)

- **Probability of A given B (tests positive given has cancer)**:
  - $P(A|B) = \frac{450}{500} = 0.9$ (90%)

- This is a 90% specific test: Probability of testing positive given you have cancer.

## Inverse Problems and Inference
- What we often want: Probability of having cancer given a positive test result ($P(B|A)$).
- This is not the same as $P(A|B)$ due to false positives.
- This is called an **inverse problem** or **inference**.
- To solve this, we use **Bayes' Theorem** (to be covered in the next lecture).

## Summary of Key Formula
- **Conditional Probability**:
  $P(A|B) = \frac{P(A \cap B)}{P(B)}$

***