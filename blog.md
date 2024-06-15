---
layout: main
title: Blogs
permalink: /blog/
--- 
<div class="page-header">
<h1>Blog</h1>
</div>

These posts have been pulled into the site from a number of sources:
- [Weeknotes](/tags/weeknotes/) - notes about my working week, written for me but shared in the open
- [Oxford City Council](/tags/oxford/) - posts as the Digital Development Team
- [Placecube](/tags/placecube/) - posts written on behalf of the company
- [Personal](/tags/personal/) - anything else I've written
- [Chatbots](https://localdigitalchatbots.github.io/archive/) - posts on the Local Digital Chatbots project
 
 
You can [view all posts by year](/all-posts/)
<div>
    <div>
         <label for="search-input">Or search for posts</label>
         <input type="search" id="search-input" placeholder=" ">

<br/><br/>
         <ul id="results-container"></ul>
    </div>

                <script>
                    window.simpleJekyllSearch = new SimpleJekyllSearch({
                        searchInput: document.getElementById('search-input'),
                        resultsContainer: document.getElementById('results-container'),
                        json: '{{ site.baseurl }}/search.json',
                        searchResultTemplate: '<li><a href="{url}?query={query}" title="{desc}">{title} [{tags}]</a></li>',
                        noResultsText: 'No results found',
                        limit: 15,
                        fuzzy: false,
                        exclude: ['Welcome'],
                        searchFields: ['title', 'content']
                    })
                </script>
    </div>  
