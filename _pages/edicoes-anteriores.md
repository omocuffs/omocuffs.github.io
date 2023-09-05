---
layout: default
permalink: "/edicoes-anteriores/"
---
{% assign edicoes = site.data.edicoes-omoc | sort: "edicao" | reverse %}
{% assign edicao-atual = edicoes[0]%}

<style>
    h1 {color: #613970; font-weight: bold;}
    .dcolor { background-color: #613970; color: #fff;}
    .dcolor2 { background-color: #613970; color: #fff;}
    .dcolor2:hover { background-color: #c6a9ff; color: #fff;}
</style>

<div class="container mt-5"  data-bs-smooth-scroll="true">
    <div class="row">
      <!-- Default dropend button -->
      <div class="btn-group dropend">
        <h1 class="mr-3">Selecione uma edição:</h1>
        <button type="button" class="btn dropdown-toggle dcolor" data-bs-toggle="dropdown" aria-expanded="false">
          Edições
        </button>
        <ul class="dropdown-menu dcolor">
          {% for edicao in edicoes %}
          <li><a class="dropdown-item dcolor2" href="{{site.url}}/edicao/{{edicao.edicao}}">{{ edicao.edicao }}</a></li>
          {% endfor %}
        </ul>
      </div>
    </div>
</div>
