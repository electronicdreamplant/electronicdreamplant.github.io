---
layout: tag_page
tag: weeknotes
permalink: /tags/weeknotes/
---
<h1>Weeknotes</h1>
<ul>
{% for post in site.tags.weeknotes %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
