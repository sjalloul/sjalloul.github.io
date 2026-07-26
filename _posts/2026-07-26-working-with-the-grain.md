---
layout: post
title: "Working With the Grain"
category: "Thought Leadership"
description: "What a woodworking shop teaches about building teams and changing architecture — and the one place the analogy breaks, which turns out to be the most useful part."
date: 2026-07-26
---

### What a woodworking shop teaches about building teams and changing architecture

There is a moment in every woodworking project that has no equivalent in a spreadsheet. You have milled your boards, cut your joints, spread the glue, and now you have roughly ninety seconds before the glue skins over and your decisions become permanent. You clamp, you check for square, you wipe the squeeze-out, and you live with what you built. The clock is the whole point. It forces you to have rehearsed.

I keep coming back to the shop when I think about software, and specifically about the two hardest parts of the job that have nothing to do with writing code: building a team of people, and changing the architecture underneath them while the thing is still running. The comparison is easy to make badly — most craft-and-code metaphors are just decoration — so it is worth being honest up front about where it holds and where it falls apart. It falls apart in an important place, and that place turns out to be the most useful thing in the whole analogy.

## The grain runs through everything

Wood has grain: a direction the fibers run, established while the tree was alive, that you did not choose and cannot change. You can work with it or against it. Plane with the grain and the surface comes up clean and bright. Plane against it and you get tearout — the fibers lift and splinter ahead of the blade, and no amount of effort fixes the torn patch afterward. Experienced hands read the grain before every cut, and when a board wants to be worked in a particular direction, they turn the board rather than fight it.

Codebases have grain, and so do organizations. The grain of a system is the set of assumptions baked in early, when it was young and green: how modules talk to each other, where state lives, which team owns which seam. The grain of an org is subtler and stronger — who actually makes decisions, which reorg left scar tissue, what the last failed migration taught everyone to fear. You can push a change against all of that, and sometimes you have to, but you should know that is what you are doing. Most of the tearout I have seen in engineering organizations came from a technically correct change shoved through against the grain of how people actually worked. The design review approved it. The org rejected it anyway, quietly, over the following six months.

Reading the grain first is not caution for its own sake. It is how you decide which board to turn.

## Joinery is where the team actually lives

A piece of furniture is not defined by its boards. It is defined by its joints — the mortise and tenon, the dovetail, the way one piece receives another. A beginner obsesses over the flat faces you can see. A joiner obsesses over the surfaces that will be hidden forever inside the joint, because those are what bear the load and decide whether the thing survives a decade of use.

This is the truest parallel to team building I know. The individual talent on a team is the boards. The joinery is the interfaces between people and between the systems they own: the API contracts, yes, but also the handoffs, the shared definitions of done, the agreements about who owns what when something breaks at 2 a.m. Strong teams are not collections of strong engineers. They are collections of engineers connected by well-cut joints, where the load passes cleanly from one person's work into the next without a gap you have to fill later with the software equivalent of wood filler.

And like joinery, the good stuff is invisible when it works. Nobody admires a dovetail on a drawer they never open. Nobody notices the interface contract that quietly prevented an integration disaster. The temptation, always, is to spend your attention on the visible faces — the demo, the org chart, the headcount — and let the joints stay loose because loose joints do not fail on the day you cut them. They fail two years later, all at once, and by then the piece is in someone's living room.

## Design for movement, or watch it crack

Here is the thing beginners never believe until a tabletop splits: wood moves forever. It expands across the grain when the air is humid and contracts when it is dry, seasonally, for the entire life of the object. A tabletop screwed rigidly to its base along its whole width will tear itself apart within a couple of years, because the top wants to move and the screws will not let it. There is no glue strong enough to win that fight. The wood always wins.

So woodworkers design for movement. Breadboard ends are attached so the panel can slide within them. Cabinet backs float in grooves rather than being nailed solid. Tabletops are fastened with clips or slotted brackets that hold firmly in one direction and let the wood breathe in the other. The craft is not preventing movement. It is anticipating it and building the accommodation in from the start.

This is the entire discipline of managing architectural change, compressed into a physical law. A system will change — the requirements will move, the load will grow, the compliance landscape will shift, the acquisition will happen. An architecture that is fastened rigidly to today's assumptions will not gracefully accommodate that movement; it will crack, usually at the seam you reinforced most confidently. The value of a good architect is not that they stop the movement. Nobody can. It is that they build the slotted brackets in advance: the abstraction boundary that lets you swap the vendor, the versioned interface that lets two halves of the system evolve at different speeds, the migration path designed before anyone needs it. You are not designing the system. You are designing the system's capacity to become a different system without being rebuilt.

The architect who insists on rigid fastening because it is simpler and tighter *today* is the one whose tabletop splits.

## The glue-up, and why you dry-fit

Which brings me back to the ninety seconds. Before any real glue-up, a competent woodworker does a dry fit: assembles the whole thing with clamps and no glue, checks that every joint closes, that the frame comes up square, that they have enough clamps within reach and in the right order. The dry fit is where you discover that this tenon is a hair too fat, or that you will need three hands you do not have. You fix it while fixing is free. Then you glue, and the rehearsed sequence protects you from the clock.

Large architectural changes have the same shape and too rarely get the same respect. A migration, a cutover, a coordinated release across teams — these are glue-ups. There is a window during which the system is half-assembled and committed, and the working time is short. The dry fit is the staging environment, the rehearsal, the runbook you walk through before the day. Teams that skip it are not being bold; they are gluing up a complicated case piece for the first time, live, hoping their hands know a sequence they never practiced. Sometimes it works. The times it does not are the outages people name.

## The shared bench

The last parallel is about the room itself. A shop with more than one person needs norms that have nothing to do with skill: how you leave the shared plane, whether you put the marking gauge back at the same setting, that you sweep before the next person's turn. A clean shop is a safe shop — not a slogan, a fact about not tripping over an offcut while holding a chisel. The house style matters too. Every hand develops its own feel, but a shop that produces coherent work has a shared sense of what "good" looks like, usually taught the slow way, by a more experienced maker handing a junior a real piece to build and letting them own the outcome.

That is team building with the woodwork stripped off: shared hygiene, a legible house style, and the deliberate act of handing someone a load-bearing project not because it is the safe assignment but because ownership of something that matters is how a journeyman becomes a master. You cannot lecture that into a person. You give them the piece and stay close enough to catch a real mistake.

## Where the grain runs out

Now the honest part, because it is the most important. Wood is a natural material with fixed properties. Its grain, its movement, its tolerances — these are given to you by physics, and they impose a discipline you did not have to invent. You measure twice because the material does not forgive. The constraint is a gift: it makes carelessness expensive immediately, so carelessness gets trained out of you fast.

Software has no such physics. It is the most malleable material humans have ever worked, and that is exactly the problem. There is no grain the universe forces you to respect, no glue clock that punishes a sloppy sequence within the hour, no tabletop that visibly splits when you fastened it wrong. You can ship the rigid design, the loose joint, the un-rehearsed cutover, and get away with it — for a while, sometimes a long while. The consequences are real but deferred, abstract, easy to discount.

So the discipline that wood imposes on the woodworker, software engineers have to manufacture for themselves. The review board, the interface contract, the staging rehearsal, the design-for-change abstraction — none of these are handed to us by the material. They are the artificial grain we agree to work with because we know that without it, the medium's infinite forgiveness is a trap. That is what a mature engineering culture actually is: a shop that chose to respect a grain that physics never forced on it, because the people in it learned the hard way what happens when nobody does.

Measure twice. Not because the wood makes you. Because you decided the work deserves it.
