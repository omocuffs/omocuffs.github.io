---
layout: "default"
title: "Provas"
permalink: /provas/
---

<div class="container-xxl" data-bs-smooth-scroll="true" >
    <br><br>
    <h1 class="text-center" style="color:#613970"><strong>Provas Anteriores:</strong></h1> <br>
    <div class="accordion accordion-flush" id="accordionPanelsStayOpenExample">
    {% assign info = site.data.edicoes-midia | sort: "edicao" | reverse %}
    {% for edicao in info %}
        {% include test_list-accordion-content.html ano-edicao=edicao.edicao fases=edicao.prova.fases %}
    {% endfor %}
    </div>
</div>