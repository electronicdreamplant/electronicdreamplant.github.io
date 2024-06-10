---
layout: post
title: "Collaboration not reinvention"
date: 2017-05-17
tags: oxford
---

As a small team we know we can’t match the resources of our larger local authority neighbours, which is why one of of our [Digital Strategy](http://digital.oxford.gov.uk/strategy/) themes is Collaboration.

We know that by collaborating with third party providers we can improve the service we offer our customers and also save ourselves time, effort and cost. There’s also a good chance that the service will work well and will have been designed more around user needs.

## Working with Democracy Club

We love [Democracy Club’s](https://democracyclub.org.uk) aim to “make the process of democracy better for everyone” which reflects our values as a local authority. They are also completely non-partisan, so no problems with pre-election communications or bias.

They have a set of tools to achieve their aims, such as their [Candidates’ Register](https://candidates.democracyclub.org.uk/) that powers their [WhoCanIVoteFor](https://whocanivotefor.co.uk/) service. We’ve helped crowdsource data for this register and we use WhoCanIVoteFor [on our website](https://www.oxford.gov.uk/info/20046/elections_and_voting/1178/general_election_-_8_june_2017).

This year we wanted to move to including their [polling station finder](http://pollingstations.democracyclub.org.uk/) on our website.

## Our previous polling station finder

When we moved to [Jadu CMS](https://www.jadu.net/content-management-system) in January 2016 we’d identified a set of services that had been provided by our old CMS that needed to be replicated, one of which was a polling station finder.

Jadu CMS has a Directories feature which allows custom content types to be developed quickly and easily. Fields can be geocoded to enable map presentation, and there is a search feature specific to the Directory to allow searching across fields. We’ve used this to create our [Garage search](https://www.oxford.gov.uk/garagesearch) service to help people find available garages to rent from us.

We created a Directory for polling stations, with the address of the station as the key field, and all relevant postcodes for that station added to a non-visible field. The search prompt invites the user to enter their own postcode which will return a suggested match.

This works OK, but is a bit rudimentary and has a few more steps in the process than we’d like.

## Moving to the Democracy Club Finder

We’d seen how good the Democracy Club Finder was in providing walking routes to a polling station from a given postcode, and could see this would benefit our residents.

Initially we’d assumed that the data requirements to meet Democracy Club’s needs were beyond our reach, figuring that complex GIS shape files were needed to power it.

We were wrong.

The necessary data (which we are obliged to hold) can come straight from our Election Management System (EMS), and the instructions are all [available on the Democracy Club website](https://democracyclub.org.uk/projects/polling-stations/upload/). Following these took our Elections Manager a few minutes only as there’s an export feature in the EMS already. All the work has been done for us!

A quick email to send the data later, and it’s [added to the Github queue](https://github.com/DemocracyClub/UK-Polling-Stations/issues/841) to load.

## Deploying the Finder on our website

Deployment can be via a simple embedded widget using an iframe - a single line of code. 

We found that the default widget didn’t work that well for us, as its background colours don’t match ours, and the fixed height nature of an iframe mean we can’t be sure how it will work on different screen sizes. We were concerned about information being cut off on the results screen, for instance.

Instead we used simple HTML form elements (styled with our website CSS classes) to redirect to Democracy Club’s site. This is a bit of a trade-off as we don’t keep visitors on our site, but we think offering a fully-functioning service is the key thing.

You can see our finished version at [www.oxford.gov.uk/pollingstation](https://www.oxford.gov.uk/pollingstation).

### Update

Democracy Club have since released a Javascript-based widget to get round the limitations of the iframe. We think it’s great, but we prefer the full set of data that is presented on the their site.

The 8 June 2017 election saw our new polling station finder being the 4th most popular page, showing there is a real user need being met by this service.
