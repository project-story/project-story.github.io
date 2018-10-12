---
layout: category
title: Elevage
description: |
    Le secteur de l'élevage aussi dynamique que nous la connaisons atteindra un 
    niveau de rentabilité supérieure en y appliquant les atouts des domaines comme 
    l'électronique. Monitoring des animaux, détection précoce des 
    événements de la reproduction et des troubles de la santé des animaux, assistance 
    dans la reproduction et contrôle des naissances sont autant d'aspect qui peuvent 
    être contrôler.
order: 10
---

{% assign nbArticle = 0 %}

{% if site.categories.breeding == null %}
<div class="row"> Aucun projet disponible! </div>
{% else %}
<div class="row">
{% for post in site.categories.breeding %}
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


