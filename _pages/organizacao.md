---
layout: "default"
title: "Organização da OMOC"
permalink: /organizacao/
---
<div class="container-xxl"  data-bs-smooth-scroll="true" >
    <br><br>
    <h1 class="text-center" style="color:#613970"><strong>Organização da Olimpíada de Matemática do Oeste Catarinense</strong></h1> <br>
    <div class="container col-10 col-sm-6 text-center">
        <p>
        Para quaisquer <strong>dúvidas</strong> e <strong>esclarecimentos</strong>, entre em contato conosco:
        </p>
        <dl class="row text-left">
        {% if site.data.contato.email %}
        <dt class="col-sm-1"><i class="fa-solid fa-envelope"></i> </dt>
            <dd class="col-sm-8">
            {{ site.data.contato.email }}
            </dd>
            <hr/>
        {% endif %}
        {% if site.data.contato.telefones %}
        <dt class="col-sm-1">{{ site.data.icons.telefone }} </dt>
        {% for telefone in site.data.contato.telefones %}
            {% if telefone.numero %}
            {% if forloop.index > 1%} <dt class="col-sm-1"></dt> {%endif%}
            <dd class="col-sm-8">
            {{ telefone.numero }}, falar com {{ telefone.responsavel }}
            </dd>
            {% endif %}
        {% endfor %}
        <hr/>
        {% endif %}
        {% if site.data.contato.endereco %}
        <dt class="col-sm-1">{{ site.data.icons.localizacao }} </dt>
            <dd class="col-sm-8">
                {{ site.data.contato.endereco.uni }}<br>
                {{ site.data.contato.endereco.responsavel }}<br>
                {{ site.data.contato.endereco.campus }}<br>
                {{ site.data.contato.endereco.logradouro }}<br>
                CEP {{ site.data.contato.endereco.cep }}<br>
            </dd>
        {% endif %}
        </dl> 
    </div>
    <div>
        <p >
        &nbsp;&nbsp;&nbsp;&nbsp;Nomes e contato das pessoas que fazem parte da Organização da OMOC. Nesta página você poderá encontrar mais informações
        sobre elas, além de informações de contato.
        </p>
    </div>
        <br>
    <h3 style="color:#613970">Coordenadores</h3>
    <hr>
    {% assign pessoas = site.data.organizacao | where:"posicao","coordenador" %}
    {% for pessoa in pessoas %}
        {% include pessoa-grid.html %}
    {% endfor %}
    <h3 style="color:#613970">Colaboradores</h3>
    <hr>
    {% assign pessoas = site.data.organizacao | where:"posicao","colaborador" %}
    {% for pessoa in pessoas %}
        {% include pessoa-grid.html %}
    {% endfor %}
    <h3 style="color:#613970">Bolsistas</h3>
    <hr>
    {% assign pessoas = site.data.organizacao | where:"posicao","bolsista" %}
    {% for pessoa in pessoas %}
        {% include pessoa-grid.html %}
    {% endfor %}
    <h3 style="color:#613970">Estagiários</h3>
    <hr>
    {% assign pessoas = site.data.organizacao | where:"posicao","estagiario" %}
    {% for pessoa in pessoas %}
        {% include pessoa-grid.html %}
    {% endfor %}
</div>