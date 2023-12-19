# Definition and Calculation techiques

## Definition of Generating function

Let $a_1, a_2, a_3, a_4, ..., a_{\infin}$ be a sequence of real number.  
The funtion
$$f(x) = a_0 + a_1 x + a_2 x^2 + ... = \sum_{i=0}^{\infin}a_i x^i$$
is called the generating function for the given sequence.

### Example 1

For any $n \in \Z^+$,  
$$(1 + x)^n = \binom{n}{0} + \binom{n}{1}x + \binom{n}{2}x^2 + ... + \binom{n}{n}x^n$$
so $(1 + x)^n$ is the generating function for the sequence
$$\binom{n}{0}, \binom{n}{1}, \binom{n}{2}, ..., \binom{n}{n}, 0, 0, 0, 0, ...$$

### Example 2

For any $n \in \mathbb{Z}^+$,
$$(1 - x^{n+1}) = (1 - x)(1 + x + x^2 + x^3 + ... + x^n)$$
by following:
$$(1-x)(1 + x + x^2 + x^3 + ... + x^n) = \\
(1 + x + x^2 + x^3 + ... + x^n) - (x + x^2 + x^3 + x^4 ... + x^{n+1}) = \\
(1 - x^{n+1})$$
So
$$\dfrac{1 - x^{n+1}}{1-x} = 1 + x + x^2 + x^3 + ... + x^n$$
and $\frac{1 - x^{n+1}}{1-x}$ is the generating function for the sequence $1, 1, 1, ..., 1, 0, 0, 0, ...$, where the $n+1$ terms are $1$.
