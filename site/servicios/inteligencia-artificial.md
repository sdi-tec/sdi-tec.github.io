---
layout: default
title: Análisis de Datos e Inteligencia Artificial
permalink: /servicios/inteligencia-artificial/
data_file: inteligencia-artificial
---
{% assign currentData = site.data[page.data_file] %}
{% include hero.html hero=currentData.hero %}
{% include components/services-cards.html data=currentData %}
{% include components/table.html data=currentData %}