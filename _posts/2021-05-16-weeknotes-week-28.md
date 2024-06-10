---
layout: post
title: "Weeknotes: week 28 - The Calm During The Storm"
date: 2021-05-16
tags: weeknotes
---

I’m told it does actually stop raining sometimes in Dorset

It’s been a wet week here, an annoying follow-up to the dry (but cold) April we had, which means we’re not yet enjoying the countryside as much as we want to. Still, the new water butts are filling up nicely, so I’ve got that going for me…

While still on the tail end (hopefully) of lockdown, with very little open, life is tending towards a work-eat-sleep-repeat cycle where weeks merge into each other and I find it harder to get engaged.

## Looking back

We did a retro on the last sprint as a team, and with Glen & JB from the ICT side. It was good to see the ‘went well’ items far outnumber the ‘didn’t go well’ items, but also to hear from others that this new platform lark was tricky and was taking time for everyone to get comfortable and really start delivering on.

This was particularly welcomed by me as I had (what I felt was) a bruising conversation the previous week about agile planning (which I’d be the first to admit I’m no expert on) that really took the wind out of my sails and left me feeling like I’d done enough self-exploration — hence no weeknotes.

When you’re in the midst of something you know is complex, and the people you’re working closely with feel is complex, it is hard to hear people on the outside take a view and see only simplicity. Still, this project is all about learning, and if I really felt I had no issues to address I’d be kidding myself.

## Digital Leaders talk

And on that subject of learning, as part of Dorset’s contribution to Digital Leader’s week, I’ll be doing a session talking about our CMS migration.

You can [book a place](https://week.digileaders.com/?sc=EsJvNxZo) if you’re interested. Shameless plug, I know, but someone did get in touch via Slack and mention they’ve been following these weeknotes about the migration, so maybe it will be of interest to others.

I really enjoyed the session I did with [Torchbox](https://medium.com/u/b5f905ef3ce3?source=post_page-----ed41c2871098--------------------------------) on the chatbot user research project we worked on, and I think having both supplier and client involved really helped. So it was great to hear that Lorna from Placecube will be joining me on the virtual stage to

I’m still not entirely sure what angle to take on this, but I do think the cultural and people side of it might be my lead, particularly after reading [rufflemuffin](https://medium.com/u/b8747643e779?source=post_page-----ed41c2871098--------------------------------)’s [Full Stack Service Design](http://sarah-drummond.com/full-stack-service-design/) during the week.

## Migration motion

We had a Show and Share last week which went OK. I focused on issues and how we’re approaching them rather than ‘doesn’t it look pretty’ as this stuff is important to reflect on. The numbers looked good though.

So, actually, we’ve achieved quite a bit really

Looking over the sprint plan this week I was struck by how we’ve become less about waiting for development work to arrive with us and more about the ancillary activities needed to make the migration a success. Planning sessions are exactly that now, focused on moving things forward and taking decisions rather than letting circumstances take charge.

It’s also been great to step back from being involved directly in everything (another annoying thing I tend to do) and let the talented people I work with shake their tail feathers.

We had a good session looking at one of our design challenges; dealing with our Traded Services pages (as [mentioned in a previous post](/blog/2021/05/01/weeknotes-week-26)). The more we talked, the more we started to focus on what was feasible to do in the time we have before launch and the likely human reaction to major changes (there’s that cultural thing again).

This also aligned nicely with a conversation with our resident ‘big brain in a cap’, Trevor our architect, around design standards. We’ve a shared ambition to get this right as it will have really positive outcomes for users, but rushing design decisions without a format or structure feels wrong. So we’re punting changes to these pages to post-launch, following our ‘As is’ approach for the rest of the project, getting our often-talked-about Design Group together (with Trevor’s help) and approaching the area with more thought than haste.

## Tightening up the Elastic(search)

While the Traded Services decision felt solid, it was nice to be proven wrong by Placecube in a decision we’d taken last week to put a hold on pushing the adoption of Elasticsearch over a tried-and-tested Cludo approach.

The thinking was that since we knew very little about Elasticsearch but much more about Cludo (implemented to rescue a previous poor implementation of Elasticsearch on our current CMS), so why take the risk given the importance of search? We also had some time on the clock with the Cludo contract so there would be no cost implication.

What we didn’t know then is how intrinsic Elasticsearch is to Liferay, so taking it out would take far more development work than we’d factored in. Placecube Dave was confident he could fix the large list of acceptance criteria our local Cludo expert (Natalie) had generated through endless hours of work to make search work, so we switched priorities to run another technical spike. Within the first day of looking at the long list he’d made huge improvements to functionality and results, meaning we were much happier about reversing our earlier decision.

Reflecting on this it struck me that we could have done a far better job in Discovery in being specific about what we needed from the functionality, but I think Placecube recognise they needed to have done more from a product perspective getting this side of things ready to explore. Hey, maybe that’s one to cover in my Digital Leader’s talk?

## Accessibility and equality

I’d been trying throughout the week to complete a couple of mandatory training modules on our online Learning Hub. I guess the benefits of ‘I can do learning at any time’ are exactly its disbenefits, as priorities are too easily switched and learning pushed back. Been doing too much of that lately.

I like how our learning modules are a mixture of fact-giving, quizzes and YouTube videos, mixing it up nicely. However, during the equality and diversity module I tried navigating through the session using just a keyboard to find that some parts wouldn’t let you do that. Oh the irony! A quick check with HR showed that this was already being discussed with the supplier, and changes coming on stream soon.

Which led nicely into a chase-up email from GDS about our accessibility audit findings. Heck, that 12 weeks just flew by! A hastily-convened meetup with Carl our Dev showed we’d actually fixed all our development items, but were struggling with two developer-related items. These had to go in the revamped accessibility statement for now.

How do you get suppliers to tow the line on this stuff? There was a good discussion in LocalGov Digital Slack this week around parking apps and where responsibility sits. TL:DR — it may be more complicated than I thought.

## And finally….

Some other things that happened this week:

*   interviews for our fixed-term Content Designer. We weren’t flooded with applicants, showing both the issues of fixed term appointments and the challenge that remote working brings to recruitment. Pleased to say we have a new starter on 7 June; Lee
*   a session on new website(s) for a school development, to be carried out by an agency, showed that we have a gap in our arsenal of how we can help services lead on these. Need to plug that one methinks
*   my paddleboard arrived on Friday! You may be asking “did that [Matt Prosser](https://medium.com/u/ba983b1e0e37?source=post_page-----ed41c2871098--------------------------------) fella come good on his promise to buy you one?” Well, dear reader, perhaps I just beat him to it….
