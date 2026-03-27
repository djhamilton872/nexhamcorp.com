---
layout: post
title: "AI Agent Teams Are Having a Moment. We've Been Running One for Months."
date: 2026-03-27
description: "A new tool called Paperclip hit 30,000 GitHub stars in three weeks with the promise of 'zero human companies.' We built something like it from scratch before any of this had a name. Here's what we learned."
author: Darren Hamilton
---

A tool called Paperclip launched in early March and hit 30,000 GitHub stars in under three weeks. The pitch: give your AI agents an org chart, goals, and budgets, and watch them run your company with zero human intervention.

The tech press is calling it a new category. Gartner logged a 1,445% surge in multi-agent system inquiries between Q1 2024 and Q2 2025. IDC says AI agents will be embedded in 80% of enterprise workplace applications by the end of this year. The AI agent market is projected to grow from $7.84 billion to $52.62 billion by 2030.

Everyone's acting like this just became real.

We've been running an AI agent team in production for months. Not as a proof of concept. As the actual operating structure of NexHam. And what I can tell you is: the moment is real, but most of the coverage is missing the point.

<!--more-->

## What We Built — and Why We Built It That Way

NexHam runs on three distinct AI agents, each with a defined role, a defined scope, and hard rules about what they don't touch.

One agent owns all product engineering. It writes code, manages deployments, reviews its own work, and escalates to me when a decision exceeds its authority. It does not touch marketing content. It does not touch infrastructure config. It does not make product decisions without flagging them first.

One agent owns infrastructure. Container operations, monitoring, system-level configuration. When the engineering agent needs an infrastructure change, it sends a message. The infrastructure agent handles it. They don't step on each other because they can't — the role boundaries are enforced in their operating context, not just suggested.

One agent handles everything else I'd call Chief of Staff work: marketing execution, email monitoring, project management, research, documentation, process improvement. It writes and publishes blog posts like this one. It manages a social media queue. It tracks open tasks across the whole team and reports to me daily.

I sit at the top. I make the calls that matter. I don't manage the day-to-day.

We didn't build this because Paperclip told us to. We built it because the alternative — one generalist AI agent trying to do everything — didn't work. A single agent that builds your software, manages your servers, writes your marketing copy, handles your email, and tracks your tasks is a context management nightmare. It loses track of things. It confuses domains. It makes decisions it shouldn't because nothing tells it not to.

Specialization fixed that. Clear roles, clear ownership, clear escalation paths. Same reason you don't have your head of engineering also run payroll.

## What the Tools Are Getting Right — and What They're Missing

Tools like Paperclip are formalizing something real. Org charts for AI agents. Defined budgets. Task queues. Approval gates. These are the right primitives.

But here's what I don't see in the demos: the startup problem.

AI agents don't remember yesterday. Every session starts cold. When my engineering agent opens a new session, it doesn't automatically know what it was working on, what decisions were made last week, or what changed in the codebase overnight. If you don't have a system for loading the right context at startup — layered, specific, role-aware context — your multi-agent team will contradict itself, repeat work, and lose track of everything the moment something complex spans more than one session.

We solved this with a boot protocol. Every agent runs a defined startup sequence: load role identity, load operational state, read the task tracker, check for messages from other agents, scan the knowledge base for anything relevant to the current work. It takes a couple of minutes. It makes the difference between an agent that picks up where it left off and one that starts from scratch every time.

The second thing missing from most tool demos: accountability infrastructure. When an agent completes a task, it updates the shared task tracker immediately. Not at the end of the session. Not "when it remembers." The update is the commit. If the tracker still shows a task as open, it isn't done. This sounds obvious. It's harder to enforce than you'd think, and it's the thing that falls apart first when teams scale.

The third thing: write ownership. Multiple agents reading a shared knowledge base works great. Multiple agents writing to a shared knowledge base creates conflicts, duplicates, and drift. We designate one agent as the sole writer for shared context. Others can request updates through messaging, but they don't write directly. Clean inputs in means clean context out.

## What This Means if You're Thinking About Deploying AI Agents

The tools are getting good fast. You can spin up a Paperclip instance in an afternoon. That's not the hard part.

The hard part is designing the operating model. Which roles do you actually need? What does each agent own, and what does it explicitly not touch? What's the startup protocol? How do agents communicate across sessions? What decisions require human approval and what can run autonomously? What does your escalation path look like when something breaks?

These are organizational design questions, not software questions. And most organizations I talk to have never had to answer them before, because they've never managed employees who don't have persistent memory and can run twenty tasks in parallel.

## The Opportunity Right Now

We're at the point in this curve where the technology is real but the organizational knowledge hasn't caught up. Most businesses are either ignoring this entirely or running single-agent experiments that don't scale. The ones who build the operating model right — now, while the tools are maturing — will have a significant head start.

NexHam has proven this works. The lessons from building and running our own AI team are the foundation of what we bring to clients. Not a framework. Not a demo. A tested playbook for deploying AI teams that operate like disciplined employees from day one.

If you're thinking about what a real AI agent deployment looks like inside your organization — not a chatbot, not a single automation, but an actual operating team — [let's talk](mailto:hello@nexhamcorp.com).
