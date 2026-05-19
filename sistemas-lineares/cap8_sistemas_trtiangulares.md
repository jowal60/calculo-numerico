---
title: "Sistemas Algébricos Triangulares"
layout: default
parent: "Sistemas Lineares"
nav_order: 1
mathjax: true
---

# Sistemas Algébricos Triangulares

Desejamos resolver sistemas do tipo

$$
Ax=b
$$
onde,

a) $A$ é uma matriz triangular superior de ordem $n$, ou
	
b) $A$ é uma matriz triangular inferior de ordem $n$

---

## Sistema Triangular Superior

Temos o sistema com $n$ equações e n desconhecidas $x_1, \ x_2, \ \cdots, x_n$:

$$
\begin{matrix}
a_{11} x_1 &+& a_{12} x_2
&+& a_{13} x_3 &+& \cdots &+& a_{1n} x_n = b_1  \\
& & a_{22} x_2 &+& a_{23} x_3 &+& \cdots &+& a_{2n} x_n = b_2 \\
&& && a_{33} x_3 &+& \cdots &+& a_{3n} x_n = b_3 \\
&& && && \ddots && \vdots \\
&& && && && a_{nn} x_n = b_n
\end{matrix}
$$

Na forma matricial o sistema é escrito como:

$$
\underbrace{
\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
0      & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots\\
0      & \dots  & 0     & a_{nn}
\end{bmatrix}
}\_{A} \ \ \
\underbrace{
\begin{bmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{bmatrix}
}\_{x}
= \underbrace{ 
\begin{bmatrix}
b_{1} \\
b_{2} \\
\vdots \\
b_{n}
\end{bmatrix}
}\_{b}
$$

onde, os elementos abaixo da diagonal principal da matriz $A$ são iguais a zero.

Resolvemos por **retro-substituição**:
\begin{itemize}
	\item
- isolando $x_n$ na ultima equação

$$
x_n = b_n/a_{nn}
$$

- substituindo $x_n$ na penúltima equação, e isolando $x_{n-1}$ obtemos

$$
x_{n-1} = ( b_{n-1} - a_{n-1,n} x_n ) / a_{n-1,n-1}
$$

- e continuando desta forma até a primeira equação obteremos

$$
x_{1} = ( b_{1} -a_{12} x_2 - \cdots -a_{1n} x_n ) / a_{11}.
$$

De forma geral, para $i=n-1,\dots,1$:

$$
\boxed{x_{i} = ( b_{i} -a_{i,i+1} x_{i+1} - \cdots - a_{i,n} x_n  ) / a_{i,i}}
$$

