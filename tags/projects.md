---
layout: tag_page
tag: projects
permalink: /tags/chatbots/
---
<h1>Projects</h1>
<ul>
{% for post in site.tags.projects %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  <br/>
  {% if project.description %}
{{ project.description }}
{% endfor %}
</ul>
