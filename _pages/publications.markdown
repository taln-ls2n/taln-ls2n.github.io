---
layout: page
title: Publications
permalink: publications.html
---

<ul>
{% assign article_by_year = site.data.hal | group_by: "producedDateY_i" %}
{% for year in article_by_year %}
  <h2>{{ year.name }}</h2>
  {% for article in year.items %}
    {% assign authors = article["authFullName_s"] | split: "," %}
    {% assign title = article["title_s"] %}
    {% assign paper_url = article["uri_s"] %}
    
    <li>{{ authors | join: ", " }}.
        {{ article["producedDate_s"]| slice: 0, 4 }}.
        <a href="{{paper_url}}">{{ title }}</a>.
        <i>{{ article["journalTitle_s"] }}{{ article["conferenceTitle_s"] }}</i>.      
    </li>

  {% endfor %}
{% endfor %}
</ul>
