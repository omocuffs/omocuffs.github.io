---
layout: "default"
title: "Listas de Treinamento"
permalink: /listas-de-treinamento/
---

<div class="container-xxl" data-bs-smooth-scroll="true" >
    <br><br>
    <h1 class="text-center" style="color:#613970"><strong>Listas de treinamento anteriores:</strong></h1> <br>
    <div class="accordion accordion-flush" id="accordionPanelsStayOpenExample">
    {% assign info = site.data.omoc-edicoes | sort: "edicao" | reverse %}
    {% for edicao in info %}
        {% include test_list-accordion-content.html ano-edicao=edicao.edicao fases=edicao.lista-de-treinamento.fases %}
    {% endfor %}
    </div>
</div>