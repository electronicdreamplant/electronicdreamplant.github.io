---
layout: tag_page
tag: personal 
permalink: /tags/{{ page.tag | slugify }}/
---
<h1>Personal</h1>
<ul>
{% for post in site.tags.personal %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

