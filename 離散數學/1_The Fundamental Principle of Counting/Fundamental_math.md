# The fundamental of Counting

## Key point

| Order is Relevant | Repetitions are Allowed | Type of Result | Formula |
| :--: | :--: | :--: | :--: |
| Yes  | No | [Permutation](#permutation) | $P(n, r) = \dfrac{n!}{(n-r)!}$ |
| No | No | [Combination](#combination) |  $C(n, r) = \dfrac{n!}{r!(n-r)!} = \dbinom{n}{r}$ |
| No | Yes | [Combination with Repetition](#combination_repetition) | $\dbinom{n + r -1}{n}$ |

---

### <span id = "permutation">What is permutation</span>

Given n **distinct** objects, any **linear arrangement** of them is called **permutation**.
$P(n, r) = \dfrac{n!}{(n-r)!}$

#### Classic Problem

1. x-y plane path problem

   - **Description:**
   Determine the number of paths in the xy-plane from the starting point $(x_1, y_1)$ to the destination $(x_2, y_2)$. At each step, you can move either one unit to the right or one unit upwards.
   - **Solution:**
   Regardless of the specific path, the total number of rightward and upward movements is fixed. By arranging these movements, you can calculate the total number of paths.
   - **Example:**
   Determine the number of paths in the xy-plane from $(2, 1)$ to $(7, 4)$.
   - **e.g. Solution:**
   You need to take 5 steps to the right and 3 steps upwards. To find the total number of arrangements, you can use the formula for permutations with 5 repeated objects and 3 repeated objects.
   In this case, the number of arrangement is $\dfrac{8!}{5!3!} = 56$

2. round table seat arrangement

    - **Description:**
    Consider a group of people seated around a round table, and we want to determine the total number of distinct arrangements. Arrangements are considered the same if one can be obtained from the other by rotation.
    - **Solution:**
    Assuming there are $n$ people seated at the round table, if everyone is seated to their right side, it still represents the same arrangement. Therefore, for any given arrangement, there are $n-1$ invalid (identical) permutations due to rotation. Consequently, the total number of distinct arrangements is given by $\dfrac{n!}{n} = (n-1)!$.
    - **Example:**
    If there are six people labeled as A, B, ..., F, seated around a round table, how many different circular arrangements are possible?
    - **e.g. Solution:**
    The number of distinct circular arrangements is given by \$dfrac{6!}{6} = 5! = 120$.

---

### <span id = "combination">What is combination</span>

Given n **distinct** objects and select r of them with no reference to order.
$C(n, r) = \dfrac{P(n, r)}{r!} \ = \dfrac{n!}{r!(n - r)!} = \dbinom{n}{r}$

### <span id = "combination_repetition">Combinations with Repetition</span>

To distribute $n$ **identical** objects among $r$ **distinct** containers, the number of combinations is equivalent to the arrangements with $n$ **identical** objects and $(r-1)$ **identical** dividers or boards.
The $r-1$ boards effectively partition the $n$ objects into $r$ sections, representing each of the containers. Therefore, the number of combinations can be calculated using the formula:
$$\dbinom{n + r - 1}{n}$$

#### Classic Problems

1. at least-distribution (identical to distinct)
    - **Description:**
    Find the number of ways to distribute $a_1$ of one type, $a_2$ of another, $a_3$, etc., among $x$ people, ensuring that each person receives at least $y$ of each kind.
    - **Solution:**
    Start by giving $y$ of each item to every person. Then, distribute the remaining items.
    - **Example:**
    How many ways can you distribute 11 chocolate cookies and 8 strawberry cookies among 4 kids if each kid must receive at least one cookie of each kind?
    - **e.g. Solution:**
    1. Begin by giving one chocolate cookie and one strawberry cookie to each kid, leaving 7 chocolate cookies and 4 strawberry cookies.
    So it will remain 7 chocolate cookies and 4 strawberry cookies.
    2. Find the number of ways to distribute the remaining 7 chocolate cookies and 4 strawberry cookies among the 4 kids.
    3. Use the formula for combinations: $\binom{n + r - 1}{r}$.
    $ \space $
    - $\dbinom{7 + 4 - 1}{7} \times \dbinom{4 + 4 - 1}{4} = \dbinom{10}{7} \times \dbinom{7}{4}$.
2. at-least-distribution (distinct to distinct)
    - **Description:**
    In how many ways can Beth place 24 **different** books on four shelves so that there is at least one book on each shelf? (For any of these arrangements consider the books on each shelf to be placed one next to the other, with the first book at the left of the shelf.)
    - **Solution:**
   1. Assume there are 24 **identical** books that need to be distributed among 4 shelves.
   2. Choose 4 books to be placed on the shelves to ensure there is at least one book on each shelf.
   3. Distribute the reaming 20 **identical** books among 4 shelves.
      - $\dbinom{20+4-1}{20} = \dbinom{23}{20}$
   4. Therefore, there are a total of 24 books on the 4 shelves. Visualize this as having 24 empty spaces on the 4 shelves, and now we need to place 24 **distinct** books into these empty spaces.
   5. Arrange the 24 different books in the empty spaces.
        - $24!$

        Therefore, the total number of distributions is $24! \dbinom{23}{20}$.

---

### Binomial Theorem

$\displaystyle
(a+b)^n = \\
\binom{n}{0}a^0b^n + \binom{n}{1}a^{1}b^{n-1} + ... + \binom{n}{n-1}a^{n-1}b^{1} + \binom{n}{n}a^nb^0 = \\
\sum_{i=0}^{n}\binom{n}{i}a^ib^{n-i}$

#### Extension of Binomial Theorem

1. $\displaystyle \sum_{i=0}^{n} \binom{n}{i} = (1 + 1)^n =  2^n$
2. $\displaystyle \sum_{i=0}^{n} (-1)^i \binom{n}{i} = (1 -1)^n = 0$

#### Classic Problems

1. **Question:** For any positive integer determine:
$$ \displaystyle \sum_{i=0}^{n} \dfrac{1}{i! \ (n-i)!} $$

**Solutions:**

- $\dbinom{n}i = \dfrac{n!}{i! \ (n-i)! }$
- $\displaystyle \sum_{i=0}^{n}\binom{n}{i} = 2^n$
- $\displaystyle \sum_{i=0}^{n} \frac{1}{i! \ (n-i)!} = \frac{1}{n!} \sum_{i=0}^{n} \frac{n!}{i! \ (n-i)!} = \frac{!}{n!}\sum_{i=0}^{n}\binom{n}{i} = \frac{2^n}{n!}$

2. **Question:** For any positive integer determine:
$$\displaystyle \sum_{i=0}^{n} \dfrac{(-1)^i}{i! \ (n-i)!}$$
**Solution:**

- $\displaystyle
\sum_{i=0}^{n} \frac{(-1)^i}{i! \ (n-i)!} =
\frac{1}{n!} \sum_{i=0}^{n} (-1)^i \frac{n!}{i! \ (n-i)!} =
\frac{1}{n!} \sum_{i=0}^{n} (-1)^i \binom{n}{i} \\
=\frac{1}{n!}(0) = 0$
