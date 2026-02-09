---
layout: tag_page
title: Projects
permalink: /tags/projects/
---
<div class="page-header">
  <h1>Projects</h1>
</div>

<ul>
{% assign project_posts = site.posts | where_exp: "item", "item.tags contains 'projects'" %}
{% for post in project_posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%-d %B %Y" }}
  </li>
{% endfor %}
</ul>
