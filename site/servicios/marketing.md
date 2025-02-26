---
layout: default
title: Marketing
permalink: /servicios/marketing/
data_file: marketing
---
{% assign currentData = site.data[page.data_file] %}
{% include hero.html hero=currentData.hero %}
{% include components/services-cards.html data=currentData %}
{% include components/table.html data=currentData %}