---
layout: work-post
title: "The Oldest Machine in the Building: What a Mainframe QA Contract Taught Me"
category: "Selected Work"
description: "A mainframe QA contract at John Hancock/Manulife, and the case for respecting the load-bearing legacy systems everyone else is itching to rewrite."
date: 2026-08-02
permalink: /work/oldest-machine-in-the-building/
tags: [portfolio, quality-assurance, legacy-systems, early-career]
---

By the middle of 2009 I had done a first contract well and learned the thing nobody warns you about: doing it well doesn't produce a job. There was no full-time role to convert into — not that year, not in that economy, not at a financial company defending its headcount through the worst downturn most of us had ever seen. What I got instead of an offer was a second contract, in a completely different corner of the same building, doing something I had never done.

The role was Quality Assurance Engineer, brought in through a consultancy to work on John Hancock/Manulife's Subsidiary 2/3 project — the accounting (eTreasury) and traditional / non-traditional product work streams. Stripped of the corporate labels, that means the statutory plumbing: the systems that move the actual money and account for the actual policies. The parts of an insurance company that cannot be wrong.

And it ran on a mainframe. So there I was, new all over again, learning the oldest layer in the entire organization.

## Respect the old machine

If you have never worked near a mainframe insurance system, the instinct is to condescend to it. It's old. The tooling is archaic. The mental model belongs to a different era. Surely the interesting work is happening somewhere newer, somewhere with a nicer editor and a friendlier deployment story.

That instinct is exactly backwards, and unlearning it was the first gift of that contract.

The mainframe was old because it *worked*. It had accounted for policies and moved money reliably for decades, and everything else in the company had been built up and around it on that assumption. It was antiquated and load-bearing for the same reason — it had earned so much trust and accumulated so much dependency that replacing it was no longer an engineering question but a risk question, and the risk answer was always "not this year." The least fashionable system in the building was also the one nobody could afford to break.

Here is a position I'll defend without much hedging: the reflex to rewrite a load-bearing legacy system is one of the most reliably destructive impulses in our field, and it is almost always vanity wearing the costume of progress. The system you want to throw away is not ugly because the people before you were stupid. It's ugly because it accreted twenty years of edge cases, regulatory carve-outs, and hard-won corrections that are encoded nowhere except in the code you find distasteful. Rewrite it clean and you don't inherit the cleanliness you imagined — you inherit the original bugs *minus* the corrections, at a scale you can't test your way back out of. Chesterton's fence stops being a quaint aphorism when the fence is a batch job that has correctly closed the books every night for a decade.

And I'll go further, because it's unfashionable and true: a well-run mainframe batch system will embarrass a lot of modern distributed architectures on the metrics that actually matter — throughput, determinism, and the ability to say with certainty exactly what happened to a given record and why. We spent the last fifteen years trading that determinism for horizontal scale and developer ergonomics, and a great deal of the time we pretended the trade was pure upside. It wasn't. Eventual consistency is a real cost, not a free lunch with a clever name. "It'll reconcile" is not the same sentence as "it is correct," and on a system that accounts for money, the distance between those two sentences is the entire job.

The real fragility in a legacy system, by the way, is almost never the technology. It's the people. What actually rots is the tacit knowledge — the handful of humans who understand which edge cases the code is quietly handling and why. Lose them and you're left with a system that works perfectly and that no one dares to change, which is a slower, more dignified way of losing it entirely. Getting dropped in front of that machine at the start of my career forced a habit I've kept: assume the old system knows something you don't, and go find out what it is before you touch it.

## The paperwork was the point

The work itself did not look like engineering, at least not to the version of me who showed up expecting to write code.

I analyzed business and functional requirements against SDLC quality controls. I wrote specifications and project plans and handed them to technical staff. I sat through requirement-gathering sessions, use-case reviews, test-plan reviews, design meetings, and risk mitigations. Day to day, it felt like paperwork wrapped around a very old computer — a bureaucracy of documents standing between an idea and the system it was allowed to touch.

I was wrong about it, and I was wrong in a way that took me years to fully see.

Let me put the technical claim plainly: requirements traceability is type-checking for an organization. A good type system makes invalid states unrepresentable; good traceability makes undefended changes unrepresentable. A requirement links to a design, which links to an implementation, which links to a test, which links to the evidence the test passed and the risk it retired. When that chain is intact, a whole category of failure becomes structurally impossible rather than merely discouraged — the change nobody can explain, the feature that satisfies no requirement, the requirement that was never verified. That is not bureaucracy. It's the same instinct that makes us reach for a compiler instead of hoping.

I'll say the harder thing too: most teams that proudly skip this in the name of speed are not actually faster. They've moved the cost downstream — into production incidents, forensic debugging, and the slow tax of nobody being sure why anything is the way it is — and then declined to measure it. Velocity you refuse to price isn't velocity. It's debt with better marketing.

And while I'm planting flags: test *coverage percentage* is a vanity metric that has fooled more engineering leaders than almost any number in our field. Ninety percent line coverage tells you what fraction of your code ran, not what fraction of your requirements or your risks you actually verified. I have seen thoroughly covered code that pinned down nothing anyone cared about, and sparse suites that nailed every failure mode capable of hurting someone. Coverage of *risk* is the number that matters. The mainframe taught me to ask the question most of the industry still tiptoes around — not "did the tests pass," but "what would have to be true for this to hurt someone, and did we test *that*."

## The blast radius should pick the method

Somewhere along the way "move fast and break things" stopped being one startup's risk posture and hardened into a monoculture — a thing engineers repeat reflexively, as if it were a law of nature rather than a bet that only pays off when nothing you break matters.

It's a luxury belief. It is affordable precisely to the degree that your failures are cheap. Break a social feed and you cost someone an annoyed afternoon. Break the ledger that accounts for a life insurance policy — or, in the work I do now, the software inside a medical device — and "we'll fix it forward" is not a methodology, it's a confession.

The right question was never "move fast" versus "move carefully" in the abstract. It's: what is the blast radius, and does my method match it? A team shipping a marketing site and a team shipping a pacemaker should not work the same way, and the fact that our industry keeps trying to sell both of them the same tempo is a failure of judgment, not a triumph of best practice. The mainframe forced that question on me before I had the vocabulary for it. Nearly everything I've believed about engineering since has been a version of the same answer: let the cost of being wrong choose how you work, and be suspicious of anyone selling a single speed for every problem.

## What it was worth

Here is the honest arc of it: I could not muster a full-time job that year, and I spent it in the two most antiquated corners of a giant insurance company — a source-control migration, then a mainframe. On paper it reads like a holding pattern, a talented person marking time in a bad market.

It wasn't. It was the best-aimed education I could have gotten and didn't have the sense to ask for. The unglamorous, legacy, load-bearing layers are where the real weight of a system lives, and they're where you learn the disciplines that outlast every framework and every hiring cycle: respect for the systems that already work, patience with the process that keeps them trustworthy, and a permanent suspicion of anyone who mistakes fashion for progress.

I learned to find my worth in the work rather than in the title I couldn't get. That turned out to be the most valuable thing the worst economy of my life ever taught me — and I learned it in front of the oldest machine in the building.
