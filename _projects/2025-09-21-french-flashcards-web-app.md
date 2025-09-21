---
layout: projects
title: Building a French Vocab Flashcards web app
date: 2025-09-21
description: Using ChatGPT to create a web app from scratch
---

After a recent visit to France I decided it was time to actually start learning the language. After all, we had been going there for over 20 years, and my schoolboy english was showing the strain.

I took an excellent Open University intro course called [Get ready for beginners’ French](https://www.open.edu/openlearn/languages/get-ready-beginners-french/content-section-overview?active-tab=description-tab) which helped me think about my objectives and learning styles, and it had some excellent tips from existing students. One of these was using flashcards to help with vocabularly. That felt like a good tool to get set up before I dive into my full course.

## What is on the market aready
As you might expect, there are dozens of apps already out there that can do this job. Some I explored were:
* Anki
* Quizlet
* Memrise
* Reverso

[Anki](https://docs.ankiweb.net/background.html) felt like it wanted to live on Linux, and claimed it had all kinds of scripts you could download to force it to do what you want. Too complicated for me (and the scripts didn't work). 

[Reverso](https://www.reverso.net/vocabulary) started off much more promisingly, as you could search for words, add the answers to Favourites and organise the Favourites into Lists to represent different subject topics.Its flashcards were nicely laid out with pronunciation options and the word used in context. 

I thought I was home and dry, but actually using it felt less easy. There were constant prompts to take out a paid subscription, and it was scarily easy to delete your Favourites! Also, I couldn't switch from French > English to English > French easily mid-learning. So this got me thinking about trying to build something myself. 

## Getting ChatGPT on the case
The organisation I work for is really keen for everyone to make use of AI as part of daily working practice, so I'm used to falling back on ChatGPT for potential solutions and time saving approaches in my work. I've never mastered coding beyond buying books and leaving them on a shelf unread, and because my work colleagues were finding AI tools a really valuable way to accelerate development, I thought I'd try a quick prompt in my personal ChatGPT account to see what it produced;

>I'm still not sure I've found the vocab learning solution I completely like, that can adapt to how I want to record and present flashcards. I'm now wondering about a Google Sheets recording method and using you to help me create an application to present flashcards (since you're good at this coding thing) via some kind of GitHub pages setup. What do you say?

Off the bat it recommended:
* using Google Sheets to capture the data and publish it to the web
* developing a single-page app on GitHub Pages to pull in and present the data 
* using a lightweight Leitner review approach (Again/Good/Easy) to mark up cards and control how often they are shown
* using themed decks and lesson filters

This was to be the start of many more interactions.....

## Working with Google Sheets
I found this a good way to work out what kind of data I needed to capture to have the right information in the flashcards and be able to organise them around my needs. 

After a bit of experimentation I came up with:
* deck - to organise my flashcards into groups that made sense to me (Food, Family, House etc)
* lesson - as I had been using a text book, using its chapter numbers was a good way to categorise
* article - as French is preedominently gender-based, knowing if words were masculine or feminine was important
* french - the actual word I wanted to learn
* english - its English translation
* sentence - using the French word in context within a sentence
* labels - an additional categorisation method for organising presentation
* tags - to sweep up any additional contextual sorting or prompts

Then it was a case of using File → Share → Publish to web to make it available as a data source for the web app.

## First app iteration
As I've been using GitHub to host my blog and other test apps I just needed a new repo within my existing account that could be served under the same domain name.

ChatGPT pushed out the first version of the app code which included test data, which was switched to the Google Sheet data soon after. As the initial version was developed without any real input from me I wasn't really taken with the presentation, but it was a starting point for working out what I did want

![Flashcards v1 with black screen, rounded selectors and initial control](/img/flashcards_1.png)

Improvements identified and actioned were:
* losing the source URL for the Google Sheet since this would be persistent
* having yellow flashcards with black text on both sides (no dark theme).
* moving top controls to a left sidebar, using bigger text and improving the presentation
* bottom controls being grouped logically and compact, and having selectors for next/previous
* a visible search input 
* flashcards to sit higher on the page
* adding a language selector (FR→EN / EN→FR segmented toggle) to switch which side is the prompt and which is the answer.
* better support for the labels field from the Google Sheet to show as a meta line on the card
* moving to more of a GDS Design System approach and making it mobile-friendly (to learn on the move)

## Being lazy with data entry
Although I'd learned on my OU course that writing things down is a great way to aid memory retention, I was finding adding info onto the Google Sheet pretty boring. So I took photos of the vocabulary text blocks in my book and uploaded to ChatGPT to convert into my Google Sheet format, including adding the context sentence. That worked out pretty well, but wasn't sustainable from a learning point of view.

Next up was a Google Form to make data entry much easier to push in. This required changing to use the Form responses tab on the sheet and setting up a Google Apps Script to publish the data more effectively for consuming in the web app. We ran into some caching issues with delays in form submissions from appearing in the app, so updated this Script to using JSON instead for instant updates. This was topped off with a nice new button on the app controls to launch the form and enter data.

## Listening to pronunciation
One aspect of Reverso I really liked was the ease of clicking an icon to hear someone speak the words, to help reinforce how to say them well as part of my learning. 

I did a bit of experimentation with the built-in speech APIs on my MacBook but they were really dreadful, sounding nothing like how the French would say it. A bit of searching found [Forvo](https://forvo.com) which has real people speaking phrases. It does have an API, but a paid one which pushed it out of scope. After a lot of back-and-forth on other options I realised that the most pragmatic way to achieve this was just to have a link to Forvo to open the right page. 

As the format of Forvo pages was consistent (e.g. https://forvo.com/word/pomme/#fr) I got ChatGPT to create a helper to take data from the sheet, combine the article + word, strip out any other unnecessary data and then automatically generate a URL to add to the flashcard icon. Job done!

## The final version
I'm pretty pleased with how the latest iteration looks and works

![desktop view of French Vocab Flashcards web app](/img/flashcards_app.png)

As we use it, my wife and I are already finding extra things we want it to do, like including verbs, idioms and phrases, so we're seeing how well it holds up to some robust user testing while we learn. But for now I'm just happy I was able to utlise tools to develop exacty what I wanted very quickly.

You can [view the code and the README on my GitHub repo](https://github.com/electronicdreamplant/french-flashcards/)
