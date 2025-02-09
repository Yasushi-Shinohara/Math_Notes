# Discrete Fourier transform
Reference: https://en.wikipedia.org/wiki/Discrete_Fourier_transform  
Discrete Fourier transform (DFT)

## Three-dimensional DFT

```math
\begin{align}
F(m_1, m_2, m_3 )
=
\frac{1}{N_1 N_2 N_3} \sum_{n_1, n_2, n_3} e^{-2\pi\mathrm{i} \frac{n_1 m_1}{N_1}}e^{-2\pi\mathrm{i} \frac{n_2 m_2}{N_2}}e^{-2\pi\mathrm{i} \frac{n_3 m_3}{N_3}} f(n_1, n_2, n_3), \\  
f(n_1, n_2, n_3)
=
\sum_{m_1, m_2, m_3} e^{+2\pi\mathrm{i} \frac{n_1 m_1}{N_1}}e^{+2\pi\mathrm{i} \frac{n_2 m_2}{N_2}}e^{+2\pi\mathrm{i} \frac{n_3 m_3}{N_3}}  F(m_1, m_2, m_3 )
\end{align}
```

### DFT for periodic functions on oblique lattices

A real-space periodic function $\phi (\mathbf{r})$, identified by the primitive vectors $\mathbf{a}_1, \mathbf{a}_2, \mathbf{a}_3$, and its reciprocal-space counterpart $\Phi (\mathbf{G})$: 
```math
\begin{align}
\phi(\mathbf{r}) = v(\mathbf{r} + \mathbf{a}_1) = \phi(\mathbf{r} + \mathbf{a}_2) = \phi(\mathbf{r} + \mathbf{a}_3), \\
\Phi ( \mathbf{G} )
=
\frac{1}{v} \int_v \! \mathrm{d}^3r \ e^{-\mathrm{i}\mathbf{G}\cdot\mathbf{r}} \phi(\mathbf{r}).
\end{align}
```
where $v=\left|\mathbf{a}_1 \cdot \left(\mathbf{a}_2 \times \mathbf{a}_3 \right)\right|$.

After the disctretizaiton along three axes by amount of $(N_1, N_2, N_e)$, we define following:
```math
\begin{align}
f(n_1, n_2, n_3)
:=
\phi \left( \frac{n_1}{N_1} \mathbf{a}_1 + \frac{n_2}{N_2} \mathbf{a}_2  + \frac{n_3}{N_3} \mathbf{a}_3 \right), \\
F'(m_1, m_2, m_3)
:=
\Phi' \left( \frac{m_1}{N_1} \mathbf{b}_1 + \frac{m_2}{N_2} \mathbf{b}_2  + \frac{m_3}{N_3} \mathbf{b}_3 \right), \\
\Phi' ( \mathbf{G} )
=
\frac{1}{v} \frac{v}{N_1 N_2 N_3}\sum_{n_1, n_2, n_3} \ e^{-\mathrm{i}\mathbf{G}\cdot \left( \frac{n_1}{N_1} \mathbf{a}_1 + \frac{n_2}{N_2} \mathbf{a}_2  + \frac{n_3}{N_3} \mathbf{a}_3 \right)} \phi(\left( \frac{n_1}{N_1} \mathbf{a}_1 + \frac{n_2}{N_2} \mathbf{a}_2  + \frac{n_3}{N_3} \mathbf{a}_3 \right)
\simeq
\Phi(\mathbf{G}).
\end{align}
```
Then, we can prove
```math
F'(m_1, m_2, m_3 )
=
\frac{1}{N_1 N_2 N_3} \sum_{n_1, n_2, n_3} e^{-2\pi\mathrm{i} \frac{n_1 m_1}{N_1}}e^{-2\pi\mathrm{i} \frac{n_2 m_2}{N_2}}e^{-2\pi\mathrm{i} \frac{n_3 m_3}{N_3}} f(n_1, n_2, n_3)
=
F(m_1, m_2, m_3 ),
```
where $F$ is the normal DFT's one defined above.

### Expression for the spatial derivative

```math
\begin{align}
\mathbf{\nabla} \phi
=
\sum_{\mathbf{G}} \mathrm{i} \mathbf{G} e^{+\mathrm{i}\mathbf{G}\cdot\mathbf{r}} \Phi(\mathbf{G})
\simeq
\sum_{\mathbf{G}} \mathrm{i} \mathbf{G} e^{+\mathrm{i}\mathbf{G}\cdot\mathbf{r}} \Phi'(\mathbf{G}), \\
\nabla^2 \phi
=
- \sum_{\mathbf{G}} \mathbf{G}^2 e^{+\mathrm{i}\mathbf{G}\cdot\mathbf{r}} \Phi(\mathbf{G})
\simeq
- \sum_{\mathbf{G}} \mathbf{G}^2 e^{+\mathrm{i}\mathbf{G}\cdot\mathbf{r}} \Phi'(\mathbf{G}).
\end{align}
```

