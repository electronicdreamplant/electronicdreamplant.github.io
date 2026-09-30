---
layout: main
title: France
permalink: /france/
---

<div class="page-header">
  <h1>Moving to France</h1>
</div>

<div class="form-group" style="padding-top: 1.5rem;">
  <h3>
    <label for="followit-email">Subscribe to France updates</label>
  </h3>
  <span id="followit-hint" class="form-hint">
    Get an automatic email whenever a new post about France is published.
  </span>

  <form action="https://api.follow.it/subscription-form/dmlpaDNwMWVJbm56dGhxb0dDUDRwTWJEc3NIK0M3MStUdU9MYkpRcG16VEZkdG8yWnRaaHVIOHVBZm9udngxUEgyVWp3REZicWs5R1g2ZUtEc0F0RkVQdm5wUGh5OGl1V0NldUZGQUQ5MzVORS9sVkMxcTUvUW9MUkhBNDAyZkl8RE96djNTQWNiMGtmU1FKOGdzc3hGZEtYY3h6YkZ4Q05LWURha0dpa0xWRT0=/8" method="post" style="margin-top: 0.75rem;">
    <input class="form-control" type="email" id="followit-email" name="email" spellcheck="false" aria-describedby="followit-hint" placeholder="you@example.com" required style="margin-bottom: 0.75rem;">
    <button type="submit" class="submit-btn">Subscribe</button>
  </form>
</div>

<div class="featured-timeline">
  <h3><a href="/france/timeline/">France: Our Journey Timeline</a></h3>
  <p>
    A current timeline of our progress and key milestones.
  </p>
</div>

<h2>Blog Posts</h2>

<div>
  {% assign sorted_france = site.france | sort: "date" | reverse %}
  {% assign years = "" %}
  <ul>
    {% for post in sorted_france %}
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
