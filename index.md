---
layout: default
title: "Inicial"
permalink: /
image:
    banner: inicio/banner-inicio-omoc-2023.png
---
{% assign edicoes = site.data.edicoes-omoc | sort: "edicao" | reverse %}
{% assign edicao-atual = edicoes[0]%}

{% assign calendarios = site.data.calendario | sort: "ano-edicao" | reverse %}
{% assign calendario-atual = calendarios[0]%}

<style>
/* Override the padding in container-fluid */
.container-fluid {
  padding: 0;
}

/* Override the margin in img-fluid */
.img-fluid {
  margin: 0;
}

span {padding: 7px; border-radius: 3px;}
.link2 {color:#613970;}
.link2:hover {color: #c6a9ff; text-decoration: none;}
</style>
<section>
<div class="container-fluid" >
  {% if edicao-atual.banner-imagem %}
  <div class="d-none d-md-block">
    <img class="img-fluid" src="{{site.url}}/images/edicoes/{{edicao-atual.edicao}}/{{edicao-atual.banner-imagem}}" alt="{{edicao-atual.banner-imagem}}">
  </div>
  <div class="d-md-none">
    <img class="img-fluid" src="{{site.url}}/images/edicoes/{{edicao-atual.edicao}}/{{edicao-atual.banner-imagem-mobile}}" alt="{{edicao-atual.banner-imagem-mobile}}">
  </div>
  {% else %}
  <h2 class="display-4" ><span class="badge bg-light" style="color: #613970;" >OMOC</span></h2>
  {% endif %}
</div>
<div class="container-xxl" data-bs-smooth-scroll="true" >
  <br>
  <div class="row g-3 " >
    <h1 style="color: #613970;" class="text-center text-uppercase" ><strong>Olimpíada de Matemática do Oeste Catarinense (OMOC)</strong></h1>
    <br><br>
    <div class="col-lg-8" >
    <!-- inicio do acesso rapido -->
      <h3 style="color: #613970;" class="text-left font-weight-bold" >Acesso rápido:</h3>
      <hr>
      <div class="card">
        <h5 class="card-title" style="background-color: #613970; color:white;padding: 5px;">Inscrições {{edicao-atual.edicao}}</h5>
        <div class="card-body">
          <div class="container">
            <div class="row">
              <div class="col-sm-12 col-12">
                <p>O processo de inscrição das escolas para participar da {{edicao-atual.numero}} Olimpíada de Matemática do Oeste Catarinense já está aberto.</p>
                <br>
                <h5>Ofício Circular 001 / Olimpíada Regional de Matemática - UFFS / 2023:</h5>
                <a class="link2" href="{{site.url}}/documents/inscricoes/{{edicao-atual.edicao}}/{{edicao-atual.oficio-circular-inscricoes}}" target="_blank">
                {{site.data.icons.pdf-document}}
                {{site.data.icons.download}} Fazer download (.pdf)</a>
                <br><br>
                <h5>Formulário de inscrição das escolas para 2023:</h5>
                <a class="link2" href="{{edicao-atual.formulario-inscricoes}}" target="_blank">Formulário do Google</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="card mt-2">
        <h5 class="card-title" style="background-color: #613970; color:white;padding: 5px;">Treinamentos {{edicao-atual.edicao}}</h5>
        <div class="card-body">
          <div class="container">
            <div class="row">
              <div class="col-sm-10 col-10">
                <p>Inscreva seus alunos nos treinamentos da {{edicao-atual.numero}} Edição da OMOC pelo email: <strong style="color:#613970;">{{site.data.contato.email}}</strong></p>
              </div>
            </div>
          </div>     
        </div>
      </div>
    </div>
    <div class="col border border-black text-center" >
      <div class="row border-bottom pt-3 pb-3" style="color: #fff; background-color: #613970;">
        <h1><strong>Calendário 2024</strong></h1>
      </div>
      <!--card -->
      {% for evento in calendario-atual.eventos %}
        {%if evento.abertura.data and evento.fechamento.data %}
          {% assign dataev = evento.abertura %}
        {% elsif evento.fechamento.data %}
          {% unless evento.abertura.data %}
            {% assign dataev = evento.fechamento %}
          {% endunless %}
        {% elsif evento.abertura.data %}
            {% assign dataev = evento.abertura %}
        {%endif%}
      <div class="row border-bottom">
        <div class="col-2 text-center" >
          <h1 class="display-4"><span class="badge" style="background-color: #613970;">{{ dataev.data | date: "%d" }}</span></h1>
          <h2 style="color: #613970;">&nbsp;{{ dataev.nome-do-mes | upcase | truncate: 3, ""}}</h2>
        </div>
        <div class="col-10 justify-content-center align-items-center">
          <br>
          <h3 class="text-uppercase"><strong>{{evento.evento}}</strong></h3>
          <ul class="list-inline">
            {% if dataev.dia-da-semana %}
            <li class="list-inline-item">{{site.data.icons.calendario}}
                {{ dataev.dia-da-semana | truncate: 3, ""}}
            </li>
            {% endif %}
            {% if dataev.horario %}
            <li class="list-inline-item">{{site.data.icons.relogio}}
                {{ dataev.horario }}                 
            </li>
            {% endif %}
            {% if evento.local-realizacao %}
            <li class="list-inline-item">{{site.data.icons.localizacao}}
                {{ evento.local-realizacao }}
            </li>
            {% endif %}
          </ul>
        </div>
      </div>
      {% endfor %}
      <!-- gen card -->
    </div>
  </div>
</div>
</section>
