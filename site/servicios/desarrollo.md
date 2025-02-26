---
layout: default
title: Desarrollo
permalink: /servicios/desarrollo/
data_file: desarrollo
---
{% assign currentData = site.data[page.data_file] %}
{% include hero.html hero=currentData.hero %}
{% include components/services-cards.html data=currentData %}
{% include components/table.html data=currentData %}