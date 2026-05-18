---
title: "Método da Secante"
layout: default
parent: "Zeros de Funções"
nav_order: 1
---

# Método da Secante

- O método da secante é um procedimento iterativo utilizado para encontrar zeros de uma função $f(x)$;
	
- Ele pertence à categoria dos métodos numéricos e é particularmente útil quando se busca uma solução aproximada para a equação $f(x)=0$;
	
- Este método é uma alternativa aos métodos de Newton e da bisseção, combinando algumas vantagens de ambos; onde $f$ é uma função contínua e diferenciável.
	
- O processo começa com duas  estimativas iniciais $x_0$ e $x_1$ para a raiz, e através de iterações sucessivas, aprimora esta estimativa.

---

## Dedução do Método da Secante

Se no método de Newton,

$\qquad x_{n+1} = x_n - \dfrac{f(x_n)}{f'(x_n)}. \quad n \geq 0$

aproximamos $f'(x_n)$, por:

$\qquad f'(x_n)  \approx \dfrac{f(x_n)-f(x_{n-1})}{x_n-x_{n-1}}$

obtemos a iteração do método da Secante:

$\qquad \boxed{ x_{n+1} = x_n - f(x_n) \cdot \left( \dfrac{x_n - x_{n-1}}{f(x_n) - f(x_{n-1})} \right),\quad n\geq 1 }$

com condições iniciais $x_0$ e $x_1$.

---

<b>Passos do Método da Secante</b>

1. Escolha dos Pontos Iniciais:
	
	- Selecione dois pontos iniciais $x_0$ e $x_1$ próximos da raiz desejada.  É importante que $f(x_0)$ e $f(x_1)$ não sejam iguais para evitar divisão por zero.

	
2. Iteração:
	
	- Calcule a próxima aproximação $x_{n+1}$ usando a fórmula: 
	
$\qquad \qquad x_{n+1} = x_n - f(x_n) \cdot \left( \dfrac{x_n -  x_{n-1}}{f(x_n) - f(x_{n-1})} \right),\quad n\geq 1$
		
$\qquad \qquad$ com condições iniciais $x_0$ e $x_1$.	
	 
3. Repetição:

	- Continue iterando até que a diferença entre os valores sucessivos $x_n$ e $x_{n+1}$ seja menor que uma tolerância predefinida, ou até que $f(x_{n+1})$ esteja suficientemente próximo de zero.

---

<b>Interpretação geométrica</b>

- O método de Newton está relacionado às retas tangentes ao gráfico da função  $f$;
	
- O método das secantes, está relacionado às retas secantes da função $f$.




