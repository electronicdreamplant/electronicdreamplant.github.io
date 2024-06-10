---
layout: post
title: "Oxford's Hidden Histories"
date: 2017-07-31
tags: oxford
---

Since forming as a team we’ve had a growing list of requests to create new websites. We love doing these as they help the business, give better information to our audiences and let us practice our design skills.

With every new site we start with the same process. We use a Design Start meeting to explore the business objectives, identify the audience it is catering to and be clear about that audience’s needs. We do some listening and some challenging, and work at it until we’re all on the same page.

For our most recent site, Oxford’s Hidden Histories we had an additional challenge in that it was to be a vehicle to help raise money to redevelop the Museum of Oxford.

## The Challenge

The Museum of Oxford is looking to begin a redevelopment project to bring its old and currently unused galleries back to life as well as introduce some great new features that will benefit residents and tourists alike.

At the time we were approached, we’d already fixed our work programme for the year for creating five new sites. But talking to the Museum team we realised that there was a pressing deadline to launch the site to help work alongside the wider fundraising project.

So we said “why not?” as we like a challenge!

## The Concept

Our Museum colleagues had been really impressed by the Design Museum’s [Adopt an Object](https://designmuseum.org/adopt/move) campaign to help it raise money to move to a new site and wanted to do something similar.

We knew we couldn’t match the design of their site, but it felt like we could use some of the features of our CMS to create a database of objects that could be used for the campaign.

The site name (“Oxford’s Hidden Histories”) was chosen to reflect that we had a wealth of great objects we couldn’t display to the public due to the lack of a modern gallery. The website would give us an opportunity to put these front and centre in order to help raise support for the redevelopment project.

## The Design

It’s always useful if there is an established brand for the area we are looking at creating a site for. The Museum of Oxford already has this in an ongoing relationship with a designer to help create its strong, visual identity.

Some initial promotional materials had already been put together for the fundraising campaign, which included the Hidden Histories logo using a purple/cream colour pallete. This felt like a great place to start, so an initial design concept was put together.

The architects being used had already produced some great mock-ups of how the galleries could look, so we had a set of visual material to display as well.

## Finding the right donation platform

There are lots of potential online platforms to use for fundraising. Through making a contact in [fundraising.co.uk](https://www.fundraising.co.uk) we had a long list to go through; [CharityCheckout](https://www.charitycheckout.co.uk), [Givey](https://www.givey.com), [DONATE (National Funding Scheme)](http://www.nationalfundingscheme.org), [LocalGiving](https://localgiving.org), [Kindlink](https://www.kindlink.com) and [Wonderful](https://wonderful.org).

Our challenge was that we needed something that could support a normal donation approach as well as something that would work for our Adopt an Object; a one-off donation linked to a particular item. We also wanted to maximise the income for the fundraising so didn’t want to use a costly option.

The partner we chose in the end was [Golden Giving](www.goldengiving.com) who were absolutely brilliant to work with. They provide APIs that can be integrated with client websites, as well as a set of widgets that can be embedded. We went with using their Donate form widget, a widget for listing the most recent donations and a donation total widget (one of the business needs we weren’t sure how to satisfy previously).

We threw the challenge of Adopt an Object at Golden Giving and they came up with the solution; create an Appeal for each object and use tagging to identify the object for when the donation was received. Each has an unique URL which we then encoded into the call to action for ‘Adopt this object’.

But Golden Giving didn’t just stop there. They themed our campaign site to match our website styling. They also troubleshooted initial problems with matching donations to adopted objects (we’d messed up our tagging).

## Creating ‘Adopt an Object’

With the rest of the site well under way we needed to make sure we could make the Adopt an Object database work in the way it was needed. We used a set of user stories to help identify what the key requirements were. These boiled down to;

*   being able to show a complete list of objects
*   ensuring we made it easy to just see those objects still available to adopt
*   being able to differentiate available objects by price
*   displaying each object to encourage adoption, but also include information on people who had adopted them (i.e. if they had adopted an object as a gift for someone else)
*   creating an interface that Museum staff could easily update as objects moved from being ‘available’ to ‘adopted’

To create a good user journey we had to hack the standard templates for our sub-sites by removing unnecessary elements in the standard breadcrumb structure and create a back button. We used hidden fields and the keyword search functionality to create the different lists of objects needed (available, adopted, by price band). We also had to wrestle the standard styling to improve on the out-of-the-box table structure.

## Doing the legwork

Every project needs a hero, and ours came in the form of Ruby; an Oxford Uni student working as an intern for us during the holidays.

Ruby had the unenviable task of creating the database of 60 objects, all with descriptions, photographs and URLs to the Golden Giving platform. With just hours to go before the end of her time with us she had uploaded the last records ready for Go Live.

## What we learned

Working on this site has been a great learning experience for us. We learned that:

*   Start where you are and use what you have - not having the best tech is no excuse
*   Be bold - changing standard templates helped us create a better user experience
*   Choose your partners well. We got it right with Golden Giving - none of the other platforms responded to our questions or requests for help
*   Use projects to extend your skills and knowledge. The next one will be easier as a result
