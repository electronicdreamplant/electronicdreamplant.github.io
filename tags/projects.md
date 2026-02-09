---
layout: tag_page
title: Projects
permalink: /tags/projects/
---

<h1>Projects</h1>
<ul>
{% for post in site.tags.projects %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
