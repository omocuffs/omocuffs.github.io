---
layout: sobre
title: "Sobre a OMOC"
permalink: /sobre-a-omoc/
---
{% assign edicoes = site.data.edicoes-omoc | sort: "edicao" | reverse %}
{% assign edicao-atual = edicoes[0]%}

<div id="sobre"></div>

# Sobre a Olimpíada de Matemática ​do Oeste Catarinense (OMOC)

<br>
&nbsp;&nbsp;&nbsp;
Ocorrerá em **{{edicao-atual.edicao}}** a **{{edicao-atual.numero}}** Olimpíada de Matemática do Oeste Catarinense (OMOC), promovida pela UNIVERSIDADE FEDERAL DA FRONTEIRA SUL (UFFS), campus Chapecó. A realização desta olimpíada é o resultado de um esforço conjunto das escolas (diretores, coordenadores, professores de Matemática e alunos), da Comissão Regional da UFFS, dentre outros. Qualquer escola pública ou privada pode participar.

&nbsp;&nbsp;&nbsp;
A Olimpíada de Matemática do Oeste Catarinense será realizada em duas fases e constará de questões objetivas, (na primeira fase) e discursivas (na segunda fase). 


<div id="objetivos"></div>

#### Objetivos da OMOC: 

&nbsp;&nbsp;&nbsp;
​A Olimpíada de Matemática do Oeste Catarinense (OMOC) tem como objetivos principais **estimular o estudo da Matemática** pelos estudantes, colocar os professores do ensino fundamental e médio em contato com **novas ideias do ensino da Matemática**, influenciar na melhoria do ensino de Matemática e **detectar jovens talentos**.

<div id="niveis"></div>

#### Níveis de Participação:

&nbsp;&nbsp;&nbsp;
A Olimpíada de Matemática do Oeste Catarinense (OMOC) é realizada anualmente em **três níveis**, de acordo com a escolaridade do aluno: 

<section>
    {% if edicao-atual.niveis-de-participacao %}
    <div class="container col-12 col-sm-8">
        <br>
        <dl class="row">
            <hr/>
            {% for nivel in edicao-atual.niveis-de-participacao %}
            <dt class="col-sm-3">{{ nivel.nivel | markdownify }}</dt>
            <dd class="col-sm-9">
            {{ nivel.descricao | markdownify }}
            </dd>
            <hr/>
            {% endfor %}
        </dl>  
    </div>
    {% endif %}
</section>

<div id="criterios"></div>

#### Critérios de classificação para a segunda fase:
&nbsp;&nbsp;&nbsp;
Os alunos que atingirem no mínimo 60 pontos serão classificados para a segunda fase

&nbsp;&nbsp;&nbsp;
**OBS**: ​As provas da primeira fase devem ser corrigidas pelo professor responsável pela olimpíada na escola.