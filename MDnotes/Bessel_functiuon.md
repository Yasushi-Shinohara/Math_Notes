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

### Integrations

```python
import sympy
a = sympy.Symbol('a', real=True)
b = sympy.Symbol('b', real=True)
x = sympy.Symbol('x', real=True)
display(sympy.integrate(x * sympy.besselj(0,b*x) * sympy.exp(-a*x**2),(x, 0, sympy.oo)))
display(sympy.simplify(sympy.integrate(x * sympy.besselj(2,b*x) * sympy.exp(-a*x**2),(x, 0, sympy.oo))))
```

$$
\begin{align}
\int_0^\infty \\! \mathrm{d}x \ x J_0(bx) e^{-ax^2} =
\frac{e^{-b^2/(4a)}}{a}, \\
\int_0^\infty \\! \mathrm{d}x \ x J_2(bx) e^{-ax^2} =
-\frac{e^{-b^2/(4a)}}{a}
+
\frac{2}{b^2}\left[ 1 - e^{-b^2/(4a)} \right].
\end{align}
$$
