---
layout: projects
title: Website restructure 
date: 2024-06-17
description: Updating the website to insource blog posts and its improve presentation
---
It's been spring clean time for the website after deciding I needed to improve the presentation and get rid of some of the uglier HTML hacks I'd used when first put together.

Changing jobs made me realise that new colleagues may be looking at who this new guy coming in was and what he's been up to. Key things I wanted to do were:
* in-source all my blog posts from the various locations they were posted in to have a single resource of the things I've written
* drop the clunky presentation of the index and projects page to create a more cohesive approach
* utilise what Jekyll can do in terms of posts and tagging

## In-sourcing the blog posts
Originally I'd thought about blogging directly on the site in 2016 when I put it together, but it was a little ahead of having anything to write. So that really just stalled.

Meantime, while at Oxford City Council I decided I wanted to use GitHub Pages for a local blog site for my team's work. Those were separated from personal blog posts which were made on Medium, which later became where I started work-related weeknotes. To top it all I had a completely separate GitHub Pages site for a project where I posted too. In all they were in five different locations. 

The shift was an entirely manual process, copying and pasting HTML. I used the [HTML to Markdown converter on CodeBeautify](https://codebeautify.org/html-to-markdown) to strip out all the unnecessary markup and do some of the conversion to markdown for me, but it still needed some manual work too. 

## Organising the content
While bringing the different sources together I wanted to keep them in distinct collections, so used tags for this as part of the Frontmatter. Each post had to have this manually added to ensure consistency.

New layout pages were created for: 
* individual posts, to display the frontmatter data and the content
* tag pages, grouped by year and create an ordered list for each of the sources
* an 'all tags' page, creating a single list of all blog posts (for the first time ever) grouped by year


