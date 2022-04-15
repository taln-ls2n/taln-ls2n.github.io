---
layout: page
title: Publications
permalink: /Publications/
---

# Test csv HAL v1

<table>
  <thead>
    <tr>
    {% for header in site.data.hal.keys %}
      <td>{{header}}</td>
    {% endfor %}
    </tr>
  </thead>
  <tbody>
    {% for row in site.data.hal.content %}
    <tr>
    {% for column in row %}
      <td>{{column}}</td>
    {% endfor %}
    </tr>
    {% endfor %}
  </tbody>
</table>
