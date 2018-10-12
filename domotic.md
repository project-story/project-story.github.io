---
layout: category
title: Domotique
description: |
    Controle de luminaire, de store, ... , la commande à distance d'équipement. 
    La domotique associe les techniques de l'électronique, de physique du bâtiment, 
    d'automatisme, de l'informatique et des télécommunications utilisées dans les 
    bâtiments, plus ou moins « interopérables » et permettant de centraliser le 
    contrôle des différents systèmes et sous-systèmes de la maison et de l'entreprise.
order: 7
---

{% assign nbArticle = 0 %}

{% if site.categories.domotic == null %}
<div class="row"> Aucun projet disponible! </div>
{% else %}
<div class="row">
{% for post in site.categories.domotic %}
<div class="col m6 s12">
<div class="card white">
<div class="card-content grey-text text-darken-2">
<span class="card-title"> {{ post.title }} </span>
<div class="row">
<div class="project-h">Mots clés</div> 
<div>
<!-- keywords -->
{% for keyword in post.tags %}
<span class="keyword"> {{ keyword }} </span>
{% endfor %}
</div>
<div class="project-h">Auteur(s)</div>
<div>
<!-- authors name -->
{% for author in post.authors %}
<span class="author"> {{ author }} </span>, 
{% endfor %}
</div>
</div>
<div class="card-action">
<a href="#" class="grey-text darken-3">lire</a>
<a href="/downloads/{{ post.download }}" class="grey-text darken-3">télécharger</a>
</div>
</div>
</div>
</div>
    {% endfor %}
</div>
{% endif %}


