# Binomial and Multinomial Coefficients for Counting

## Unordered samples without replacement
- The number of unordered samples of size $r$ drawn without replacement from $n$ objects is the binomial coefficient $\binom{n}{r}$, given by $\binom{n}{r} = \frac{n!}{(n-r)!\,r!}$, where $n!$ denotes $n \times (n-1) \times \cdots \times 1$.  
- Example: the number of 5‑card poker hands from a 52‑card deck is $\binom{52}{5}$ because order does not matter and drawing is without replacement.  

## Binomial coefficient and polynomial expansion
- The coefficients in the expansion of $(x+y)^n$ are the binomial coefficients: $(x+y)^n = \sum_{k=0}^{n} \binom{n}{k} x^{k} y^{\,n-k}$ .  
- Pascal’s triangle generates these coefficients row by row via addition of neighboring entries, producing sequences like $1$, $1\,1$, $1\,2\,1$, $1\,3\,3\,1$, $1\,4\,6\,4\,1$, $1\,5\,10\,10\,5\,1$.  
- For large $n$, the shape of these coefficient rows visually approaches a normal (Gaussian) profile; a physical analogy is balls dropping through a lattice of pegs and accumulating in a bell‑shaped pattern.  

## Multinomial coefficient: dividing into multiple groups
- When $n$ objects are partitioned into $R$ classes of sizes $N_1, N_2, \ldots, N_R$ with $N_1+\cdots+N_R=n$ and order not important, the count is the multinomial coefficient  
  $$
  \binom{n}{N_1, N_2, \ldots, N_R} = \frac{n!}{N_1!\,N_2!\,\cdots\,N_R!}.
  $$  
- Interpretation: this generalizes “dealing one hand” to “dealing multiple hands”; e.g., splitting a deck among several players or allocating items into several labeled groups.  

## Derivation by successive choices
- Build the partition sequentially: first choose $N_1$ items from $n$, then $N_2$ from the remaining $n-N_1$, then $N_3$ from $n-N_1-N_2$, and so on, yielding  
  $$
  \binom{n}{N_1}\,\binom{n-N_1}{N_2}\,\binom{n-N_1-N_2}{N_3}\cdots \binom{n-\sum_{i=1}^{R-1}N_i}{N_R}.
  $$  
- Writing each binomial as factorials and canceling the telescoping terms leaves exactly $\frac{n!}{N_1!\cdots N_R!}$; note the final remainder is $0! = 1$ because $N_1 + \cdots + N_R = n$.  

## Practical uses and prompts
- Cards: the binomial counts single 5‑card hands; the multinomial counts ways to deal multiple hands or split an entire deck among players.  
- Quality control: grouping items into categories (e.g., good vs. bad) is naturally modeled by multinomial counting when tallying exact category counts in a draw without replacement.  
- Exercises to try:  
  - With $2n$ people, how many distinct ways can they be paired into $n$ disjoint pairs?  
  - From 7 people, how many ways can you form subcommittees of sizes $2,3,2$ (order of subcommittees unlabeled but sizes fixed)?  

## Key takeaways
- Use $\binom{n}{r}$ for unordered, without‑replacement selections of size $r$ from $n$.  
- The same coefficients govern $(x+y)^n$, link to Pascal’s triangle, and exhibit a bell‑shaped profile for large $n$.  
- For multiple labeled groups with fixed sizes summing to $n$, use the multinomial $\frac{n!}{\prod_i N_i!}$, derivable by successive binomial selections that telescope.
