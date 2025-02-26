---
layout: default
title: Ciberseguridad y Administración de Sistemas
permalink: /admin-sistemas/
data_file: sys
---
{% assign currentData = site.data[page.data_file] %}
{% include hero.html hero=currentData.hero %}
{% include components/services-cards.html data=currentData %}
{% include components/table.html data=currentData %}