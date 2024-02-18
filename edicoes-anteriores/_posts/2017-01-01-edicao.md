---
layout: edicao-anterior
permalink: "/edicao/:year"
link-imagens-drive: 
---

{% assign ano = page.date |  date: "%Y" %}
{% assign edicao = site.data.edicoes-omoc | where: "edicao", ano | first %}
