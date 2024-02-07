# Bessel function

Reference : [Pauli matrices - Wikipedia](https://en.wikipedia.org/wiki/Pauli_matrices)

## The definition

$$
\begin{align}
\sigma_1 =
\begin{pmatrix}0 & 1 \\
1 & 0\end{pmatrix},
\qquad
\sigma_2 =
\begin{pmatrix}0 & -\mathrm{i} \\
\mathrm{i} & 0\end{pmatrix},
\qquad
\sigma_3 =
\begin{pmatrix}1 & 0 \\
0 & -1\end{pmatrix}.
\tag{*}
\end{align} 
$$
$ \sigma_0 = I$.

## Eigenproblems

$$
\begin{align}
A =
\sum_j a_j \sigma_j \tag{e1} \\
a_1 = 
a \sin \theta \cos \phi,
\qquad
a_2 = 
a \sin \theta \sin \phi,
\qquad
a_3 = 
a \cos \theta.\tag{e2}
\end{align} 
$$

$$
\begin{align}
A x_{\pm} =
\pm \left| a \right| x_{\pm}, 
\qquad
\left| a \right| = \sqrt{\left(a_1 \right)^2 + \left(a_2 \right)^2 + \left(a_2 \right)^2} \tag{e3} \\
x_{+} =
\begin{pmatrix}
\cos \left( \theta/2 \right) \\
\sin \left( \theta/2 \right) e^{\mathrm{i}\phi}
\end{pmatrix},
\qquad
x_{-} =
\begin{pmatrix}
-\sin \left( \theta/2 \right) e^{-\mathrm{i}\phi} \\
\cos \left( \theta/2 \right)
\end{pmatrix}. \tag{e4}
\end{align} 
$$

## Matrix function
$$
\begin{align}
  \left( \frac{A}{a} \right)^2 = \sigma_0, \\
  e^{\pm \mathrm{i} A} =
  \cos (a ) \sigma_0 
  \pm
  \mathrm{i} \sin (a) \left( \frac{A}{a} \right), \\
  e^{- \mathrm{i} A} \sigma_i e^{+ \mathrm{i} A} =
  \cos^2 (a ) \sigma_i
  +
  \sin (2a) \frac{\left(\mathbf{a} \times \mathbf{\sigma} \right)_i}{a}
  +
  \sin^2 (a ) \frac{A \sigma_i A}{a^2} =
  \cos (2a ) \sigma_i
  +
  \sin (2a) \frac{\left(\mathbf{a} \times \mathbf{\sigma} \right)_i}{a}
  +
  \frac{1 -\cos (2a )}{2(?)} \frac{a_i}{a} \frac{A}{a}.
\end{align}
$$
