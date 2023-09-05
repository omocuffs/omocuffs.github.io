---
layout: "default"
title: "Medalhistas"
permalink: /medalhistas/
---

<div class="container-xxl" data-bs-smooth-scroll="true" >
    <br><br>
    <h1 class="text-center" style="color:#613970"><strong>Alunos e Escolas medalhistas:</strong></h1> <br>
    <div class="accordion accordion-flush" id="accordionPanelsStayOpenExample">
    {% assign medalhistas = site.data.medalhistas | sort: "ano-edicao" | reverse %}
    {% for medalhista in medalhistas %}
            {% include medalhista-colapse.html %}
    {% endfor %}
    </div>
</div>