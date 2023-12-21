# Definition and Calculation techiques

## The extension of $\binom{n}{r}$

With $n, r \in \mathbb{Z}^+$, and $n \geq r \gt 0$, we have
$$\binom{n}{r} = \frac{n!}{r!(n-r)!} = \frac{n(n-1)(n-2)...(n-r+1)}{r!}$$

as the definition of $\binom{n}{r}$, for any $n \in \mathbb{Z}^+$, we have
$$\binom{-n}{r} = \frac{-n(-n-1)(-n-2)...(-n-r+1)}{r!} = (-1)^r \frac{(n+r-1)!}{r!(n-1)!} = (-1)^r \binom{n+r-1}{r}$$

<font color=#FF5151>**Note:** For each *real* number $n$, we define $\binom{n}{0} = 1$.</font>

---

## $(1 + x)^{-n}$

For any $n \in \mathbb{Z}^+$, the Maclaurin series expansion for $(1+x)^n$ is given by
$$(1+x)^{-n} = 1 + \frac{(-n)(-n-1)x^2}{2!} +\frac{(-n)(-n-1)(-n-2)x^3}{3!} + ... \\ = 1 + \sum_{r=1}^{\infin} \frac{(-n)(-n-1)(-n-2)...(-n-r+1)}{r!} x^r \\ =\sum_{r=0}^{\infin}(-1)^r\binom{n+r-1}{r}x^r = \sum_{r=0}^{\infin}\binom{-n}{r}x^r$$

### Example

#### Find the coefficient of $x^5$ in $(1-2x)^{-7}$

With the definition of $(1 + x)^{-n}$, the coefficient of $x^5$ is $\binom{-7}{5}(-2)^{5} = (-1)^{5}\binom{7+5-1}{5}(-2)^5 = 14787$.

#### What sequence does $(1+3x)^{-1/3}$ generate

With the definition of $(1+x)^{-n}$,  
$$(1+3x)^{-1/3} = 1 + \sum_{r=1}^{\infin}\frac{(-1/3)(-4/3)(-7/3)...((2-3r)/3)}{r!}(3x)^r \\ =1 + \sum_{r=1}^{\infin}\frac{(-1)(-4)(-7)...(2-3r)}{r!}x^r$$
Therefore, $(1+3x)^{-1/3}$ generates the sequence $1, -1, (-1)(-4)/2!, (-1)(-4)(-7)/3!, ..., (-1)(-4)(-7)...(2-3r)/r!, ...$.

---

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

---

Extending *Example 2* from the *Definition of Generating Function*, we find that $\frac{1-x^{n+1}}{1-x}$ represents the **sum of a geometric series** with $a_0 = 1$, $d = x$, and length $n+1$. The geometric series **converges** when $|x| < 1$. As $x$ approaches infinity, $\lim\limits_{x\rightarrow\infty}\frac{1-x^{n+1}}{1-x} = \frac{1}{1-x}$.

Therefore, $\frac{1}{1-x}$ serves as the generating function for the sequence $1, 1, 1, 1, \ldots$.

<font color=#FF5151>**Note:** Our main focus should be on the coefficients of the powers of $x$.</font>

### Example

#### Determine the coefficient of $x^{15}$ in $f(x) = (x^2 + x^3 + x^4 + ...)^4$

Since $(x^2 + x^3 + x^4 +...) = x^2(1 + x^2 + x^3 +...) = x^2 / (1-x)$
The coefficient of $x^{15}$ is the coefficient of $x^{15}$ in $f(x) = [x^2/(1-x)]^4 = x^8 / (1-x)^{-4}$.
Hence, the coefficient sought is that of $x^7$ in $(1-x)^{-4}$.
Namely, the coefficient is $(-1)^7\binom{-4}{7} = (-1)^7(-1)^7\binom{10}{7} = 120$.

#### Verify that for all $n \in \mathbb{Z}^+$, $\binom{2n}{n} = \sum_{i=0}^{n}\binom{n}{i}^2$

Since $(1+x)^{2n} = [(1+x)^n]^2$, by comparing the coefficients, the coefficient of $x^n$ must be equal to the coefficient of $x^n$ in $(1+x)^n(1+x)^n$.
Let $x^n = x^px^q$, then $p+q=10$. Consequently, the coefficient of $x^n$ in $(1+x)^n(1+x)^n$ is $\binom{n}{0}\binom{n}{n} + \binom{n}{1}\binom{n}{n-1} + ... + \binom{n}{n}\binom{n}{0} = \sum_{r=0}^{n}\binom{n}{r}\binom{n}{n-r}$.
With $\binom{n}{r} = \binom{n}{n-r}$, for all $0 \leq r \leq n$, the result follows.
