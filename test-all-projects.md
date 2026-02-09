---
layout: main
title: Projects
permalink: /projects/
---
<div class="page-header">
  <h1>Projects</h1>
</div>
<div>
  {% assign project_posts = site.posts | where_exp: "item", "item.tags contains 'projects'" | sort: "date" | reverse %}
  {% assign years = "" %}
  {% for project in project_posts %}
    {% capture year %}{{ project.date | date: "%Y" }}{% endcapture %}
    {% if year != years %}
      {% unless forloop.first %}</ul>{% endunless %}
      <h2>{{ year }}</h2>
      <ul>
      {% assign years = year %}
    {% endif %}
    <li>
      <p>
        <a href="{{ project.url }}">{{ project.title }}</a>
        <br/>
        {% if project.description %}{{ project.description }}{% endif %}
      </p>
    </li>
  {% endfor %}
  </ul>
</div>
