---
layout: main
title: All blog posts
permalink: /all-posts/
---
<div class="page-header">
<h1>All blog posts</h1>
</div>

 {% assign sorted_posts = site.posts | sort: "date" | reverse %}
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
          <span>{{ post.date | date: "%B %-d, %Y" }}</span>
          <span>
            {% for tag in post.tags %}
              {% assign tag_title = tag | split: ' ' | map: 'capitalize' | join: ' ' %}
              <a href="/tags/{{ tag | slugify }}/">{{ tag_title }}</a>{% if forloop.last == false %}, {% endif %}
            {% endfor %}
          </span>
        </li>
      {% endfor %}
    </ul>
