---
title: "Método da Bisseção"
layout: default
parent: "Zeros de Funções"
nav_order: 1
---

# Método da Bisseção

O método da bisseção é uma técnica numérica simples, robusta e eficiente para determinar raízes de funções contínuas.

> “Seu objetivo é encontrar uma raiz da função f(x) em um intervalo [a, b], tal que f(a) e f(b) tenham sinais opostos.”  
> *(CN_metodo_da_bissecao.pdf)*

---

## Hipóteses

- f é contínua em $[a, b]$
- $f(a)\cdot f(b) < 0$

---

## Entrada (Input)

- Extremos $a$ e $b$
- Tolerância `tol`
- Número máximo de iterações `maxit`

## Saída (Output)

- Aproximação da raiz  
- Ou mensagem de falha

---

# Algoritmo

1. Inicialize $x = a$, $y = b$
2. Defina `iter = 0`
3. Enquanto $y - x > tol$ e `iter < maxit`:
   - $m = \frac{x + y}{2}$
   - Se $f(x)\cdot f(m) < 0$, então $y = m$
   - Se $f(x)\cdot f(m) > 0$, então $x = m$
   - Se $f(m) = 0$, pare: $m$ é raiz exata
   - `iter = iter + 1`
4. Retorne $m$

---

# Vantagens

- Simplicidade
- Convergência garantida
- Estabilidade numérica

# Desvantagens

- Convergência lenta (linear)
- Exige mudança de sinal no intervalo

---

# Exemplo 1  
**Aproximar pelo método da Bisseção a raiz de** $f(x) = x^3 - x - 2$ **em** $[1, 2]$ com o criterio de parada $|b_k-a_k| < 10^{-6}$.

## Solução

Para determinar uma raiz da função 
	$f(x)=x^3-x-2$ no intervalo 
	$[1, \; 2]$ pelo método da bisseção, segue-se os seguintes passos: 
	
1. **Intervalo Inicial**: $f(1)=-2$ e $f(2)=4$.

Como $f$ é contínua e $f(1) \cdot f(2)<0$, há uma raiz no intervalo  $[1, \; 2]$;
		
3. **Ponto Médio**: $c=\dfrac{1+2}{2}=1.5$, e $f(1.5)=1.5^3-1.5-2=-0.125$;  
		
4. **Novo intervalo**: 	Como $f(1) \cdot f(1.5)>0$, a raiz está em 	$[1.5, \; 2]$;      
		
5. **Repetição**: Continue repetindo os passos, recalculando o ponto médio e ajustando o intervalo até atingir a precisão desejada.

### Tabela de iterações

| k | x | y | m | (y-x)/2 |
|---|---|---|---|---------|
| 1 | 1.000000 | 2.000000 | 1.500000 | 0.500000 |
| 2 | 1.500000 | 2.000000 | 1.750000 | 0.250000 |
| 3 | 1.500000 | 1.750000 | 1.625000 | 0.125000 |
| 4 | 1.500000 | 1.625000 | 1.562500 | 0.062500 |
| 5 | 1.500000 | 1.562500 | 1.531250 | 0.031250 |
| 6 | 1.500000 | 1.531250 | 1.515625 | 0.015625 |
| 7 | 1.515625 | 1.531250 | 1.523438 | 0.007812 |
| 8 | 1.515625 | 1.523438 | 1.519531 | 0.003906 |
| 9 | 1.519531 | 1.523438 | 1.521484 | 0.001953 |
| 10 | 1.519531 | 1.521484 | 1.520508 | 0.000977 |

**Raiz aproximada:** **1.5205**

![$f(x) = x^3 - x - 2$ ](../assets/images/fig_bissecao1.JPG)


---

# Exemplo 2  
**Aproximar pelo método da Bisseção a raiz de** $f(x) = x^3 + 4x^2 - 10$ **em** \([1, 2]\), tolerância $10^{-3}$

Tabela:

| k | x | y | m | (y-x)/2 |
|---|---|---|---|---------|
| 1 | 1.000000 | 2.000000 | 1.500000 | 0.500000 |
| 2 | 1.000000 | 1.500000 | 1.250000 | 0.250000 |
| 3 | 1.250000 | 1.500000 | 1.375000 | 0.125000 |
| 4 | 1.250000 | 1.375000 | 1.312500 | 0.062500 |
| 5 | 1.312500 | 1.375000 | 1.343750 | 0.031250 |
| 6 | 1.343750 | 1.375000 | 1.359375 | 0.015625 |
| 7 | 1.359375 | 1.375000 | 1.367188 | 0.007812 |
| 8 | 1.359375 | 1.367188 | 1.363281 | 0.003906 |
| 9 | 1.363281 | 1.367188 | 1.365234 | 0.001953 |
| 10 | 1.363281 | 1.365234 | 1.364258 | 0.000977 |

**Raiz aproximada:** **1.3642**

---

# Exemplo 3  
**Aproximar pelo método da Bisseção a raiz de** $f(x) = e^x - x - 2$ **em** $[-2, 0]$

**Raiz aproximada:** **–1.8408**

---

# Exemplo 4  
**\(f(x) = \cos(x) - x\)** em \([0, \pi/2]\)

**Raiz aproximada:** **0.7386**

---

# Exemplo 5  
Resolver:



\[
e^x - 2 = \cos(x - 2)
\]



Equivalente a:



\[
f(x) = e^x - \cos(x - 2) - 2
\]



**Raiz aproximada:** **0.8955**

---

# Convergência do Método da Bisseção

O método gera intervalos encaixados:



\[
[a_{k+1}, b_{k+1}] \subset [a_k, b_k]
\]



E:

- \(a_k\) é crescente  
- \(b_k\) é decrescente  
- \(b_k - a_k = \frac{b_0 - a_0}{2^k}\)

Logo:



\[
\lim_{k\to\infty} a_k = \lim_{k\to\infty} b_k = r
\]



E:



\[
f(r) = 0
\]



---

# Ordem de Convergência

Erro:



\[
e_k = |r - c_k|
\]



E:



\[
e_{k+1} \approx \frac{1}{2} e_k
\]



→ Convergência **linear**.

---

# Número de Iterações

Para erro \(e\):



\[
k \ge \log_2\left(\frac{b_0 - a_0}{e}\right)
\]



Exemplo:



\[
k = \log_2\left(\frac{1}{10^{-3}}\right) \approx 9.96 \Rightarrow 10\ \text{iterações}
\]



---

# Exercícios

1. Aplique o método da bisseção para:
   - \(f(x) = x^3 + 4x^2 - 10\)
   - \(f(x) = e^x - x - 2\)
   - \(f(x) = \cos(x) - x\)

2. Calcule o número mínimo de iterações para erro \(10^{-4}\) em \([1, 2]\).

