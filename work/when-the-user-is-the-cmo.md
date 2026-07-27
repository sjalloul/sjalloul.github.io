---
layout: work-post
title: "When the User Is the CMO"
category: "Selected Work"
description: "Early on, I built marketing dashboards for people who had three minutes and a hard question. The audience has changed since. The discipline hasn't."
date: 2026-07-27
permalink: /work/when-the-user-is-the-cmo/
tags: [portfolio, business-intelligence, data-visualization, requirements, career]
---

Before I was writing update logic for devices that keep hearts beating, I was making numbers legible to people who ran companies. It's a strange lineage on paper, but the through-line is cleaner than it looks: figure out what someone actually needs, build it under real controls, and never let a wrong number reach the room.

The setting was a multidisciplinary group building marketing visualization tools for the C-suite — CMOs and CXOs at Fortune 100 companies, domestic and international. The client list read like a brand-recognition test: Bank of America, American Express, Oral-B, General Motors, Renault Nissan, Emirates. What that meant in practice was that the person on the other end of the dashboard wasn't a data analyst who'd forgive a rough edge. It was an executive with a few minutes and a specific question about where their marketing spend was going. That constraint shaped everything. When your user is the CMO, "technically correct but hard to read" is just a nicer way of saying wrong.

## The work happened before the code

The part that taught me the most wasn't the building — it was the engagement that came before it. I spent real time in the requirements process: sitting with business stakeholders to understand what they were trying to see, translating that into functional specifications, and aligning the whole thing against standard SDLC controls so that what we promised and what we shipped were the same artifact.

That sounds procedural. It isn't. Most of the failure modes in software live in that gap between what someone asks for and what they mean, and closing it is genuinely hard work. You learn to ask the second and third question, to notice when a request for "a chart of campaign performance" is really a request to justify a budget to a board. You learn that a well-run engagement process is not bureaucratic overhead — it's the thing that keeps you from building a beautiful dashboard nobody needed. It was my first real taste of disciplined delivery, and it turns out that taste doesn't leave you. Years later, the controls got heavier and the regulator replaced the CMO, but the instinct is the same one I formed here.

## Mockups first, then the real thing

The build itself ran on Business Objects. I worked the way I still prefer to: mockups first, because a picture is cheap to argue with and expensive to rebuild, then functional dashboards once the shape was agreed. Getting a client to react to a mockup surfaces the disagreement early, while it's still just pixels — far better than discovering it after you've wired everything to live data.

Alongside the dashboards, I picked up the surrounding toolset — Business Objects itself, Flex, and the marketing analytics stack the work sat on top of. The specific tools have aged the way tools do, but the underlying skill of learning a platform well enough to bend it to a stakeholder's intent has not.

## The dashboard was the tip of it

What an executive sees is a clean panel with a few decisive numbers on it. What sits underneath is plumbing, and the plumbing was most of the job.

Marketing data doesn't live in one place. A single campaign leaves its traces scattered across platforms — Google Analytics, ad networks, and the other major marketing systems these notable customers ran their spend through — each with its own API, its own authentication dance, its own schema, and its own idea of what a "session" or a "conversion" means. There is no dashboard until someone reconciles all of that. Early in my career, that someone was me.

I wrote a .NET console application to do it: hit each platform's API, pull the campaign data down, organize it into a consistent shape, and automate the curation so the whole thing ran without a human babysitting every step. That work had an unglamorous prerequisite that I've come to respect more the further I get from it — reading. A *lot* of documentation. API references, auth flows, rate limits, pagination quirks, the undocumented edge where the docs and the actual response disagree. You don't build a reliable pull by guessing; you build it by reading the spec closely enough to know where it lies to you, and then handling that.

By the time any of this reached a Business Objects dashboard, the hard part was already done. The data had been gathered from half a dozen platforms, normalized, curated, and automated into something trustworthy. The visualization was the last, most visible ten percent sitting on top of a pipeline nobody in the corner office ever saw — which is exactly how it should be.

## The number has to be right

Then there was QA, across both the demo builds and the production dashboards. This is the part people skip in the retelling because it isn't glamorous, but it was the part with the sharpest stakes. A demo dashboard sits in front of an executive who will make a decision based on what it shows. If the number is wrong, you haven't shipped a bug — you've handed someone a reason to be wrong in public, with their name on it. So I checked. Demo and production both, because a client's trust doesn't distinguish between environments.

That was, in a quiet way, my first lesson in the thing I now do for a living: correctness isn't a feature you add at the end. It's the whole point, and everything else is in service of it.

## What carried forward

I don't romanticize this era. It was early-career work with a well-defined scope, and I was one contributor in a capable group. But it's where the habits started. Understand the requirement before you build. Read the documentation until it stops surprising you. Work inside the controls, not around them. Assume the number will be trusted, and earn that. The audience has moved from marketing executives to auditors and clinicians, and the cost of a mistake has moved from an awkward meeting to something far more serious — but the shape of the discipline is the one I first learned making dashboards legible to the corner office.

Same job, really. Make the truth clear, and make sure it's true.
