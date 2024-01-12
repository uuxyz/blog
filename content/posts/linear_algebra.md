---
title: linear algebra
date: 2023-12-09
math: true
---
# matrix
## identity matrix
{{<raw>}}

$$
I_1=\begin{bmatrix}
1
\end{bmatrix},
I_2=\begin{bmatrix}
1 & 0 \\
0 & 1 \\
\end{bmatrix}

I_3=\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix},\dots,I_n=\begin{bmatrix}
1 & 0 & 0 & \cdots & 0 \\
0 & 1 & 0 & \cdots & 0 \\
0 & 0 & 1 & \cdots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \cdots & 1 \\
\end{bmatrix}.
$$

{{</raw>}}
# determinant

$$\left|kA\right|=k^n\left|A\right|$$

$$AA^*=\left|A\right|E$$

$$A^{-1}=\frac{A^*}{\left|A\right|}$$

$$\det ({\rm adj}(A))=(\det{A})^{n-1}$$
$${\rm adj}(cA)=c^{n-1}{\rm adj}(A)$$
$${\rm adj}(AB)={\rm adj}(B){\rm adj}(A)$$

$$\overbrace{{\rm adj}\cdots{\rm adj}}^{k}(A)=\det(A)^{\frac{(n-1)^k-(-1)^k}{n}}A^{(-1)^k}$$
$$\det(\overbrace{{\rm adj}\cdots{\rm adj}}^{k}(A))=\det(A)^{(n-1)^k}$$


{{<raw>}}
$$\left(A^*\right)^*=\left|A\right|^{n-2}A$$

$$\det\begin{bmatrix}
A & O \\
O & D \\
\end{bmatrix}=
\det\begin{bmatrix}
A & O \\
C & D \\
\end{bmatrix}=
\det\begin{bmatrix}
A & B \\
O & D \\
\end{bmatrix}=\det \left ( A \right ) \det \left ( D \right )$$
{{</raw>}}