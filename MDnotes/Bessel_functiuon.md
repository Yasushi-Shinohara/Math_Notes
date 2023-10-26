# Bessel function

Reference : [Bessel function - Wikipedia](https://en.wikipedia.org/wiki/Bessel_function)

## Bessel functions of the first kind: $J_\alpha$

$$
J_{-n}(x) = (-1)^n J_n(x)
$$

$$
\begin{align}
e^{\mathrm{i}z \cos \phi} =
\sum_{n=-\infty}^\infty \mathrm{i}^n J_n(z) e^{\mathrm{i}n \phi}, \\
e^{\pm \mathrm{i}z \sin \phi} = 
J_0 (z)
+
2 \sum_{n=1}^\infty J_{2n} (z) \cos (2n \phi)
\pm 
2 \mathrm{i} \sum_{n=0}^\infty J_{2n+1} (z) \sin ((2n+1)\phi)
\end{align}
$$


$$
\int_0^\infty x J_\alpha(ux) J_\beta(vx) \mathrm{d}x =
\frac{1}{u} \delta(u-v)
$$

for $\alpha > -1/2$
