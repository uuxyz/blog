---
title: lists of integrals
date: 2024-01-13
math: true
---
# (I)
1. $$\int\frac{{\rm d}x}{ax+b}=\frac{1}{a}\int\frac{{\rm d}(ax+b)}{ax+b}=\frac{1}{a}\ln|ax+b|+C$$
2. $$\int(ax+b)^\mu{\rm d}x=\frac{1}{a}\int(ax+b)^\mu{\rm d}(ax+b)=\frac{1}{a(\mu+1)}(ax+b)^{\mu+1}+C$$
3. $$\int\frac{x}{ax+b}{\rm d}x=\int\frac{1}{a}-\frac{b}{a(ax+b)}{\rm d}x=\frac{1}{a}x-\frac{b}{a}\int\frac{{\rm d}x}{ax+b}$$
$$=\frac{1}{a^2}(ax+b-b\ln|ax+b|)+C$$
4. $$\int\frac{x^2}{ax+b}{\rm d}x=\int\frac{x}{a}+\frac{b^2}{a^2(ax+b)}-\frac{b}{a^2}{\rm d}x$$
$$=\frac{1}{a^3}\left[\frac{1}{2}(ax+b)^2-2b(ax+b)+b^2\ln|ax+b|\right]+C$$
5. $$\int\frac{{\rm d}x}{x(ax+b)}=\int\frac{1}{bx}-\frac{a}{b(ax+b)}{\rm d}x$$
$$=-\frac{1}{b}\ln\left|\frac{ax+b}{x}\right|+C$$
6. $$\int\frac{{\rm d}x}{x^2(ax+b)}=\int\frac{1}{bx^2}-\frac{a}{b^2x}+\frac{a^2}{b^2(ax+b)}{\rm d}x$$
$$=-\frac{1}{bx}+\frac{a}{b^2}\ln\left|\frac{ax+b}{x}\right|+C$$
7. $$\int\frac{x}{(ax+b)^2}{\rm d}x=\int-\frac{b}{a(ax+b)^2}+\frac{1}{a(ax+b)}{\rm d}x$$
$$=\frac{1}{a^2}\left(\ln\left|ax+b\right|+\frac{b}{ax+b}\right)+C$$
8. $$\int\frac{x^2}{(ax+b)^2}{\rm d}x=\int\frac{1}{a^2}+\frac{b^2}{a^2(ax+b)^2}-\frac{2b}{a^2(ax+b)}{\rm d}x$$
$$=\frac{1}{a^3}\left(ax+b-2b\ln|ax+b|-\frac{b^2}{ax+b}\right)+C$$
9. $$\int\frac{{\rm d}x}{x(ax+b)^2}=\int\frac{1}{b^2x}-\frac{a}{b(ax+b)^2}-\frac{a}{b^2(ax+b)}{\rm d}x$$
$$=\frac{1}{b(ax+b)}-\frac{1}{b^2}\ln\left|\frac{ax+b}{x}\right|+C$$
# (II)
1. $$\int\sqrt{ax+b}\ {\rm d}x=\frac{1}{a}\int\sqrt{ax+b}\ {\rm d}(ax+b)=\frac{3}{2a}\sqrt{(ax+b)^3}+C$$
2. $$\int x\sqrt{ax+b}\ {\rm d}x=\frac{1}{a^2}\int(ax+b-b)\sqrt{ax+b}\ {\rm d}(ax+b)$$
$$=\frac{1}{a^2}\int\sqrt{(ax+b)^3}-b\sqrt{ax+b}\ {\rm d}(ax+b)$$
$$=\frac{2}{15a^2}(3ax-2b)\sqrt{(ax+b)^3}+C$$
3. $$\int x^2\sqrt{ax+b}\ {\rm d}x=\frac{1}{a^3}\int (ax)^2\sqrt{ax+b}\ {\rm d}(ax+b)=$$$$=\frac{1}{a^3}\int\left[(ax+b)^2-2abx-b^2\right]\sqrt{ax+b}\ {\rm d}(ax+b)$$
$$=\frac{1}{a^3}\left[\frac{2}{7}\sqrt{(ax+b)^7}-\frac{4b}{15}(3ax-2b)\sqrt{(ax+b)^3}-\frac{2b^2}{3}\sqrt{(ax+b)^3}\right]+C$$
$$=\frac{1}{a^3}\left[\frac{2}{7}(ax+b)^2-\frac{4b}{15}(3ax-2b)-\frac{2b^2}{3}\right]\sqrt{(ax+b)^3}+C$$
$$=\frac{1}{a^3}\left[\frac{2}{7}a^2x^2-\frac{8}{35}abx+\frac{16}{105}b^2\right]\sqrt{(ax+b)^3}+C$$
$$=\frac{2}{105a^3}\left[15a^2x^2-12abx+8b^2\right]\sqrt{(ax+b)^3}+C$$
4. $$\int \frac{x}{\sqrt{ax+b}}{\rm d}x=\frac{1}{a^2}\int\frac{ax+b-b}{\sqrt{ax+b}}{\rm d}(ax+b)$$
$$=\frac{1}{a^2}\left[\int\sqrt{ax+b}\ {\rm d}(ax+b)-b\int\frac{{\rm d}(ax+b)}{\sqrt{ax+b}}\right]$$
$$=\frac{1}{a^2}\left[\frac{2}{3}(ax+b)-2b\right]\sqrt{ax+b}+C$$
$$=\frac{2}{3a^2}(ax-2b)\sqrt{ax+b}+C$$
5. $$\int\frac{x^2}{\sqrt{ax+b}}{\rm d}x=\frac{2}{15a^3}(3a^2x^2-4abx+8b^2)\sqrt{ax+b}+C$$
6. $$\int\frac{{\rm d}x}{x\sqrt{ax+b}}=\frac{1}{\sqrt{b}}\ln\left|\frac{\sqrt{ax+b}-\sqrt{b}}{\sqrt{ax+b}+\sqrt{b}}\right|+C(b>0)$$
7. $$\int\frac{{\rm d}x}{x\sqrt{ax-b}}=\frac{2}{\sqrt{b}}\arctan\sqrt{\frac{ax-b}{b}}+C(b<0)$$
8. $$\int\frac{{\rm d}x}{x^2\sqrt{ax+b}}=-\frac{\sqrt{ax+b}}{bx}-\frac{a}{2b}\int\frac{{\rm d}x}{x\sqrt{ax+b}}$$
9. $$\int\frac{\sqrt{ax+b}}{x}{\rm d}x=2\sqrt{ax+b}+b\int\frac{{\rm d}x}{x\sqrt{ax+b}}$$
10. $$\int\frac{\sqrt{ax+b}}{x^2}{\rm d}x=-\frac{\sqrt{ax+b}}{x}+\frac{a}{2}\int\frac{{\rm d}x}{x\sqrt{ax+b}}$$
# (III)
1. $$\int\frac{{\rm d}x}{x^2+a^2}=\frac{1}{a}\int\frac{{\rm d}\frac{x}{a}}{(\frac{x}{a})^2+1}=\frac{1}{a}\arctan\frac{x}{a}+C$$
2. $$\int\frac{{\rm d}x}{(x^2+a^2)^n}=\frac{x}{2(n-1)a^2(x^2+a)^{n-1}}+\frac{2n-3}{2(n-1)a^2}\int\frac{{\rm d}x}{(x^2+a^2)^{n-1}}$$
3. $$\int\frac{{\rm d}x}{x^2-a^2}=\frac{1}{2a}\ln\left|\frac{x-a}{x+a}\right|+C$$
# (IV)
# (V)
# (VI)
# (VII)
# (VIII)
# (IX)
# (X)
# (XI)
# (XII)
# (XIII)
$$\int a^x{\rm d}x=\frac{1}{\ln a}a^x+C$$
$$\int e^{ax}=\frac{1}{a}e^{ax}+C$$
$$\int xe^{ax}=\frac{1}{a^2}(ax-1)e^{ax}+C$$
$$\int x^ne^{ax}=\frac{1}{a}x^ne^{ax}-\frac{n}{a}\int x^{n-1}e^{ax}{\rm d}x$$
$$\int xa^x{\rm d}x=\frac{1}{\ln a}a^x-\frac{1}{(\ln a)^2}a^x+C$$
$$\int x^na^x{\rm d}x=\frac{1}{\ln a}x^na^x-\frac{n}{\ln a}\int x^{n-1}a^x{\rm d}x$$
$$e^{ax}\sin bx\ {\rm d}x=\frac{1}{a^2+b^2}e^{ax}(a\sin bx-b\cos bx)+C$$
$$e^{ax}\cos bx\ {\rm d}x=\frac{1}{a^2+b^2}e^{ax}(b\sin bx+a\cos bx)+C$$
# (XIV)
1. $$\int \ln x{\rm d}x=x\ln x-x+C$$
2. $$\int\frac{{\rm d}x}{x\ln x}=\ln|\ln x|+C$$
3. $$\int x^n\ln x{\rm d}x=\frac{1}{n+1}x^{n+1}(\ln x-\frac{1}{n+1})+C$$
4. $$\int (\ln x)^n{\rm d}x=x(\ln x)^n-n\int(\ln x)^{n-1}{\rm d}x$$
5. $$\int x^m(\ln x)^n{\rm d}x=\frac{1}{m+1}x^{m+1}(\ln x)^n-\frac{n}{m+1}\int x^m(\ln x)^{n-1}{\rm d}x$$
# (XV)
1. $$\int\sinh x{\rm d}x=\cosh x+C$$
2. $$\int\cosh x{\rm d}x=\sinh x+C$$
3. $$\int\tanh x{\rm d}x=\ln\cosh x+C$$
4. $$\int\sinh^2 x{\rm d}x=-\frac{x}{2}+\frac{1}{4}\sinh 2x+C$$
5. $$\int\cosh^2x{\rm d}x=\frac{x}{2}+\frac{1}{4}\sinh2x+C$$
# (XVI)
1. $$\int_{-\pi}^\pi\cos nx{\rm d}x=\int_{-\pi}^\pi\sin nx{\rm d}x=0$$
2. $$\int_{-\pi}^\pi\cos mx\sin nx{\rm d}x=0$$
3. $$\int_{-\pi}^\pi\cos mx\cos nx{\rm d}x=0(m\neq n),\pi(m=n)$$
4. $$\int_{-\pi}^\pi\sin mx\sin nx{\rm d}x=0(m\neq n),\pi(m=n)$$
5. $$\int_0^\pi\sin mx\sin nx{\rm d}x=\int_0^\pi\cos mx\cos nx{\rm d}x=0(m\neq n),\frac{\pi}{2}(m=n)$$
6. $$I_n=\int_0^{\frac{\pi}{2}}\sin^nx{\rm d}x=\int_0^{\frac{\pi}{2}}\cos^n x{\rm d}x,I_n=\frac{n-1}{n}I_{n-2}$$
# rational functions
# irrational functions
# trigonometric functions
# inverse trigonometric functions
# hyperbolic functions
# inverse hyperbolic functions
# exponential functions
# logarithmic functions
# gaussian functions