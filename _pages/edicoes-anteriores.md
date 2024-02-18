---
layout: default
permalink: "/edicoes-anteriores/"
---
{% assign edicoes = site.data.edicoes-midia | sort: "edicao" | reverse %}

<style>
    h1 {color: white; font-weight: bold;}
    .dcolor { background-color: #613970; color: #fff;}
    .dcolor2 { background-color: #613970; color: #fff;}
    .dcolor2:hover { background-color: #c6a9ff; color: #fff;}
</style>


<div class="container-xxl" data-bs-smooth-scroll="true" >
    <br><br>
    <h1 class="text-center" style="color:#613970;"><strong>Saiba mais sobre uma Edição OMOC!</strong></h1>
    <h3 class="text-center" style="color:#613970; font-weight: bold;">(níveis, calendário, imagens)</h3>
    <br>
    <div class="d-grid gap-2 col-6 mx-auto">
    {% for edicao in edicoes %}
      <a class="btn" href="{{site.url}}/edicao/{{edicao.edicao}}" style="background-color: #613970;"><h1>{{edicao.edicao}}</h1></a>
    {% endfor %}
    </div>
</div>