# Finite difference method (FDM)
Finite difference method is an approximation method to solve derivation equation by approximate function's derivation. Refer from [finite difference method](https://en.wikipedia.org/wiki/Finite_difference_method) and [finite difference](https://en.wikipedia.org/wiki/Finite_difference).
There are some [practices](https://askfilo.com/user-question-answers-smart-solutions/1-a-state-the-three-point-forward-difference-formula-for-3339343339383031).

### Definition of finite difference
there are three types definition: forward, backward and central finite difference

1. forward finite difference
$$
\Delta_h [f](x) = f(x+h) - f(x)
$$

2. backward finite difference
$$
\nabla_h[f](x) = f(x) - f(x-h)
$$

3. central finite difference
$$
\delta_h[f](x) = f(x+\frac{h}{2}) - f(x-\frac{h}{2})
$$

for higher order finite difference check the reference given at the beginning.

### Formula derivate
The approximation of derivation can express by 
$$
f'(x_0) \approx \frac{f(x_0+h)-f(x_0)}{h}
$$
This is derivate from Taylor series.
For a n-times differentiable function, it have Taylor series
$$
f(x_0 + h) = f(x_0) + \frac{f'(x_0)}{1!}h + \frac{f''(x_0)}{2!}h^2 + \cdots + \frac{f^{(n)}(x_0)}{n!}h^n + R(x_0)
$$
where $R(x_0)$ is reminder term.
Consider first order truncation
$$
f(x_0+h) = f(x_0) + \frac{f'(x_0)}{1!}h + R(x_0)
$$
both side divide by $h$
$$
\frac{f(x_0+h)}{h} = \frac{f(x_0)}{h} + f'(x_0) + \frac{R(x_0)}{h}
$$
so $f'(x_0)$ can approximate by 
$$
f'(x_0) \approx \frac{f(x_0+h)-f(x_0)}{h}
$$
where assume reminder term is smaller enough.

if truncate to second order (named **three-point forward difference**)
$$
\begin{equation}
    f(x_0 + h) = f(x_0) + f'(x_0)h + \frac{f''(x_0)}{2!}h^2 + R(x_0)
\end{equation}
$$
$$
\begin{equation}
    f(x_0 + 2h) = f(x_0) + f'(x_0)2h + \frac{f''(x_0)}{2!}(2h)^2 + R(x_0)
\end{equation}
$$
use 4 multiply (1) and subscirbe (2) can get
$$
\begin{aligned} 
    & 4f(x_0 + h) - f(x_0 + 2h) = 3f(x_0) + 2f'(x_0)h + 3R(x_0)\\
    & f'(x_0) \approx \frac{-3f(x_0) + 4f(x_0+h)-f(x_0+2h)}{2h}
\end{aligned}
$$

### Error of finite difference method
Obviously, the error origin from $R(x_0)$. Consider first order truncation, again use finite difference method
$$
\begin{aligned}
f(x_0+ih) 
&= f(x_0) + f'(x_0)ih + R(x_0)\\
&= f(x_0) + f'(x_0)ih + \frac{f''(x_0)}{2!}(ih)^2\\
\frac{f(x_0+ih)-f(x_0)}{ih} 
&= f'(x_0) + \frac{f''(x_0)}{2!}ih\\
\frac{f(x_0+ih)-f(x_0)}{ih} 
&= f'(x_0) + \mathcal{O}(h)\\
\end{aligned}
$$
consider seconde order truncation 
$$
\begin{equation}
    \begin{aligned}
    f(x_0+ih) 
    &= f(x_0) + f'(x_0)ih + \frac{f''(x_0)}{2!}(ih)^2 + R(x_0)\\
    &= f(x_0) + f'(x_0)ih + \frac{f''(x_0)}{2!}(ih)^2 + \frac{f^{(3)}(x_0)}{3!}(ih)^3\\
    \end{aligned}
\end{equation}
$$
$$
\begin{equation}
    \begin{aligned}
    f(x_0+2ih) 
    &= f(x_0) + f'(x_0)2ih + \frac{f''(x_0)}{2!}(2ih)^2 + R(x_0)\\
    &= f(x_0) + f'(x_0)2ih + \frac{f''(x_0)}{2!}(2ih)^2 + \frac{f^{(3)}(x_0)}{3!}(2ih)^3\\
    \end{aligned}
\end{equation}
$$
also use 4 multiply (3) and subscirbe (4) can get
$$
\begin{aligned}
    & 4f(x_0 + ih) - f(x_0 + 2ih) = 3f(x_0) + 2f'(x_0)ih + \frac{2}{3}f^{(3)}(x_0)(ih)^3\\
    & \frac{-3f(x_0) + 4f(x_0+ih)-f(x_0+2ih)}{2ih} \approx f'(x_0) + \frac{2}{3}f^{(3)}(x_0)(ih)^3\\
    & \frac{-3f(x_0) + 4f(x_0+ih)-f(x_0+2ih)}{2ih} \approx f'(x_0) + \mathcal{O}(h^3)
\end{aligned}
$$
higher order truncation is same.

### Extension 
Higher order derivation can approximate by lower order derivation finite difference 
$$
f''(x) \approx \frac{f'(x+h)-f'(x)}{h} \approx \frac{\frac{f(x+2h)-f(x+h)}{h} - \frac{f(x+h)-f(x)}{h}}{h}
$$
or according to Taylor series derivative.