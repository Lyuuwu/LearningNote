# Relation and Matrix

## The composite reltaion

If $A$, $B$ and $C$ are sets with $\char"1d4ad _1 \sube A \times B$, $\char"1d4ad _2 \sube B \times C$, then the **composite relation** $\char"1d4ad _1 \circ \char"1d4ad _2$ is the relation from $A$ to $C$. Formally, $ \mathcal{R}_1 \circ \mathcal{R}_2 = \{ (x, z) \ | \ x \in A, z \in C, \exists y \in B \text{ such that } (x, y) \in \mathcal{R}_1, (y, z) \in \mathcal{R}_2 \} $.

### Example

Given $A = \{ 1, 2, 3, 4 \}$, $B = \{ x, y, z \}$ and $C = \{ 5, 6, 7 \}$.
Consider $\char"1d4ad _1 = \{ (1, x), (2, x), (3, y), (3, y) \}$, a relation from $A$ to $B$, and $\char"1d4ad _2 = \{ (x, 5), (z, 7) \}$, a relation from $B$ to $C$.
Then $\char"1d4ad _1 \circ \char"1d4ad _2 = \{ (1, 6), (2, 6) \}$ is a relation from $A$ to $C$. If $\char"1d4ad _3 = \{ (z, 5), (z, 6) \}$ is another relation from $A$ to $C$, then $\char"1d4ad _1 \circ \char"1d4ad _3 = \empty$.

---

## Composition of multiple relations

Let $A$, $B$, $C$ and $D$ be the sets with $\char"1d4ad _1 \sube A \times B$, $\char"1d4ad _2 \sube B \times C$, and $\char"1d4ad _3 \sube C \times D$.
Then $\char"1d4ad _1 \circ \char"1d4ad _2 \circ \char"1d4ad _3 = \char"1d4ad _1 \circ (\char"1d4ad _2 \circ \char"1d4ad _3) = (\char"1d4ad _1 \circ \char"1d4ad _2) \circ \char"1d4ad _3 $.

### Proof

$\char"1d4ad _1 \circ (\char"1d4ad _2 \circ \char"1d4ad _3)$ and $(\char"1d4ad _1 \circ\char"1d4ad _2) \circ \char"1d4ad _3$ are equal.
If $(a, d) \in \char"1d4ad _1 \circ (\char"1d4ad _2 \circ \char"1d4ad _3)$, then $\exist b \in B$ such that $(a, b) \in \char"1d4ad _1$ and $(b, d) \in \char"1d4ad _2 \circ \char"1d4ad _3$.
Because $(b, d) \in \char"1d4ad _2 \circ \char"1d4ad _3$, $\exist c \in C$ such that $(b, c) \in \char"1d4ad _2$ and $ (c, d) \in \char"1d4ad _3$.
Moreover, $(a, b) \in \char"1d4ad _1$ and $(b, c) \in \char"1d4ad _2 \Rightarrow (a, c) \in \char"1d4ad _1 \circ \char"1d4ad _2$.
Finally, $(a, c) \in \char"1d4ad _1 \circ \char"1d4ad _2$ and $(c, d) \in \char"1d4ad _3 \Rightarrow (a, d) \in (\char"1d4ad _1 \circ \char"1d4ad _2) \circ \char"1d4ad _3 $.
Consequently, $\char"1d4ad _1 \circ (\char"1d4ad _2 \circ \char"1d4ad _3) \sube (\char"1d4ad _1 \circ \char"1d4ad _2) \circ \char"1d4ad _3$.

<font color=#FF5151>**Conclusion:** There is no ambiguity arises from we write $\char"1d4ad_1 \circ \char"1d4ad _2 \circ \char"1d4ad _3$ for either of the relations $\char"1d4ad _1 \circ (\char"1d4ad _2 \circ \char"1d4ad _3)$ or $ (\char"1d4ad _1 \circ \char"1d4ad _2) \circ \char"1d4ad _3$.</font>

---

## <span id="powerR">Power of $\char"1d4ad$</span>

Given a relation $\char"1d4ad$ on set $A$, we define the power of $\char"1d4ad$ recursively by

- $\char"1d4ad ^1 = \char"1d4ad$
- $\char"1d4ad ^{n+1} = \char"1d4ad \circ \char"1d4ad ^{n}$, $n \in \Z ^+$

<font color = #FF5151>**Note:** $\forall n \in \Z ^+$, $\char"1d4ad ^n$ is the relation on $A$.</font>

### Example

If $A = \{ 1, 2, 3, 4 \}$, $\char"1d4ad = \{ (1, 2), (1, 3), (2, 4), (3, 2) \}$, then $\char"1d4ad ^2 = \{ (1, 4), (1, 2), (3, 4) \}$, $\char"1d4ad ^3 = \{ (1, 4) \}$, and $\forall n \geq 4$, $\char"1d4ad ^n \in \emptyset$.

### Details

#### $\char"1d4ad ^2$

- $(\char"1d4ad)(1, 2), (\char"1d4ad)(2, 4) \Rightarrow (\char"1d4ad ^2)(1, 4)$
- $(\char"1d4ad)(1, 3), (\char"1d4ad)(3, 2) \Rightarrow (\char"1d4ad ^2)(1, 2)$
- $(\char"1d4ad)(3, 2), (\char"1d4ad)(2, 4) \Rightarrow (\char"1d4ad ^2)(3, 4)$

#### $\char"1d4ad ^3$

- $(\char"1d4ad)(1, 3), (\char"1d4ad ^2)(3, 4) \Rightarrow (\char"1d4ad ^3)(1, 4)$

---

## Zero-one matrix | (0, 1)-matirx

An $m \times n$ (0, 1)-matrix $E = (e_{ij})_{m \times n}$ is a rectangular array of numbers organized into $m$ rows and $n$ columns. Each $e{ij}$, where $1 \leq i \leq m$ and $1 \leq j \leq n$, represents the entry in the $i$-th row and $j$-th column of $E$, with each entry being either 0 or 1.

<font color=#FF5151>**Note:** In the context of a matrix, the terms "*entry*," "*element*," and "*item*" are interchangeable and refer to the individual values within the matrix.</font>

### Example

The matrix
$$E =
\begin{bmatrix}
1 & 0 & 0 & 1 \\ 0 & 1 & 0 & 1 \\ 1 & 0 & 0 & 0
\end{bmatrix}$$
is a $3 \times 4$ (0, 1)-matrix where, for instance, $e_{11} = 1$, $e_{23} = 0$, $e_{31} = 1$, and $e_{34} = 0$.

---

## Composite relation and Zero-one matrix
If $A = \{ 1, 2, 3, 4 \}$, $B = \{ w, x, y, z \}$, and $C = \{ 5, 6, 7 \}$.
Consider $\char"1d4ad _1 = \{ (1, x), (2, x), (3, y), (3, z) \}$, a relation from $A$ to $B$, and $\char"1d4ad _2 = \{ (w, 5), (x, y) \}$, a relation from $B$ to $C$.
We expect $\char"1d4ad_1 \circ \char"1d4ad_2 = \{ (1, 6), (2, 6) \}$.

$$
M(\char"1d4ad_1) =
\begin{bmatrix}
0&1&0&0 \\ 0&1&0&0 \\ 0&0&1&1 \\ 0&0&0&0
\end{bmatrix},
M(\char"1d4ad_2) =
\begin{bmatrix}
1&0&0 \\ 0&1&0 \\ 0&0&0 \\ 0&0&0
\end{bmatrix}
$$

$$M(\char"1d4ad_1)*M(\char"1d4ad_2)
=\begin{bmatrix}
0&1&0&0 \\ 0&1&0&0 \\ 0&0&1&1 \\ 0&0&0&0
\end{bmatrix}
\begin{bmatrix}
1&0&0 \\ 0&1&0 \\ 0&0&0 \\ 0&0&0
\end{bmatrix}
=\begin{bmatrix}
0&1&0 \\ 0&1&0 \\ 0&0&0 \\ 0&0&0
\end{bmatrix}
=M(\char"1d4ad_1 \circ \char"1d4ad_2)
$$

Apparently, $M(\char"1d4ad_1) * M(\char"1d4ad_2)$ represents our intended outcome.

### Example

Let $A = \{ 1, 2, 3, 4 \}$ and $\char"1d4ad = \{ (1, 2), (1, 3), (2, 4), (3, 2) \}$, as in the example of [**Power of $\char"1d4ad$**(click me to jump)](#powerR). We define the relation matrix for $\char"1d4ad$ as follows:
$M(\char"1d4ad)$ is the $4 \times 4$ (0,1)-matrix whose entries $m_{ij}$, for $1 \leq i,j \leq 4$, are given by
$$ m_{ig}
= \begin{cases}
1 &\text{if (i, j)} \in \char"1d4ad, \\
0 &\text{otherwise.}
\end{cases}$$

In this case, we find that
$$ M(\char"1d4ad)
= \begin{bmatrix}
0&1&1&0 \\ 0&0&0&1 \\ 0&1&0&0 \\ 0&0&0&0
\end{bmatrix} $$

We compute $(M(\char"1d4ad))^2$ using $M(\char"1d4ad) * M(\char"1d4ad)$, we find that
$$ (M(\char"1d4ad))^2
=\begin{bmatrix}
0&1&0&1 \\ 0&0&0&0 \\ 0&0&0&1 \\ 0&0&0&0
\end{bmatrix} $$
which coincides with the relation matrix for $\char"1d4ad \circ \char"1d4ad = \char"1d4ad^2$. Furthermore
$$(M(\char"1d4ad))^4
=\begin{bmatrix}
0&0&0&0 \\ 0&0&0&0 \\ 0&0&0&0 \\ 0&0&0&0
\end{bmatrix}
$$
which is also the relation matrix for the relation $\char"1d4ad^4$.

In this example, we observe that $ (M(\char"1d4ad))^4 = M(\char"1d4ad^4) $, and this observation generalizes to other cases.

Let $A$ be a set with $|A| = n$ and $\char"1d4ad$ a relation on $A$. If $M(\char"1d4ad)$ is the relation matrix for $\char"1d4ad$, then

  1. $M(\char"1d4ad) = 0$ (the matrix of all 0's) if and only if $\char"1d4ad = \emptyset$
  2. $M(\char"1d4ad) = 1$ (the matrix of all 1's) if and only if $\char"1d4ad = A \times A$
  3. $M(\char"1d4ad ^ m) = [M(\char"1d4ad)]^m$, for $m \in \Z^+$

---

## Matrix Order Relations: $E \leq F$

Let $E = (e_{ij})_{m \times n}$, $F = (f_{ij})_{m \times n}$ be two $m \times n$ (0, 1)-matrix.
We say that $E$ **precedes**, or **is less than**, $F$, and we write $E \leq F$ if $e_{ij} \leq f_{ij}$, for all $1 \leq i \leq m$, $1 \leq j \leq n$.

Briefly, for $E \leq F$, two conditions must be met:

1. The sizes of the two relation matrices are equal.
2. Each element in matrix $F$ is greater than or equal to the corresponding element in matrix $E$.

### Example

With $E = \begin{bmatrix} 1&0&1 \\ 0&0&1 \end{bmatrix} $ and $F = \begin{bmatrix} 1&0&1 \\ 0&1&1 \end{bmatrix}$, we have $E \leq F$.
In fact, there are 8 different (0, 1)-matrix $G$ for $E \leq G$.

---

## Identity matrix

An identity matrix, denoted as $I_n$, for $n \in \Z^+$, is defined by the matrix $(\delta_{ij})_{n \times n}$ where
$$ \delta_{ij} = \begin{cases} 1 &\text{if} &i = j, \\
0 &\text{if} &i \neq j. \end{cases} $$

---

## Transpose

Let $A = (a_{ij})_{m \times n}$ be a (0, 1)-matrix. The transpose of $A$ is written as $A^{tr}$, is the matrix $(a^*_{ji})_{n \times m}$ where $a^*_{ji} = a_{ij}$, for all $1 \leq i \leq m$ and $1 \leq j \leq n$.

### Example

For $A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \\ 1 & 1 \end{bmatrix}$, we find that $A^{tr} = \begin{bmatrix} 0 & 0 & 1 \\ 1 & 0 & 1 \end{bmatrix}$.

As demonstrated in this example, the $i$-th row(column) of $A$ is equal to the $i$-th column(row) of $A^{tr}$. This demonstration highlights the relationship between the original matrix $A$ and its transpose $A^{tr}$.

---

## Properties of Relation Matrices : Reflexivity, Symmetry, Transitivity, and Antisymmetry

Given a set $A$ with $|A| = n$ and a relation $\char"1d4ad$ on A, let $M$ denote the relation matrix for $\char"1d4ad$
Then

- $\char"1d4ad$ is reflexive if and only if $I_n \leq M$.
- $\char"1d4ad$ is symmetric if and only if $M = M^{tr}$
- $\char"1d4ad$ is transitive if and only if $M^2 \leq M$
- $\char"1d4ad$ is antisymmetric if and only if $M \cap M^{tr} \leq I_n$

### Proof (transitive)
To prove $\char"1d4ad$ is transitive if and only if $M^2 \leq M$
If $(x, y), (y, z) \in \char"1d4ad$, then there are 1's in row($x$), column($y$) and in row($y$), column($z$) of $M$.
Consequently, in row($x$), column($z$) of $M^2$, there is also a 1's to satisy the transitive property.
And this 1 must also occur in row($x$), column($z$) of $M$.

In summary, because each element that is 1 in row($i$), column($j$) of $M^2$ will also occur in row($j$), column($i$) of $M$ but not vice versa, $\char"1d4ad$ is transitive if and only if $M^2 \leq M$.
