# Basic Probability: Definitions and Simple Examples

## What is Probability?

Probability calculates how likely an event is to happen. The fundamental formula is:

$
P(A) = \frac{\text{Number of ways A can happen}}{\text{Total number of things that can happen}}
$

where $A$ represents a specific event.

## Example 1: Flipping a Coin Twice

**Setup:** Flip a fair coin twice.

**Sample Space ($\Omega$):** The set of all possible outcomes:
- Heads, Heads (HH)
- Heads, Tails (HT)
- Tails, Heads (TH)
- Tails, Tails (TT)

Total possible outcomes: 4

### Event A: At Least One Heads

**Favorable outcomes:** HH, HT, TH (excludes TT)

**Calculation:**
$
P(A) = \frac{3}{4} = 0.75 = 75\%
$

Three out of four outcomes contain at least one heads.

### Event B: No Heads

**Favorable outcomes:** TT only

**Calculation:**
$
P(B) = \frac{1}{4} = 0.25 = 25\%
$

Only one outcome has no heads.

## Example 2: Rolling Two Dice

**Setup:** Roll two fair six-sided dice with equal probabilities, where each roll is independent.

**Sample Space:** Total possible outcomes = $6 \times 6 = 36$

Outcomes include: (1,1), (1,2), (1,3), ..., (5,2), (5,3), ..., (6,6)

### Event: At Least One Die Shows Five

**Method 1: Enumeration** (listing all favorable outcomes)

Favorable outcomes:
- First die not 5, second die is 5: (1,5), (2,5), (3,5), (4,5)
- First die is 5, second die anything: (5,1), (5,2), (5,3), (5,4), (5,5), (5,6)
- First die is 6, second die is 5: (6,5)

Total favorable outcomes: 11

**Calculation:**
$
P(\text{at least one 5}) = \frac{11}{36}
$

This is just under one in three chances.

**Method 2: Probabilistic Reasoning**

$
P(A) = P(D_1 = 5) + P(D_1 \neq 5) \times P(D_2 = 5)
$

$
P(A) = \frac{1}{6} + \frac{5}{6} \times \frac{1}{6} = \frac{6}{36} + \frac{5}{36} = \frac{11}{36}
$

This approach reasons through the ways events can happen without listing all possibilities.

## Core Principle: Probability as Counting

Probability is fundamentally about **clever ways of counting**. It involves:
- Counting how many ways an event can happen
- Counting total possible outcomes
- Computing their ratio

This counting principle extends to complex systems like entropy in statistical mechanics and gas dynamics.

## Key Assumptions

When solving probability problems, clearly state assumptions:

**Fair Coin:** Equal probability of heads or tails

**Independent Events:** The outcome of one event doesn't affect another (e.g., second coin flip doesn't depend on the first)

**Fair Dice:** All six sides have equal probability

## Real-World Applications

Probability models are used for:
- Weather forecasting
- Health outcomes (likelihood of disease given symptoms)
- Part failure predictions in manufacturing
- Safety outcomes (e.g., self-driving car risks)
- Critical component reliability

While enumeration works for simple cases, more complex scenarios require formulas and clever counting methods. For example, computing the probability of getting 300 heads in 1,000 coin flips would be impractical using basic enumeration.

## Randomness vs Deterministic Systems

### The Nature of Randomness

**Coin flips** are technically deterministic physical systems governed by $F = ma$, involving:
- Mass and inertia
- Gravity
- Wind resistance

These systems are predictable with sufficient information. However, the outcome appears **random** because it's too hard to predict with available information.

**Practical randomness:** When a system is too complex to model or predict with current information, it's treated as random for practical purposes.

### Machine Learning Perspective

With enough information (e.g., video of a coin flip), machine learning algorithms might predict outcomes better than 50/50 by analyzing the coin's trajectory at its peak. This would be an interesting classifier project.

### Weather as a Deterministic System

Weather is driven by deterministic physics (climate, clouds, storms). However, with measurement uncertainty and information limitations, forecasts beyond certain time horizons become probabilistic. Better measurements and models lead to tighter probabilistic estimates and potentially deterministic predictions.

### Truly Random Processes

**Radioactive decay** is an example of a truly random (stochastic) quantum mechanical process, not merely complex and deterministic.

## Statistical Mechanics Example

**Gas molecules:** Cannot model every atom in a room individually. Instead, we model the average velocity and call it **temperature**—a probabilistic/statistical way of quantifying information.

## Probability vs Statistics

### Probability
- **Given:** Known model/distribution
- **Find:** Predictions about future data
- **Example:** With a fair coin (known 50% probability), what's the chance of getting 10 heads in 10 flips?

### Statistics
- **Given:** Collected data/observations
- **Find:** Properties of the underlying model
- **Example:** After flipping a coin 10 times and getting 10 heads, what's the probability the coin is fair?