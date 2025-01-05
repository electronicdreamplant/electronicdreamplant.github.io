---
layout: main
title: Portugal
permalink: /portugal/
---
<div class="page-header">
  <h1>Portugal Posts</h1>
</div>
<div>
  {% assign sorted_portugal = site.portugal | sort: "date" | reverse %}
  {% assign years = "" %}
  <ul>
    {% for post in sorted_portugal %}
      {% capture year %}{{ post.date | date: "%Y" }}{% endcapture %}
      {% if year != years %}
        {% if forloop.index > 1 %}</ul>{% endif %}
        <h2>{{ year }}</h2>
        <ul>
        {% assign years = year %}
      {% endif %}
      <li>
        <p>
          <a href="{{ post.url }}">{{ post.title }}</a>
        <br/>
        {% if post.description %}
          {{ post.description }}
        {% endif %}
        </p>
      </li>
    {% endfor %}
  </ul>
