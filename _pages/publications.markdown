---
layout: page
title: Publications
permalink: /Publications/
---

{% assign row = site.data.hal.2022-04-15[0] %}
{% for pair in row %}
  {{ pair | inspect }}
{% endfor %}
