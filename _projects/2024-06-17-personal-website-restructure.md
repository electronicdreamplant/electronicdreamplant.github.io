---
layout: projects
title: Personal website restructure
date: 2024-06-17
description: Updating the website to insource blog posts and improve presentation
---
It's been spring cleaning time for the website after I decided I needed to improve its presentation and get rid of some of the uglier HTML hacks I'd used when first putting it together. Changing jobs made me think about new colleagues trying to find out just who this new guy coming in is and what he's been up to. 

Key things I wanted to do were:
* in-source all my blog posts from the various locations they were posted in to have a single resource of everything I've written
* drop the clunky presentation of the index and projects page to create a more cohesive design across the site
* utilise what Jekyll and Liquid can do in terms of posts and tagging

## In-sourcing the blog posts
Back in 2016 when I put the site together, I'd thought about writing blogs directly on it, but it was a little ahead of having anything to write, so that idea stalled.

While at Oxford City Council I decided I wanted to use GitHub Pages for a local blog site for my team's work. Separate to that I'd started writing personal blog posts hosted on Medium, which later became where I started work-related weeknotes too. To top it all, I had a completely separate GitHub Pages site for a project where I posted too. In all they were in five different locations used.

The shift to insource was an entirely manual process, just copying and pasting HTML. I used the [HTML to Markdown converter on CodeBeautify](https://codebeautify.org/html-to-markdown) to strip out all the unnecessary markup and do some of the conversion to markdown for me, but it still needed manual work too.

## Organising the content
Previously, the Blog page on the site was a hack, bringing in a blogroll from Medium, running the rss feed through [rsstojson](https://rss2json.com/) to show the posts better (but not that well).

In bringing the different sources together I wanted to keep them in their distinct collections, so used tags for this as part of the post frontmatter. Each post had to have this metadata manually added to ensure consistency.

New template pages were created for:
* individual posts, to display the frontmatter data and the content
* tag pages, grouped by year and creating an ordered list for each of the sources
* an 'all tags' page, creating a single list of all blog posts (for the first time ever) grouped by year

A final polish was to create an _includes file to fetch the latest 3 posts and add them at the foot of the new Blogs page.

I had thought adding Open Graph metadata would be really difficult, but in reality it just took a few minutes. Although I couldn't make the LinkedIn 'published date' requirement happy (it turns out this isn't an OG tag anyway)

## Adding search
As I hadn't included a description or excerpt for each post, I didn't have an easy way to find a particular post. I'd tried to use [Tipue search](https://github.com/jekylltools/jekyll-tipue-search) some time back but the code had been archived 7 years ago and I couldn't get it to work due to clashing Jquery versions on the site. With a bit of help from someone clever, I switched to [Simple Search](https://github.com/christian-fei/Simple-Jekyll-Search) (which is also archived!).

After a bit of wrangling it started spitting out results, but was only searching titles and tags. I updated this to bring in content too, then spent a little too long validating JSON in order to get that to work.

In truth, it's really not that good and I'll need to look at something better that allows for multi-word searches and displays the search terms in context. It will do for now.

## Changing the Projects page
The original idea of the site was to try out bit of coding, or capture the odd personal project. Looking back over the content, much of it didn't feel appropriate any longer, and some projects (e.g. a live analytics dashboard for the Oxford City Council website) were no longer working.

The presentation stuck out like a sore thumb too compared to the new presentation of blogs, so I decided to mirror it by creating a new posts collection called 'projects',creating similar layout pages for them, and moving everything across to markdown.

For this (much smaller) set of content I've added description in the frontmatter to give a bit more info on each one in the listing as well as the post presentation.

## Updating RSS
An age ago I created an Atom feed for the posts, which had completely stopped working, but a quick addition of 'jekyll-feed' to the plugins in _config.yml, along with the feed metatdata, meant it was up and running in minutes

## Using ChatGPT
I have to say ChatGPT was pretty much indispensable for practical help. No question was too stupid, each answer was backed with a full explanation of why certain code was suggested, and this helped me to get more confident about what to do next and try out some of it solo.
