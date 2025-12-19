# Formula

## 期望值 (mean / expected value)

$\mu_x = E(X) = \sum_x xf(x)$
$\mu_x = E(X) = \int_{-\infty}^{\infty} xf(x)dx$

g(X) 的期望值

$\mu_{g(X)} = E[g(X)] = \sum_x g(x)f(x)$

$\mu_{g(X)} = E[g(X)] = \int_{-\infty}^{\infty} g(x)f(x)$

聯合機率的期望值

$\mu_{g(X, Y)} = E[g(X, Y)] = \sum_x \sum_y g(x, y)f(x, y)$

$\mu_{g(X, Y)} = E[g(X, Y)] = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x, y)f(x, y) dxdy$

---

## 變異數 (variance)

$\sigma^2 = E[(X - \mu)^2] = \sum_x (x - \mu)^2f(x)$

$\sigma^2 = E[(X - \mu)^2] = \int_{-\infty}^{\infty} (x-\mu)^2f(x) dx$

變異數 - 化簡後
$\sigma^2 = E(X^2) - E(X)^2 = E(X^2) - \mu^2$

共變異數(Covariance)

符號: $\sigma_{XY}$ 或是 $Cov(X, Y)$

$\sigma _{XY} = E[(X - \mu_X)(Y - \mu_Y)] = \sum_x \sum_y (x - \mu_x)(y - \mu_y)f(x, y)$

$\sigma _{XY} = E[(X - \mu_X)(Y - \mu_Y)] = \int _{-\infty}^{\infty} \int _{-\infty}^{\infty} (x - \mu_x)(y - \mu_y)f(x, y) dxdy$

共變異數 - 化簡後

$\sigma _{XY} = E(XY) - \mu_X \mu_Y$

---

## 相關係數 Correlation Coefficient

$\rho_{XY} = \dfrac{\sigma_{XY}}{\sigma_{X}\sigma_{Y}}$

---

## 期望值 與 變異數 的線性組合

$E(aX + b) = aE(X) + b$

求 $E(2X - 1)$
先算出 $E(X) = t$
則 $(2X - 1) = 2E(X) - 1 = 2t - 1$

$E[g(X) \pm h(X)] = E[g(X)] \pm E[h(X)]$

$E[g(X, Y) \pm h(X, Y)] = E[g(X, Y)] \pm E[h(X, Y)]$

$E[g(X) \pm h(Y)] = E[g(X)] \pm E[h(Y)]$

$E[X \pm Y] = E[X] \pm E[Y]$

$E(XY) = E(X)E(Y)$

如果 X, Y 獨立，則 $\sigma_{XY} = 0$

$Var(\sum _{i=1} ^{n} a_i X_i) = \sum _{i=1} ^n a_i^2 Var(X_i) + 2 \sum _{1 \leq i \lt j \leq 1} a_i a_j Cov(X_i, X_j)$

---

## Bernoulli Process (白努力過程)

### 成功機率

結果只有兩種 (二項分配)，並且每次的機率相同，每次的實驗獨立

寫作 $b(x;n, p)$

$n$ 是總共實驗的次數

$x$ 是成功的次數

$p$ 是成功的機率

因此 $b(x;n,p) = \dbinom{n}{x} p^x (1-p)^{n-x}$

### Bernoulli Process $b(x;n,p)$ 的平均數與變異數

$\mu = np$

$\sigma ^2 = npq = np(1-p)$

---

## Multinomial Distribution (多項分布)

$f(x_1, x_2, ..., x_n; p_1, p_2, ..., p_n, n) = \dbinom{n}{x_1, x_2, ..., x_n} p^{x_1} p^{x_2} ... p^{x_n} $

$\sum_{i=1}^{k} x_i = n$

$\sum_{i=1}^{k} p_i = 1$

---

## Hypergeometric Distribution (超幾何分配): 不放回抽樣

$h(x; N, n, k)=$ 母體有 $N$ 個，當中有 $k$ 個是成功，抽樣 $n$ 個，剛好有 $x$ 個成功的機率

### x 的合理範圍

$max(0, n - (N - k)) \leq x \leq min(n, k)$

#### lower_bound

$max(0, n - (N - k))$: $N-k$ 是失敗總共的數量，如果失敗的數量比 $n$ 大，那麼最差的情況是0，否則就是把失敗全拿後，剩下都成功

#### upper_bound

$min(n, k)$: 如果抽 $n$ 個，但是 $k$ 比較大，最好的情況就是全部都是成功，或是 $k$ 比較小，最好的情況就是把成功都拿了，剩下都是失敗

### 公式

$h(x; N, n, k) = \dfrac{\binom{k}{x} \binom{N-k}{n-x}}{\binom{N}{n}}$

成功的有 $k$ 個，抽到成功的有 $x$ 個，組合為 $\dbinom{k}{x}$

$\rightarrow$ 從成功中挑選 $x$ 個

失敗的有 $N-k$ 個，總共抽樣 $n$ 次，有 $x$ 次都是成功，剩 $n-x$ 次是失敗，組合為 $\dbinom{N-k}{n-x}$

$\rightarrow$ 從失敗中挑選 $n-x$ 個

無論成功與否，總共抽樣的組合為 $\dbinom{N}{n}$

$\rightarrow$ 從全部中挑選 $n$ 個

### hypergeometric distribution 的平均值與變異數

$\mu = \dfrac{nk}{N}$

$\sigma^2=\dfrac{N-n}{N-1} * n * \dfrac{k}{N} (1-\dfrac{k}{N})$

---

## Multivariate Hypergeometric Distribution (多變量超幾何分配)

當母體不只一個，變成有 $k$ 個，就是 multivariate hypergeometric distribution

### 公式

從總共數量 $N$ 個裡面挑出 $n$ 個物品出來， $a_1$ 有 $x_1$ 且 $a_2$ 有 $x_2$ 且 ... 且 $a_k$ 有 $x_k$ 個機率為:

$f(x_1, x_2, ..., x_k; a_1, a_2, ..., a_k, N, n) = \dfrac{\binom{a_1}{x_1}\binom{a_2}{x_2} ... \binom{a_k}{x_k}}{\binom{N}{n}}$

$\sum_{i=1}^{k}x_i = n$

$\sum_{i=1}^{k}a_i = N$

### 例子

盒子裡面有 5個藍球，3個紅球，2個綠球，總共有10顆球
不放回抽4次，求抽到 `藍色2、紅色1、綠色1` 的機率

$N=10$, $a_1 = 5$, $a_2 = 3$, $a_3 = 2$

$x_1 = 2$, $x_2 = 1$, $x_3 = 1$

因此機率為:

$P(X_1=2, X_2=1, X_3=1) = \dfrac{\binom{5}{2}\binom{3}{1}\binom{2}{1}}{\binom{10}{4}}$

---

## Negative Binomial (負二項分配)

定義: 每次成功機率為 $p$，實驗獨立，在第 $k$ 次成功發生在第 $n$ 實驗的機率

### 公式

在第 $x$ 次實驗的時候，剛好成功了 $k$ 次，且成功機率為 $p$

$b^*(x;k,p) = \dbinom{x-1}{k-1}p^k q^{x-k}, x = k, k+1, ...$

要成功 $k$ 次，至少要實驗 $k$ 次，因此 $x$ 最小值為 $k$

因為指定第 $x$ 次實驗的時候要成功第 $k$ 次，結尾一定要成功，前面 $x-1$ 次只要成功 $k-1$ 次就好，因此有 $\dbinom{x-1}{k-1}$ 種組合

## Geometric Distribution (幾何分配)

定義: 做了 $x$ 次終於第一次成功的機率 (k = 1)

geometric distribution 是 negative binomial 的特例

### 公式

$g(x;p) = pq^{x-1}$

## Geometric Distribution 的平均數與變異數

$\mu=\dfrac{1}{p}$

$\sigma^2=\dfrac{1-p}{p^2}$

---

## Poisson Experiment (卜瓦松實驗)

觀察一段時間或一塊區域，某事件發生了幾次

將 **發生的次數** 計為隨機變數 $X$，這種實驗就稱之為 **Poisson experiment**

## Poisson Process (卜瓦松過程)

Poisson process 將事件視為 **隨機散落在時間/空間中**，並且滿足:

1. 互不重疊的區間的發生次數彼此獨立 (independent increments)
即`不同時間段`或`不同區域`互不影響

2. 在`很短的時間`或`很小的空間` $\Delta t$ 內，**發生1次**的機率與長度/大小**成正比**，約是 $\lambda\Delta$
$\lambda$ 是指 **平均發生率**

3. 在很短的時間/空間 $\Delta t$ 中，**同時發生2次以上的機率可以忽略**

## Poisson Distribution

如果事件符合 poisson process，則在 `長度為 t 的時間/空間內發生的次數`

$$X ∼ Poisson(\lambda t)$$

機率為:

$$P(X=x) = \dfrac{e^{-\lambda t}(\lambda t)^x}{x!}$$

- $\lambda$: 每單位的平均發生次數
- $t$: 觀測的時間長度或是區域大小
- $\lambda t$: 這段時間或空間中的平均發生次數

### 結論

$E[X] = \lambda t$

$Var(X) = \lambda t$

## Binomial Distribution & Poisson Distribution

當二項分配的`成功率很低`或是`次數很多`的時候，二項分配會逼近於卜瓦松分配

$b(x;n, p) \approx p(x;\lambda t = np)$

---

## Continuous Uniform Distribution (連續均勻分布)

density function(一個區間內的機率):

$f(x;A,B)=
\begin{cases}
\dfrac{1}{B-A}, & A \le x \le B,\\
0, & \text{elsewhere}.
\end{cases}$

$\mu = \dfrac{A+B}{2}$

$\sigma^2 = \dfrac{(B-A)^2}{12}$

---

## Normal Distribution (常態分佈)

Normal Distribution 又被稱為 Gaussian Distribution(高斯分布)

常態分布的機率會根據 $\mu$ 跟 $\sigma$，因此記為 $n(x; \mu, \sigma)$

$n(x;\mu,\sigma)=\dfrac{1}{\sqrt{2 \pi} \sigma} e^{-\dfrac{1}{2 \sigma^2}(x-\mu)^2}$

### Property of normal distribution

1. mode(眾數) 發生在 $\mu$ 的位置 \
$mean = median = mode = \mu$
2. $x=\mu$ 為對稱軸
3. 反曲線(往下凹變成往上凹)發生在 $\mu \pm \sigma$

### Standardization of normal distribution (標準化)

此標準化叫作 Z-score

$$Z=\dfrac{X-\mu}{\sigma}$$

#### 為什麼要標準化

每個分布都有自己的 $\mu$ 跟 $\sigma$，在積分的時候很麻煩，如果都**一起搬到同一個尺度** ($\mu =0$, $\sigma =1$)

#### 計算區間機率

把端點對齊到 z-score 的空間，即可直接積分運算

$$P(x_1 \lt X \lt x_2)$$

$$z_1=\dfrac{x_1-\mu}{\sigma}, \qquad z_2=\dfrac{x_2-\mu}{\sigma}$$

$$P(x_1 \lt X \lt x_2) = P(z_1 \lt Z \lt z_2)$$

因此

$$P(x_1 \lt X \lt x_2) = \int _{z_1} ^{z_2} n(z; 0, 1) = P(z_1 \lt Z \lt z_2)$$

### Binomial

只要二項分布的實驗次數夠多，就會趨近於常態分布

$$\mu = np, \qquad \sigma^2 = npq$$

$$Z=\dfrac{X-np}{\sqrt{(npq)}}$$

當 $n \rightarrow \infty$ 的時候，就會是常態分佈 $n(z;0,1)$

#### 常態近似簡單公式

經驗法則: 只有當 $np$ 與 $n(1-p)$ 均大於等於5時，才會有比較好的結果

- $P(X \le x) \rightarrow x + 0.5$
- $P(X \lt x) \rightarrow x - 0.5$
- $P(X \ge x) \rightarrow x - 0.5$
- $P(X \gt x) \rightarrow x + 0.5$
