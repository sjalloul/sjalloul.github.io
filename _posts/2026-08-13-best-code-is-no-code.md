---
layout: post
title: "The Best Code Is No Code: Why Every Line You Write Is a Liability"
category: "Software Engineering"
description: "Code isn't the asset — the problem it solves is. Every line you write is a standing debt of reading, testing, and carrying, and that math only gets more urgent now that writing code is nearly free."
date: 2026-08-13
---

We have the accounting backwards.

Walk into most engineering cultures and you'll find code treated as output — as productivity, as progress, as the *asset* you're accumulating. Commits are wins. Features shipped are trophies. Lines written are, somewhere deep in the collective subconscious, evidence that work happened. And nearly all of it is a category error, because code is not an asset. Code is a liability. Every line you write is a small standing debt that has to be read, understood, tested, debugged, secured, refactored, and carried by someone — often future you — for as long as the system lives. The asset is the *problem you solved*. The code is just the reluctant, expensive price you paid to solve it, and like any debt, the interest never stops.

## Writing is the cheapest moment in a line's life

The seductive thing about a line of code is that the moment you type it is the only cheap moment it will ever have.

After that, the bills start arriving. That line will be *read* far more times than it was written — by teammates, by newcomers who've never seen it, by you at 2 a.m. eighteen months from now with no memory of why it exists. It will need tests. It will have to survive every refactor that happens around it. It widens your attack surface. It has to be understood before it can be safely changed, and changed carefully so it doesn't quietly take three other things down with it. Multiply that by every line in the system and you arrive at the real number: the total cost of *owning* a line of code utterly dwarfs the cost of producing it. You didn't write an asset today. You signed a maintenance contract, in perpetuity, on behalf of everyone who will ever touch this system.

Dijkstra saw this decades ago and put it about as well as it can be put: we should count lines of code not as lines *produced* but as lines *spent*. Every line is money out.

## We celebrate the wrong direction

The trouble is that our instincts, and our incentives, point the wrong way.

Adding is visible. The engineer who ships two thousand new lines and a shiny feature gets the applause. The engineer who *deletes* two thousand lines — who finds the redundant subsystem, the speculative abstraction nobody ended up needing, the dead code rotting behind a flag that's been false since 2019 — did the more valuable work by a wide margin, and gets a fraction of the credit, because subtraction doesn't demo well. There's a line, often attributed to Bill Gates, that measuring progress by lines of code is like measuring an aircraft's progress by its weight. It's right, and it's worse than a joke: the metric is inverted. More weight is not more plane. More code is not more product. Usually it's just more plane to keep in the air.

And this isn't only a culture problem; it seems to be wired into us. Researchers have found that people faced with a problem systematically reach for solutions that *add* something and overlook the ones that *remove* something — even when removing is simpler and clearly better. We are, by default, additive creatures working in a medium where addition is the expensive move. That's a bad combination, and fighting it is a real part of the job.

## What "no code" actually looks like

None of this is an argument for laziness. "The best code is no code" is not a slogan for shipping less; it's a discipline for *owning* less. In practice it looks like a set of unglamorous habits.

It looks like YAGNI — *you aren't gonna need it* — building for the problem in front of you instead of the six hypothetical ones that may never arrive. Speculative generality is one of the great liability multipliers: the flexible framework you built for future requirements that never showed up is now permanent weight you carry for nothing. It looks like deleting dead code without sentiment, because dead code is never free — it's cognitive load, a hiding place for bugs, and a lie the codebase tells every new reader about what still matters. It looks like choosing boring, proven, well-understood tools over clever new ones. It looks like pushing behavior into data and configuration instead of into branches and special cases. It looks, very often, like *not* adding the service, the layer, the abstraction that everyone's reflex says to add.

And most of all it looks like the highest-leverage move in the whole craft: talking a stakeholder out of a feature. The best requirement is frequently the one you kill in the room, before it becomes code, before it becomes a maintenance contract nobody remembers signing. Every feature you thoughtfully decline is a lifetime of liability you simply never take on. That conversation is engineering — real engineering — even though not one line gets written.

## The honest complication

Now let me complicate my own thesis, because taken naively it curdles into something dumb.

"No code" is not a license to under-build, and it is emphatically not a license to solve every problem by gluing together fifteen dependencies you don't understand. That instinct feels like writing less code, and technically it is — but you haven't *eliminated* the liability, you've *outsourced* it. Every dependency is code you didn't write and still own: you own its bugs, its security holes, its abandonment when the maintainer loses interest, its place in a supply chain you now have to reason about. In regulated work this stops being abstract — you literally have to enumerate every commercial, open-source, and off-the-shelf component in a bill of materials and answer for all of it, forever. Imported liability is still liability. Sometimes writing the fifty lines yourself, and understanding them completely, is genuinely *less* debt than pulling in a library that does a thousand things when you needed three.

So the real principle isn't "write zero code." It's this: minimize the *total liability you own and must maintain* — written or borrowed — and treat every line as something you have to justify rather than default to. Code should be *earned*. Sometimes it's absolutely earned, and you write it, and that's correct. The discipline is in making it prove its worth first.

## Why this matters far more now

If this principle was important when writing code was slow, it is *urgent* now that writing code is nearly free.

AI can generate five hundred lines before you finish your coffee, and that changes exactly one thing: it collapses the cost of the cheapest part. The typing was never the expensive part. The owning was — the reading, the debugging, the securing, the understanding, the carrying-it-for-years. All of that cost sits precisely where it always sat, and arguably worse, because now there is *more* code, produced *faster*, and understood *less* by the people nominally responsible for it. A tool that makes it effortless to generate liability, absent any discipline about whether you should, is a machine for quietly bankrupting a codebase. Which means the old wisdom — that the best code is the code you didn't write — isn't obsolete in the age of AI. It's the counterweight the age of AI most badly needs.

## The mature instinct

Somewhere along the way, if you do this long enough, the reflex flips. You stop feeling proud of how much you wrote and start feeling proud of how little you had to. You reach, by instinct, for the smallest amount of code that fully solves the problem and not one line more. You treat every line you *do* write as a promise you'll be paying on for years, and you write it accordingly — clearly, carefully, as though it's going to outlive you, because it very well might.

The best code is no code — not because code is bad, but because code is *expensive*, in a currency you keep paying long after the writing is done. The engineers I trust most are the ones who feel that cost in their bones, who reach for the delete key as readily as the keyboard, and who take a quiet, unglamorous pride in the most valuable thing they built all week: the code that, in the end, they were wise enough not to write at all.
