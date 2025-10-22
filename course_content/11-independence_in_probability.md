# Independence in Probability

## Definition of Independence
- **Two events A and B are independent** if knowing that one occurred gives no extra information about the other.
- Formally: If knowing that A happened does not change the probability of B, and knowing that B happened does not change the probability of A, then A and B are independent.

## Mathematical Formulation
- **Independence means:**
  - $P(A|B)=P(A)$
  - $P(B|A)=P(B)$

## Consequence: Multiplication Rule
- If A and B are independent:
  - $P(A\cap B)=P(A)\times P(B)$
- This follows from the conditional probability formula:
  - $P(A|B)=\frac{P(A\cap B)}{P(B)}$
  - If $P(A|B)=P(A)$, then $P(A\cap B)=P(A)\times P(B)$

## Example: Cards
- Deck of 52 cards: 4 suits (clubs, hearts, diamonds, spades), 13 values (1–10, Jack, Queen, King).
- Event A: Card is a spade (1 in 4 chance).
- Event B: Card is a queen (1 in 13 chance).
- Probability of both (Queen of Spades):
  - $P(A\cap B)=P(A)\times P(B)=\frac{1}{4}\times\frac{1}{13}=\frac{1}{52}$
- Knowing the card is a queen tells you nothing about whether it is a spade, and vice versa.

## Example: Coin Flips
- Flipping a coin multiple times: Each flip is independent of the others.
- The outcome of one flip does not affect the outcome of another.

## Reliability: Series and Parallel Systems
### Series System
- **n components in series**, each with probability $p$ of failure.
- If any one fails, the whole system fails.
- Probability of all components succeeding: $(1-p)^n$
- Probability of system failure:
  - $1-(1-p)^n$

### Parallel System
- **n components in parallel**, each with probability $p$ of failure.
- System fails only if all components fail.
- Probability of system failure:
  - $p^n$
- Much lower chance of failure compared to series.

## Summary of Key Formulas
- **Independence:**
  - $P(A|B)=P(A)$
  - $P(B|A)=P(B)$
  - $P(A\cap B)=P(A)\times P(B)$
- **Series system failure:**
  - $1-(1-p)^n$
- **Parallel system failure:**
  - $p^n$