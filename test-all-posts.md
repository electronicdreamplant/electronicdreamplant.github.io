---
layout: main
title: Test All Posts
permalink: /test-all-posts/
---
<div class="page-header">
  <h1>All blog posts (Test)</h1>
</div>

<div>
  {% assign all_content = site.posts | concat: site.projects %}
  {% assign sorted_posts = all_content | sort: "date" | reverse %}

  {% assign years = "" %}
  <ul>
    {% for post in sorted_posts %}
      {% capture year %}{{ post.date | date: "%Y" }}{% endcapture %}
      {% if year != years %}
        {% unless forloop.first %}</ul>{% endunless %}
        <h2>{{ year }}</h2>
        <ul>
        {% assign years = year %}
      {% endif %}

      <li>
        <a href="{{ post.url }}">{{ post.title }}</a> -
        <span>{{ post.date | date: "%-d %B" }}</span>

        <span> in
          {% comment %} Display existing tags if they exist {% endcomment %}
          {% for tag in post.tags %}
            <a href="/tags/{{ tag }}/">{{ tag }}</a>{% if forloop.last == false %}, {% endif %}
          {% endfor %}

          {% comment %} If it's a project, append the 'projects' tag {% endcomment %}
          {% if post.collection == "projects" %}
            {% if post.tags.size > 0 %}, {% endif %}
            <a href="/projects/">projects</a>
          {% endif %}
        </span>
      </li>
    {% endfor %}
  </ul>
</div>
