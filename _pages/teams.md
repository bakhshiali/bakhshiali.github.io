---
title: "Teams"
layout: gridlay
excerpt: "Teams"
permalink: /teams/
---

<h1 style="text-align: center">Teams</h1>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>

<h2 style="text-align: center">Biomedical Chapters</h2>
{%for member in site.data.teams.book %}
<div class="grid__team">
<div class="grid__box" style="text-align: center">
  <img src="{{member.photo}}" width="50%" />
  <h3 width="50%">{{ member.name }}</h3>
  <i>{{ member.info }}</i>
</div>
</div>
{% endfor %}

Outcomes : 2 ACS, 6 Elsevier and 1 Taylor and Francis

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>

<h2 style="text-align: center">CPNB</h2>
{%for member in site.data.teams.CPNB %}
<div class="grid__team">
<div class="grid__box" style="text-align: center">
  <img src="{{member.photo}}" width="50%" />
  <h3 width="50%">{{ member.name }}</h3>
  <i>{{ member.info }}</i>
</div>
</div>
{% endfor %}
Outcomes : 1 silver medal (IFIA, Switzerland) and 1 invention
<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>

<h2 style="text-align: center">Plasma</h2>

{%for member in site.data.teams.plasma %}
<div class="grid__team">
<div class="grid__box" style="text-align: center">
  <img src="{{member.photo}}" width="50%" />
  <h3 width="50%">{{ member.name }}</h3>
  <i>{{ member.info }}</i>
</div>
</div>
{% endfor %}
Outcomes : 1 <a href="https://github.com/bakhshiali/PeSuT">VLC translation plugin</a>, 1 conference paper and 1 Invention
<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

<h2 style="text-align: center">Chitin and Chitosan</h2>
{%for member in site.data.teams.chitin %}
<div class="grid__team">
<div class="grid__box" style="text-align: center">
  <img src="{{member.photo}}" width="50%" />
  <h3 width="50%">{{ member.name }}</h3>
  <i>{{ member.info }}</i>
</div>
</div>
{% endfor %}
Outcomes : 1 <a href="https://bakhshiali.github.io/patent/3">patent</a> and 1 translated book
<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

<h2 style="text-align: center">Nanofiber</h2>
{%for member in site.data.teams.nanofiber %}
<div class="grid__team">
<div class="grid__box" style="text-align: center">
  <img src="{{member.photo}}" width="50%" />
  <h3 width="50%">{{ member.name }}</h3>
  <i>{{ member.info }}</i>
</div>
</div>
{% endfor %}   
Outcomes : 1  <a href="https://bakhshiali.github.io/patent/2">patent</a> and 1 <a href="https://www.researchgate.net/publication/373648994_Silver_medal_of_the_International_Invention_and_Innovation_Competition_2022_Switzerland_Geneva">silver medal</a> (IFIA, Switzerland)

