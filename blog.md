---
layout: main
title: Blogs
permalink: /blog/
---
<div class="page-header">
<h1>Blog</h1>
</div>

Pick a topic or [view all posts by year](/all-posts/)

## Topics
* [France](/france) - capturing our journey to living in France after stopping work
* [Weeknotes](/tags/weeknotes/) – posts about my working week, written for me but shared in the open (2020-2025)
* [Oxford City Council](/tags/oxford/) - posts as the Oxford City Digital Development Team (2016-2019)
* [Placecube](/tags/placecube/) - posts written on behalf of the company (2022-2023)
* [Chatbots](/tags/chatbots/) - posts on the Local Digital Chatbots project (2018-2019)
* [Projects](/tags/projects/) - tech projects I've worked on
* [Personal](/tags/personal/) - anything else I've written

<div class="form-group" style="margin-top: 2rem; border-top: 1px solid #ccc; padding-top: 1.5rem;">
  <h3>
    <label for="followit-email">Subscribe to France updates</label>
  </h3>
  <span class="form-hint">
    Get an automatic email whenever a new post about France is published.
  </span>

  <form action="https://follow.it/subscribe" method="post" target="_blank" style="margin-top: 0.75rem;">
    <input type="hidden" name="url" value="https://www.ox1digital.co.uk/france.xml">
    <input class="form-control" type="email" id="followit-email" name="email" placeholder="you@example.com" required style="margin-bottom: 0.75rem;">
    <button type="submit" class="submit-btn">Subscribe via Follow.it</button>
  </form>
</div>

{% include latest_post.html %}
