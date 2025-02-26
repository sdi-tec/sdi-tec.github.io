---
layout: default
title: "Nuestros Servicios"
permalink: /servicios/
---

<h1>Nuestros Servicios</h1>

{% assign servicios_values = site.data.servicios | values %}
<ul>
  {% for pair in servicios_values %}
    {% assign servicio = pair[1] %}
    <li>
      {% if servicio.hero.permalink %}
        <a href="{{ servicio.hero.permalink }}">{{ servicio.hero.title }}</a>
      {% else %}
        <a href="#">{{ servicio.hero.title }}</a>
      {% endif %}
    </li>
  {% endfor %}
</ul>