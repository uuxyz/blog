---
title: avatar
date: 2023-10-12
math: true
---
```xml
<path d="M 676.7589339498916 1175.5006796557807 A 987 987 0 0 0 676.7589339498916 2018.4993203442193 L 1974.0004531038537974 1597 L 676.7589339498916 1175.5006796557807" fill="white" id="sector"/>
```
$$\varphi=\frac{\sqrt{5}-1}{2},\Phi=\frac{\sqrt{5}+1}{2}$$
$$\mathrm{fib}(15)=610,\mathrm{fib}(16)=987,\mathrm{fib}(17)=1597$$
Let's draw a square with length $2L=2\times 1597=3194$ pixels.
In this square. Here are a pentagon like pattern.
There circle's radius should be $R = \mathrm{fib}(17)\times \varphi\approx \mathrm{fib}(16) = 987$
$$\frac{\varphi}{\Phi}=\frac{\sqrt{5}-1}{\sqrt{5}+1}\approx 0.381966$$
$$r=R\frac{\varphi}{\Phi}=L\varphi^3\approx 337$$
$$R+r=987+337=1364$$
$$L-(R+r)\sin\left(\frac{\tau}{20}\right)\approx 1175.5006796557807$$
$$L+(R+r)\sin\left(\frac{\tau}{20}\right)\approx 2018.4993203442193$$
$$L+r-(R+r)\cos\left(\frac{\tau}{20}\right)\approx 676.7589339498916$$
Maybe I should use complex number?
Those points should be solutions of a equation.
$$(x_i,y_i)=(R+Rj)+R(-1)^{i/5}(\cos\theta+\imath\sin\theta)=(L+L\imath)+R\exp(\imath(i\frac{\tau}{5}+\theta))$$
$$(x_i,y_i)=(L+L\imath)+R\exp(\imath(i\frac{\tau}{5}-\theta))$$
$$(x_i,y_i)=(L+L\imath)+r\exp(\imath i\frac{\tau}{5})$$
$$A=\frac{(5-3\sqrt{5})\sqrt{5-2\sqrt{5}}}{2(-5+\sqrt{5(5-2\sqrt{5})})}$$
$$A=\frac{(1-3\varphi)\sqrt{3-4\varphi}}{-5+\sqrt{5}\sqrt{3-4\varphi}}$$
$$\theta=\sin^{-1}A$$
And A equals the fourth root of $-1 - 6x + 54 x^2  + 44 x^3  + 4 x^4=0$
```mathematica
a=ArcSin[Root[-1-6#+54#^2+44#^3+4#^4&,4]]
L=Fibonacci[17]
R=Fibonacci[16]
r=Fibonacci[17]*GoldenRatio^-3
f[i_]=L+L*I+R*Exp[I*(Mod[1+i-(-1)^i,5]*2*Pi/5+(-1)^i*a)]
Table[f[x],{x,0,9}]
```
