---
layout: main
title: France
permalink: /france/
---

<div class="page-header">
  <h1>France Posts</h1>
</div>
<div>
  {% assign sorted_france = site.france | sort: "date" | reverse %}
  {% assign years = "" %}
  <ul>
    {% for post in sorted_france %}
      {% capture year %}{{ post.date | date: "%Y" }}{% endcapture %}
      {% if year != years %}
        {% if forloop.index > 1 %}</ul>{% endif %}
        <h2>{{ year }}</h2>
        <ul>
        {% assign years = year %}
      {% endif %}
      <li>
        <p>
          <a href="{{ post.url }}">{{ post.title }}</a> -
          <span>{{ post.date | date: "%-d %B" }}</span>
        <br/>
        {% if post.description %}
          {{ post.description }}
        {% endif %}
        </p>
      </li>
    {% endfor %}
  </ul>
