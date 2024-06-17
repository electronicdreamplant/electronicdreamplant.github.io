---
layout: main
title: Projects
permalink: /projects-new/
---
<div class="page-header">
<h1>Projects</h1>
</div>
<div>
 {% assign sorted_projects = site.projects | sort: "date" | reverse %}
    {% assign years = "" %}
    <ul>
      {% for project in sorted_projects %}
        {% capture year %}{{ project.date | date: "%Y" }}{% endcapture %}
        {% if year != years %}
          {% unless forloop.first %}</ul>{% endunless %}
          <h2>{{ year }}</h2>
          <ul>
          {% assign years = year %}
        {% endif %}
        <li>
          <a href="{{ project.url }}">{{ project.title }}</a> - 
          <span>{{ project.date | date: "%-d %B" }}</span>
          <p>{{ project.description }}</p>
           {% if forloop.last == false %}, {% endif %}
            {% endfor %}
          </span>
        </li>
      {% endfor %}
    </ul>
</div>
