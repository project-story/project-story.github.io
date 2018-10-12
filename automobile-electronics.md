---
layout: category
title: Electronique automobile
description: |
    Dans une automobile moderne, l’électronique et l’informatique occupent une place importante. 
    Des capteurs - éléments qui transforment une grandeur physique (une vitesse 
    de rotation, une température...) en un signal électrique - informent en permanence 
    des calculateurs sur le fonctionnement du moteur, le comportement du véhicule 
    ou les actions du conducteur.
order: 3
---

{% if site.categories.automobile == null %}
<div class="row"> Aucun projet disponible! </div>
{% else %}
<div class="row">
{% for post in site.categories.automobile %}
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
<div class="row">
<div class="h-project">Preview</div>
{% for snapshot in post.snapshot %}
<div class="col l6 m6 s12">
    <img class="responsive-img" src="/images/{{ snapshot }}" />
</div>
{% endfor %}
</div>
<div class="card-action">
<a href="{{ post.url }}" class="grey-text darken-3">lire</a>
<a href="/downloads/{{ post.download }}" class="grey-text darken-3">télécharger</a>
</div>
</div>
</div>
</div>
    {% endfor %}
</div>
{% endif %}


