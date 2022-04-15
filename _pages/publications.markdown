---
layout: page
title: Publications
permalink: /Publications/
---

<ul>
{% for article in site.data.hal %}

  {% assign authors = article["authFullName_s"] | split: "," %}
  {% assign title = article["title_s"] %}
  {% assign paper_url = article["uri_s"] %}
  
  <li>{{ authors | join: ", " }}.
      {{ article["producedDate_s"]| slice: 0, 4 }}.
      <a href="{{paper_url}}">{{ title }}</a>.
      <i>{{ article["journalTitle_s"]] }}{{ article["conferenceTitle_s"]] }}</i>.      
  </li>

{% endfor %}
</ul>
