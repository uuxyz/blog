---
title: quaternion
date: 2024-01-22
math: true
---
Rotate a point $P=(a, b, c)$ counterclockwise around an axis defined by a vector $Q=(x, y, z)$ by an angle $\theta$. This process can be described using the following formula.
$$q=\cos\frac{\theta}{2}+\sin\frac{\theta}{2}\left(x\mathbf{i}+y\mathbf{j}+z\mathbf{k}\right)$$
$$q^{-1}=\frac{q^\ast}{|q|^2}$$
$$p=a\mathbf{i}+b\mathbf{j}+c\mathbf{k}$$
$$p^\prime=qpq^{-1}$$
# rodrigues' rotation formula
$$\mathbf{v}_\mathrm{rot}=\mathbf{v}\cos\theta+(\mathbf{k}\times\mathbf{v})\sin\theta+\mathbf{k}~(\mathbf{k}\cdot\mathbf{v})(1-\cos\theta)$$
