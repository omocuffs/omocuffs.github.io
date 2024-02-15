---
layout: "default"
title: "Medalhistas"
permalink: /medalhistas/
---

<div class="container-xxl" data-bs-smooth-scroll="true" >
    <br><br>
    <h1 class="text-center" style="color:#613970"><strong>Alunos e Escolas medalhistas:</strong></h1> <br>
    <div class="accordion accordion-flush" id="accordionPanelsStayOpenExample">
    
    {% assign edicoes = site.data.omoc-edicoes | sort: "edicao" | reverse %}
    
    {% for edicao in edicoes %}
            {% include med-accordion-content.html ano-edicao=edicao.edicao documentos=edicao.premiados.documentos %}
    {% endfor %}
    </div>
</div>