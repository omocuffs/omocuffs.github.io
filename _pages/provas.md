---
layout: "default"
title: "Provas"
permalink: /provas/
---

<div class="container-xxl" data-bs-smooth-scroll="true" >
    <br><br>
    <h1 class="text-center" style="color:#613970"><strong>Provas Anteriores:</strong></h1> <br>
    <div class="accordion accordion-flush" id="accordionPanelsStayOpenExample">
    {% assign provas = site.data.provas | sort: "ano-edicao" | reverse %}
    {% for prova in provas %}
            {% include prova-colapse.html %}
    {% endfor %}
    </div>
</div>