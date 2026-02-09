---
layout: main
title: Test Specific Project Tag
permalink: /test-projects/
---
<div class="page-header">
  <h1>Projects (Tag Test)</h1>
</div>

<div>
  {% comment %} This specifically filters your BLOG posts for the 'projects' tag {% endcomment %}
  {% assign tagged_posts = site.posts | where_exp: "item", "item.tags contains 'projects'" | sort: "date" | reverse %}

  <ul>
  {% for post in tagged_posts %}
    <li>
      <p>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <br/>
        {% if post.description %}
          {{ post.description }}
        {% endif %}
      </p>
    </li>
  {% endfor %}
  </ul>
</div>
