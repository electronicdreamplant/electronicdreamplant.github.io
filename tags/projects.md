---
layout: tag_page
tag: projects
permalink: /tags/projects/
---
<h1>Projects</h1>
<ul>
{% for post in site.tags.projects %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    {% if post.description %}
      <br/>{{ post.description }}
    {% endif %}
  </li>
{% endfor %}
</ul>
