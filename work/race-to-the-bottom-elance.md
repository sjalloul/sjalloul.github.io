---
layout: work-post
title: "The Race to the Bottom: Bidding for Code on eLance, 2009–2011"
category: "Selected Work"
description: "Two years bidding for code on eLance and oDesk, and the lesson that outlasted the money: the typing gets commoditized, the judgment never does."
date: 2026-08-02
permalink: /work/race-to-the-bottom-elance/
tags: [portfolio, freelance, requirements, early-career]
---

Contracting kept the lights on, but it didn't do much more than that, and in 2009 "the lights are on" was not a sentence anyone said with confidence. So at night, after the day's tie came off, I did what a lot of people were quietly doing in those years: I went looking for extra money on the internet, one small job at a time.

The place you went to do that was a freelance marketplace — eLance, mostly, though I bid across oDesk and Guru and the site everybody eventually called vWorker too. These were the ancestors of what later merged into Upwork, and they ran on a simple, merciless idea: a client posts a job, freelancers from every corner of the planet bid on it, and the market sorts it out. I spent the better part of two years in that market. It taught me more about the economics of software — and about where the value in this work actually lives — than most of the full-time roles I've held before or since.

## The market

The first thing you learn on a bidding platform is that you are not special, and neither is your code.

A job would post — build a WordPress site, write a scraper, fix a broken PHP checkout, automate an Excel report, patch a .NET bug someone else had abandoned — and within an hour it would have thirty bids on it. Mine, sitting in a suburb of Boston with U.S. rent to pay, and twenty-nine others from places where three dollars an hour was a real wage and mine was a fantasy. The platform took a cut of every job and metered how many bids you could even submit, so you were paying, in fees and in scarce bid credits, for the privilege of losing most of them.

And there was the cold-start trap that every one of these markets is built on: you can't win jobs without a feedback history, and you can't build a feedback history without winning jobs. The only way through the wall is to underprice yourself badly at the start — to work the first several jobs at something close to a loss, buying five-star reviews with your own time, so that later you might charge what the work is worth. It is a reputation market wearing the costume of a labor market, and the entry fee is paid in dignity.

## What actually won, and it was never the price

Here is the thing that took me a few humbling months to understand: you cannot win a race to the bottom against someone whose bottom is far below yours, so you must refuse to run that race at all.

I stopped trying to be the cheapest bid and started being the *legible* one. The bid that asked the right two questions the client hadn't thought of. The bid written in clear, confident English by someone in a workable timezone who would actually answer a message. The bid from the person who, when the client's description was a vague paragraph of wishes, could say back to them — in plain terms — here is what I think you actually need, here is what it will and won't do, here is how we'll know it's done.

That is the opinion I'll stake, and it has only gotten truer with time: those marketplaces commoditized the *typing* of code, ruthlessly and completely, but they could not commoditize judgment or trust. The clients who'd been burned by the lowest bid — and there was an endless supply of them, because the lowest bid burns people constantly — were exactly the ones who became repeat business at a real rate. They weren't paying for code. Code was free; there were thirty bids on it. They were paying for someone who would not disappear, would not surprise them, and could turn their confusion into a bounded thing.

## The scrape and the pit

Two kinds of job came through that market, and I remember them now as two different kinds of weather.

The ones I loved — the ones I still remember fondly — were almost all the same shape underneath. A script, a small tool, a bit of automation: scrape these fields off these pages, watch this source and pull that, turn a pile of malformed records into a clean CSV, parse some ugly proprietary file into something a human could use. A few hours of focused work, a clean deliverable, and often money that felt almost embarrassing for the time it took. Scraping and parsing were the work I found genuinely satisfying, and for a long time I thought I just liked the puzzle of it.

It took me a while to understand *why* those were the good jobs, and the answer turned out to be the most valuable thing the whole market taught me. Scraping and parsing work arrives with its requirements very nearly built in. The input is concrete — this page, this format, this source. The output is concrete — these fields, this structure. And "done" is verifiable: either the data comes out correct or it doesn't. There is almost no room for the client and me to quietly mean different things, because the task is *defined by* its inputs and outputs. Those jobs were joyful because the specification was nearly impossible to get wrong.

And then there was the other kind.

The pit always began the same way: a job that sounded simple and was never actually defined. "Build me a tool that does X," where X was a paragraph of hopes with no edges. I'd bid it, win it, start it — and then the requirements would begin to *move*. A change order. Then another. Each one reasonable-sounding on its own, each one quietly revealing that the thing the client actually wanted had never been written down anywhere, least of all in their own head. And then, often enough, somewhere around the third or fourth revision, the client would simply walk away — the project collapsing not because the code had failed but because the target had never existed to hit.

For a long time I took those endings personally, as some failure of my execution. They weren't. The walk-away was the *predictable terminal state* of a project that was never bounded to begin with. A change order is not the disease; it's a symptom. The disease was that we started building before anyone agreed on what "finished" looked like. And on a fixed-price bid, the freelancer is the one who eats that failure — the unpaid milestone, the wasted hours, the dispute that dings a reputation you underpriced yourself for months to earn.

## Before a line of code

So I learned, early and at my own expense, the thing that has organized how I think about software ever since: the health of a project is mostly decided before a single line of code is written, by one question — can we state what "done" is, and can we verify it? When the answer is yes, the work tends to go like a scraping job: bounded, checkable, satisfying, and often quick. When the answer is no, no amount of talent downstream will rescue it. You are only choosing how many change orders it will take to discover you were doomed at the start.

Everything I did after that reflected it. I stopped quoting against a paragraph of wishes and started writing the client a short statement of what I understood the job to be — inputs, outputs, and an explicit list of what was *not* included — and pricing that. Half the time, the act of writing it down surfaced that we'd meant different things all along, which is exactly the discovery you want to make before you've named a number rather than after.

The principle underneath it is one I'll still argue with anyone: an estimate is not a guess about how long the code will take. It's a price on risk — and the risk is almost never the code. It's the ambiguity in the requirements. The freelancers who survived that market weren't the fastest typists. They were the ones who refused to start until "done" had edges.

## The education nobody designed

For all its brutality, that market was one of the best engineering teachers I ever had, precisely because it was indifferent to my comfort. In two years I shipped across more stacks than a normal job would have shown me in ten, and I spent a great deal of that time debugging code I'd never seen, with no documentation, written by someone long gone, for a client who was already annoyed. You learn a specific competence in that arena: how to get oriented in a stranger's mess fast, how to ship something that works under real ambiguity and a real deadline, and how to tell the difference between the fix the client asked for and the fix they actually need. No mentor, no runbook, no forgiveness — just the work and whether it ran.

## Where the value actually lives

Step back far enough and those marketplaces were not a side hustle. They were an early, unusually honest preview of software labor as a global commodity market — a look, a decade early, at what happens when the act of writing code gets exposed to unlimited price competition. And the lesson that market taught, over and over, in the plainest possible terms, was this: the commodity part of engineering, the typing, is the part that gets competed straight to zero. The durable value is always upstream of it — in deciding what to build, in pricing the risk, in translating a confused human's wish into a bounded scope, in being someone a client can hand money and ambiguity to and trust to come back with the right thing.

I think about this constantly now, because the same thing is happening again at a far larger scale. AI is doing to the writing of code roughly what those bidding markets started doing to it in 2009 — driving the cost of the typing toward zero. The reflexive panic about that misreads the history. The typing was already a commodity; the marketplaces proved it fifteen years ago. What was never a commodity, what the race to the bottom could never reach and the models still can't, is judgment: knowing what is worth building, what the requirement actually is beneath what was asked, where the risk is hiding, and when the honest answer is *no*. The survival move is the same today as it was at 2009 rates — climb out of the layer that's being commoditized and into the layer that isn't.

I made some extra money in those years, and I needed it. But the thing I actually took away was worth more than the money: I learned, the hard way and early, the single most important economic fact about this whole career. Pay lives where the judgment is — and the judgment starts with knowing what "done" means before you build a thing toward it.
