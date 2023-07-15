---
title: "Probability theory"
date: 2022-10-23T00:11:22+08:00
draft: false
math: true
---

# Bernoulli distribution

| Mean     | $$p$$         |
|----------|---------------|
| Variance | $$p(1-p)=pq$$ |

# Binomial distribution

| Notation   | $$B(n,p)$$                                                  |
|------------|-------------------------------------------------------------|
| Parameters | $$n\in \\{0,1,2,\ldots \\}  $$  $$ p\in [0,1] $$ $$ q=1-p$$ |
| Support    | $$k\in \\{0,1,\ldots ,n\\}$$                                |
| PMF        | $$\binom {n}{k}p^kq^{n-k}$$                                 |
| Mean       | $$np$$                                                      |
| Median     | $$\lfloor np\rfloor$$       $$\lceil np\rceil$$             |
| Variance   | $$npq$$                                                     |

# Normal distribution

| Notation | $$\mathcal{N}(\mu,\sigma^2)$$                                                                           |
|----------|---------------------------------------------------------------------------------------------------------|
| PDF      | $${\frac{1}{\sigma{\sqrt{2\pi}}}}\exp\left(-{\frac{1}{2}}\left({\frac{x-\mu}{\sigma}}\right)^2\right)$$ |
| Mean     | $$\mu$$                                                                                                 |
| Median   | $$\mu$$                                                                                                 |
| Variance | $$\sigma^2$$                                                                                            |

# Geometric distribution

| Parameters | $$0<p\leq 1$$               | $$0<p\leq 1$$                 |
|------------|-----------------------------|-------------------------------|
| Support    | $$k\in \\{1,2,3,\dots \\}$$ | $$k\in \\{0,1,2,3,\dots \\}$$ |
| PMF        | $$(1-p)^{k-1}p$$            | $$(1-p)^{k}p$$                |
| Mean       | $$\frac{1}{p}$$             | $$\frac {1-p}{p}$$            |
| Variance   | $$\frac{1-p}{p^{2}}$$       | $$\frac{1-p}{p^{2}}$$         |

# Hypergeometric distribution

| Parameters | $$\begin{aligned}N&\in \left\\{0,1,2,\dots \right\\}\\\\K&\in \left\\{0,1,2,\dots,N\right\\}\\\\n&\in \left\\{0,1,2,\dots,N\right\\}\end{aligned}$$ |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| PMF        | $${{K\choose k}{{N-K} \choose {n-k}}} \over {N \choose n} $$                                                                                        |
| Mean       | $$n{K\over N} $$                                                                                                                                    |
| Variance   | $$n{K\over N}{N-K \over N}{N-n \over N-1} $$                                                                                                        |

# Chi-squared distribution

| Notation   | $$\chi_{k}^{2}$$                                                        |
|------------|-------------------------------------------------------------------------|
| Parameters | $$k\in \mathbb {N} ^{*}$$                                               |
| PDF        | $$\frac{1}{2^{k/2}\Gamma (k/2)}x^{k/2-1}\exp\left(-\frac{x}{2}\right)$$ |

<!--

# Bernoulli distribution

| Parameters         | $$0\leq p\leq 1$$   $$q=1-p$$                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------|
| Support            | $$ k\in \\{0,1\\} $$                                                                                             |
| PMF                | $$  \begin{cases}q=1-p&{\text{if }}k=0\\\\p&{\text{if }}k=1\end{cases} $$                                        |
| CDF                | $$ \begin{cases}0&{\text{if }}k<0\\\\1-p&{\text{if }}0\leq k<1\\\\1&{\text{if }}k\geq 1\end{cases} $$            |
| Mean               | $$   p $$                                                                                                        |
| Median             | $$  \begin{cases}0&{\text{if }}p<1/2\\\\\left[0,1\right]&{\text{if  }}p=1/2\\\\1&{\text{if }}p>1/2\end{cases} $$ |
| Mode               | $$  \begin{cases}0&{\text{if }}p<1/2\\\\0,1&{\text{if }}p=1/2\\\\1&{\text{if }}p>1/2\end{cases}$$                |
| Variance           | $$          p(1-p)=pq  $$                                                                                        |
| MAD                | $$ \frac {1}{2}$$                                                                                                |
| Skewness           | $$ \frac {q-p}{\sqrt {pq}} $$                                                                                    |
| Ex. kurtosis       | $$ \frac {1-6pq}{pq}   $$                                                                                        |
| Entropy            | $$  -q\ln q-p\ln p $$                                                                                            |
| MGF                | $$  q+pe^{t} $$                                                                                                  |
| CF                 | $$    q+pe^{it}  $$                                                                                              |
| PGF                | $$  q+pz $$                                                                                                      |
| Fisher information | $$  \frac {1}{pq}$$                                                                                              |

# Binomial distribution

| Notation           | $$B(n,p)$$                                                           |
|--------------------|----------------------------------------------------------------------|
| Parameters         | $$ n\in \\{0,1,2,\ldots \\}  $$  $$ p\in [0,1] $$ $$ q=1-p$$         |
| Support            | $$ k\in \\{0,1,\ldots ,n\\}$$                                        |
| PMF                | $$ \binom {n}{k}p^kq^{n-k} $$                                        |
| CDF                | $$ I_q(n-k,1+k)$$                                                    |
| Mean               | $$np$$                                                               |
| Median             | $$\lfloor np\rfloor$$       $$\lceil np\rceil$$                      |
| Mode               | $$\lfloor (n+1)p\rfloor $$      $$ \lceil (n+1)p\rceil -1$$          |
| Variance           | $$ npq$$                                                             |
| Skewness           | $$\frac {q-p}{\sqrt {npq}}$$                                         |
| Ex. kurtosis       | $$ {\frac {1-6pq}{npq}}$$                                            |
| Entropy            | $$ {\frac {1}{2}}\log _{2}(2\pi enpq)+O\left({\frac {1}{n}}\right)$$ |
| MGF                | $$(q+pe^{t})^{n}$$                                                   |
| CF                 | $$(q+pe^{it})^{n}$$                                                  |
| PGF                | $$G(z)=[q+pz]^{n}$$                                                  |
| Fisher information | $$g_{n}(p)={\frac {n}{pq}}$$    $$n$$                                |

# Normal distribution

| Notation                    | $$\mathcal{N}(\mu,\sigma^2)$$                                                                                                                                                   |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parameters                  | $$ \mu \in \mathbb {R}$$ $$\sigma^2\in \mathbb{R}_{>0}$$                                                                                                                        |
| Support                     | $$ x\in \mathbb {R} $$                                                                                                                                                          |
| PDF                         | $$ {\frac {1}{\sigma {\sqrt {2\pi }}}}e^{-{\frac {1}{2}}\left({\frac {x-\mu }{\sigma }}\right)^{2}}$$                                                                           |
| CDF                         | $$ {\frac {1}{2}}\left[1+\operatorname {erf} \left({\frac {x-\mu }{\sigma {\sqrt {2}}}}\right)\right]$$                                                                         |
| Quantile                    | $$ \mu +\sigma {\sqrt {2}}\operatorname {erf} ^{-1}(2p-1)$$                                                                                                                     |
| Mean                        | $$ \mu $$                                                                                                                                                                       |
| Median                      | $$ \mu $$                                                                                                                                                                       |
| Mode                        | $$ \mu $$                                                                                                                                                                       |
| Variance                    | $$ \sigma ^{2}$$                                                                                                                                                                |
| MAD                         | $$ \sigma {\sqrt {2/\pi }}$$                                                                                                                                                    |
| Skewness                    | $$ 0$$                                                                                                                                                                          |
| Ex. kurtosis                | $$ 0$$                                                                                                                                                                          |
| Entropy                     | $$ {\frac{1}{2}}\log(2\pi \sigma ^{2})+{\frac {1}{2}}$$                                                                                                                         |
| MGF                         | $$ \exp(\mu t+\sigma^2t^2/2)$$                                                                                                                                                  |
| CF                          | $$ \exp(i\mu t-\sigma^2t^2/2)$$                                                                                                                                                 |
| Fisher information          | $$ \mathcal{I}(\mu,\sigma)=\begin{pmatrix}1/\sigma^2&0\\\\0&2/\sigma^2\end{pmatrix}$$ $$\mathcal{I}(\mu,\sigma^2)=\begin{pmatrix}1/\sigma^2&0\\\\0&1/(2\sigma^4)\end{pmatrix}$$ |
| Kullback-Leibler divergence | $$ {1 \over 2}\left\\{\left({\frac{\sigma_0}{\sigma_1}}\right)^2+{\frac{(\mu_1-\mu_0)^2}{\sigma_1^2}}-1+\ln {\sigma_1^2 \over \sigma _0^2}\right\\}$$                           |

# Geometric distribution

| Parameters   | $$ 0<p\leq 1$$                                                              | $$ 0<p\leq 1$$                                                                |
|--------------|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Support      | $$ k\in \\{1,2,3,\dots \\}$$                                                | $$ k\in \\{0,1,2,3,\dots \\}$$                                                |
| PMF          | $$ (1-p)^{k-1}p$$                                                           | $$ (1-p)^{k}p$$                                                               |
| CDF          | $$ 1-(1-p)^{\lfloor k\rfloor }$$ $$ k\geq 1$$ $$0$$ $$k<1$$                 | $$1-(1-p)^{\lfloor k\rfloor +1}$$ $$k\geq 0$$ $$0$$ $$k<0$$                   |
| Mean         | $$\frac{1}{p}$$                                                             | $$\frac {1-p}{p}$$                                                            |
| Median       | $$\left\lceil \frac{-1}{\log_{2}(1-p)}\right\rceil $$  $$-1/\log_{2}(1-p)$$ | $$\left\lceil\frac{-1}{\log_{2}(1-p)}\right\rceil -1 $$ $$ -1/\log_{2}(1-p)$$ |
| Mode         | $$1$$                                                                       | $$0$$                                                                         |
| Variance     | $$\frac{1-p}{p^{2}}$$                                                       | $$\frac{1-p}{p^{2}}$$                                                         |
| Skewness     | $$\frac {2-p}{\sqrt {1-p}} $$                                               | $$\frac {2-p}{\sqrt {1-p}} $$                                                 |
| Ex. kurtosis | $$6+\frac{p^{2}}{1-p}$$                                                     | $$6+\frac{p^{2}}{1-p}$$                                                       |
| Entropy      | $$\tfrac{-(1-p)\log_{2}(1-p)-p\log _{2}p}{p}$$                              | $$\tfrac{-(1-p)\log_{2}(1-p)-p\log _{2}p}{p}$$                                |
| MGF          | $$\frac {pe^{t}}{1-(1-p)e^{t}}$$ $$t<-\ln(1-p)$$                            | $$\frac {p}{1-(1-p)e^{t}}$$ $$t<-\ln(1-p)$$                                   |
| CF           | $$\frac {pe^{it}}{1-(1-p)e^{it}}$$                                          | $$\frac {p}{1-(1-p)e^{it}}$$                                                  |

# Hypergeometric distribution

| Parameters   | $$\begin{aligned}N&\in \left\\{0,1,2,\dots \right\\}\\\\K&\in \left\\{0,1,2,\dots,N\right\\}\\\\n&\in \left\\{0,1,2,\dots,N\right\\}\end{aligned}$$       |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Support      | $$k\in\left\\{\max {(0,n+K-N)},\dots,\min {(n,K)}\right\\}$$                                                                                              |
| PMF          | $${{K \choose k}{{N-K} \choose {n-k}}} \over {N \choose n} $$                                                                                             |
| CDF          | $$1-{{{n \choose {k+1}}{{N-n} \choose {K-k-1}}}\over{N \choose K}}{}_3F_2\left[\begin{array}{c}1, k+1-K, k+1-n\\\\k+2, N+k+2-K-n  \end{array};1\right] $$ |
| Mean         | $$ n{K \over N} $$                                                                                                                                        |
| Mode         | $$ \left\lceil {\frac {(n+1)(K+1)}{N+2}}\right\rceil -1,\left\lfloor {\frac {(n+1)(K+1)}{N+2}}\right\rfloor$$                                             |
| Variance     | $$   n{K \over N}{N-K \over N}{N-n \over N-1} $$                                                                                                          |
| Skewness     | $$  {\frac {(N-2K)(N-1)^{\frac {1}{2}}(N-2n)}{[nK(N-K)(N-n)]^{\frac {1}{2}}(N-2)}}$$                                                                      |
| Ex. kurtosis | $$ \frac{1}{nK(N-K)(N-n)(N-2)(N-3)}\cdot\Big[(N-1)N^2\Big(N(N+1)-6K(N-K)-6n(N-n)\Big)+6nK(N-K)(N-n)(5N-6)\Big]  $$                                        |
| MGF          | $$   \frac{{N-K \choose n}{}_2F_1(-n,-K;N-K-n+1;e^{t})}{N \choose n}$$                                                                                    |
| CF           | $$   \frac{{N-K \choose n}{}_2F_1(-n,-K;N-K-n+1;e^{it})}{N \choose n}$$                                                                                   |

# Chi-squared distribution

|   Notation   |   $$\chi^{2}(k)$$ $$\chi_{k}^{2}$$
|--|--|
|  Parameters  |$$k\in \mathbb {N} ^{*}$$|
|    Support   | $$ x\in(0,+\infty )$$ $$k=1$$ $$x\in [0,+\infty )$$|
|      PDF     |  $$\frac{1}{2^{k/2}\Gamma (k/2)}x^{k/2-1}e^{-x/2}$$|
|      CDF     |   $$\frac{1}{\Gamma (k/2)}\gamma\left({\frac {k}{2}}{\frac {x}{2}}\right)$$|
|     Mean     | $$k$$|
|    Median    | $$\approx k{\bigg (}1-{\frac {2}{9k}}{\bigg )}^{3}$$|
|     Mode     | $$\max(k-2,0)$$ $$2k$$|
|   Skewness   |       $$\sqrt {8/k}$$|
| Ex. kurtosis |   $$\frac{12}{k}$$|
|    Entropy   |    $$\begin{aligned}{\frac {k}{2}}&+\ln(2\Gamma ({\frac  {k}{2}}))\\\\&\!+(1-{\frac {k}{2}})\psi ({\frac  {k}{2}})\end{aligned}$$ |
|      MGF     |    $$ (1-2t)^{-k/2}{\text{ for }}t<{\frac {1}{2}}$$|
|      CF      |          $$ (1-2it)^{-k/2}$$|
|      PGF     |                  $$ (1-2\ln t)^{-k/2}{\text{ for }}0<t<{\sqrt {e}}$$|

-->
