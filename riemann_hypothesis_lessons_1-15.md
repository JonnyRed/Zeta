# Riemann Zeta Function and Prime Numbers

## Lesson 1 — Prime Numbers

### 1. What is a prime?

A prime number is an integer greater than 1 whose only
positive divisors are 1 and itself.

The first primes are:

$$
2,3,5,7,11,13,17,19,23,29,\ldots
$$

The number 2 is the only even prime.

### 2. Composite numbers

A composite number is an integer greater than 1 that
is not prime.

For example:

$$
12=2\times2\times3
$$

$$
35=5\times7
$$

### 3. Unique prime factorisation

For example:

$$
84=2^2\times3\times7
$$

The Fundamental Theorem of Arithmetic says every
integer greater than 1 can be expressed as a product
of primes, and this factorisation is unique apart from
the order of the factors.

### 4. Why primes matter

Primes appear irregularly, but they obey deep
statistical patterns.

The Riemann Hypothesis is connected to how accurately
we can describe the distribution of primes.

### Exercises — Lesson 1

1. Is 1 prime? Explain your answer.
2. Write 60 as a product of primes.
3. List all primes between 20 and 50.
4. Explain why every even integer greater than 2
   is composite.

---

## Lesson 2 — Patterns Among the Primes

The primes become less frequent as numbers get larger,
but they never stop. We begin to describe their
distribution.

### 1. Counting primes

Let $\pi(x)$ denote the number of primes less than
or equal to $x$.

For example:

$$
\pi(10)=4
$$

because the primes up to 10 are 2, 3, 5 and 7.

### 2. Gaps between primes

The gap between consecutive primes is not constant:

- 2 and 3 differ by 1.
- 3 and 5 differ by 2.
- 23 and 29 differ by 6.

There is no simple repeating pattern.

### 3. The Prime Number Theorem

For large $x$:

$$
\pi(x)\approx\frac{x}{\ln(x)}
$$

The Prime Number Theorem describes the average
density of primes.

It says:

$$
\frac{\pi(x)}{x/\ln(x)}\longrightarrow1
$$

as $x$ grows.

This is an approximation, not an exact formula.

### 4. Why accuracy matters

The Riemann Hypothesis concerns the size of the error
in approximating $\pi(x)$ by its main term.

Better control of this error means a more precise
understanding of prime distribution.

### Exercises — Lesson 2

1. Calculate $\pi(20)$.
2. How many primes are there between 1 and 30?
3. Use $100/\ln(100)$ as an approximation to
   $\pi(100)$.
4. Why is the Prime Number Theorem an approximation
   rather than an exact counting rule?

---

## Lesson 3 — The Riemann Zeta Function

The zeta function is the central object in our course.
We first define it for real numbers $s>1$.

### 1. Definition — Lesson 3

$$
\zeta(s)=
1+\frac{1}{2^s}+\frac{1}{3^s}
+\frac{1}{4^s}+\cdots
$$

More compactly:

$$
\boxed{
\zeta(s)=\sum_{n=1}^{\infty}\frac{1}{n^s}
}
$$

Here $s$ is a real number greater than 1.

The expression means that we add one term for every
positive integer $n$.

### 2. A famous value

$$
\zeta(2)=
1+\frac14+\frac19+\frac1{16}+\cdots
$$

Euler proved that:

$$
\boxed{\zeta(2)=\frac{\pi^2}{6}}
$$

Numerically:

$$
\zeta(2)\approx1.644934
$$

This identity is known as the Basel problem.

### 3. Other values

$$
\zeta(3)\approx1.2020569
$$

The value $\zeta(3)$ is called Apéry's constant.

It is known to be irrational, although it does not
have a comparably simple expression in terms of $\pi$.

### 4. A first computation

A finite approximation is obtained by adding the first
$N$ terms:

$$
\zeta(s)\approx\sum_{n=1}^{N}\frac{1}{n^s}
$$

Increasing $N$ improves the approximation when $s>1$.

### Exercises — Lesson 3

1. Write the first five terms of $\zeta(3)$.
2. Explain what $\zeta(2)$ represents.
3. Why must we specify a value of $s$?
4. Estimate $\zeta(2)$ by adding its first four terms.

---

## Lesson 4 — Infinite Sums and Convergence

An infinite series is the sum of the terms of a
sequence.

The central question is whether its partial sums
approach a finite limit.

### 1. Partial sums

For a series:

$$
\sum_{n=1}^{\infty}a_n
$$

the partial sum of its first $N$ terms is:

$$
S_N=a_1+a_2+\cdots+a_N
$$

A series converges if the sequence of partial sums
$S_N$ approaches a finite number as $N$ increases.

Otherwise it diverges.

### 2. Geometric series

$$
1+r+r^2+r^3+\cdots=\frac{1}{1-r}
$$

provided:

$$
|r|<1
$$

For example:

$$
1+\frac12+\frac14+\frac18+\cdots=2
$$

If $|r|\geq1$, the infinite geometric series does
not converge.

### 3. The harmonic series

$$
1+\frac12+\frac13+\frac14+\cdots
$$

This series diverges.

Its terms approach zero, but the partial sums grow
without bound.

Small terms alone do not guarantee convergence.

### 4. Zeta connection — Lesson 4

The defining series for $\zeta(s)$ converges for
real $s>1$ and diverges for real $s\leq1$.

We will prove this threshold using tests for
convergence.

### Exercises — Lesson 4

1. What is a partial sum?
2. Find the sum of:

   $$
   1+\frac13+\frac19+\frac1{27}+\cdots
   $$

3. Does the harmonic series converge?
4. Does the fact that terms approach zero guarantee
   convergence?

---

## Lesson 5 — Euler's Product and the Primes

Euler discovered that the zeta function can also be
expressed as a product over all prime numbers.

This creates a direct link between the zeta function
and prime numbers.

### 1. A geometric-series identity

$$
1+x+x^2+x^3+\cdots=\frac{1}{1-x}
$$

provided:

$$
|x|<1
$$

For a prime $p$, substitute $x=1/p^s$.

This gives a series containing powers of that prime.

### 2. One prime at a time

$$
\frac{1}{1-p^{-s}}
=
1+p^{-s}+p^{-2s}+p^{-3s}+\cdots
$$

Multiplying these expansions over the primes generates
terms corresponding to integers with prime
factorisations.

### 3. Euler's product formula

For real $s>1$:

$$
\boxed{
\zeta(s)=
\prod_{p\ \text{prime}}
\frac{1}{1-p^{-s}}
}
$$

Unique prime factorisation ensures that each positive
integer appears exactly once in the expanded product.

This is why the product encodes all the terms of the
zeta series.

### 4. Why it matters

The series definition lists all positive integers.

The product definition lists primes.

Euler's formula connects the additive description
of the zeta function with the multiplicative structure
of integers.

### Exercises — Lesson 5

1. Expand $\frac{1}{1-2^{-s}}$ as a geometric series.
2. What mathematical fact ensures that each integer
   is represented once in Euler's product?
3. Write the first three prime factors of the
   Euler product.
4. Why is Euler's product important for number theory?

## Lesson 6 — Complex Numbers

The Riemann Hypothesis is about the zeta function
when its input is a complex number.

We therefore need to understand complex numbers.

### 1. The imaginary unit

$$
i^2=-1
$$

A complex number has a real part and an imaginary
part. It is written:

$$
z=a+bi
$$

where $a$ and $b$ are real numbers.

### 2. Real and imaginary parts

$$
\operatorname{Re}(z)=a
$$

$$
\operatorname{Im}(z)=b
$$

For $z=3+2i$:

- Real part = 3
- Imaginary part = 2

### 3. The complex plane

A complex number can be represented as a point
$(a,b)$ in a plane.

The horizontal axis is the real axis.

The vertical axis is the imaginary axis.

### 4. Modulus

$$
|z|=\sqrt{a^2+b^2}
$$

The modulus is the distance from the origin.

For $z=3+4i$:

$$
|z|=\sqrt{3^2+4^2}=5
$$

### 5. Complex conjugate

If:

$$
z=a+bi
$$

then:

$$
\overline{z}=a-bi
$$

The conjugate reflects a point across the real axis.

Also:

$$
z\overline{z}=|z|^2
$$

### Exercises — Lesson 6

1. Write the real and imaginary parts of $5-3i$.
2. Calculate $(2+3i)+(4-i)$.
3. Calculate $i^2$ and $i^3$.
4. Find the modulus of $3+4i$.
5. Find the conjugate of $7-2i$.

---

## Lesson 7 — Functions of a Complex Variable

A complex function takes a complex number as its
input and produces a complex number as its output.

The zeta function will eventually be studied
in this setting.

### 1. Function notation

$$
f:\mathbb{C}\to\mathbb{C}
$$

The symbol $\mathbb{C}$ denotes the set of complex
numbers.

A function $f$ assigns an output $f(z)$ to each
input $z$ in its domain.

### 2. A simple example

$$
f(z)=z^2
$$

If $z=1+i$, then:

$$
f(z)=(1+i)^2
$$

$$
=1+2i+i^2
$$

Since $i^2=-1$:

$$
f(z)=2i
$$

Complex functions can be evaluated using the usual
algebra rules, remembering that $i^2=-1$.

### 3. Limits and continuity

A complex function has a limit at a point if its
values approach the same complex number as the input
approaches that point from any direction in the
complex plane.

This is more demanding than approaching along
just one line.

### 4. Analytic functions

A function is analytic in a region if it is complex
differentiable throughout that region.

Analytic functions have strong structural properties
and are central to complex analysis.

### Exercises — Lesson 7

1. Evaluate $f(z)=z^2$ at $z=2+i$.
2. What does $\mathbb{C}$ represent?
3. In the complex plane, what does approaching a
   point from different directions mean?
4. In broad terms, what does it mean for a function
   to be analytic?

---

## Lesson 8 — Zeros of the Zeta Function

A zero of a function is an input at which the
function's output is zero.

The locations of certain zeros of the zeta function
are at the heart of the Riemann Hypothesis.

### 1. What is a zero?

If:

$$
f(z_0)=0
$$

then $z_0$ is called a zero of $f$.

For example:

$$
f(z)=z-3
$$

has a zero at:

$$
z=3
$$

### 2. Zeta zeros

The zeta function has so-called trivial zeros at
the negative even integers:

$$
-2,-4,-6,\ldots
$$

It also has non-trivial zeros in the critical strip.

### 3. The critical strip

$$
0<\operatorname{Re}(s)<1
$$

The critical strip is the region of the complex plane
in which the non-trivial zeros lie.

### 4. The critical line

$$
\operatorname{Re}(s)=\frac12
$$

The Riemann Hypothesis states that every
non-trivial zero has real part exactly $1/2$.

This is a conjecture, not a proven theorem.

### Exercises — Lesson 8

1. Find the zero of $f(x)=x-7$.
2. List the first three trivial zeros of $\zeta(s)$.
3. Write the inequalities defining the critical strip.
4. What does the Riemann Hypothesis assert about
   non-trivial zeros?

---

## Lesson 9 — The Integral Test

The integral test connects an infinite series with
an improper integral.

It is useful when the terms come from a positive,
decreasing function.

### 1. The test

Suppose $f(x)$ is positive, continuous and decreasing
for $x\geq1$, and:

$$
a_n=f(n)
$$

Then:

$$
\sum_{n=1}^{\infty}a_n
$$

and:

$$
\int_1^{\infty}f(x)\,dx
$$

either both converge or both diverge.

### 2. Example: the p-series

Consider:

$$
\int_1^{\infty}\frac{1}{x^p}\,dx
$$

For $p\ne1$, an antiderivative is:

$$
\frac{x^{1-p}}{1-p}
$$

If $p>1$, the improper integral is finite.

If $p<1$, it diverges.

### 3. The boundary case

$$
\int_1^{\infty}\frac1x\,dx
$$

$$
=\lim_{b\to\infty}\ln(b)
$$

$$
=\infty
$$

At $p=1$, the integral diverges.

This helps establish the convergence boundary
for the zeta series.

### 4. Zeta connection — Lesson 9

The integral test shows that:

$$
\sum_{n=1}^{\infty}\frac1{n^s}
$$

converges for real $s>1$ and diverges for
$0<s\leq1$.

For $s\leq0$, the terms do not approach zero,
so divergence follows immediately.

### Exercises — Lesson 9

1. Use the integral test to decide whether
   $\sum1/n^2$ converges.
2. What happens to $\int_1^{\infty}1/x\,dx$?
3. For which real $p$ does the p-series converge?
4. Why must $f$ be decreasing in the usual
   integral test?

---

## Lesson 10 — The Direct Comparison Test

The comparison test lets us decide whether a
positive-term series converges by comparing it
with a simpler series whose behaviour is known.

### 1. Comparison for convergence

If:

$$
0\leq a_n\leq b_n
$$

and:

$$
\sum b_n
$$

converges, then:

$$
\sum a_n
$$

also converges.

A positive-term series bounded above by a
convergent series must converge.

### 2. Comparison for divergence

If:

$$
0\leq b_n\leq a_n
$$

and:

$$
\sum b_n
$$

diverges, then:

$$
\sum a_n
$$

also diverges.

A positive-term series that is at least as large
term-by-term as a divergent series must diverge.

### 3. Example: convergence — Lesson 10

$$
\frac{1}{n^2+3}<\frac{1}{n^2}
$$

Since:

$$
\sum\frac1{n^2}
$$

converges, therefore:

$$
\sum\frac1{n^2+3}
$$

converges by comparison.

### 4. Example: divergence

For $n\geq1$:

$$
\frac{1}{\sqrt n}\geq\frac1n
$$

Since the harmonic series:

$$
\sum\frac1n
$$

diverges, therefore:

$$
\sum\frac1{\sqrt n}
$$

diverges by comparison.

### 5. Dominant terms

For large $n$, the highest powers often determine
the scale of a rational expression.

For example:

$$
\frac{3n+5}{n^3+2}
$$

behaves like:

$$
\frac{3}{n^2}
$$

This suggests comparison with $1/n^2$.

### Exercises — Lesson 10

1. Does $\sum1/(n^2+10)$ converge or diverge?
   Give a comparison.
2. Does $\sum1/(\sqrt n+1)$ converge or diverge?
3. Compare $(5n+2)/(n^3+7)$ with a p-series.
4. Why must the terms be non-negative for these
   simple comparison rules?

## Lesson 11 — The Limit Comparison Test

Sometimes a direct inequality is awkward.

The limit comparison test compares the long-term
size of two positive sequences using a ratio.

### 1. The main rule

Let:

$$
L=\lim_{n\to\infty}\frac{a_n}{b_n}
$$

If:

$$
0<L<\infty
$$

then $\sum a_n$ and $\sum b_n$ either both
converge or both diverge, provided the terms are
positive.

### 2. Example: divergence

Let:

$$
a_n=\frac{3n+5}{n^2+4}
$$

and:

$$
b_n=\frac1n
$$

Then:

$$
\begin{aligned}
L&=\lim_{n\to\infty}\frac{a_n}{b_n}\\
&=\lim_{n\to\infty}
\frac{3n^2+5n}{n^2+4}\\
&=3
\end{aligned}
$$

The harmonic series diverges, and the limit is a
finite positive number.

Therefore the original series diverges.

### 3. Example: convergence — Lesson 11

Let:

$$
a_n=\frac{2n^2+7}{n^4+3n}
$$

and:

$$
b_n=\frac1{n^2}
$$

Then:

$$
\begin{aligned}
L&=\lim_{n\to\infty}\frac{a_n}{b_n}\\
&=\lim_{n\to\infty}
\frac{2n^4+7n^2}{n^4+3n}\\
&=2
\end{aligned}
$$

Since $\sum1/n^2$ converges and the limit is 2,
the original series converges.

### 4. Choosing a comparison

For rational expressions in $n$, compare the
highest powers in the numerator and denominator.

This usually identifies the relevant p-series.

### Exercises — Lesson 11

1. Compare $\sum(4n+3)/(n^2+5)$ with $1/n$.
   Find $L$ and decide convergence.
2. Compare $\sum(n^2+3)/(n^4+8)$ with $1/n^2$.
3. Compare $\sum(3n^2+1)/(n^3+5)$ with $1/n$.
4. What does the test conclude if $L$ is positive
   and finite?

---

## Lesson 12 — The p-Series

The p-series is a fundamental family of infinite
series.

It provides a simple convergence rule and is the
basic reference series for much of our earlier work.

### 1. Definition — Lesson 12

$$
\sum_{n=1}^{\infty}\frac1{n^p}
$$

The exponent $p$ controls how quickly the terms
decrease.

### 2. The convergence rule

$$
\boxed{p>1\implies\text{converges}}
$$

$$
\boxed{p\leq1\implies\text{diverges}}
$$

For $p>1$ the terms decrease sufficiently quickly
for the total sum to be finite.

For $p\leq1$ the series diverges.

### 3. Examples

$$
\sum\frac1n\quad\text{diverges}
$$

$$
\sum\frac1{n^2}=\frac{\pi^2}{6}
$$

$$
\sum\frac1{n^3}\approx1.2020569
$$

Larger positive exponents generally make terms
decrease faster.

The $p=1$ boundary is critical.

### 4. Integral explanation

For $p>1$:

$$
\int_1^{\infty}x^{-p}\,dx
=\frac1{p-1}
$$

The integral test proves the rule.

At $p=1$ the integral is logarithmic and diverges.

For $p<1$ it also diverges.

### 5. Zeta connection

$$
\zeta(s)=\sum_{n=1}^{\infty}\frac1{n^s}
$$

The p-series is precisely the defining zeta series
when $p$ is replaced by the real variable $s$.

### Exercises — Lesson 12

1. Does the p-series converge for $p=1.2$?
2. Does it converge for $p=0.8$?
3. What happens at $p=1$?
4. Why does being close to 1 not change the rule?
5. What is $\zeta(2)$?

---

## Lesson 13 — Sequences, Limits and the nth-Term Test

A sequence is a list of numbers.

A series is the sum of the terms in a sequence.

Keeping these ideas separate is essential.

### 1. Sequences

$$
a_1,a_2,a_3,\ldots
$$

For example:

$$
a_n=\frac1n
$$

A sequence has a limit if its terms approach
a fixed number as $n$ grows.

### 2. Limits

$$
\lim_{n\to\infty}\frac1n=0
$$

The limit describes what the terms approach.

$n$ does not literally become infinity.

### 3. Partial sums

$$
S_n=a_1+a_2+\cdots+a_n
$$

A series converges when its partial sums approach
a finite limit.

### 4. Necessary condition

If:

$$
\sum a_n
$$

converges, then:

$$
\boxed{\lim_{n\to\infty}a_n=0}
$$

Since:

$$
a_n=S_n-S_{n-1}
$$

and both partial sums approach the same limit,
their difference must approach zero.

### 5. The warning

If the terms do not approach zero, the series
definitely diverges.

If the terms do approach zero, the test is
inconclusive.

For example:

$$
\sum\frac1n\quad\text{diverges}
$$

but:

$$
\sum\frac1{n^2}\quad\text{converges}
$$

### Exercises — Lesson 13

1. Find $\lim_{n\to\infty}5/n$.
2. Find $\lim_{n\to\infty}(2n+3)/(n+5)$.
3. Find $\lim_{n\to\infty}(n^2+4)/(3n^2+1)$.
4. Use the nth-term test on $\sum(n+2)/n$.
5. Can the nth-term test decide $\sum1/n^2$?
   Explain.

---

## Lesson 14 — Alternating Series and Conditional Convergence

An alternating series has terms that switch between
positive and negative.

Cancellation can make such a series converge even
when the corresponding positive-term series diverges.

### 1. Alternating harmonic series

$$
1-\frac12+\frac13-\frac14+\cdots=\ln(2)
$$

The harmonic series with all positive terms diverges.

But the alternating harmonic series converges to:

$$
\ln(2)\approx0.693147
$$

### 2. Alternating series test

An alternating series:

$$
\sum_{n=1}^{\infty}(-1)^{n+1}b_n
$$

converges if $b_n$ decreases to zero.

More precisely, the positive magnitudes $b_n$ must
be non-increasing eventually and must tend to zero.

### 3. Absolute convergence

$$
\sum|a_n|\text{ converges}
\implies
\sum a_n\text{ converges}
$$

For example, the alternating series with terms
$1/n^2$ converges absolutely because:

$$
\sum\frac1{n^2}
$$

converges.

### 4. Conditional convergence

A series is conditionally convergent if:

$$
\sum a_n\text{ converges}
$$

but:

$$
\sum|a_n|\text{ diverges}
$$

The alternating harmonic series is conditionally
convergent.

It converges, but its absolute-value series is
the divergent harmonic series.

### 5. Why it matters

Absolute and conditional convergence behave
differently under rearrangement.

This leads to the next lesson and to the work
of Riemann.

### Exercises — Lesson 14

1. Does $1-1/3+1/5-1/7+\cdots$ converge?
2. Is $\sum(-1)^{n+1}/n^2$ absolutely or
   conditionally convergent?
3. Does $\sum(-1)^{n+1}/\sqrt n$ converge?
4. What is conditional convergence?
5. Explain the difference between $\sum1/n^2$
   and $\sum(-1)^{n+1}/n$.

---

## Lesson 15 — Rearrangement of Infinite Series

For finite sums, changing the order of addition
does not change the answer.

For infinite series, the situation depends on
the kind of convergence.

### 1. Absolute convergence

If:

$$
\sum|a_n|
$$

converges, then every rearrangement of the terms
converges to the same sum.

The order does not affect the result.

### 2. Conditional convergence

A conditionally convergent series converges,
but its absolute-value series diverges.

The alternating harmonic series is the standard
example.

### 3. Riemann rearrangement theorem

A conditionally convergent real series can be
rearranged to converge to any prescribed rea
