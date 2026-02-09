---
layout: main
title: Blogs (Test)
permalink: /test-blog/
---
<div class="page-header">
<h1>Blog (Test)</h1>
</div>

[... Keep your existing topic list and search HTML here ...]

<div id="latest-posts">
  <h3>Latest Posts</h3>

  {% comment %} 1. Merge all three collections {% endcomment %}
  {% assign all_content = site.posts | concat: site.projects | concat: site.france %}

  {% comment %} 2. Sort and limit to the 10 most recent {% endcomment %}
  {% assign latest_items = all_content | sort: "date" | reverse | limit: 10 %}

  <ul>
    {% for item in latest_items %}
      <li>
        <a href="{{ item.url }}">{{ item.title }}</a> -
        <span>{{ item.date | date: "%-d %B %Y" }}</span>

        {% if item.collection == "projects" %}
          <span> in <a href="/projects/">projects</a></span>
        {% elsif item.collection == "france" %}
          <span> in <a href="/all-france/">france</a></span>
        {% elsif item.tags.size > 0 %}
          <span> in
          {% for tag in item.tags %}
            <a href="/tags/{{ tag }}/">{{ tag }}</a>{% unless forloop.last %}, {% endunless %}
          {% endfor %}
          </span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
