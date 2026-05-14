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

<a target="_blank" href="https://colab.research.google.com/github/jowal60/calculo-numerico/blob/main/zeros/cap3_metodo_bissecao.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Executar no Colab"/>
</a>

---

# Exemplo 1  
**Aproximar pelo método da Bisseção a raiz de** $f(x) = x^3 - x - 2$ **em** $[1, 2]$ com o criterio de parada $|b_k-a_k| < 10^{-6}$.

## Solução

Para determinar uma raiz da função 
	$f(x)=x^3-x-2$ no intervalo 
	$[1, \; 2]$ pelo método da bisseção, segue-se os seguintes passos: 
	
1. **Intervalo Inicial**: $f(1)=-2$ e $f(2)=4$.
   
   Como $f$ é contínua e $f(1) \cdot f(2)<0$, há uma raiz no intervalo  $[1, \; 2]$;
		
3. **Ponto Médio**: $pm=\dfrac{1+2}{2}=1.5$, e $f(1.5)=1.5^3-1.5-2=-0.125$;  
		
4. **Novo intervalo**: 	Como $f(1) \cdot f(1.5)>0$, a raiz está em 	$[1.5, \; 2]$;      
		
5. **Repetição**: Continue repetindo os passos, recalculando o ponto médio e ajustando o intervalo até atingir a precisão desejada.

### Tabela de iterações

| k | a | b | pm | (b - a)/2 | f(pm) |
|---|---|---|----|--------|--------|
| 1 | 1.00000000 | 2.00000000 | 1.50000000 | 0.50000000 | -1.25000000e-01 |
| 2 | 1.50000000 | 2.00000000 | 1.75000000 | 0.25000000 | 1.60937500e+00 |
| 3 | 1.50000000 | 1.75000000 | 1.62500000 | 0.12500000 | 6.66015625e-01 |
| 4 | 1.50000000 | 1.62500000 | 1.56250000 | 0.06250000 | 2.52197266e-01 |
| 5 | 1.50000000 | 1.56250000 | 1.53125000 | 0.03125000 | 5.91125488e-02 |
| 6 | 1.50000000 | 1.53125000 | 1.51562500 | 0.01562500 | -3.40538025e-02 |
| 7 | 1.51562500 | 1.53125000 | 1.52343750 | 0.00781250 | 1.22504234e-02 |
| 8 | 1.51562500 | 1.52343750 | 1.51953125 | 0.00390625 | -1.09712481e-02 |
| 9 | 1.51953125 | 1.52343750 | 1.52148438 | 0.00195312 | 6.22175634e-04 |
| 10 | 1.51953125 | 1.52148438 | 1.52050781 | 0.00097656 | -5.17888647e-03 |
| 11 | 1.52050781 | 1.52148438 | 1.52099609 | 0.00048828 | -2.27944332e-03 |
| 12 | 1.52099609 | 1.52148438 | 1.52124023 | 0.00024414 | -8.28905861e-04 |
| 13 | 1.52124023 | 1.52148438 | 1.52136230 | 0.00012207 | -1.03433124e-04 |
| 14 | 1.52136230 | 1.52148438 | 1.52142334 | 0.00006104 | 2.59354252e-04 |
| 15 | 1.52136230 | 1.52142334 | 1.52139282 | 0.00003052 | 7.79563135e-05 |
| 16 | 1.52136230 | 1.52139282 | 1.52137756 | 0.00001526 | -1.27394677e-05 |
| 17 | 1.52137756 | 1.52139282 | 1.52138519 | 0.00000763 | 3.26081572e-05 |
| 18 | 1.52137756 | 1.52138519 | 1.52138138 | 0.00000381 | 9.93427837e-06 |
| 19 | 1.52137756 | 1.52138138 | 1.52137947 | 0.00000191 | -1.40261126e-06 |
| 20 | 1.52137947 | 1.52138138 | 1.52138042 | 0.00000095 | 4.26582940e-06 |

Raiz aproximada: 1.521380

Iterações: 20

![$f(x) = x^3 - x - 2$ ](../assets/images/fig_bissecao1.JPG)


---

# Exemplo 2  
**Aproximar pelo método da Bisseção a raiz de** $f(x) = x^3 + 4x^2 - 10$ **em** \([1, 2]\), tolerância $10^{-3}$

## Solução

Pelo método da bisseção, segue-se os seguintes passos:

1. **Intervalo Inicial**: $f(1)=-5$ e $f(2)=14$.
	
	Como $f$ é contínua e $f(1) \cdot f(2)<0$, há uma raiz no intervalo $[1, \; 2]$;

2. **Ponto Médio**: $pm=\dfrac{1+2}{2}=1.5$, e $f(1.5)=1.5^3+4 \cdot 1.5^2-10=2.375$;

3. **Novo intervalo**: Como $f(1) \cdot f(1.5)<0$, a raiz está em $[1, \; 1.5]$;

4. **Repetição**: Continue repetindo os passos, recalculando o ponto médio e ajustando o intervalo até atingir a precisão desejada.

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

