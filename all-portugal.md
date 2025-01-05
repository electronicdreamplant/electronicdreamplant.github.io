---
layout: main
title: Portugal
permalink: /portugal/
---
<span style="display: block; width: 100vw; margin-left: calc(50% - 50vw); margin-right: calc(50% - 50vw); margin-top: 25px;">
![](/img/portugal_header.jpg)
</span>

<div class="page-header">
  <h1>Portugal Posts</h1>
</div>
<div>
  {% assign sorted_portugal = site.portugal | sort: "date" | reverse %}
  {% assign years = "" %}
  <ul>
    {% for post in sorted_portugal %}
      {% capture year %}{{ post.date | date: "%Y" }}{% endcapture %}
      {% if year != years %}
        {% if forloop.index > 1 %}</ul>{% endif %}
        <h2>{{ year }}</h2>
        <ul>
        {% assign years = year %}
      {% endif %}
      <li>
        <p>
          <a href="{{ post.url }}">{{ post.title }}</a> -
          <span>{{ post.date | date: "%-d %B" }}</span>
        <br/>
        {% if post.description %}
          {{ post.description }}
        {% endif %}
        </p>
      </li>
    {% endfor %}
  </ul>
