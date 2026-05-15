---
title: Índice Geral
layout: default
nav_order: 0
---

# 📘 Índice Geral do Livro

Este índice lista automaticamente todas as seções e capítulos.

## Aritmética

{% for page in site["01-aritmetica"].docs %}
- [{{ page.title }}]({{ page.url | relative_url }})
{% endfor %}

## Zeros de Funções

{% for page in site["02-zeros"].docs %}
- [{{ page.title }}]({{ page.url | relative_url }})
{% endfor %}

## Sistemas Lineares

{% for page in site["03-sistemas-lineares"].docs %}
- [{{ page.title }}]({{ page.url | relative_url }})
{% endfor %}
