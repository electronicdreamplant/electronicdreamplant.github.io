---
layout: projects
title: Website restructure 
date: 2024-06-17
description: Updating the website to insource blog posts and improve presentation
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
Previously, the Blog page on the site was a hack, bringing in a blogroll from Medium, running the rss feed through [rsstojson](https://rss2json.com/) to show the posts better (but not that well). No use now that Medium wasn't being used, so it needed to go.  

In bringing the different sources together I wanted to keep them in their distinct collections, so used tags for this as part of the post frontmatter. Each post had to have this metadata manually created to ensure consistency.

New layout pages were created for: 
* individual posts, to display the frontmatter data and the content
* tag pages, grouped by year and create an ordered list for each of the sources
* an 'all tags' page, creating a single list of all blog posts (for the first time ever) grouped by year

A final polish was to create an _includes file to fetch the latest 3 posts and add them at the foot of the new Blogs page.

## Adding search 
As I hadn't included a description or excerpt for each post , I wanted a way to be able to find a particular post. I'd tried to use [Tipue search](https://github.com/jekylltools/jekyll-tipue-search) but this had been archived 7 years ago and I couldn't get it to work due to clashing Jquery versions. With a bit of help from someone clever, I switched to [Simple Search](https://github.com/christian-fei/Simple-Jekyll-Search) (which is also archived!).

After a bit of wrangling it started spitting out results, but was only searching titles and tags. I updated this to bring in content too, then spent a little too long validating JSON in order to get that to work.

In truth, it's really not that good and I'll need to look at something better that allows for multi-word searches and displays the search terms in context. It will do for now.

## Changing the Projects page
The original idea of the site was to try out bit of coding, or capture the odd personal project. Looking back over the content much of it didn't feel appropriate, and some projects (e.g. a live analytics dashboard for the Oxford City Council website) were no longer working or live.

The presentation stuck out like a sore thumb too compared to the new presentation of blogs, so I decided to mirror this by creating a new posts collection called 'projects',creating similar layout pages for projects, and moving them across to markdown.

For this (much smaller) set of content I've added description in the frontmatter to give a bit more info on each one in the listing as well as the post presentation. 

## Using ChatGPT
I have to say ChatGPT was pretty much indispensable for practical help. No question was too stupid, each answer was backed with a full explanation of why certain code was suggested, and this helped me to get more confident about what to do next and try out some of it solo. 
