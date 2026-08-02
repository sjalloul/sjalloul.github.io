---
layout: work-post
title: "First Contract, Worst Economy: What Six Months at John Hancock Taught Me"
category: "Selected Work"
description: "A six-month contract in the worst economy of my life, a tie I didn't want, and a CVS-to-ClearCase migration that taught me the trade every tooling decision makes."
date: 2026-08-02
permalink: /work/first-contract-worst-economy/
tags: [portfolio, release-engineering, version-control, early-career]
---

I started my first contract in January 2009, which, if you were anywhere near the financial services industry at the time, you will recognize as roughly the bottom of the world falling out. Lehman had collapsed the previous September. The word "unprecedented" had been used so many times it stopped meaning anything. And I, brand new to the idea of being a contractor, walked into a large insurance company in Boston to do a job most people had never heard of and fewer wanted: release engineering.

It was a six-month contract. It felt, at the time, like the length of it was the point. Everything about that year was provisional. You did not plan a career in early 2009; you planned a quarter, maybe two, and you were grateful for it. I have never since taken a paycheck quite so seriously as I took that first one, and I think that's a healthy thing to have learned early. Scarcity teaches you what the good times let you forget.

## The tie

My first real lesson had nothing to do with software.

A manager pulled me aside, kindly but unmistakably, to explain that in this role, at this company, I wore a tie. Not because the work required it. Release engineering does not care what's around your neck. But because a contractor sitting between the developers and the release process, touching production, training full-time engineers on a system they didn't ask for, occupies a strange and slightly suspicious position in an organization. The tie was not about fabric. It was about signaling that I understood the seriousness of the thing I'd been let near.

I was a little insulted at the time. I understand it completely now. When you are the outside person with the keys to the build, credibility is not granted to you — you assemble it, out of small things, before anyone has seen your work. The tie was the cheapest and fastest of those small things. Reading a room, understanding where you sit in someone else's hierarchy, knowing that trust has to be earned sideways and not just proven technically — that's a skill I've used in every role since, and I learned the first version of it from a dress code I resented.

## The tedium

The actual work was, to be honest, tedious in a way I was not prepared for.

My job was to migrate and maintain source repositories out of CVS and into IBM ClearCase, across both .NET/NAnt and Java/Maven builds, without disrupting the development teams. I resolved release conflicts. I babysat merges. I stood up deployments through QA, UAT, and production. I wrote Perl and shell and Gmake scripts on an ad-hoc basis for whoever needed them — release management, QA, engineering. And I ran what amounted to a small ongoing training seminar teaching full-time engineers concepts they largely wished they didn't have to know.

Very little of this is glamorous. Nobody writes a case study about a clean merge. The entire value of a release engineer is measured in the absence of disasters, which means the better you do the job, the more invisible it becomes. That was a genuinely useful thing to internalize at twenty-something: some of the most important work in software leaves no trace when it goes well. If you need constant visible wins to stay motivated, infrastructure work will break your heart.

## The resistance

The most instructive part was the human one.

The engineers did not want to move to ClearCase. And here is the thing I could not fully appreciate at the time, being new: they weren't wrong. I was hired to execute a migration, and I did it well, but the engineers pushing back weren't simply being change-averse or precious about their habits. ClearCase in 2009 was a heavyweight, expensive, slow, licensing-heavy enterprise tool — and the industry, quietly, was already moving the other direction. Subversion had taken over the "reasonable centralized" middle. Git and Mercurial were three years old and gathering. The center of gravity in version control was shifting toward lighter, faster, distributed models, and here we were migrating *into* the heaviest thing IBM sold.

From the company's side, it was a defensible choice. A financial institution in the middle of a regulatory reckoning wants audit trails, hard access control, governance you can show an examiner. ClearCase gave you that. But it charged for it every single day in developer friction — in dynamic views that hung, in merges that hurt, in a mental model nobody enjoyed carrying. The engineers weren't resisting change. They were resisting a *specific trade* they could feel in their fingertips: governance bought at the cost of velocity, paid daily, by them.

I was the person selling that trade to them. Learning to do that honestly — to acknowledge the real cost of a decision I was implementing rather than pretending it was free — was probably the most durable thing I took out of that contract.

## What it left me with

Two convictions formed in that basement of a job, and I've never let go of either.

The first is that tooling decisions are architecture decisions, and source control is the most load-bearing one of all. Everything in the software lifecycle sits on top of how you version, branch, merge, and release. That foundation is brutally expensive to reverse once teams, scripts, muscle memory, and years of history have poured into it. You do not get to casually change your mind. Which means the choice has to be made looking *forward* — not at what's mature and safe and enterprise-blessed today, but at where the practice is heading and where you'll be stuck standing in five years. In 2009 the "safe" choice and the *forward* choice were pulling in opposite directions, and the safe one won, and the friction was real and lasting. That taught me to always ask, of any tooling decision: are we optimizing for the org we are, or the one we're becoming?

The second is that the friction developers feel is data, not noise. Resistance is usually a signal that a real cost is being paid somewhere, and the engineer feeling it in their daily work often understands that cost better than the person who authorized the decision from a slide deck. Dismissing that resistance as conservatism is how organizations talk themselves into carrying dead weight for a decade.

I think about that contract more than you'd expect, because the tension at the heart of it — governance and traceability on one side, developer velocity and forward motion on the other — turned out not to be a 2009 problem or a ClearCase problem. It's the permanent problem. I work in safety-critical, heavily regulated software now, where the governance side of that ledger is not a preference but a legal and ethical requirement, and the same instinct applies: respect the constraint, but never pretend it's free, and always design as if you'll have to live with the choice long after the person who made it is gone.

I learned that from a six-month contract in the worst economy of my life, wearing a tie I didn't want, running a migration the engineers didn't want, in a language I didn't yet know I'd build a whole career around thinking in.

Best six months of tedium I ever spent.
