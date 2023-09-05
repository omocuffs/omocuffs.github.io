---
layout: "default"
title: "Listas de Treinamento"
permalink: /listas-de-treinamento/
---

<div class="container-xxl" data-bs-smooth-scroll="true" >
    <br><br>
    <h1 class="text-center" style="color:#613970"><strong>Listas de treinamento anteriores:</strong></h1> <br>
    <div class="accordion accordion-flush" id="accordionPanelsStayOpenExample">
    {% assign listas = site.data.listas-treinamento | sort: "ano-edicao" | reverse %}
    {% for prova in listas %}
            {% include prova-colapse.html %}
    {% endfor %}
    </div>
</div>