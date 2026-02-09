---
layout: tag_page
tag: projects
permalink: /tags/projects/
---
<h1>Projects</h1>
<ul>
{% assign project_posts = site.posts | where_exp: "item", "item.tags contains 'projects'" %}
{% for post in project_posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%-d %B %Y" }}
    {% if post.description %}
      <br/>{{ post.description }}
    {% endif %}
  </li>
{% endfor %}
</ul>
