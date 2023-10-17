# 
忘れちゃう数学の関数周りの事項の備忘録

# Gauss関数
$$
\begin{align}
1 = \frac{1}{\sqrt{\pi}}\int_{-\infty}^{\infty} \mathrm{d}x \ \exp \left[ -x^2 \right] \\
= \\
\frac{1}{\sqrt{2\pi}\sigma}\int_{-\infty}^{\infty} \mathrm{d}x \ \exp \left[ -\frac{1}{2}\frac{x^2}{\sigma^2} \right] \\
= \\
\frac{1}{\sqrt{\pi} \alpha}\int_{-\infty}^{\infty} \mathrm{d}x \ \exp \left[ -\frac{x^2}{\alpha^2} \right] 
\end{align}
$$
$$
\iint \mathrm{d}x \mathrm{d}y \ \exp \left[ -(x^2 + y^2) \right] = \left( \int_0^{2\pi} \mathrm{d}\theta \right)\left( \int_0^\infty \mathrm{d}r \ r \exp \left[ - r^2 \right]\right) = \pi
$$
$$
\begin{align}
1 = \\
\frac{1}{(\sqrt{2\pi})^D\sqrt{\left|\Sigma \right|}}\int_{-\infty}^{\infty} \mathrm{d}^Dx \ \exp \left[ -\frac{1}{2} x^T \Sigma^{-1} x\right], \quad x \in \mathbb{R}^D
\end{align}
$$

## いくつかの公式
`∫[0,infty] exp(-iax) exp(-x**2/2)dx`

$$
\begin{align}
\phi(\omega; T) = \int_0^\infty \\! \mathrm{d}t \ e^{-\mathrm{i}\omega t}e^{-t^2/(T^2 2)} = T \int_0^\infty \\! \mathrm{d}\tau \ e^{-\mathrm{i}\omega T \tau}e^{-\tau^2/2} = T \sqrt{\frac{\pi}{2}} e^{-(\omega T)^2/2}\left[1 - \mathrm{i} \ \mathrm{erfi} \left(\frac{\omega T}{\sqrt{2}}\right)\right]\\\\
= T \left[\sqrt{\frac{\pi}{2}} e^{-(\omega T)^2/2} - \mathrm{i} \sqrt{2}\mathrm{Dawson}\left(\frac{\omega T}{\sqrt{2}}\right) \right] \\\\
F(\omega; T) = \frac{\mathrm{i}}{\pi} \phi(\omega; T) , \\\\
\int_{-\infty}^\infty \\! \mathrm{d} \omega \ F(\omega; T) = \mathrm{i}, \qquad
\lim_{T \to \infty} \Im F(\omega; T) = \lim_{T \to \infty} \frac{T}{\sqrt{2\pi}} e^{-\omega^2/(2T^2)}= \delta(\omega)
\end{align}
$$

$\mathrm{erfi} (x) = -\mathrm{i} \ \mathrm{erf} (\mathrm{i}x) = -\mathrm{i} \frac{2}{\sqrt{\pi}}\int_0^{\mathrm{i}x} \\! \mathrm{d}t \ e^{-t^2}$
$\mathrm{Dawson}(x) = \frac{\sqrt{\pi}}{2}e^{-x^2}\mathrm{erfi} (x)$


# Lorentz関数
$$
\begin{align}
\lim_{\gamma \to 0} \frac{1}{\pi} \frac{\gamma}{x^2 + \gamma^2} = \delta (x)
\end{align}
$$

## いくつかの公式
$$ 
\begin{align}
\phi(\omega; \gamma) = \int_0^\infty \\! \mathrm{d}t \ e^{-\mathrm{i}\omega t}e^{-\gamma t} = \frac{-\mathrm{i}}{\omega - \mathrm{i} \gamma}\\\\
F(\omega, \gamma) = \frac{\mathrm{i}}{\pi} \phi(\omega; \gamma) = \frac{1}{\pi}\frac{1}{\omega - \mathrm{i} \gamma}, \\\\
\frac{1}{\pi} \frac{\gamma}{\omega^2 + \gamma^2} = \Im F(\omega, \gamma)
\end{align}
$$

# Sinc関数
[sinc関数 - Wikipedia](https://ja.wikipedia.org/wiki/Sinc%E9%96%A2%E6%95%B0)

$$
\begin{align}
\lim_{k\to\infty} \frac{\sin kx}{\pi x} = \delta(x)
\end{align}
$$

$$
\mathrm{Si}(x) := \int_0^x \\! \mathrm{d}x \ \frac{\sin x}{x} 
$$
$$
\int_{-a}^{a} \\! \mathrm{d}x \ \frac{\sin x}{x} = 2 \mathrm{Si}(a) , \quad
\int_{-a}^{a} \\! \mathrm{d}x \ \frac{\sin^2 x}{x^2} = 2 \mathrm{Si}(2a) -  \frac{2 \sin^2 a}{a}
$$

`1/π*∫[-∞,∞]sin(x)/x dx`
$$
\begin{align}
\frac{1}{\pi} \int_{-\infty}^{\infty} \\! \mathrm{d}x \ \frac{\sin x}{x} = 1, \\\\
\frac{1}{\pi} \int_{-\infty}^{\infty} \\! \mathrm{d}x \ \frac{\sin^2 x}{x^2} = 1, 
\end{align}
$$

$$
\begin{align}
\frac{1}{\pi} \int_{-2\pi}^{2\pi} \\! \mathrm{d}x \ \frac{\sin x}{x} \simeq 0.902823, \\\\
\frac{1}{\pi} \int_{-4\pi}^{4\pi} \\! \mathrm{d}x \ \frac{\sin x}{x} \simeq 0.949939, \\\\
\frac{1}{\pi} \int_{-6\pi}^{6\pi} \\! \mathrm{d}x \ \frac{\sin x}{x} \simeq 0.96641.
\end{align}
$$
$$
\begin{align}
\frac{1}{\pi} \int_{-2\pi}^{2\pi} \\! \mathrm{d}x \ \frac{\sin^2 x}{x^2} \simeq 0.949939, \\\\
\frac{1}{\pi} \int_{-4\pi}^{4\pi} \\! \mathrm{d}x \ \frac{\sin^2 x}{x^2} \simeq 0.974748, \\\\
\frac{1}{\pi} \int_{-6\pi}^{6\pi} \\! \mathrm{d}x \ \frac{\sin^2 x}{x^2} \simeq 0.983137.
\end{align}
$$

## ある冪函数のFourier変換

$$
\phi (\omega;T) = \int_0^T \\! \mathrm{d}t \ e^{-\mathrm{i}\omega t} \left(1 -3 \frac{t^2}{T^2} + 2 \frac{t^3}{T^3} \right) = T \int_0^1 \\! \mathrm{d}\tau \ e^{-\mathrm{i}\omega T \tau} \left(1 -3 \tau^2 + 2 \tau^3 \right)
$$

`∫[0,1]exp(-i*a*x) dx - 3.0*∫[0,1]exp(-i*a*x)x**2 dx + 2.0*∫[0,1]exp(-i*a*x)x**3 dx`
$$
\int_0^1 \\! \mathrm{d}x \ e^{-\mathrm{i}a x} \left(1 -3 x^2 + 2 x^3 \right) = 12 \frac{1 - e^{-\mathrm{i}a}}{a^4} - 6\mathrm{i}\frac{1 + e^{-\mathrm{i}a}}{a^3} - \frac{i}{a} \to \frac{1}{2} (a\to 0)
$$

$$
\begin{align}
\phi (\omega;T) = T \left[12 \frac{1 - e^{-\mathrm{i}\omega T}}{(\omega T)^4} - 6\mathrm{i}\frac{1 + e^{-\mathrm{i}\omega T}}{(\omega T)^3} - \frac{i}{\omega T} \right] \to \frac{T}{2} (\omega \to 0) 
\end{align}
$$

$$
\begin{align}
\frac{12-12\cos x - 6x\sin x}{x^4} \simeq \frac{1}{2} - \frac{x^2}{30} + \frac{x^4}{1120} (x\ll 1) \\\\
\frac{12\sin(x)-6x(1+\cos(x)) - x^3}{x^4} \simeq -\frac{3}{20}x + \frac{x^3}{168} - \frac{x^5}{8640} (x\ll 1)
\end{align}
$$


`∫[0,a](12 - 12*cos(x)-6*x*sin(x))/x**4 dx`
$$
\begin{align}
\int_0^a \\! \mathrm{d}x \ \frac{12-12\cos x - 6x\sin x}{x^4} = \frac{(a^4+4)\cos a + a \sin a -4}{a^3} + \mathrm{Si}(a) \\\\
\int_{-\infty}^{\infty} \\! \mathrm{d} \omega \ \phi (\omega;T) = 2\mathrm{Si}(\infty) = \pi
\end{align}
$$



$\phi = \phi_r + \mathrm{i}\phi_i$
$$
\phi_r (\omega) = \phi_r ( -\omega), \quad
\phi_i (\omega) = -\phi_i (-\omega), \quad
$$

## Note
$$
\begin{align}
F(\omega; T) = \frac{\mathrm{i}}{\pi} \phi (\omega;T)  \\\\
\lim_{T \to \infty} \Im F(\omega; T) = \delta(\omega).
\end{align}
$$


# 指数関数
$$
\begin{align}
\int_{0}^{\infty} \\! \mathrm{d}r \ e^{-r/a} \\
=\\
a \\\\
\int_{0}^{\infty} \\! \mathrm{d}r \ r e^{-r/a} \\
=\\
a^2 \\\\
\int_{0}^{\infty} \\! \mathrm{d}r \ \frac{r^2}{2} e^{-r/a} \\
=\\
a^3 \\\\
\int_{0}^{\infty} \\! \mathrm{d}r \ \frac{r^n}{n!} e^{-r/a} \\
=\\
a^{n+1} \\\\
\end{align}
$$

# 離散Fourier変換
数ベクトル$x \in \mathbb{C}^N$の要素 $x_i (i=0,\dots,N-1)$ に対しての離散Fourier変換を$X_i$とする:
$$
\begin{align}
  x_i = \frac{1}{N}\sum_{j=0}^{N-1} e^{+2\pi\mathrm{i} \frac{ij}{N}}X_j,
  \qquad
  X_j = \sum_{i=0}^{N-1} e^{-2\pi\mathrm{i} \frac{ij}{N}}x_i.
\end{align}
$$

## 総和に対して成り立つ式
このとき実数ベクトル$x, y \in \mathbb{R}^N$について
$$
\begin{align}
x^T y =
\sum_{i=0}^{N-1} x_i y_i =
\frac{1}{N} \sum_{i=0}^{N-1} \bar{X_i} Y_i =
\frac{1}{N} X^H Y
\end{align}
$$
が成り立つ。
というか、そもそも$x, y \in \mathbb{C}^N$について
$$
\begin{align}
x^H y =
\frac{1}{N} X^H Y
\end{align}
$$
が成り立つ。

## 周期関数のFourier級数展開
周期$a$の周期関数: $f(x+a)=f(x)$$$
\begin{align}
f(x) = \sum_{G} e^{\mathrm{i}Gx} \tilde{f}(G) , G=n\frac{2\pi}{a}\\\\
\tilde{f}(G) = \frac{1}{a}\int_0^a \\! \mathrm{d}x \ e^{-\mathrm{i}Gx} f(x)
\end{align}
$$

二種類の周期$a,b$の周期関数: $f(x+a,y)=f(x,y), f(x,y+b)=f(x,y)$
$$
\begin{align}
f(x,y) = \sum_{G,H} e^{\mathrm{i}(Gx + Hy)} \tilde{f}(G,H), G=n\frac{2\pi}{a},  H=m\frac{2\pi}{b} \\\\
\tilde{f}(G,H) = \frac{1}{ab}\int_0^a \\! \mathrm{d}x \int_0^b \\! \mathrm{d}y \ e^{-\mathrm{i}(Gx+Hy)} f(x,y)
\end{align}
$$

実数$a$、整数$N$に対して: $f(x+Na,y)=f(x,y), f(x,y+Na)=f(x,y), f(x+a,y+a)=f(x,y)$ 
$$
\begin{align}
f(x,y) = \sum_{q,G,H} e^{\mathrm{i}(q+G)x} \tilde{f}_q(G,H)e^{-\mathrm{i}(q+H)y}, G=n\frac{2\pi}{a},  H=m\frac{2\pi}{b}, q = l\frac{2\pi}{Na}\\\\
\tilde{f}_q(G,H) = \frac{1}{(Na)^2}\int_0^{Na} \\! \mathrm{d}x \int_0^{Na} \\! \mathrm{d}y \ e^{-\mathrm{i}(q+G)x} f(x,y) e^{+\mathrm{i}(q+H)y}
\end{align}
$$

$f(x-y + Na) = f(x-y)$
$$
\begin{align}
f(x-y) = \sum_{q,G} e^{\mathrm{i}(q+G)x} \tilde{f}_q(G)e^{-\mathrm{i}(q+G)y}, G=n\frac{2\pi}{a},  q = l\frac{2\pi}{Na}\\\\
\tilde{f}_q(G) = \frac{1}{Na}\int_0^{Na} \\! \mathrm{d}x \ e^{-\mathrm{i}(q+G)x} f(x-y) e^{+\mathrm{i}(q+G)y}
\end{align}
$$

# Fourier変換
連続関数$f(x)$に対してのFourier変換を$\tilde{f}(k)$とする:
$$
\begin{align}
  f(x) = \frac{1}{2\pi}\int_{-\infty}^{\infty} \\! \mathrm{d}k \ e^{+\mathrm{i}kx} \tilde{f}(k),
  \qquad
  \tilde{f}(k) = \int_{-\infty}^{\infty} \\! \mathrm{d}x \ e^{-\mathrm{i}kx} f(x),.
\end{align}
$$

## 総和に対して成り立つ式
$$
\begin{align}
\left\langle \left. f \right| g \right\rangle =
\int_{-\infty}^{\infty} \\! \mathrm{d}x \  \bar{f(x)} g(x) =
\frac{1}{2\pi}\int_{-\infty}^{\infty} \\! \mathrm{d}k \  \bar{\tilde{f}(k)} g(k)
\end{align}
$$

# 常微分方程式

## 一階線形同次

$$
\frac{\mathrm{d}}{\mathrm{d}t} f = g(t) f
$$

$$
f(t) = f(0)e^{\int_0^t \mathrm{d}t' g(t')} 
$$

## 一階線形非同次

$$
\frac{\mathrm{d}}{\mathrm{d}t} f = g(t) f + h(t)
$$

$$
f(t) = \int_0^t \mathrm{d}t' h(t') e^{- \int_t^{t'} \mathrm{d}t'' g(t'')} + f(0)e^{\int_0^t \mathrm{d}t' g(t')} 
$$

