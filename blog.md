---
layout: main
title: Blogs
permalink: /blog/
--- 
<div class="page-header">
<h1>Blog</h1>
</div>

These posts have been pulled into the site from a number of sources:
- [Weeknotes](/tags/weeknotes/) - posts about my working week, written for me but shared in the open
- [Oxford City Council](/tags/oxford/) - posts as the Digital Development Team
- [Placecube](/tags/placecube/) - posts written on behalf of the company
- [Chatbots](/tags/chatbots/) - posts on the Local Digital Chatbots project
- [Personal](/tags/personal/) - anything else I've written
 
 
You can [view all posts by year](/all-posts/)
<div>
    <div>
         <label for="search-input">Or search for posts by keyword</label>
         <input type="search" id="search-input" placeholder=" ">

<br/><br/>
         <h3 id="search-results-title" style="display:none;">Search Results</h3>
         <ul id="results-container"></ul>

    {% include latest_post.html %}
         
    </div>

                <script>
                    window.simpleJekyllSearch = new SimpleJekyllSearch({
                        searchInput: document.getElementById('search-input'),
                        resultsContainer: document.getElementById('results-container'),
                        json: '{{ site.baseurl }}/search.json',
                        searchResultTemplate: '<li><a href="{url}?query={query}" title="{desc}">{title} [{tags}]</a> - {date}</li>',
                        noResultsText: 'No results found',
                        limit: 15,
                        fuzzy: false,
                        exclude: ['Welcome'],
                        searchFields: ['title', 'content']
                    })
    // Monitor changes in the results container
    const resultsContainer = document.getElementById('results-container');
    const resultsTitle = document.getElementById('search-results-title');

    const observer = new MutationObserver(() => {
        if (resultsContainer.children.length > 0) {
            resultsTitle.style.display = 'block';
        } else {
            resultsTitle.style.display = 'none';
        }
    });

    observer.observe(resultsContainer, { childList: true });
    
                </script>
    </div>  


