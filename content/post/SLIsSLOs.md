---
title: "SLIs and SLOs"
date: 2022-12-22T11:45:39-08:00
draft: true
---

# SLIs and SLOs
So today I have been thinking a lot on SLIs and SLOs. You see, I work as an SRE and I work alongside a lot SREs, and this often a point of confusion for the new and experienced alike.

## Engineering, Agile, and the One True Way
Software Engineering has a bit of a disease on their hand. A fear of learning outside of their box. Sure, we can code until our fingers bleed, but how often do we think about the title of "Software Engineer?" Well, before I can jump to the easy answer, we have to do some 101 work first.

### Engineering vs Developing
So What is the difference between Engineer and Developer. Like all things in tech aren't they the same thing?

Well, bluntly, no.

This website uses a tool, Hugo. I downloaded the tool, Go Lang, and some useful Markdown utilities, and am building the site, then letting Hugo do its magic to get it ready for show time, Git to host it, and some fancy pipeline work in Github Actions to make it available. I didn't build anything more than the content. I am a Site Developer when i am working on it.

I am doing little in the form of Engineering, outside of the words that i am conveying. Which if we are being cheeky, an author is a "word engineer". But i am not solving a problem with a tool, or building a solution to solve that problem. Nor am I creating anything more than content. I'm using a tools someone else made to accomplish my work.

There is nothing wrong with Developing. We all use Network standards, programming languages, and tools that others have built to accomplish a great many things.

But building a log-in page does not an engineer you make. Just as sticking feathers up your butt does not make you a chicken.

And this is find. Chill out. Unruffle the newly inserted feathers. Because You can still *be* and engineer. You just might not *be* and engineer currently.

To further emphasis this, lets look at the old cliche. The definition of Engineer those closest fits our role as "Software Engineer:
> **Engineer** <br>
>1. A designer or Builder of Engines.<br>
>1. a person who runs or supervises an engine or an apparatus.

And

> **Developer**<br>
>1. One that Develops. <br>
><br>
>
>**Develops**<br>
>1. to set forth or make clear by degrees or in detail.

## Why the Long Winded, Controversial Hot Take?
Because words matter.

In Agile Project Management, there is an emphasis on roles, responsibilities, and breaking down barriers. The governance of this all build up accountability.

Engineers need remember that, if you wear the Engineering hate, that you are a *designer, builder, and runner of an engine or machine.* You have to focus on what that means when it comes to running that machine.

How does this relate to SLIs and SLOs?

## The Process for Making SLIs
Well, because Service Level Indicators(SLIs) are not just simple metrics you farm out to the nerds that run whatever Monitoring stack you use. SLIs are indicators of your service level. To make this less technical, lets look at a car.

Cars are machines, that many engineers and developers have worked on. Cars have a simple objective. Move things with mechanical power. In my case, they take energy (fuel), they use that energy to create power (explosion), that is delivered Power through a machine (the engine block and the transmission) to the wheels. This makes forward motion. Simple, right? (Mike with the Hot Takes)

But Gas, power, and engines are dangerously complicated. If it gets too much power, it can overwhelm the system, if it drives too fast, it could crash, if it any number of parameters gets too out of whack, the vehicle could have a number of negative consequences. So how do we keep this fire driven explosive device under control. Well, by determining what we want to measure to keep in under control.

You see, we have an objective. Forward motion. We have a goal. Don't blow up, die, or loose control. Our testers have determined the limits. So now what?

Well, we measure them and then make decisions based upon our hypothetical findings.

If out testers determine that going 50 MPH on a wet road will create a "loss of control" incident in a turn, and (doing an SLA shout out here) the government deems that there is a limit on this turn of 45 MPH, how would we measure success or failure of this condition?

Well, with a Speedometer since it measures our SLI - Speed. Our SLI will be MPH, which can measure both the SLA for corners (45 MPH >) and since the cops hang out at that corner and are strict with a speed camera (we could set our SLO for 44 MPH >).

# How to create SLIs and SLOs
After this long worded essay, here is the simple answer. Site Reliability Engineers don't. SREs *enforce* SLOs.

Going back to Engineering, SREs are Reliability Engineers. I'll do a whole post on the RE of SRE, but to put it simply, Reliability is a set of processes and procedures that keeps software reliable.

The only people who can create SLIs, and the subsequent SLOs, are the team that has ownership of the product in question.

So theory aside, what does this practically look like? Should SREs just toss this over the wall to engineering?

NO!

SREs should set aside time to define team ownership, and then work with the team that owns the product to define the SLIs. The SRE can and should assist.