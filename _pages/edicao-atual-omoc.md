---
layout: default
title: "Calendário OMOC"
permalink: /edicao-atual-omoc/
---
{% assign calendarios = site.data.calendario | sort: "ano-edicao" | reverse %}
{% assign calendario-atual = calendarios[0]%}

{% assign edicoes = site.data.edicoes-omoc | sort: "edicao" | reverse %}
{% assign edicao-atual = edicoes[0]%}

<style>
    .ancor-link {color: #613970; padding: 5px;}
    .ancor-link:hover {border-radius: 3px; color: #fff; background-color: #613970;  text-decoration: none;}
    .ancor-link-title { padding: 7px; background-color: #613970; color: #fff;}
    h2 {color: #613970; font-weight: bold;}
</style>

<div class="container-xxl justify-content-center text-center" >
    <br><br>
    <div class="row">
        <div class="col-lg-2 text-left ">
            <div class="sticky-top" style="top:50px;">
                <p class="ancor-link-title"><strong>Índice do Calendário:</strong></p>
                <nav id="navbar-example3" class="h-100 flex-column align-items-stretch pe-3 border-end ">
                    <nav class="nav nav-underline flex-column">
                    {% for evento in calendario-atual.eventos %}
                    <a class="ms-2 ancor-link" href="#{{evento.evento-fmt}}"><i class="fa-solid fa-circle align-middle" style="font-size: 7px; "></i> {{evento.evento}}</a>
                    {% endfor %}
                    </nav>
                </nav>
                <br><br><br>
            </div>
        </div>
        <div class="col-lg-10 text-justify " data-bs-smooth-scroll="true">
          <div class="text-center" id="sobre">
            <h1  style="color:#613970"><strong>Calendário da OMOC {{calendario-atual.ano-edicao}}</strong></h1> <br>
            <p >
                &nbsp;&nbsp;&nbsp;&nbsp;Para eventuais dúvidas, visite as <strong>informações de CONTATO</strong> na <strong>aba: <a style="color: #613970;" href="/organizacao/">Organização</a></strong>
            </p>
          </div>

            <!-- Calendario -->
            {% for evento in calendario-atual.eventos %}
                {% include calendar-item-full.html %}
            {% endfor %}
        </div>
    </div>
</div>