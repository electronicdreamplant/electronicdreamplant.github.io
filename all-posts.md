---
layout: main
title: All blog posts
permalink: /all-posts/
---
<div class="page-header">
<h1>All blog posts</h1>
</div>
<div>
  {% assign main_posts = site.posts %}
  {% assign france_posts = site.france %}
  {% assign all_combined = main_posts | concat: france_posts %}
  {% assign sorted_posts = all_combined | sort: "date" | reverse %}
  {% assign years = "" %}

  {% for post in sorted_posts %}
    {% capture year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% if year != years %}
      {% unless forloop.first %}</ul>{% endunless %}
      <h3>{{ year }}</h3>
      <ul>
      {% assign years = year %}
    {% endif %}

    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%-d %B" }} in

      {% if post.collection == "france" %}
        <a href="/france/">france</a>
      {% else %}
        {% for tag in post.tags %}
          {% assign tag_title = tag %}
          <a href="/tags/{{ tag | slugify }}/">{{ tag_title }}</a>{% unless forloop.last %}, {% endunless %}
        {% endfor %}
      {% endif %}
    </li>
  {% endfor %}
  </ul>
