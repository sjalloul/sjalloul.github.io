---
layout: post
title: "Novel Isn't Free"
category: "Thought Leadership"
description: "Building hardware and software together in a regulated world — and learning where to spend the hard part."
date: 2026-07-26
---

### Building hardware and software together in a regulated world — and learning where to spend the hard part

There is a demo, and there is a device, and the distance between them is where most of the work actually lives.

In most of software, that distance is a few weeks of hardening. You get the thing working, you fix the sharp edges, you ship. In medical devices the distance can be years, and the strange, humbling truth is that most of those years have very little to do with whether the thing works. Getting it to work is the part you can put on a screen. Proving it is safe, sourced, documented, secure, and defensible — proving it deserves to be connected to a person who has no other options and no way to check your work — that is the part that takes the years.

Building novel technology, both the software and the hardware underneath it, has not been easy. It is worth being specific about why, because the difficulty is not the kind you can outwork with a bigger team or a longer sprint. It is structural. And understanding its structure changes how you build.

## A part is a marriage, not a date

It starts with the components, and the components start teaching you the rules immediately. Selecting a new part is not choosing what to buy this quarter. It is choosing what you will be accountable for over the entire life of the device — a decade or more in the field, for something implanted-adjacent or life-sustaining.

Qualifying a part is a commitment. You inherit its supplier, its failure modes, its lot-to-lot variation, its end-of-life timeline. You take on incoming inspection, change-notification handling, counterfeit risk, and the slow-motion emergency of obsolescence, because the part you qualified today will go end-of-life long before your device does, and its replacement will not be a drop-in no matter what the datasheet promises. A "better" part that appears two years later is never free; it drags a re-qualification, and possibly a re-verification, behind it like a chain.

And novel hardware makes this worse in a way that is easy to miss. A well-worn component arrives with field history — millions of device-hours of other people's evidence that it behaves. Novel silicon, a new radio, a new sensor, arrives with none of that. There is no track record because you are the track record. You are not just designing with the part; you are generating, from scratch, the evidence that it can be trusted.

## You are building two products

Then come the design controls, and with them the realization that you are not building one thing. You are building two: the system, and the argument that the system is safe and effective.

The second one is not paperwork sitting on top of the real work. It is work, and it has an architecture of its own. User needs flow into design inputs, inputs into outputs, outputs into verification and validation, all of it stitched together by traceability and threaded through with risk management under ISO 14971, so that every requirement can be followed to the test that proves it and the hazard it guards against. The Design History File is a genuine deliverable. In a real sense it is the product; the device is just the part of it you can hold.

This is where regulated development stops feeling like other software, and it comes down to the cost of change. Elsewhere, refactoring is close to free — you rewrite a module on a Tuesday because it will be cleaner, and no one signs anything. Here, a one-line firmware change can ripple outward into regression testing, re-verification, a risk re-assessment, and a stack of document updates, because the change has to stay coherent with the argument you already made. Change is not paid for in code. It is paid for in evidence.

Which quietly turns architecture into a cost-control discipline. Clean interfaces, real modularity, careful isolation of third-party and open-source software — the things that limit the blast radius of a change — are not just good taste in this world. They are how you keep the evidence bill from bankrupting the program. An architecture that contains change pays for itself in verification you never have to redo.

## Novelty destroys precedent

The regulatory pathway is where "novel" reveals its true price, and the mechanism is precedent.

A large share of the FDA machinery runs on prior art. The 510(k) pathway, in particular, leans on a predicate — you argue your device is substantially equivalent to something already cleared, and much of the existing understanding comes along for the ride. It is the regulatory version of standing on an established foundation.

Novelty, by definition, kicks that foundation out. When you build something genuinely new, there may be no predicate to point at, which pushes you toward De Novo or PMA — pathways where you do not get to inherit anyone's argument. You construct the safety case from the ground up. Sometimes you have to invent the test method itself, because no established method exists for the thing you just built. This is the tax that surprises people: engineering-novel silently forces evidence-novel. You are not only building a feature no one has built; you are building the way to prove a feature no one has had to prove. The cost of novelty is not linear, and this is why.

## The device outlives the threat model

Cybersecurity adds a dimension the others do not: time, and an adversary who does not stand still.

Every other constraint is, in a sense, satisfiable at a point — you verify, you clear, you ship. Security is never finished, because the device is going to sit in the field for years while the threat landscape churns every month. Section 524B is the law catching up to that reality. It makes you commit, at premarket, to keeping the device secure across its entire life: a plan to monitor and disclose and address vulnerabilities, the ability to deliver patches on a schedule and out of cycle when something critical lands, and a software bill of materials so that when the next Log4j-shaped event arrives, you — and everyone downstream — actually know what is inside the box.

The mental shift this forces is real. You are not shipping a product and walking away. You are entering a relationship, one you have promised to maintain for the supported life of the device. And the very mechanism that lets you keep that promise — the update path — is itself a feature, an attack surface, and a safety-relevant function all at once. An update system on a medical device has to be secure, has to be safe, and has to be impossible to turn into a weapon, simultaneously. It is one of the hardest things in the build, and it exists entirely in service of a promise about the future.

## The hardware pins you to the physical world

It is easy, deep in the software, to forget that the thing is a physical object with a power supply, sitting near a patient, surrounded by other equipment that does not care about your architecture. The IEC 60601 family exists to remind you.

Basic safety and essential performance under 60601-1 is the floor. Electromagnetic compatibility under 60601-1-2 is where a lot of elegant connectivity features go to be humbled: your radio radiates, and it also has to keep functioning when the electrosurgical unit two beds over floods the room with noise. Usability engineering and alarm behavior have their own standards and their own unforgiving logic. None of this yields to a clever refactor, because none of it is software. The hardware nails you to the physical world and its laws, and physics has never once accepted a pull request.

## Spend your novelty deliberately

Put it all together and the shape of the problem becomes clear. In this field you are never building one thing. You are building three at once: the device, the evidence that the device is safe and effective, and the machinery to keep it both for a decade — and all three have to stay coherent with one another. Novelty taxes every one of them, non-linearly, because novelty is precisely the thing that strips away precedent, field history, and established method from each.

Which leads to the discipline nobody puts on a slide: you cannot afford to be novel everywhere. Novelty is a budget, not a virtue. The teams that actually ship are not the ones that are new in the most places. They are the ones that were new in exactly the right places — the two or three where the novelty is the whole point, where it creates the differentiation that justifies the program's existence — and were disciplined enough to be aggressively boring everywhere else. The proven part with a decade of field history. The established pattern. The standard interface. The open-source component with a real track record and a clean license.

Innovation in a regulated environment is as much about what you refuse to reinvent as what you invent. Every place you choose the boring, qualified, precedented building block is a place you get to keep your novelty budget for where it matters. Spend it carelessly, be new in a dozen places at once, and you will drown — not in engineering, but in evidence.

The constraints do not make any of this easy. They are not supposed to. They exist because the thing we are building ends up connected to someone who is out of other options and cannot audit our work, and who is trusting, without knowing it, that we did the hard, unglamorous, non-linear part instead of just the demo.

Getting it to work was never the hard part. Earning the right to put it near them is the whole job. And it is worth doing right.
