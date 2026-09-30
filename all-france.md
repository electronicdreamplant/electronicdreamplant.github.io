---
layout: main
title: France
permalink: /france/
---

<div class="page-header">
  <h1>Moving to France</h1>
</div>

<div class="featured-timeline">
  <h3><a href="/france/timeline/">France: Our Journey Timeline</a></h3>
  <p>
    A current timeline of our progress and key milestones.
  </p>
</div>

<h2>Blog Posts</h2>

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
