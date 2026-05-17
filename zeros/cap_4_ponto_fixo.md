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

  ![ ](../assets/images/fig_pontofixo1.JPG)
	
- O problema de achar um zero: $f(p)=0$, pode-se transformar num problema de ponto fixo: $g(p)=p$, definindo a função $g$ de várias formas.
	
  Por exemplo, se $g(x)=x - \alpha f(x)$:
  
$\qquad f(p)=0 \Rightarrow g(p)=p - \alpha f(p)=p - \alpha \cdot 0=p,$

$\qquad$ portanto, $g(p)=p$.
		
- Reciprocamente, o problema de ponto fixo: $g(p)=p$, pode-se transformar num problema de achar um zero fazendo $f(x)=g(x)-x$:

$g(p)=p \Rightarrow f(p)=g(p) - p =p - p =0,$
  
$\qquad$ portanto, $f(p)=0$.		

---

## Exemplo
Determine se a função $g(x)=x^2-2$ tem um ponto fixo.

### Solução
Deve-se resolver: $\color{white}{g(x)=x}$:

$g(x) = x$

$x^2-2 = x$

$x^2-x-2 = 0$

$(x+1) \cdot (x-2) = 0$

Logo, os pontos fixos de $g$ são: $x=-1$ e $x=2$.

Geometricamente os pontos fixos $x=-1$ e  $x=2$ são as interseções do gráfico de $g(x)=x^2-2$ e a reta $y=x$.

![ ](../assets/images/fig_pontofixo2.JPG)

---

<b>Teorema (Existência e Unicidade)</b> 

1. Se $g \in C^0[a, \ b]$ e $g(x) \in [a, \ b]$, então $g$ admite um ponto fixo em $[a, \ b]$;

2. Se além mais, $g \in C^1 (a, \ b)$ e existe uma constante $0<k<1$ tal que
   
$\qquad \| g^{'}(x) \| \leq k, \ \forall x \in (a, \ b)$,

então existe um único ponto fixo em $[a, \ b]$.

![ ](../assets/images/fig_pontofixo3.JPG)

<b>Demonstração</b>

<b>Prova da existência:</b>

- Se $g(a)=a$ ou $g(b)=b$, então $a$ ou $b$ é um ponto fixo;
			
- Se $a<g(x)<b$, seja $f(x)=g(x)-x$, temos:
	
	- $f(a)=g(a)-a>0$, e	
				
	- $f(b)=g(b)-b<0$,
				
	- pelo teorema de Bolzano, existe $p$ tal que $f(p)=0$;
				
	- logo, $f(p)=g(p)-p=0$ e portanto, $g(p)=p$.
			
<b>Prova da unicidade:</b>
		
Por contradição: vamos supor que $p$ e $q$ são dois pontos fixos diferentes, logo:
		
- pelo TVM, existe $r \in [p, \ q]$, tal que $\dfrac{g(q)-g(p)}{q-p}=g^{'}(r)$;
		
- $|q-p| = |g(q)-g(p)| = |g^{'}(r)| \ |q-p| \leq k |q-p| < |q-p|$;
		
- portanto, $|q-p| < |q-p|$, o qual é uma contradição.
		
Conclui-se que existe um único ponto fixo em $[a, \ b]$.

---

<div class="exemplo">
<b>Exemplo</b>

Verificar que $g(x)=\dfrac{x^2-1}{3}$ tem um único ponto fixo em $[-1, \; 1]$.

<b> Solução </b>

- $g \in C^0 [-1, \ 1]$;
	
- se $-1 \leq x \leq 1$, então
  
$\qquad 0 \leq x^2 \leq 1 \Rightarrow -\dfrac{1}{3} \leq \dfrac{x^2-1}{3} \leq 0 \quad \Rightarrow \quad g(x) \subset [-1, \ 1]$
		
- se $x \in [-1, \ 1]$, então
  
$\qquad |g^{'}(x)| = \dfrac{2 |x|}{3} \leq \dfrac{2}{3} = k < 1$

Logo, $g$ admite um único ponto fixo em $[-1, \ 1]$.

<b>Cálculo dos pontos fixos</b>.

$\qquad g(x) = x \; \Rightarrow \dfrac{x^2-1}{3} = x \quad \Rightarrow \quad x^2-3x-1=0$

$\qquad x = \dfrac{-(-3) \pm \sqrt{(-3)^2-4(1)(-1)}}{2 \cdot 1} = \dfrac{3 \pm \sqrt{13}}{2}$
	
logo, os pontos fixos são
	
$\qquad p_1 = \dfrac{3-\sqrt{13}}{2} \in [-1, \ 1]$

$\qquad p_2 = \dfrac{3+\sqrt{13}}{2} \notin [-1, \ 1]$
	
portanto, $g$ admite um único ponto fixo no intervalo $[-1, \ 1]$.

![ ](../assets/images/fig_pontofixo4.JPG)

</div>

---

<div class="observaçao">
<b> Observação </b>
	
- Considerando $g(x)=(x^2-1)/3$ no intervalo $[3, \ 4]$, temos o ponto fixo $p_2 = (3+\sqrt{13})/2$;
	
- temos que $p_2 \in [3, \ 4]$, mas $g([3, \ 4]) \not\subset [3, \ 4]$, por exemplo $g(4)=5 \notin [3, \ 4]$;
	
- assim, $p_2$ é um ponto fixo de $g$, entretanto não satisfaz as condições do Teorema.

O Teorema da condições suficientes, mas não necessárias.

</div>

---

<div class="exemplo">
<b> Exemplo </b>

Mostre que o teorema não garante a unicidade de um ponto fixo de $g(x)=3^{-x}$ em $[0, \ 1]$, ainda que exista um único ponto fixo nesse intervalo.

<b>Solução</b>

- $g \in C^0[0, \; 1]$;
	
- $g'(x) = -3^{-x} \cdot ln(3) < 0$, logo $g$ é estritamente decrescente;
	
- como $0<g(x)<g(0)=1$, então $g([0, \ 1]) \subset [0, \ 1]$. O teorema garante a existência de um ponto fixo de $g$ em $[0, \ 1]$;
	
- como $g'(0)=-ln(3)<-1$, então $|g'(x)| \nless 1$ em $[0, \ 1]$.

O teorema não garante a unicidade. Entretanto o gráfico mostra a existência de um único ponto fixo de $g$ em $[0, \ 1]$.

![ ](../assets/images/fig_pontofixo5.JPG)
</div>

<div class="observacao">
<b> Observação</b>

Como determinar o ponto fixo de $g(x)=3^{-x}$ no intervalo $[0, \ 1]$?

- como a função $g$ é contínua em $[0, \ 1]$ pode-se aplicar o método da bisseção para $f(x)=g(x)-x$;
	
- ou, desenvolver métodos numéricos para aproximar os pontos fixos. !!!

</div>

---

# Método da iteração do Ponto Fixo

<div class="problema">
<b> Problema:</b>

Dada uma função $g(x)$ desejamos resolver a equação $x=g(x)$.
	
O **método da iteração do ponto fixo** consiste em computar a seguinte sequência recursiva:
	
$\qquad x_{n+1} = g(x_n), \quad n>0$
	
com $x_0$ sendo uma aproximação inicial do ponto fixo.

![ ](../assets/images/fig_pontofixo6.JPG)
</div>

---

<div class="exemplo">
<b> Exemplo</b>

Aplicando o método de iteração do ponto fixo, determinar o zero da função $f(x)=xe^x - 10$.

<b> Solução</b>

- Construindo um problema de ponto fixo equivalente:
		
$\qquad f(x)=0 \Rightarrow \alpha f(x)=0 \Rightarrow x- \alpha f(x) =x,$
		
$\qquad$ para qualquer parâmetro $\alpha \neq 0$.
	
- Consideremos, então, as seguintes duas funções:
		
$\qquad g_1(x) = x-0.5 f(x)$, e

$\qquad g_2(x) = x-0.05 f(x)$.
		
- O ponto fixo destas duas funções coincide com o zero de $f(x)$, pois se $g(p)=p$ então:
		
$\qquad g_1(p) = p-0.5f(p) \quad \Rightarrow \quad  p=p-0.5 f(p) \quad \Rightarrow \quad  f(p)=0$, e

$\qquad g_2(p) = p-0.05 f(p) \quad \Rightarrow \quad  p=p-0.05f(p) \quad \Rightarrow \quad f(p)=0$.
		
- Construindo as iterações do ponto fixo:

$\begin{matrix} x_{n+1} = g_1(x_n) \\ x_0 = 1.7 \end{matrix} \quad \Rightarrow \quad \begin{matrix} x_{n+1} = x_n - 0.5 f(x_n) \\ x_0 = 1.7 \end{matrix}$


e
		\[
		\left\\{
		\begin{matrix}
			z_{n+1} = g_2(z_n) \\
			z_0 = 1.7
		\end{matrix}
		\right.
		\Rightarrow
		\left\{
		\begin{matrix}
			z_{n+1} = z_n - 0.05 f(x_n) \\
			z_0 = 1.7
		\end{matrix}
		\right.
		\]
		obtém-se a seguinte tabela com os resultados:
		\vskip0.2cm
		\begin{center}
			\begin{tabular}{|c|c|c|}
			\hline 
			$n$ & $x_n$ & $z_n$ \\ 
			\hline 
			0 & 1.700 & 1.700 \\ 
			\hline 
			1 & 2.047 & 1.735 \\ 
			\hline 
			2 & -0.8812 & 1.743 \\ 
			\hline 
			3 & 4.3013 & 1.746 \\ 
			\hline 
			4 & -149.4 & 1.746 \\ 
			\hline 
		\end{tabular} 
		\end{center}
		A sequência $x_n$ é divergente, enquanto a sequência 
		$z_n$ é convergente.
\end{itemize}
</div>
