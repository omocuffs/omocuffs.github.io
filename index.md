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
                <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-file-earmark-pdf-fill" viewBox="0 0 16 16">
                    <path d="M5.523 12.424c.14-.082.293-.162.459-.238a7.878 7.878 0 0 1-.45.606c-.28.337-.498.516-.635.572a.266.266 0 0 1-.035.012.282.282 0 0 1-.026-.044c-.056-.11-.054-.216.04-.36.106-.165.319-.354.647-.548zm2.455-1.647c-.119.025-.237.05-.356.078a21.148 21.148 0 0 0 .5-1.05 12.045 12.045 0 0 0 .51.858c-.217.032-.436.07-.654.114zm2.525.939a3.881 3.881 0 0 1-.435-.41c.228.005.434.022.612.054.317.057.466.147.518.209a.095.095 0 0 1 .026.064.436.436 0 0 1-.06.2.307.307 0 0 1-.094.124.107.107 0 0 1-.069.015c-.09-.003-.258-.066-.498-.256zM8.278 6.97c-.04.244-.108.524-.2.829a4.86 4.86 0 0 1-.089-.346c-.076-.353-.087-.63-.046-.822.038-.177.11-.248.196-.283a.517.517 0 0 1 .145-.04c.013.03.028.092.032.198.005.122-.007.277-.038.465z"/>
                    <path fill-rule="evenodd" d="M4 0h5.293A1 1 0 0 1 10 .293L13.707 4a1 1 0 0 1 .293.707V14a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2a2 2 0 0 1 2-2zm5.5 1.5v2a1 1 0 0 0 1 1h2l-3-3zM4.165 13.668c.09.18.23.343.438.419.207.075.412.04.58-.03.318-.13.635-.436.926-.786.333-.401.683-.927 1.021-1.51a11.651 11.651 0 0 1 1.997-.406c.3.383.61.713.91.95.28.22.603.403.934.417a.856.856 0 0 0 .51-.138c.155-.101.27-.247.354-.416.09-.181.145-.37.138-.563a.844.844 0 0 0-.2-.518c-.226-.27-.596-.4-.96-.465a5.76 5.76 0 0 0-1.335-.05 10.954 10.954 0 0 1-.98-1.686c.25-.66.437-1.284.52-1.794.036-.218.055-.426.048-.614a1.238 1.238 0 0 0-.127-.538.7.7 0 0 0-.477-.365c-.202-.043-.41 0-.601.077-.377.15-.576.47-.651.823-.073.34-.04.736.046 1.136.088.406.238.848.43 1.295a19.697 19.697 0 0 1-1.062 2.227 7.662 7.662 0 0 0-1.482.645c-.37.22-.699.48-.897.787-.21.326-.275.714-.08 1.103z"/>
                </svg>
                <i class="fa-solid fa-download"></i> Fazer download (.pdf)</a>
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
        <h1><strong>Calendário 2023</strong></h1>
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
            <li class="list-inline-item"><i class="fa fa-calendar-o" aria-hidden="true"></i>
                {{ dataev.dia-da-semana | truncate: 3, ""}}
            </li>
            {% endif %}
            {% if dataev.horario %}
            <li class="list-inline-item"><i class="fa fa-clock-o" aria-hidden="true"></i>
                {{ dataev.horario }}                 
            </li>
            {% endif %}
            {% if evento.local-realizacao %}
            <li class="list-inline-item"><i class="fa fa-location-arrow" aria-hidden="true"></i> 
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
