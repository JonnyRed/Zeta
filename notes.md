# Notes on the zeta function

## The prime number theorem

The prime number theorem describes the asymptotic distribution of prime
numbers. It states that the number of primes less than a given number
$n$ is approximately $\frac{n}{\log n}$, where $\log$ denotes the
natural logarithm. Formally, if $\pi(n)$ denotes the prime-counting
function, then
$$
\pi(n) \sim \frac{n}{\log n} \quad \text{as } n \to \infty.
$$

## Riemann zeta function

The Riemann zeta function is defined for complex numbers $s$ with real
part greater than 1 by the series
$$
\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}.
$$
It can be analytically continued to other values of $s$ (except $s=1$,
where it has a simple pole) and plays a central role in number theory,
particularly in the distribution of prime numbers.

One of the key connections between the zeta function and prime
numbers is given by the Euler product formula:
$$
\zeta(s) = \prod_{p \text{ prime}} \frac{1}{1 - p^{-s}},
\quad \text{for } \Re(s) > 1.
$$
This formula shows that the zeta function encodes information about all
prime numbers.

Moreover, the non-trivial zeros of the Riemann zeta function are deeply
connected to the distribution of prime numbers, as conjectured by the
Riemann Hypothesis. Understanding these zeros can provide insights into
the error term in the prime number theorem and the precise distribution
of primes.

## Connection to the prime number theorem

The prime number theorem can be derived from properties of the Riemann
zeta function. In particular, the fact that $\zeta(s)$ has no zeros on
the line $\Re(s) = 1$ (except for the trivial zeros at negative even
integers) is crucial in establishing the asymptotic formula for
$\pi(n)$. The Riemann Hypothesis, which posits that all non-trivial
zeros lie on the critical line $\Re(s) = \frac{1}{2}$, would further
refine our understanding of the error term in the prime number theorem.
