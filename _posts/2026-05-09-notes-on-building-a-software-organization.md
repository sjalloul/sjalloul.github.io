---
layout: post
title: "Notes on Building a Software Organization"
category: "Building Teams"
description: "A working set of principles for growing an engineering org that ships — hiring, ownership, cadence, and the unglamorous parts that actually compound."
date: 2026-05-09
---

I've spent the last few years less in the code and more in the thing that produces the code: the organisation. Hiring loops, ownership, meeting cadence, the slow negotiation between autonomy and alignment. It's a different discipline, and most of what I believed about it at the start turned out to be half-right.

These are working notes — the principles I keep coming back to. None are original. All are hard-won.

## Hire for the loop, not the interview

The single highest-leverage thing I've built isn't a feature. It's a structured hiring loop. Before it, interviews were a collection of individual opinions loosely stapled together at the end. Afterward, every candidate faced the same calibrated questions, every interviewer knew what signal they owned, and the debrief argued about evidence instead of vibes.

The point isn't rigidity. It's that a good loop turns hiring from a gamble into a *repeatable process you can improve*. When a hire doesn't work out, you can look at the loop and ask what it missed. You can't do that with a gut feeling.

## Give away the work you'd most like to keep

The instinct as a lead is to hold the interesting problems — they're interesting for a reason. It's exactly the wrong instinct.

The most deliberate thing I did last year was hand a principal engineer full ownership of our over-the-air update feature. Not "help me with," not "implement my design" — *own it*, including the parts I'd have enjoyed doing myself. It was a stretch, and it was meant to be. Ownership is the only thing that actually grows people; you can't mentor someone into seniority while doing the load-bearing thinking for them.

> The work you're most reluctant to delegate is usually the work someone most needs to grow into.

## Distributed teams are a design problem, not a compromise

Part of our delivery runs through an offshore team several time zones away. The failure mode everyone warns you about — "it's slower, communication is hard" — is real but misdiagnosed. The problem isn't distance. It's ambiguity, and distance just makes ambiguity expensive.

The fix is the same fix as for any interface: **specify the contract precisely and let each side own their implementation.** Crisp interface documents, clear acceptance criteria, and demos on a rhythm did more for velocity than any amount of "more overlap hours." Treat the org like a system with well-defined boundaries and it behaves like one.

## Cadence is culture

Meetings are the most maligned and most underrated tool a leader has. Too many and you drown; too few and the org fragments into private realities.

The two changes that mattered most for us were subtractive and additive. We **consolidated** overlapping standing meetings until each one had a clear job. And we **added** a bi-weekly demo where teams show working software to each other. The demo isn't a status update — it's a forcing function. Nothing exposes a stuck project or aligns a drifting one faster than "show us the thing, live, in two weeks."

## The unglamorous parts compound

None of this is the stuff that gets applause. Nobody celebrates a well-run debrief or a tightened meeting schedule. But organisations aren't built out of the dramatic moments. They're built out of a thousand small decisions about how work flows, who owns what, and what "done" means — decisions that either compound into a team that ships or erode into one that argues.

I still think of it as engineering. The system is just made of people.
