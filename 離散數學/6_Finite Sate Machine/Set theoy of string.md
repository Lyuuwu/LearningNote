# Set Theory of Strings

## Alphbet

$\sum$ : the symbol of alphbet

<font color = #FF5151>**Notice**</font> : We don't list elements that can be formed by other alphabets of $\sum$ by juxtaposition.  

### Example

$\sum$ = {1, 2, 12} or $\sum$ = {a, b, c, ab} are not acceptable.

---

## Power of $\sum$

If n $\in \Z^+$, we define the power of $\sum$ recursively follows bellow:

1. $\sum^1 = \sum$
2. $\sum^{n + 1} = {xy|x \in \sum, y \in \sum ^ n}$

### Example

$\sum = \{ 1, 2 \}$, then $\sum ^ 2 = \{ 11, 22, 12, 21 \}$, $\sum^3 = \{ 111, 222, 112, 121, 211, 122, 212, 221 \}$

With the example above, we can find that $| \sum^n| = | \sum | ^n$  
For instance, if $| \sum | = 2$, then $| \sum^2| = 2^2 = 4, | \sum^3| = 2^3 = 8$

---

## Empty String

For any alphbet $\sum$, we define $\sum^0 = \{ \lambda \}$ as empty string. **And $\lambda$ denotes the empty string**.

---

## The definition of $\sum ^ +$ and $\sum ^ *$

$\sum^+ = \bigcup _{n=1} ^{\infin} \sum^n$  
$\sum^n = \bigcup _{n \in \Z ^ +} \sum^n$  
$\sum^* = \bigcup _{n=0} ^{\infin} \sum^n$  

We can find that the only differnce between $\sum^+$ and $\sum^*$ is that $\sum^*$ includes $\lambda$.  
Both $\sum^+$ and $\sum^*$ refer to the
<font color = #FF5151>*words and sentences*</font>  
And finally, both $\sum^+$ and $\sum^* $ are **infinite**, the elements of theses sets are **finite**.

## The equality of two strings

We say that two strings are equal only when they have **same number of symbols from $\sum$**, and **corresponding symbols in the two strings match identically**.  

### Example

$\sum = \{ 1, 2 \}$, string1,string2 $\in \sum^+$, string1 = $ \{ 11,12,22 \}$, string2 = $\{ 11,12,22 \}$, then we can say that string1 and string2 are equal.

---

## The length of string

Let $w="12300"$, we define $||w|| = 5$.  
<font color = #FF5151>**Note:** $||\lambda|| = 0$</font>

## The power of string

For any $x \in \sum ^*$, we define $x^0 = \lambda, x^1 = x, x^2 = xx, x^{n+1} = xx^n$.  

### Example

$x = 12, \space x^5 = 1212121212$

<font color = #FF5151>**Note:** For the string, $||w|| = x, then \space ||w|| ^ n = x \times n$</font>  

---

## Prefix and Suffix

Let $x,y \in \sum^*$, and $w = xy$, we call $x$ is the prefix of $w$, and $y$ is the suffix of $w$.  
<font color = #FF5151>**Note:** A **proper prefix** or **proper suffix** of a string cannot be the string itself. Specifically, for strings $xy$, $x$ is a proper prefix if $y \neq \lambda$, and $y$ is a proper suffix if $x \neq \lambda$.</font>  

### Example

$w = 12345$, $\{ 1, 12,123, 1234 \}$ are the proper prefix of $w$, but $12345$ is not the proper prefix of $w = 12345$.  

<font color = #FF5151>**Note:** $\lambda$ is both the proper prefix and poper suffix of any strings $\in \sum^+$</font>  

---

## Substring

If $x, y, z \in \sum^*$, $w = xyz$  
Substring: y  
Proper substring: y (If $y$ if different from $w$)

---

## Language

For a given alphbet $\sum$, any subset of $\sum^*$ is called the language over $\sum$.  
<font color = #FF5151>**Note:** This inclueds subset $\empty$, which is called **empty language**</font>  

---

## The concatenation of strings and The cross product

1. Concatenation
   1. $AB \neq BA$
   2. $|AB| \neq |BA|$
2. Cross Product
   1. $A \times B \neq B \times A$
   2. $|A \times B| = |B \times A|$

e.g. $A = \{ 1, 12, 3 \}, B = \{ \lambda, 2 \}$  

1. Concatenation
   1. $AB = {1, 12, 122, 3, 32}$
   2. $BA = {1, 12, 3, 21, 212, 23}$  
    We find that $|AB| = 5 \neq |BA| = 6$ and also $AB \neq BA$
2. Cross Product
   1. $A \times B = {1, 12, 12, 122, 3, 32}$
   2. $B \times A = {1, 12, 3, 21, 212, 23}$
    We find that $|A \times B| = 6 = |B \times A|$ and also $A \times B \neq B \times A$

<font color = #FF5151>**Conclusion:** Concatenation possesses uniqueness, whereas the cross product does not. Consequently, for finite languages A and B, $|AB| \leq |A \times B|.$</font>
