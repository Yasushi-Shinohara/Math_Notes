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

A real space function $\phi (\mathbf{r})$ and its reciprocal counterpart $\Phi (\mathbf{G})$: 
```math
\Phi ( \mathbf{G} )
=
\frac{1}{v} \int_v \! \mathrm{d}^3r \ e^{-\mathrm{i}\mathbf{G}\cdot\mathbf{r}} \phi(\mathbf{r}).
```
 $v=\left|\mathbf{a}_1 \cdot \left(\mathbf{a}_2 \times \mathbf{a}_3 \right)\right|$

```math
\begin{align}
f(n_1, n_2, n_3)
=
\phi \left( \frac{n_1}{N_1} \mathbf{a}_1 + \frac{n_2}{N_2} \mathbf{a}_2  + \frac{n_3}{N_3} \mathbf{a}_3 \right), \\
F(m_1, m_2, m_3)
=
\Phi' \left( \frac{m_1}{N_1} \mathbf{b}_1 + \frac{m_2}{N_2} \mathbf{b}_2  + \frac{m_3}{N_3} \mathbf{b}_3 \right), \\
\Phi' ( \mathbf{G} )
=
\frac{1}{v} \frac{v}{N_1 N_2 N_3}\sum_{n_1, n_2, n_3} \ e^{-\mathrm{i}\mathbf{G}\cdot \left( \frac{n_1}{N_1} \mathbf{a}_1 + \frac{n_2}{N_2} \mathbf{a}_2  + \frac{n_3}{N_3} \mathbf{a}_3 \right)} \phi(\left( \frac{n_1}{N_1} \mathbf{a}_1 + \frac{n_2}{N_2} \mathbf{a}_2  + \frac{n_3}{N_3} \mathbf{a}_3 \right)
\simeq
\Phi(\mathbf{G}).
\end{align}
```



