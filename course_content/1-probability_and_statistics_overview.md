## Why Probability and Statistics Matter

Probability and statistics rank alongside differential equations, calculus, and linear algebra as foundational mathematical tools for describing complexity in the real world. They are especially critical in the modern era for data science and machine learning applications. 

### Key Applications

**Thermodynamics and Gas Molecules:** With $10^{23}$ molecules in a mole of gas (Avogadro's number), it's impossible to measure or simulate every particle's position and velocity. Probability provides elegant descriptions through simplified statistical quantities like temperature and entropy, using distributions such as Boltzmann or Maxwell distributions. 

**Turbulence:** Similar to gases, turbulent fluids (like air over airplane wings) contain too many degrees of freedom to measure or model with certainty, making them excellent candidates for probabilistic models. 

**Measurement Error:** One of the foundational applications of probability, pioneered by Laplace. When repeating physical measurements (like acceleration of gravity or electron charge), results vary slightly and typically follow a normal (Gaussian) distribution. Laplace was a key founder of modern probability and statistics, developing theory to quantify uncertainty in models of the real world. 

**Control Theory:** The Kalman filter merges dynamics and control with probabilistic perspectives, modeling measurement errors (typically Gaussian) and external forces beyond our ability to model. 

**Weather and Human Behavior:** Throughout history, humans have grappled with uncertainty through various means, from ancient divination practices (astrology, augury, tea reading) to modern scientific approaches. Laplace and others transformed understanding from divination to probability and statistics-similar to how astrology became astronomy and alchemy became chemistry. 

## Deterministic vs Probabilistic Systems

Many systems modeled probabilistically are fundamentally deterministic but too complex to predict precisely. Example: A coin flip follows $F = ma$ with gravity, wind resistance, mass, and inertia-technically deterministic but practically random due to measurement and modeling uncertainty. Weather phenomena are chaotic dynamical systems that are deterministic but have finite prediction horizons, requiring probabilistic models beyond certain time scales. 

## Probability vs Statistics: Core Definitions

**Probability:** Assumes a known probability distribution and predicts future samples/data. Example: With a fair coin (known 50% probability), probability quantifies the likelihood of specific outcomes like getting 5, 7, or 10 heads in 10 flips. 

**Statistics:** The inverse problem-data/samples are known, but the probability distribution is unknown. Example: After flipping a coin 100 times, statistics determines if it's fair and estimates the probability of heads. 

These are dual problems, two sides of the same coin. Learning probability first provides the family of models needed when working with actual data. 

## Course Outline: Probability Topics

### Topic 1: Introduction to Probability

Focus on **examples and intuition**, understanding that probability is fundamentally about **counting sets** of possible events. Example problems include: 
- Probability of flipping 7 heads in 10 coin flips
- Number of poker hands from a 52-card deck
- Probability that three dice sum to 13

### Topic 2: Random Variables and Distributions

**Random Variable:** A variable $X$ with a probability of taking specific values given parameters $\theta$. For normally distributed variables, parameters include mean and standard deviation:on: $P(X = v | \theta)$ where $\theta = (\mu, \sigma)$ .

Random variables support operations like squaring, logarithms, and calculus, just like traditional variables. 

**Key Probability Distributions:**

**Bernoulli:** Describes events with two outcomes (heads/tails, success/failure). 

**Binomial:** Describes the sum of multiple independent Bernoulli random variables (e.g., number of heads in multiple coin flips). In the large sample limit, binomial distributions approach normal distributions. 

**Normal (Gaussian):** Arises when measurement error comes from multiple additive factors. The sum of many random variables tends toward normal distribution regardless of individual distributions-this is the Central Limit Theorem. 

**Poisson:** The limit of binomial distribution for rare events (e.g., light bulb failures, radioactive alpha particle emissions). 

**Exponential:** Describes waiting times between Poisson events, such as time between radioactive decay emissions. 

The course will cover approximately 10 of the most useful distributions. 

**Unknown Distributions:** When distributions are unknown but data exists, this becomes a machine learning problem-learning distributions from data for complex systems like turbulence and human behavior. 

### Topic 3: Functions of Random Variables

Key statistical measures for quantifying distributions:

**Expected Value:** The predicted value a random variable will take. 

**Variance/Standard Deviation:** Measures spread in predictions. 

**Median:** Robust alternative to mean. 

These numbers provide essential information about distributions, analogous to how temperature and entropy characterize gas distributions. In statistics, these quantities are estimated from data. 

### Topic 4: Central Limit Theorem

One of the most important topics in probability and the cornerstone of statistics. It states that averaging or summing random variables with the same distribution produces a normally distributed result, regardless of the original distribution. 

For random variables $X_i$ where $i = 1$ to $n$, the sample mean:

$
\bar{X} = \frac{1}{n} \sum_{i=1}^{n} X_i
$

tends to be normally distributed with some mean and variance, even if the original data had Poisson, binomial, exponential, or other distributions. This explains why Gaussian measurement error is so common and is fundamental to statistical inference. 

## Preview: Statistics Topics

Statistics flips the probability framework: instead of $P(\text{data} | \theta)$, statistics finds $P(\theta | \text{data})$-the probability of model parameters given observed data .

**Hypothesis Testing:** Determining if treatments work (e.g., clinical drug trials) with quantifiable confidence levels like "95% confident this drug works". 

**Survey Sampling:** Using small samples (e.g., 1,000 people) to infer properties of large populations (e.g., 300+ million Americans). 

**Parameter Estimation:** Finding the most likely model parameters from data. In machine learning, $\theta$ represents neural network weights learned from data-fundamentally a statistics problem. 

**Bayesian Statistics:** Incorporates prior knowledge with data to build better probabilistic models, commonly used in modern machine learning. 