---
title: "Regra de Cramer"
layout: default
parent: "Sistemas Lineares"
nav_order: 1
---

# Sistemas Algébricos

Desejamos resolver sistemas do tipo

$$Ax = b$$

onde:
* $A$ é uma matriz de coeficientes de ordem $n$,
* $x$ é um vetor das desconhecidas de ordem $n$, e
* $b$ é um vetor de dados de ordem $n$.

Temos o sistema algébrico linear com $n$ equações e $n$ desconhecidas $x_1, x_2, \dots, x_n$:

$$a_{11} x_1 + a_{12} x_2 + a_{13} x_3 + \dots + a_{1n} x_n = b_1$$
$$a_{21} x_1 + a_{22} x_2 + a_{23} x_3 + \dots + a_{2n} x_n = b_2$$
$$a_{31} x_1 + a_{32} x_2 + a_{33} x_3 + \dots + a_{3n} x_n = b_3$$
$$\vdots$$
$$a_{n1} x_1 + a_{n2} x_2 + a_{n3} x_3 + \dots + a_{nn} x_n = b_n$$

Na forma matricial o sistema é escrito como:

$$
\begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \dots & a_{nn}
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{bmatrix}
=
\begin{bmatrix}
b_1 \\
b_2 \\
\vdots \\
b_n
\end{bmatrix}
$$
