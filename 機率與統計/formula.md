# Formula

期望值 (mean \ expected value)
$\mu_x = E(X) = \sum_x xf(x)$
$\mu_x = E(X) = \int_{-\infty}^{\infty} xf(x)dx$

g(X) 的期望值
$\mu_{g(X)} = E[g(X)] = \sum_x g(x)f(x)$

$\mu_{g(X)} = E[g(X)] = \int_{-\infty}^{\infty} g(x)f(x)$

聯合機率的期望值
$\mu_{g(X, Y)} = E[g(X, Y)] = \sum_x \sum_y g(x, y)f(x, y)$

$\mu_{g(X, Y)} = E[g(X, Y)] = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x, y)f(x, y) dxdy$

---

變異數 (variance)
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

相關係數 Correlation Coefficient
$\rho_{XY} = \dfrac{\sigma_{XY}}{\sigma_{X}\sigma_{Y}}$

---

期望值 與 變異數 的線性組合
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
