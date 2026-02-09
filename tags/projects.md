---
layout: tag_page
tag: projects
permalink: /tags/projects/
---
<div class="page-header">
  <h1>Projects</h1>
</div>

<ul>
{% for post in site.tags.projects %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
