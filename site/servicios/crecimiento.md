---
layout: default
title: Servicios Especializados y Nichos en Crecimiento
permalink: /servicios/nicho-crecimiento/
data_file: crecimiento
---
{% assign currentData = site.data[page.data_file] %}
{% include hero.html hero=currentData.hero %}
{% include components/services-cards.html data=currentData %}
{% include components/table.html data=currentData %}