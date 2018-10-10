---
layout: category
title: Electronique automobile
description: La majorité des véhicules qui sont produits de jours intègre de l'électronique afin d'assurer un meilleur confort pour l'utilisateur.
order: 3
---
{% if site.categories.automobile-electronic == null %}
  <div class="row ">Aucun projet disponible.</div>
{% else %}
  {% for post in site.categories.automobile-electronic %}
  <div class="row">
    <a href="{{ post.url }}">
      {{ post.title }}
    </a>
  </div>
  {% endfor %}
{% endif %}
