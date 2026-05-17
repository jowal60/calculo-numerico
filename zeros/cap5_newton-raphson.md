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

$g(x) = x + \alpha(x)f(x), \quad \alpha(x) \neq 0$,

onde, $\alpha(x)$ é uma função arbitrária.
