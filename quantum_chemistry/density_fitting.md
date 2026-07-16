# Density fitting
This note refer from [sherrill's note](https://vergil.chemistry.gatech.edu/static/content/df.pdf).

$$
\begin{aligned}
(pq|rs) 
&= \int d\bold{r_1} \int d\bold{r_2}\phi_{p}(\bold{r_1})\phi_{q}(\bold{r_1})\frac{1}{r_{12}}\phi_{r}(\bold{r_2})\phi_{s}(\bold{r_2})\\
&= \int d\bold{r_1} \int d\bold{r_2}\rho_{pq}(\bold{r_{1}})\frac{1}{r_{12}}\rho_{rs}(\bold{r_2})
\end{aligned}
$$
其中
$$
\rho_{pq}(\bold{r}) 
= \phi_{p}(\bold{r})\phi_q(\bold{r}) 
\approx \tilde{\rho}_{pq}(\bold{r})
= \sum_{P}^{N_{fit}}c_{pq}^{P}\chi_{P}(\bold{r})
$$

### 为什么 K 比 J 难计算

### 为什么 $\frac{1}{r_{12}}$ 需要是正定
