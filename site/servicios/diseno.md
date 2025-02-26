---
layout: default
title: Diseño y Multimedia
permalink: /servicios/diseno-multimedia/
data_file: diseno
---
{% assign currentData = site.data[page.data_file] %}
{% include hero.html hero=currentData.hero %}
{% include components/services-cards.html data=currentData %}
{% include components/table.html data=currentData %}