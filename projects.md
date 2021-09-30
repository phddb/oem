---
layout: page
title: pages.projects
namespace: projects
permalink: "/projects/"
---


{% assign sorted_pages = site.pages | sort:"projectyear" %}
{% assign allyears = "2020,2019,2018,2017,2016,2015,2014,2013,2012" | split: "," %}
<div class="item">


{% for year in allyears %}

    <h3 style="color: #566a90; margin-left: -1rem; margin-bottom: 1.5rem">{{year}}</h3>
    <ul style="list-style-type: none; padding: 0; margin-bottom: 4rem">

    {% for page in sorted_pages %}
      {% if page.projectyear==year %}
        {% if page.categories contains 'project' %}
          <li>
            <h3><a href="{{ page.url | relative_url }}">{{ page.title }}</a></h3>
            <p>{{page.description}}</p>  
          </li>
        {% endif %}
      {% endif %}
    {% endfor %}
     </ul>

{% endfor %}

</div>

