---
title: "Método de Iteração do Ponto Fixo"
layout: default
parent: "Zeros de Funções"
nav_order: 1
---

# Método de Iteração do Ponto Fixo

## Definição
$p$ é um ponto fixo da função $g$, se e somente se, $g(p)=p$.

## Observação

  - Geometricamente, um ponto fixo de uma função é um ponto de intersecção entre a reta $y=x$ com o gráfico da função $g(x)$.
	
	- O problema de achar um zero: $f(p)=0$, pode-se transformar num problema de ponto fixo: $g(p)=p$, definindo a função $g$ de várias formas.
	
  Por exemplo, se $g(x)=x - \alpha f(x)$:
	$$
	f(p)=0 \Rightarrow g(p)=p - \alpha f(p)=p - \alpha \cdot 0=p,
	$$
	portanto, $g(p)=p$.
		
- Reciprocamente, o problema de ponto fixo: $g(p)=p$, pode-se transformar num problema de achar um zero fazendo $f(x)=g(x)-x$:

$$
				g(p)=p \Rightarrow f(p)=g(p) - p =p - p =0,
$$

portanto, $f(p)=0$.		

