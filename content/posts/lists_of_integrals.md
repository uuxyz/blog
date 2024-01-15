---
title: lists of integrals
date: 2024-01-13
math: true
tags:
  - math
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
1. $$\int\sqrt{ax+b}\ {\rm d}x=\frac{1}{a}\int\sqrt{ax+b}\ {\rm d}(ax+b)=\frac{2}{3a}\sqrt{(ax+b)^3}+C$$
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
5. $$\int\frac{x^2}{\sqrt{ax+b}}{\rm d}x=\frac{1}{a^3}\int\frac{(ax+b)^2-2abx-b^2}{\sqrt{ax+b}}{\rm d}(ax+b)$$
   $$=\frac{1}{a^3}\left(\frac{2}{5}(ax+b)^2-\frac{4b}{3}(ax+b)-2b^2\right)\sqrt{ax+b}+C$$
   $$=\frac{2}{15a^3}(3a^2x^2-4abx+8b^2)\sqrt{ax+b}+C$$
6. $$\int\frac{{\rm d}x}{x\sqrt{ax+b}}=\int\frac{{\rm d}(ax+b)}{(ax+b-b)\sqrt{ax+b}}$$
$$=2\int\frac{{\rm d}\sqrt{ax+b}}{ax+b-b}$$
$$=\frac{1}{\sqrt{b}}\ln\left|\frac{\sqrt{ax+b}-\sqrt{b}}{\sqrt{ax+b}+\sqrt{b}}\right|+C(b>0)$$

7. $$\int\frac{{\rm d}x}{x\sqrt{ax-b}}=\int\frac{{\rm d}(ax-b)}{(ax-b+b)\sqrt{ax-b}}$$
$$=2\int\frac{{\rm d}\sqrt{ax-b}}{ax-b+b}$$
$$=\frac{2}{\sqrt{b}}\arctan\sqrt{\frac{ax-b}{b}}+C(b>0)$$
8. $$\int\frac{{\rm d}x}{x^2\sqrt{ax+b}}=-\frac{\sqrt{ax+b}}{bx}-\frac{a}{2b}\int\frac{{\rm d}x}{x\sqrt{ax+b}}$$
9. $$\int\frac{\sqrt{ax+b}}{x}{\rm d}x=2\sqrt{ax+b}+b\int\frac{{\rm d}x}{x\sqrt{ax+b}}$$
10. $$\int\frac{\sqrt{ax+b}}{x^2}{\rm d}x=-\frac{\sqrt{ax+b}}{x}+\frac{a}{2}\int\frac{{\rm d}x}{x\sqrt{ax+b}}$$
# (III)
1. $$\int\frac{{\rm d}x}{x^2+a^2}=\frac{1}{a}\int\frac{{\rm d}\frac{x}{a}}{(\frac{x}{a})^2+1}=\frac{1}{a}\arctan\frac{x}{a}+C$$
2. $$\int\frac{{\rm d}x}{(x^2+a^2)^n}=\frac{x}{2(n-1)a^2(x^2+a)^{n-1}}+\frac{2n-3}{2(n-1)a^2}\int\frac{{\rm d}x}{(x^2+a^2)^{n-1}}$$
3. $$\int\frac{{\rm d}x}{x^2-a^2}=\frac{1}{2a}\int\frac{2a}{x^2-a^2}{\rm d}x$$
$$=\frac{1}{2a}\int\frac{1}{x-a}-\frac{1}{x+a}{\rm d}x=\frac{1}{2a}\ln\left|\frac{x-a}{x+a}\right|+C$$
# (IV)
1. $$\int\frac{{\rm d}x}{ax^2+b}=\frac{1}{\sqrt{ab}}\arctan\sqrt{\frac{a}{b}}+C$$
2. $$\int\frac{{\rm d}x}{ax^2-b}=\frac{1}{\sqrt{ab}}\ln\left|\frac{\sqrt{a}x-\sqrt{b}}{\sqrt{a}x+\sqrt{b}}\right|+C$$
3. $$\int\frac{x}{ax^2+b}{\rm d}x=\frac{1}{2a}\ln\left|ax^2+b\right|+C$$
4. $$\int\frac{x^2}{ax^2+b}{\rm d}x=\frac{x}{a}-\frac{b}{a}\int\frac{{\rm d}x}{ax^2+b}$$
5. $$\int\frac{{\rm d}x}{x(ax^2+b)}=\frac{1}{2b}\ln\frac{x^2}{|ax^2+b|}+C$$
6. $$\int\frac{{\rm d}x}{x^2(ax^2+b)}=-\frac{1}{bx}-\frac{a}{b}\int\frac{{\rm d}x}{ax^2+b}$$
7. $$\int\frac{{\rm d}x}{x^3(ax^2+b)}=\frac{a}{2b^2}\ln\frac{|ax^2+b|}{x^2}-\frac{1}{2bx^2}+C$$
8. $$\int\frac{{\rm d}x}{(ax^2+b)^2}=\frac{x}{2b(ax^2+b)}+\frac{1}{2b}\int\frac{{\rm d}x}{ax^2+b}$$
# (V)
1. $$\int\frac{{\rm d}x}{ax^2+bx+c}=\frac{2}{\sqrt{4ac-b^2}}\arctan\frac{2ax+b}{\sqrt{4ac-b^2}}+C(b^2<4ac)$$
2. $$\int\frac{{\rm d}x}{ax^2+bx+c}=\frac{1}{\sqrt{b^2-4ac}}\ln\left|\frac{2ax+b-\sqrt{b^2-4ac}}{2ax+b+\sqrt{b^2-4ac}}\right|+C(b^2>4ac)$$
3. $$\int\frac{x}{ax^2+bx+c}{\rm d}x=\frac{1}{2a}\ln\left|ax^2+bx+c\right|-\frac{b}{2a}\int\frac{{\rm d}x}{ax^2+bx+c}$$
# (VI)
1. $$\int\frac{{\rm d}x}{\sqrt{x^2+a^2}}=\int\frac{{\rm d}\frac{x}{a}}{\sqrt{\frac{x^2}{a^2}+1}}$$$$=\operatorname{arsinh}\frac{x}{a}+C_1=\ln\left(x+\sqrt{x^2+a^2}\right)+C$$
2. $$\int\frac{{\rm d}x}{\sqrt{(x^2+a^2)^3}}=\frac{x}{a^2\sqrt{x^2+a^2}}+C$$
3. $$\int\frac{x}{\sqrt{x^2+a^2}}{\rm d}x=\sqrt{x^2+a^2}+C$$
4. $$\int\frac{x}{\sqrt{(x^2+a^2)^3}}{\rm d}x=-\frac{1}{\sqrt{x^2+a^2}}+C$$
5. $$\int\frac{x^2}{\sqrt{x^2+a^2}}{\rm d}x=\frac{x}{2}\sqrt{x^2+a^2}-\frac{a^2}{2}\ln\left(x+\sqrt{x^2+a^2}\right)+C$$
6. $$\int\frac{x^2}{\sqrt{(x^2+a^2)^3}}{\rm d}x=-\frac{x}{\sqrt{x^2+a^2}}+\ln\left(x+\sqrt{x^2+a^2}\right)+C$$
7. $$\int\frac{{\rm d}x}{x\sqrt{x^2+a^2}}=\frac{1}{a}\ln\frac{\sqrt{x^2+a^2}-a}{|x|}+C$$
8. $$\int\frac{{\rm d}x}{x^2\sqrt{x^2+a^2}}=-\frac{\sqrt{x^2+a^2}}{a^2x}+C$$
9. $$\int\sqrt{x^2+a^2}{\rm d}x=\frac{x}{2}\sqrt{x^2+a^2}+\frac{a^2}{2}\ln\left(x+\sqrt{x^2+a^2}\right)+C$$
10. $$\int\sqrt{(x^2+a^2)^3}{\rm d}x=\frac{x}{8}(2x^2+5a^2)\sqrt{x^2+a^2}+\frac{3}{8}a^4\ln\left(x+\sqrt{x^2+a^2}\right)+C$$
11. $$\int x\sqrt{x^2+a^2}{\rm d}x=\frac{1}{3}\sqrt{(x^2+a^2)^3}+C$$
12. $$\int x^2\sqrt{x^2+a^2}{\rm d}x=\frac{x}{8}(2x^2+a^2)\sqrt{x^2+a^2}-\frac{a^4}{8}\ln\left(x+\sqrt{x^2+a^2}\right)+C$$
13. $$\int\frac{\sqrt{x^2+a^2}}{x}{\rm d}x=\sqrt{x^2+a^2}+a\ln\frac{\sqrt{x^2+a^2}-a}{|x|}+C$$
14. $$\int\frac{\sqrt{x^2+a^2}}{x^2}{\rm d}x=-\frac{\sqrt{x^2+a^2}}{x}+\ln\left(x+\sqrt{x^2+a^2}\right)+C$$
# (VII)
1. $$\int\frac{{\rm d}x}{\sqrt{x^2-a^2}}=\frac{x}{|x|}\operatorname{arcsinh}\frac{|x|}{a}+C_1=\ln\left|x+\sqrt{x^2-a^2}\right|+C$$
2. $$\int\frac{{\rm d}x}{\sqrt{(x^2-a^2)^3}}=-\frac{x}{a^2\sqrt{x^2-a^2}}+C$$
3. $$\int\frac{x}{\sqrt{x^2-a^2}}{\rm d}x=\sqrt{x^2-a^2}+C$$
4. $$\int\frac{x}{\sqrt{(x^2-a^2)^3}}{\rm d}x=-\frac{1}{\sqrt{x^2-a^2}}+C$$
5. $$\int\frac{x^2}{\sqrt{x^2-a^2}}{\rm d}x=\frac{x}{2}\sqrt{x^2-a^2}+\frac{a^2}{2}\ln\left|x+\sqrt{x^2-a^2}\right|+C$$
6. $$\int\frac{x^2}{\sqrt{(x^2-a^2)^3}}{\rm d}x=-\frac{x}{\sqrt{x^2-a^2}}+\ln\left|x+\sqrt{x^2-a^2}\right|+C$$
7. $$\int\frac{{\rm d}x}{x\sqrt{x^2-a^2}}=\frac{1}{a}\arccos\frac{a}{|x|}+C$$
8. $$\int\frac{{\rm d}x}{x^2\sqrt{x^2-a^2}}=\frac{\sqrt{x^2-a^2}}{a^2x}+C$$
9. $$\int\sqrt{x^2-a^2}\ {\rm d}x=\frac{x}{2}\sqrt{x^2-a^2}-\frac{a^2}{2}\ln\left|x+\sqrt{x^2-a^2}\right|+C$$
10. $$\int\sqrt{(x^2-a^2)^3}{\rm d}x=\frac{x}{8}\left(2x^2-5a^2\right)\sqrt{x^2-a^2}+\frac{3}{8}a^4\ln\left|x+\sqrt{x^2-a^2}\right|+C$$
11. $$\int x\sqrt{x^2-a^2}\ {\rm d}x=\frac{1}{3}\sqrt{(x^2-a^2)^3}+C$$
12. $$\int x^2\sqrt{x^2-a^2}\ {\rm d}x=\frac{x}{8}\left(2x^2-a^2\right)\sqrt{x^2-a^2}-\frac{a^4}{8}\ln\left|x+\sqrt{x^2-a^2}\right|+C$$
13. $$\int\frac{\sqrt{x^2-a^2}}{x}{\rm d}x=\sqrt{x^2-a^2}-a\arccos\frac{a}{|x|}+C$$
14. $$\int\frac{\sqrt{x^2-a^2}}{x^2}{\rm d}x=-\frac{\sqrt{x^2-a^2}}{x}+\ln\left|x+\sqrt{x^2-a^2}\right|+C$$
# (VIII)
1. $$\int\frac{{\rm d}x}{\sqrt{a^2-x^2}}=\arcsin\frac{x}{a}+C$$
2. $$\int\frac{{\rm d}x}{\sqrt{(a^2-x^2)^3}}=\frac{x}{a^2\sqrt{a^2-x^2}}+C$$
3. $$\int\frac{x}{\sqrt{a^2-x^2}}{\rm d}x=-\sqrt{a^2-x^2}+C$$
4. $$\int\frac{x}{\sqrt{(a^2-x^2)^3}}{\rm d}x=\frac{1}{\sqrt{a^2-x^2}}+C$$
5. $$\int\frac{x^2}{\sqrt{a^2-x^2}}{\rm d}x=-\frac{x}{2}\sqrt{a^2-x^2}+\frac{a^2}{2}\arcsin\frac{x}{a}+C$$
6. $$\int\frac{x^2}{\sqrt{(a^2-x^2)^3}}{\rm d}x=\frac{x}{\sqrt{a^2-x^2}}-\arcsin\frac{x}{a}+C$$
7. $$\int\frac{{\rm d}x}{x\sqrt{a^2-x^2}}=\frac{1}{a}\ln\frac{a-\sqrt{a^2-x^2}}{|x|}+C$$
8. $$\int\frac{{\rm d}x}{x^2\sqrt{a^2-x^2}}=-\frac{\sqrt{a^2-x^2}}{a^2x}+C$$
9. $$\int\sqrt{a^2-x^2}\ {\rm d}x=\frac{x}{2}\sqrt{a^2-x^2}+\frac{a^2}{2}\arcsin\frac{x}{a}+C$$
10. $$\int\sqrt{\left(a^2-x^2\right)^3}\ {\rm d}x=\frac{x}{8}\left(5a^2-2x^2\right)\sqrt{a^2-x^2}+\frac{3}{8}a^4\arcsin\frac{x}{a}+C$$
11. $$\int x\sqrt{a^2-x^2}\ {\rm d}x=-\frac{1}{3}\sqrt{\left(a^2-x^2\right)^3}+C$$
12. $$\int x^2\sqrt{a^2-x^2}\ {\rm d}x=\frac{x}{8}\left(2x^2-a^2\right)\sqrt{a^2-x^2}+\frac{a^4}{8}\arcsin\frac{x}{a}+C$$
13. $$\int\frac{\sqrt{a^2-x^2}}{x}{\rm d}x=\sqrt{a^2-x^2}+a\ln\frac{a-\sqrt{a^2-x^2}}{|x|}+C$$
14. $$\int\frac{\sqrt{a^2-x^2}}{x^2}\ {\rm d}x=-\frac{\sqrt{a^2-x^2}}{x}-\arcsin\frac{x}{a}+C$$
# (IX)
1. $$\int\frac{{\rm d}x}{\sqrt{ax^2+bx+c}}=\frac{1}{\sqrt{a}}\ln|2ax+b+2\sqrt{a}\sqrt{ax^2+bx+c}|+C$$
2. $$\int\sqrt{ax^2+bx+c}\ {\rm d}x=\frac{2ax+b}{4a}\sqrt{ax^2+bx+c}+\frac{4ac-b^2}{8\sqrt{a^3}}\ln\left|2ax+b+2\sqrt{a}\sqrt{ax^2+bx+c}\right|+C$$
3. $$\int\frac{x}{\sqrt{ax^2+bx+c}}\ {\rm d}x=\frac{1}{a}\sqrt{ax^2+bx+c}-\frac{b}{2\sqrt{a^3}}\ln\left|2ax+b+2\sqrt a \sqrt{ax^2+bx+c}\right|+C$$
4. $$\int\frac{{\rm d}x}{\sqrt{c+bx-ax^2}}=\frac{1}{\sqrt{a}}\arcsin\frac{2ax-b}{\sqrt{b^2+4ac}}+C$$
5. $$\int\sqrt{c+bx-ax^2}\ {\rm d}x=\frac{2ax-b}{4a}\sqrt{c+bx-ax^2}+\frac{b^2+4ac}{8\sqrt{a^3}}\arcsin\frac{2ax-b}{\sqrt{b^2+4ac}}+C$$
6. $$\int\frac{x}{\sqrt{c+bx-ax^2}}\ {\rm d}x=-\frac{1}{a}\sqrt{c+bx-ax^2}+\frac{b}{2\sqrt{a^3}}\arcsin\frac{2ax-b}{\sqrt{b^2+4ac}}+C$$
# (X)
1. $$\int\sqrt\frac{x-a}{x-b}{\rm d}x=(x-b)\sqrt{\frac{x-a}{x-b}}+(b-a)\ln\left(\sqrt{|x-a|}+\sqrt{|x-b|}\right)+C$$
2. $$\int\sqrt\frac{x-a}{b-x}{\rm d}x=(x-b)\sqrt\frac{x-a}{b-x}+(b-a)\arcsin\sqrt\frac{x-a}{b-a}+C$$
3. $$\frac{{\rm d}x}{\sqrt{(x-a)(b-x)}}=2\arcsin\sqrt\frac{x-a}{b-a}+C(a<b)$$
4. $$\int\sqrt{(x-a)(b-x)}{\rm d}x=\frac{2x-a-b}{4}\sqrt{(x-a)(b-x)}+\frac{(b-a)^2}{4}\arcsin\sqrt\frac{x-a}{b-a}+C(a<b)$$
# (XI)
1. $$\int\sin x\ {\rm d}x=-\cos x+C$$
2. $$\int\cos x\ {\rm d}x=\sin x+C$$
3. $$\int\tan x\ {\rm d}x=\int\frac{\sin x}{\cos x}{\rm d}x=-\int\frac{{\rm d}\cos x}{\cos x}=-\ln|\cos x|+C$$
4. $$\int\cot x\ {\rm d}x=\int\frac{\cos x}{\sin x}{\rm d}x=-\int\frac{{\rm d}\sin x}{\sin x}=\ln|\sin x|+C$$
5. $$\int\sec x\ {\rm d}x=\int\frac{\cos x}{\cos^2x}\ {\rm d}x=\int\frac{{\rm d}\sin x}{1-\sin^2x}=\frac{1}{2}\int\frac{1}{1-\sin x}-\frac{1}{1+\sin x}{\rm d}\sin x$$$$=\ln\left|\tan\left(\frac{\pi}{4}+\frac{x}{2}\right)\right|+C=\ln|\sec x + \tan x|+C$$
6. $$\int\csc x{\rm d}x=\ln\left|\tan\frac{x}{2}\right|+C=\ln|\csc x-\cot x|+C$$
7. $$\int\sec^2x\ {\rm d}x=\tan x+C$$
8. $$\int\csc^2x\ {\rm d}x=-\cot x+C$$
9. $$\int\sec x\tan x\ {\rm d}x=\sec x+C$$
10. $$\int\csc x\cot x\ {\rm d}x=-\csc x+C$$
11. $$\int\sin^2x\ {\rm d}x=\frac{x}{2}-\frac{1}{4}\sin{2x}+C$$
12. $$\int\cos^2x\ {\rm d}x=\frac{x}{2}+\frac{1}{4}\sin2x+C$$
13. $$\int\sin^nx\ {\rm d}x=-\frac{1}{n}\sin^{n-1}x\cos x+\frac{n-1}{n}\int\sin^{n-2}x\ {\rm d}x$$
14. $$\int\cos^nx\ {\rm d}x=\frac{1}{n}\cos^{n-1}x\sin x+\frac{n-1}{n}\int\cos^{n-2}x\ {\rm d}x$$
15. $$\int\frac{{\rm d}x}{\sin^n x}=-\frac{1}{n-1}\frac{\cos x}{\sin^{n-1}x}+\frac{n-2}{n-1}\int\frac{{\rm d}x}{\sin^{n-2}x}$$
16. $$\int\frac{{\rm d}x}{\cos^n x}=\frac{1}{n-1}\frac{\sin x}{\cos^{n-1}x}+\frac{n-2}{n-1}\int\frac{{\rm d}x}{\cos^{n-2}x}$$
17. $$\int\cos^mx\sin^nx\ {\rm d}x=\frac{1}{m+n}\cos^{m-1}x\sin^{n+1}x+\frac{m-1}{m+n}\int\cos^{m-2}x\sin^nx\ {\rm d}x$$
18. $$=-\frac{1}{m+n}\cos^{m+1}x\sin^{n-1}x+\frac{n-1}{m+n}\int\cos^mx\sin^{n-2}x\ {\rm d}x$$
19. $$\int\sin ax\cos bx\ {\rm d}x=-\frac{1}{2(a+b)}\cos(a+b)x-\frac{1}{2(a-b)}\cos(a-b)x+C$$
20. $$\int\sin ax\sin bx\ {\rm d}x=-\frac{1}{2(a+b)}\sin(a+b)x+\frac{1}{2(a-b)}\sin(a-b)x+C$$
21. $$\int\cos ax\cos bx\ {\rm d}x=\frac{1}{2(a+b)}\sin(a+b)x+\frac{1}{2(a-b)}\sin(a-b)x+C$$
22. $$\int\frac{{\rm d}x}{a+b\sin x}=\frac{2}{\sqrt{a^2-b^2}}\arctan\frac{a\tan \frac{x}{2}+b}{\sqrt{a^2-b^2}}+C(a^2>b^2)$$
23. $$\int\frac{{\rm d}x}{a+b\sin x}=\frac{1}{\sqrt{b^2-a^2}}\ln\left|\frac{a\tan\frac{x}{2}+b-\sqrt{b^2-a^2}}{a\tan\frac{x}{2}+b+\sqrt{b^2-a^2}}\right|+C(a^2<b^2)$$
24. $$\int\frac{{\rm d}x}{a+b\cos x}=\frac{2}{a+b}\sqrt\frac{a+b}{a-b}\arctan\left(\sqrt\frac{a-b}{a+b}\tan\frac{x}{2}\right)+C(a^2>b^2)$$
25. $$\int\frac{{\rm d}x}{a+b\cos x}=\frac{1}{a+b}\sqrt\frac{a+b}{a-b}\ln\left|\frac{\tan\frac{x}{2}+\sqrt\frac{a+b}{b-a}}{\tan\frac{x}{2}-\sqrt\frac{a+b}{b-a}}\right|+C(a^2<b^2)$$
26. $$\int\frac{{\rm d}x}{a^2\cos^2x+b^2\sin^2x}=\frac{1}{ab}\arctan\left(\frac{b}{a}\tan x\right)+C$$
27. $$\int\frac{{\rm d}x}{a^2\cos^2x-b^2\sin^2x}=\frac{1}{2ab}\ln\left|\frac{b\tan x+a}{b\tan x-a}\right|+C$$
28. $$\int x\sin ax\ {\rm d}x=\frac{1}{a^2}\sin ax-\frac{1}{a}x\cos ax+C$$
29. $$\int x^2\sin ax\ {\rm d}x=-\frac{1}{a}x^2\cos ax+\frac{2}{a^2}x\sin ax+\frac{2}{a^3}\cos ax+C$$
30. $$\int x\cos ax\ {\rm d}x=\frac{1}{a^2}\cos ax+\frac{1}{a}x\sin ax+C$$
31. $$\int x^2\cos ax\ {\rm d}x=\frac{1}{a}x^2\sin ax+\frac{2}{a^2}x\cos ax-\frac{2}{a^3}\sin ax+C$$
# (XII)
1. $$\int\arcsin\frac{x}{a}\ {\rm d}x=x\arcsin\frac{x}{a}+\sqrt{a^2-x^2}+C$$
2. $$\int x\arcsin\frac{x}{a}\ {\rm d}x=\left(\frac{x^2}{2}-\frac{a^2}{4}\right)\arcsin\frac{x}{a}+\frac{x}{4}\sqrt{a^2-x^2}+C$$
3. $$\int x^2\arcsin\frac{x}{a}{\rm d}x=\frac{x^3}{3}\arcsin\frac{x}{a}+\frac{1}{9}\left(x^2+2a^2\right)\sqrt{a^2-x^2}+C$$
4. $$\int\arccos\frac{x}{a}\ {\rm d}x=x\arccos\frac{x}{a}-\sqrt{a^2-x^2}+C$$
5. $$\int x\arccos\frac{x}{a}\ {\rm d}x=\left(\frac{x^2}{2}-\frac{a^2}{4}\right)\arccos\frac{x}{a}-\frac{x}{4}\sqrt{a^2-x^2}+C$$
6. $$\int x^2\arccos\frac{x}{a}\ {\rm d}x=\frac{x^3}{3}\arccos\frac{x}{a}-\frac{1}{9}\left(x^2+2a^2\right)\sqrt{a^2-x^2}+C$$
7. $$\int\arctan \frac{x}{a}\ {\rm d}x=x\arctan\frac{x}{a}-\frac{a}{2}\ln\left(a^2+x^2\right)+C$$
8. $$\int x\arctan \frac{x}{a}\ {\rm d}x=\frac{1}{2}\left(a^2+x^2\right)\arctan\frac{x}{a}-\frac{a}{2}x+C$$
9. $$\int x^2\arctan \frac{x}{a}\ {\rm d}x=\frac{x^3}{3}\arctan\frac{x}{a}-\frac{a}{6}x^2+\frac{a^3}{6}\ln\left(a^2+x^2\right)+C$$
# (XIII)
1. $$\int a^x{\rm d}x=\frac{1}{\ln a}a^x+C$$
2. $$\int e^{ax}=\frac{1}{a}e^{ax}+C$$
3. $$\int xe^{ax}=\frac{1}{a^2}(ax-1)e^{ax}+C$$
4. $$\int x^ne^{ax}=\frac{1}{a}x^ne^{ax}-\frac{n}{a}\int x^{n-1}e^{ax}{\rm d}x$$
5. $$\int xa^x{\rm d}x=\frac{1}{\ln a}a^x-\frac{1}{(\ln a)^2}a^x+C$$
6. $$\int x^na^x{\rm d}x=\frac{1}{\ln a}x^na^x-\frac{n}{\ln a}\int x^{n-1}a^x{\rm d}x$$
7. $$e^{ax}\sin bx\ {\rm d}x=\frac{1}{a^2+b^2}e^{ax}(a\sin bx-b\cos bx)+C$$
8. $$e^{ax}\cos bx\ {\rm d}x=\frac{1}{a^2+b^2}e^{ax}(b\sin bx+a\cos bx)+C$$
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