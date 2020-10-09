{% assign sorted_pages = site.pages | sort:"projectyear" %}
{% assign allyears = "2027,2026,2025,2024,2023,2022,2021,2020,2019,2018,2017,2016,2015,2014,2013,2012" | split: "," %}
<div class="item">
{% for year in allyears %}
  {% for page in sorted_pages %}
    {% if page.projectyear==year %}
      {% if page.categories contains 'project' %}
        <h3><a href="{{ page.url | relative_url }}">{{ page.title }}</a></h3>
        <p>{{page.description}}</p>  
      {% endif %}
    {% endif %}
  {% endfor %}
 {% endfor %}
</div>