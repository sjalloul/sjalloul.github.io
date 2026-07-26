---
layout: post
title: "What Regulated Software Taught Me About Speed"
category: "Thought Leadership"
description: "Move fast and break things doesn't survive contact with a device that's keeping someone alive. Here's what constraint teaches you about going fast — everywhere."
date: 2026-04-02
---

I came up in enterprise software, where the reigning philosophy was some version of *move fast and break things.* Then I moved into medical devices, where breaking things means something entirely different, and I braced myself to slow down forever.

What actually happened was stranger. The constraints didn't just slow me down. They taught me what speed is actually made of — and made me suspicious of most of what passes for "fast" in software.

## Fast is a measure of the whole system, not the first commit

In an unregulated environment, "fast" usually means *fast to first deploy.* You can have a feature in production this afternoon. It feels incredible right up until you count the weeks you later spend on the bug it caused, the incident it triggered, the trust it cost, and the rewrite it forced.

Regulated software makes that hidden cost visible and up-front. You *can't* ship the thing this afternoon, so you're forced to ask the questions — what could go wrong, what does correct even mean, how will we know — before the code exists instead of after it ships. The first commit is slower. The whole system is often faster.

Speed is throughput over the entire lifecycle. Optimising the first ten minutes at the expense of the next ten months isn't fast. It's just impatient.

## Constraints are a design input, not an obstacle

The useful reframe is to stop treating regulation, safety, and process as walls you work around, and start treating them as **requirements like any other.**

A latency budget, a memory limit, a safety requirement, an audit trail — these are all just constraints, and constrained problems are *easier* to design for, not harder. An infinite design space is paralysing. "Build anything" is a worse brief than "build the thing that recovers cleanly from a power loss mid-update, provably." The second one tells you what to do.

> The teams that resent their constraints spend their energy fighting the brief. The teams that internalise them spend it solving the actual problem.

## The discipline transfers; the paranoia doesn't have to

Here's the part I didn't expect: almost everything rigor teaches you is worth keeping *even where it isn't required.*

Writing down what "done" means before you start. Designing for the failure case, not just the happy path. Making change safe instead of just possible. Being able to explain *why* the system does what it does, not just *that* it works. None of that is specific to medical software. It's specific to software you intend to still be running, and trust, in five years.

What you *don't* have to carry over is the ceremony. The lesson of regulated development isn't "add more process." It's "understand what each piece of rigor buys you, and pay for exactly that." A startup doesn't need a formal hazard analysis. It absolutely needs to know what happens when the thing it's building fails — and most of them have never asked.

## The uncomfortable conclusion

The industry frames rigor and speed as a trade-off: you can be careful *or* you can be fast, pick one. I no longer think that's true. I think most teams are slow *because* they're careless — they just don't see the bill until later.

The fastest teams I know aren't the ones who skip the hard questions. They're the ones who've made asking them cheap.
