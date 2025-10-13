# Counting in Probability: Sequences, Permutations, and Combinations

## Fundamental Principle: Probability as Counting

Probability is about computing how likely an event is to happen. For simple cases (coin flips, dice rolls, poker hands), this means:

$P(A) = \frac{\text{Number of ways A can happen}}{\text{Total number of possible outcomes}}$

As the number of possibilities grows, direct enumeration becomes impractical. Instead, we use **combinatorics**—clever counting methods—to calculate probabilities efficiently.

***

## Example 1: Sequences of Coin Flips

**Question:** How many unique sequences are possible when flipping a coin 10 times?

- Each flip is independent and has 2 outcomes (heads or tails).
- Order matters: "HTHT..." is different from "THTH...".

**Calculation:**
- For 10 flips: $2^{10}$ possible sequences.
- This is because each flip multiplies the number of possibilities by 2.

**General Formula (Order Matters, With Replacement):**
- If you have $n$ choices and $r$ trials: $n^r$
- Example: 2 choices (coin), 10 trials: $2^{10}$

***

## Example 2: Ordered Poker Hands (Without Replacement)

**Question:** How many ordered 5-card runs can you deal from a 52-card deck?

- Each card is drawn without replacement (once a card is dealt, it's not put back).
- Order matters: "King, Queen, 3, 5, 7" is different from "Queen, King, 3, 5, 7".

**Calculation:**
- First card: 52 choices
- Second card: 51 choices
- Third card: 50 choices
- Fourth card: 49 choices
- Fifth card: 48 choices
- Total: $52 \times 51 \times 50 \times 49 \times 48$
- Shorthand: $\frac{52!}{47!}$

**General Formula (Order Matters, Without Replacement):**
- $\frac{n!}{(n-r)!}$
- Example: 52 cards, 5 drawn: $\frac{52!}{47!}$

***

## Factorials

- $n! = n \times (n-1) \times (n-2) \times \ldots \times 1$
- Example: $5! = 5 \times 4 \times 3 \times 2 \times 1 = 120$

***

## When Order Doesn't Matter: Combinations

**Poker Hand Example:**
- The order of cards in a hand doesn't matter ("King, Queen, 3, 5, 7" is the same as "Queen, King, 3, 5, 7").
- To account for this, divide by the number of ways to arrange the hand ($r!$).

**Formula:**
$\text{Number of combinations} = \frac{n!}{r!\,(n-r)!}$
- This is called "n choose r" or $\binom{n}{r}$.

***

## Summary Table

| Scenario                      | Formula                        | Order Matters? | Replacement?        |
|-------------------------------|-------------------------------|---------------|--------------------|
| Coin flips (10 times)         | $2^{10}$                    | Yes           | With replacement   |
| Ordered 5-card run (deck)     | $\frac{52!}{47!}$           | Yes           | Without replacement|
| Poker hand (order doesn't matter) | $\frac{52!}{5!\,47!}$   | No            | Without replacement|

***

## License Plate Example

Suppose a license plate has 4 letters (A-Z) and 2 numbers (0-9):
- **Order matters** ("ABCD12" ≠ "DCBA21")
- **With replacement** (letters/numbers can repeat)

**Calculation:**
- 26 choices for each letter, 10 for each number
- Total: $26^4 \times 10^2$

If letters/numbers can't repeat (without replacement), use factorial formulas.

***

## Key Takeaways

- **Order matters:** Use powers or factorials
- **Without replacement:** Use factorial division
- **Order doesn't matter:** Divide by $r!$ (combinations)
- These principles let you count possibilities for complex probability problems without direct enumeration.

Next, you'll use these tools to model real-world scenarios and calculate probabilities for more sophisticated events.