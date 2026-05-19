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

---

<b>Exemplo</b>

Resolver:

$$
\begin{matrix}
		3 x_1 + 2 x_2 &=  \ 12 \\
		2 x_1 - 3 x_2 &= -5
	\end{matrix}
$$

<b>Solução</b>

$$
D_1 = 
\begin{vmatrix}
12 & 2 \\
-5 & -3
\end{vmatrix} 
= -36+10 = -26
$$

$$
D_2  = 
\begin{vmatrix}
3 & 12 \\
2 & -5
\end{vmatrix}
= -15 -24 = -39
$$

$$
D = 
\begin{vmatrix}
3 & 2 \\
2 & -3
\end{vmatrix}
= -9-4 = -13
$$
	
logo,

$$
\begin{matrix}
x_1 &= \dfrac{D_1}{D} = \dfrac{-26}{-13} = 2 \\
& \\
x_2 &= \dfrac{D_2}{D} = \dfrac{-39}{-13} = 3
\end{matrix}
$$

---

<b>Exemplo</b>

Resolver usando o método de Cramer:

$$
\begin{matrix}
2 x_1 + 3 x_2 - 2 x_3  &= 4 \\
3 x_1 - 4 x_2 + x_3    &= 1  \\
-x_1 + 2 x_2 + 3 x_3  &= 11
\end{matrix}	
$$
