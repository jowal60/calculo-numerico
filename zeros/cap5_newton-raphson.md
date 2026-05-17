---
title: "Método de Newton-Raphson"
layout: default
parent: "Zeros de Funções"
nav_order: 1
---

# Método de Newton-Raphson
- O método de Newton, também conhecido como método de Newton-Raphson, é uma eficiente técnica numérica utilizada para encontrar raízes de funções;
	
- Sua eficácia e rapidez o tornam uma ferramenta fundamental em várias áreas da matemática aplicada, engenharia, física e ciência da computação;
	
- O método de Newton é uma abordagem que busca solucionar a equação $f(x)=0$ de forma iterativa, onde $f$ é uma função contínua e diferenciável;
	
- O processo começa com uma estimativa inicial $x_0$ para a raiz e, através de iterações sucessivas, aprimora esta estimativa.

---

## Aspectos Teóricos do Método de Newton
Seja $x^{\star}$ solução de $f(x)=0$, onde $f \in C^1$.

Associamos à determinação do zero de $f$, a iteração de ponto fixo:

$\qquad g(x) = x + \alpha(x)f(x), \quad \alpha(x) \neq 0$,

onde, $\alpha(x)$ é uma função arbitrária.

**Objetivo**: Escolher $\alpha(x)$ de forma que a iteração do ponto fixo tenha ótima taxa de convergência.

"QUANTO MENOR FOR $|g'(x)|$, A TAXA DE CONVERGÊNCIA SERÁ MAIOR E O ERRO DECAIRÁ MAIS RÁPIDO"

O caso ótimo acontece se, $g'(x^{\star})=0$.

Derivando a função: $g(x) = x + \alpha(x) f(x)$, resulta 

$g'(x) =1+\alpha(x) f'(x) + \alpha'(x) f(x)$.

No ponto $x=x^{\star}$, temos:

$g'(x^{\star}) = 1 + \alpha(x^*) f'(x^{\star}) + \alpha'(x^{\star}) \underbrace{f(x^{\star})}_{=0}$.

Como $f(x^{\star})=0$, temos:

$g'(x^{\star}) = 1 + \alpha(x^{\star}) f'(x^{\star})$.

escolhendo: $g'(x^{\star})=0$, resulta:

$\alpha(x^{\star}) = -\dfrac{1}{f'(x^{\star})}, \qquad f'(x^{\star})\neq 0$.

Logo,

$g(x) = x + \alpha(x) f(x) = x - \dfrac{f(x)}{f'(x)}$.

Do método iterativo do ponto fixo: $x_{n+1}=g(x_n)$, obtém-se o **método de Newton** para calcular os zeros de $f$:

$\boxed{x_{n+1} = x_{n} - \dfrac{f\left(x_n \right)}{f'\left(x_{n}\right)}, \quad n\geq 0,}$

sendo $x_0$ uma aproximação inicial dada.
