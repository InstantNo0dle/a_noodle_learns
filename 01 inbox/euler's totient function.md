date: 2022-11-14
tags: #math/numbertheory
# euler's totient function

> [!info] Formal definition and formula
> This function $\phi (n)$ counts the number of relatively prime integers less than $n$.
> $$\phi(n) = n(1-\frac{1}{p_1})(1-\frac{1}{p_2})  ...(1-\frac{1}{p_k})$$

Mathematically, it can also be represented as the number of integers $[1,n)$ such that:
$$ gcd(m, n)=1$$

These relatively prime integers are part of a **set** $(\mathbb{Z}/n)^*$ so $\phi(n)$ is just the size of that set.
- $(\mathbb{Z}/n)$ is the set of integers less than $n$ without the gcd restriction and represents the integers *modulo* $n$.

A well known *property* is **divisor sum**:
$$
\sum_{d|n} \phi(d) = n
$$

## derivation of formula
This function is multiplicative if $gcd(a,b) = 1$ the two numbers are relatively prime themselves:
$$
\phi(ab) = \phi(a)\phi(b)
$$

Since the function is multiplicative, it can be decomposed in terms of primes:
$$
\phi(n) = \phi(p_1^{e_1})\phi(p_2^{e_2}) ...
$$
Each prime function can be written as:
$$
\phi(p^e) = p^e - p^{e-1}=p^e(1-\frac{1}{p})
$$
- Subtraction accounts for the multiples of the prime

Substituting this in yields:
$$\phi(n) = n(1-\frac{1}{p_1})(1-\frac{1}{p_2})  ...(1-\frac{1}{p_k})
$$


---
## Sources
[Euler's Totient Function | Brilliant Math & Science Wiki](https://brilliant.org/wiki/eulers-totient-function/?)