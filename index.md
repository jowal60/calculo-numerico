---
title: Índice Geral
layout: default
nav_order: 0
---

# 📘 Índice Geral do Livro

Este índice lista automaticamente todas as seções e capítulos.

{% for collection in site.collections %}
## {{ collection.label | replace: '01-', '' | replace: '02-', '' | replace: '03-', '' | capitalize }}

{% for page in collection.docs %}
- [{{ page.title }}]({{ page.url | relative_url }})
{% endfor %}
{% endfor %}
