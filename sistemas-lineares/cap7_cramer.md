---
title: "Regra de Cramer"
layout: default
parent: "Sistemas Lineares"
nav_order: 1
---

# Sistemas Algébricos
Desejamos resolver sistemas do tipo

$\qquad Ax = b$, onde

- $A$ é uma matriz de coeficientes de ordem $n$,

- $x$ é um vetor das desconhecidas de ordem  $n$, e
  
- $b$ é um vetor de dados de ordem $n$.

Temos o sistema algébrico linear com $n$ equações e n desconhecidas $x_1, \ x_2, \ \cdots, x_n$:

$\qquad a_{11} x_1 + a_{12} x_2 + a_{13} x_3 + \cdots + a_{1n} x_n = b_1$

$\qquad a_{21} x_1 + a_{22} x_2 + a_{23} x_3 + \cdots + a_{2n} x_n = b_2$

$\qquad a_{31} x_1 + a_{32} x_2 + a_{33} x_3 + \cdots + a_{3n} x_n = b_3$

$\qquad \vdots  \qquad \quad \vdots    \qquad \quad  \vdots  \qquad \qquad \quad \vdots  \qquad \vdots$

$\qquad a_{n1} x_1 + a_{n2} x_2 + a_{n3} x_3 + \cdots + a_{nn} x_n = b_n$

Na forma matricial o sistema é escrito como:

$$
\underbrace{
\begin{bmatrix}
    a_{11} & a_{12} & \cdots & a_{1n} \\
    a_{21} & a_{22} & \cdots & a_{2n} \\
    \vdots & \vdots & \vdots & \vdots\\
    a_{n1} & a_{n2} & \dots  & a_{nn}
\end{bmatrix}}\_{A} \ \ \
\underbrace{
\begin{bmatrix}
    x_{1} \\
    x_{2} \\
    \vdots \\
    x_{n}
\end{bmatrix}}\_{x}
= \underbrace{
\begin{bmatrix}
    b_{1} \\
    b_{2} \\
    \vdots \\
    b_{n}
\end{bmatrix}}\_{b}
$$

