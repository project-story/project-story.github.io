---
layout: category
title: Systèmes embarqués
description: |
    un système électronique et informatique autonome, souvent temps réel, spécialisé dans une tâche bien précise.
order: 5
---

{% assign nbArticle = 0 %}

{% if site.categories.embed == null %}
<div class="row"> Aucun projet disponible! </div>
{% else %}
<div class="row">
{% for post in site.categories.embed %}
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
<div class="project-h">Preview</div>
{% for snapshot in post.snapshot %}
<div class="col l6 m6 s12">
    <img class="responsive-img" src="/images/{{ snapshot }}" />
</div>
{% endfor %}
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


