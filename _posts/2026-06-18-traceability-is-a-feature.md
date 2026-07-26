---
layout: post
title: "Traceability Is a Feature, Not Paperwork"
category: "Software Engineering"
description: "In regulated software, traceability gets treated as a tax on shipping. Done right, it's the opposite — it's the thing that lets you ship at all."
date: 2026-06-18
---

Ask most engineers about traceability and you'll get a small sigh. It's the spreadsheet nobody wants to own, the column of requirement IDs that has to be reconciled before an audit, the reason a two-line code change takes a day. In regulated software — medical devices, avionics, anything where a defect has a body count — it's treated as a tax you pay to keep the auditors away.

I want to make the opposite case. Traceability, done well, isn't overhead on top of engineering. It *is* engineering. It's the difference between a system you can reason about and a pile of code you're afraid to touch.

## What traceability actually buys you

Strip away the compliance language and traceability is one claim: **every behaviour in the system exists on purpose, and you can prove it.** A requirement links to a design element, which links to code, which links to a test that demonstrates it. Pull any thread and you can walk the whole chain.

That chain does real work long before any audit:

- **It kills orphan code.** If a function can't be traced to a requirement, either the requirement is missing or the code shouldn't exist. Both are worth knowing.
- **It makes change safe.** Change a requirement and the links tell you exactly which design, code, and tests are now suspect. That's not bureaucracy — that's an impact analysis you'd want anyway.
- **It turns "it works" into "we verified it."** A green test suite tells you the tests pass. Traceability tells you the tests *cover the thing you promised to build.*

None of that is unique to regulated industries. Every team that's ever asked "wait, why does it do that?" is paying the cost of missing traceability. They just don't have a name for it.

## Where it goes wrong

Traceability gets a bad reputation because it's usually implemented as a *record* of engineering rather than a *product* of it. Someone builds the feature, then someone else — often much later — reverse-engineers the links into a document to satisfy a process. That's the tax. It's late, it's manual, and it's always slightly wrong.

The fix is to move it upstream and make it a byproduct of work you're already doing:

> Traceability you author by hand rots. Traceability that falls out of your normal workflow stays true.

Link requirements to design in the same review where you agree on the design. Reference the requirement in the commit and the test name. Let the tooling assemble the matrix instead of a human maintaining it. The goal is that being traceable is the path of least resistance, not a second job.

## Diagrams-as-code is a traceability tool

This is why I'm relentless about diagrams-as-code. A `draw.io` file that lives outside the repo is a screenshot of a decision. A Mermaid diagram in the same pull request as the change is *part* of the decision — it reviews like code, versions like code, and ties the architecture to the commit that changed it.

When the design lives next to the code that implements it, traceability stops being a separate artifact you maintain and starts being a view onto work you already did.

## The reframe

The teams I've seen struggle with regulated development are the ones who treat the requirements-design-code-test chain as four separate deliverables. The teams that move fast treat it as one system with four faces.

Traceability isn't the price of shipping safely. It's the mechanism. Build it in and it disappears into the work. Bolt it on and it's a spreadsheet forever.
