---
layout: post
title: "Repair My House"
date: 2017-02-04
tags: oxford
---

## Some background information

Oxford City Council owns and operates its own council housing, about 8,300 properties, and is making plans to increase this number through [large developments in the city](https://www.oxford.gov.uk/info/20105/council_housing/309/new_council_homes_being_built) over the coming years.

Unlike many other social housing providers we also carry out all our own property maintenance, including gas servicing. This, in turn, generates a large demand for users contacting us, largely to report an issue that needs fixing.

Council housing represents by far the highest volume of calls, with some 40,000 each year. We were keen to find ways we could make it easier for users to get in touch with us to report housing repairs and cut out the need to make a phone call.

## How things were

We had developed an online service using our CRM system and its forms engine some time ago. However, this had some significant shortcomings, both for users and staff:

*   There was no way to make an appointment online; users would submit their request and be contacted by Contact Centre staff to complete it through offering available dates over the phone. This meant two transactions were required instead of one
*   While the submitted request created a record in our CRM system, it was incomplete and staff had to (effectively) create a new one using much of the information from the original record. This caused some frustration for our Contact Centre staff
*   The service was ‘blind’ about the user requesting the service; it didn’t know what type of property they lived in, their status (i.e. an actual council tenant or not) so this all needed checking by staff once the request was received
*   There was no way for users to keep track of the repairs they had requested, or their progress, resulting in further calls to our Contact Centre
*   Despite having an efficient approach behind the scenes, with repairs appointments being dispatched automatically to the correct repair operatives via their hand-held devices, we were not taking advantage of this to make the whole service an end-to-end digital process

## Testing the project feasibility

We had already worked with council tenants to test out the idea of an improved digital service for housing repairs, including the idea of a progressive form to drill down to the repair required.

Before we jumped in with developing a full service, we wanted to test the concept of a user account for repairs and other council services that would work alongside our CRM.

We decided to employ ‘loose coupling’ of systems in line with the [Gubbins of Government approach](https://www.youtube.com/watch?v=02__3UTqXmU) where web services are used to join them together to provide the functionality for the overall service.

To help us do this we worked with a local Drupal agency, [Agile Collective](https://agile.coop/), who took us through our first agile process for developing a new digital service. We worked on a set of user stories that took us through the account creation process, checking an address and displaying repairs history for a valid property/council tenant. These were delivered over a series of ‘sprints’

By the end of this feasibility project we were able to demonstrate that the overall approach was sound, we could ensure user data was kept safe and we could have different council IT systems talk to teach other to make things work.

## Finding the best way to provide the service

We knew that a service that worked well for users was the key to success so wanted to get some expert help, as well as work with users themselves to ensure we met their needs.

We asked [Mando](http://www.mando.agency/) to work with us as they had already done work on reviewing our online forms to identify issues with usability. They helped us work through the issues we had with the current process and identify what success would look like.

Challenges and the solutions we adopted were:

*   **solving user ‘blindness’** - we used an address lookup to check our property records to see if the user was in a council property in our area, what type of property (house or flat) it is and its status (no repairs possible if it has been sold or in the Right to Buy process). This still allows us to provide the service without having to create an account
*   **dealing with emergencies** - we introduced an initial filter of questions about emergency situations that directed users to call instead of progress through the form so they can get the help they need more quickly
*   **pinpointing the repair** - we used a progressive triage, presenting limited choices on screens to drill-down from inside/outside the house, through to the room, then to the area of the room and finally to the fault itself. This set of choices was enhanced by using simple graphics (house, floor, bath, tap etc)
*   **allocating the repair to the right trade** - in order for an end-to-end process to work we had to make sure the right jobs were allocated to the right trades. A look-up table was created listing the 159 repair permutations, their trade and the High Level Descriptor code used together with other relevant metadata in order to create the right record in the repair job system.
*   **not all repairs need appointments** - for repairs to fencing it is not feasible for an appointment to be made as lower priority jobs like this may take up to 3 months to be undertaken. We decided that while the process should appear largely the same to users, raising the appointment would be done by Contact Centre staff

Mando carried out wireframe testing with users, checking that the information architecture was sound and the copy made sense to them. From this we had a good sense of what worked and how we needed to improve it. Then it was on to developing the form itself.

## Making everything work together

Getting the groundwork on the process design first meant we were clear about what needed to be delivered before any work on the form started. Despite this, the complexity of what was required presented some real challenges.

While the digital service appears simple to users, there is a lot of work going on behind the scenes:

*   5 different core IT systems are used to host, operate and accept the outputs of the process
*   30 different form pages are needed due to the branching of the main form at different points
*   13 different web services and 5 SQL calls are necessary to make each system communicate effectively and deliver the outputs needed

The outputs of the process are:

*   a repair job raised, and allocated to the correct trade
*   an appointment allocated to the repair job
*   the correct repair operative receiving the job to action on their hand-held device
*   a confirmation email to the user about their repair and appointment
*   an SMS confirmation to the user (plus reminders nearer the time)
*   repairs history being available to users with a valid online account

## Iterate, iterate, iterate

Once we went live in January 2016 we were keen to get some [early feedback from council tenants](/downloads/Tenants Portal User Testing 18Jan16 - report.pdf) to see if we’d got it right. We invited them to bring in their own devices to test it on, and gave them a set of scenarios to work through.

We discovered:

*   Users found the process straightforward and easy to use, and they liked being able to make appointments online
*   We needed to make the account registration process more simple and remove some questions
*   The form progress indicator caused some confusion
*   We needed to make available appointments more visible to users to help them make a choice. Removing Saturdays and Sundays from the view, when no repair slots are available anyway, created less screen clutter and helped mobile device viewing

After the initial first weeks we also found that duplicate repairs were being raised, one with no appointment. This caused some issues for our repairs staff so we needed to resolve it. After using [Hotjar](https://www.hotjar.com) to analyse user behaviour we identified that the problem was caused by users abandoning the form having not found a suitable appointment slot. We’ve now put in place a fix to remove these jobs and will be watching to see if our other improvements make appointments more visible.

## What next?

The Repair My House service is now running well and we’ve started to roll out more publicity to encourage more of our tenants to use it.

We are working on introducing more appointments for low priority repairs, so that even if the repair itself may take some time, an initial inspection would be made that the user can book.

We will be adding functionality to amend or cancel a repair to further reduce the need to call us.

We will be developing a new service - Make a Gas Service Appointment - to enable our tenants to book a gas boiler service online rather than have to call

## More information

[Download the repairs process architecture](/downloads/Repairs Process architecture.pdf)
