---
layout: page
title: "2020"
permalink: "/projects/2020/"
---
<div class="item">
  {% for page in site.pages %}
    {% if page.projectyear =='2020' %}
      {% if page.categories contains 'project' %}
        <h3><a href="{{ page.url | relative_url }}">{{ page.title }}</a></h3>
        <p>{{page.description}}</p>  
      {% endif %}
    {% endif %}
  {% endfor %}
</div>