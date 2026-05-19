---
title: "Regra de Cramer"
layout: default
parent: "Sistemas Lineares"
nav_order: 1
mathjax: true
---

# Sistemas Algébricos

Desejamos resolver sistemas do tipo

$$Ax = b$$

onde:

* $A$ é uma matriz de coeficientes de ordem $n$,
* $x$ é um vetor das desconhecidas de ordem $n$, e
* $b$ é um vetor de dados de ordem $n$.

Temos o sistema algébrico linear com $n$ equações e $n$ desconhecidas $x_1, x_2, \dots, x_n$:

$$
\begin{bmatrix}
a_{11} x_1 + a_{12} x_2 + a_{13} x_3 + \dots + a_{1n} x_n = b_1 \\
a_{21} x_1 + a_{22} x_2 + a_{23} x_3 + \dots + a_{2n} x_n = b_2 \\
a_{31} x_1 + a_{32} x_2 + a_{33} x_3 + \dots + a_{3n} x_n = b_3 \\
\vdots \\
a_{n1} x_1 + a_{n2} x_2 + a_{n3} x_3 + \dots + a_{nn} x_n = b_n
\end{bmatrix}
$$

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
\end{bmatrix} =
\begin{bmatrix}
b_1 \\
b_2 \\
\vdots \\
b_n
\end{bmatrix}
$$

---

## Regra de Cramer
A solução do sistema $Ax=b$ é dada pela **Regra de Cramer**:
$$
x_k = \dfrac{D_k}{D}, \quad k=1,2,\cdots,n
$$

onde,

$$
D_k = 	\begin{vmatrix}
	a_{11} & \cdots & a_{1,k-1} 
	& \boxed{b_1} & a_{1,k+1} & \cdots
	& a_{1n}
	\\
	a_{21}      & \cdots & a_{2,k-1} 
	&\boxed{ b_2} & a_{2,k+1} & \cdots
	& a_{2n} \\
	\vdots & & \vdots &  \vdots & \vdots & & \vdots
	\\
	a_{n1} & \cdots & a_{n,k-1} 
	& \boxed{b_n} & a_{n,k+1} & \cdots
	& a_{nn}
\end{vmatrix}
$$

e

$$
D = 	\begin{vmatrix}
	a_{11} & \cdots & a_{1,k-1}
	& a_{1k} & a_{1,k+1} & \cdots
	& a_{1n}
	\\
	a_{21} & \cdots & a_{2,k-1} 
	& a_{2k} & a_{2,k+1} & \cdots
	& a_{2n} \\
	\vdots & & \vdots &  \vdots & \vdots & & \vdots
	\\
	a_{n1} & \cdots & a_{n,k-1}
	& a_{nk} & a_{n,k+1} & \cdots
	& a_{nn}
\end{vmatrix}
$$
