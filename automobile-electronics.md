---
layout: category
title: Electronique automobile
description: La majorité des véhicules qui sont produits de jours intègre de l'électronique afin d'assurer un meilleur confort pour l'utilisateur.
pagination:
    enable: true
    category: automobile
order: 3
---

{% if site.categories.automobile == null %}
<div class="row"> Aucun projet disponible! </div>
{% else %}
<div class="row">
{% for post in paginator.posts %}
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
<a href="#" class="grey-text darken-3">télécharger</a>
</div>
</div>
</div>
</div>
    {% endfor %}
</div>
{% endif %}


