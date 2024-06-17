---
layout: main
title: Blogs
permalink: /blog/
--- 
<div class="page-header">
<h1>Blog</h1>
</div>
Pick a topic or [view all posts by year](/all-posts/)
- [Weeknotes](/tags/weeknotes/) - posts about my working week, written for me but shared in the open
- [Oxford City Council](/tags/oxford/) - posts as the Digital Development Team
- [Placecube](/tags/placecube/) - posts written on behalf of the company
- [Chatbots](/tags/chatbots/) - posts on the Local Digital Chatbots project
- [Personal](/tags/personal/) - anything else I've written
 
<div>
    <div>
         <label for="search-input">Search for posts by keyword</label>
         <input type="search" id="search-input" placeholder=" ">

<br/><br/>
         <h3 id="search-results-title" style="display:none;">Search Results</h3>
         <ul id="results-container"></ul>

    {% include latest_post.html %}

    {% include search_results.html %}
    

