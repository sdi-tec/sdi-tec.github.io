---
layout: default
title: Ciberseguridad y Administración de Sistemas
permalink: /servicios/admin-sistemas/
data_file: admin-sistemas
---
{% assign currentData = site.data[page.data_file] %}
{% include hero.html hero=currentData.hero %}
{% include components/services-cards.html data=currentData %}
{% include components/table.html data=currentData %}