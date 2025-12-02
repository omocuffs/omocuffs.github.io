---
layout: default
title: "Inicial"
permalink: /
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

.date-nums h1,.date-nums h4,.date-nums h5 {
  display: inline;
}
</style>
<section>
<div class="container-xxl" data-bs-smooth-scroll="true" >
  <h1 style="visibility: hidden;">Olimpíada de Matemática do Oeste Catarinense</h1>
  <div class="row g-3" >
    <div class="d-none d-md-block text-center">
      <img class="img-fluid" src="{{site.url}}/images/common/index-banner.png" alt="Banner OMOC" >
    </div>
    <div class="d-md-none">
        <img class="img-fluid" src="{{site.url}}/images/common/index-banner-mobile.png" alt="Banner OMOC" >
    </div>
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
                <h5>Carta convite / Olimpíada de Matemática do Oeste Catarinense - UFFS / {{edicao-atual.edicao}}:</h5>
                <a class="link2" href="{{site.url}}/documents/inscricoes/{{edicao-atual.edicao}}/{{edicao-atual.oficio-circular-inscricoes}}" target="_blank">
                {{site.data.icons.pdf-document}}
                {{site.data.icons.download}} Fazer download (.pdf)</a>
                <br><br>
                <h5>Formulário de inscrição das escolas para {{edicao-atual.edicao}}:</h5>
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
        <h1><strong>Calendário {{calendario-atual.ano-edicao}}</strong></h1>
      </div>
      <!--card -->
      {% for evento in calendario-atual.eventos %}
        {%if evento.fechamento.data %}
          {% assign dataev = evento.fechamento %}
        {% else %}
          {% assign dataev = evento.abertura %}
        {%endif%}
      <div class="row" style="border-bottom: 2px solid #613970;">
        <div class="col-12 text-center date-nums" style="margin-top:5px;">
          <h3 class="text-uppercase"><strong>{{evento.evento}}</strong></h3>
          <span class="badge" style="background-color: #613970; ">
            {% if evento.fechamento.data and evento.abertura.data %}
              <h5> De: </h5>
              <h1>{{evento.abertura.data | date: "%d" }}</h1> 
              <h4>{{evento.abertura.data | date: "/%m/%Y" }}</h4>
              <h5> Até: </h5>
              <h1>{{evento.fechamento.data | date: "%d" }}</h1>
              <h4>{{evento.fechamento.data | date: "/%m/%Y" }}</h4>
            {% else %}
              <h1>{{evento.abertura.data | date: "%d" }}</h1> 
              <h4>{{evento.abertura.data | date: "/%m/%Y" }}</h4>
            {% endif %}
          </span>
        </div>
        <div class="col-12 justify-content-center align-items-center">
          <ul class="list-inline">
            {% if evento.fechamento.data and evento.abertura.data %}
            {% elsif evento.abertura.data %}
              {% if evento.abertura.dia-da-semana %}
                <li class="list-inline-item">{{site.data.icons.calendario}}
                    {{ evento.abertura.dia-da-semana | truncate: 3, ""}}
                </li>
              {% endif %}
              {% if evento.abertura.horario %}
                <li class="list-inline-item">{{site.data.icons.relogio}}
                    {{ evento.abertura.horario }}                 
                </li>
              {% endif %}
            {% else %}
              {% if evento.fechamento.dia-da-semana %}
                <li class="list-inline-item">{{site.data.icons.calendario}}
                    {{ evento.fechamento.dia-da-semana | truncate: 3, ""}}
                </li>
              {% endif %}
              {% if evento.fechamento.horario %}
                <li class="list-inline-item">{{site.data.icons.relogio}}
                    {{ evento.fechamento.horario }}                 
                </li>
              {% endif %}
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
