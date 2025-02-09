# Discrete Fourier transform
Reference: https://en.wikipedia.org/wiki/Discrete_Fourier_transform  
Discrete Fourier transform (DFT)

## Three-dimensional DFT

```math
\begin{align}
F(m_1, m_2, m_3 )
=
\frac{1}{N_1 N_2 N_3} \sum_{n_1, n_2, n_3} e^{-\mathrm{i} \frac{n_1 m_1}{N_1}}e^{-\mathrm{i} \frac{n_2 m_2}{N_2}}e^{-\mathrm{i} \frac{n_3 m_3}{N_3}} f(n_1, n_2, n_3), \\  
f(n_1, n_2, n_3)
=
\sum_{m_1, m_2, m_3} e^{+\mathrm{i} \frac{n_1 m_1}{N_1}}e^{+\mathrm{i} \frac{n_2 m_2}{N_2}}e^{+\mathrm{i} \frac{n_3 m_3}{N_3}}  F(m_1, m_2, m_3 )
\end{align}
```

### DFT for periodic functions on oblique lattices

A real space function $\phi (\mathbf{r})$ and its reciprocal counterpart $\Phi (\mathbf{G})$.

