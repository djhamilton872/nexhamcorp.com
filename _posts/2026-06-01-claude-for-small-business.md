---
layout: post
title: "What Anthropic's Claude for Small Business Gets Right (And What It Misses)"
date: 2026-06-01
description: "Anthropic launched Claude for Small Business on May 13 with prebuilt connectors for QuickBooks, HubSpot, and Canva. The prebuilt layer is a real step forward. But there's a gap between what the connectors give you and what a custom implementation can do — and that gap is where the actual competitive advantage lives."
author: Darren Hamilton
---

On May 13, Anthropic launched Claude for Small Business — prebuilt agentic workflows wired into QuickBooks, PayPal, HubSpot, Canva, DocuSign, and Google Workspace. The pitch is that 33 million small businesses can now access the kind of AI automation that enterprises have been deploying for the past year.

That's a real step forward. But there's a gap between what the prebuilt connectors give you and what a custom implementation can do. That gap is where the actual competitive advantage lives, and it's worth understanding before you decide how much to lean on the out-of-the-box solution.

<!--more-->

## What the launch gets right

The connector strategy is sound. Most small businesses aren't going to write Python. They don't want to think about MCP servers or API authentication. They want to open Claude, say "chase the overdue invoices from last month," and have it work.

QuickBooks and HubSpot connectors handle the authentication problem that kills most AI integrations before they start. Getting Claude authorized to read and write data in your business systems is genuinely hard to set up from scratch. Anthropic is absorbing that complexity for you, which has real value.

The SMB Tour — free half-day workshops in ten cities — is a smart distribution move. This is a tool that rewards hands-on exposure. Watching Claude chase an invoice, draft a follow-up, and log the interaction in one prompt is more convincing than any product page.

## Where it falls short

The prebuilt workflows are general-purpose. They're built for the median small business, not yours.

Here's a concrete example. The HubSpot connector can handle "summarize my open deals and draft follow-up emails." That's useful. But if your sales process has a specific qualification step, a particular follow-up cadence, or terminology that matters to your industry, the general workflow doesn't know any of that. It produces correct but generic output.

The businesses getting the most out of Claude right now are the ones who have spent time teaching it how they specifically work — what their customer segments are, what their standard objections sound like, what their contracts require, what "done" means for their team. That context doesn't come with the connector. You have to build it.

There's also a ceiling on what the prebuilt layer can orchestrate. Single-step tasks — draft this, summarize that — are well-served. Multi-step autonomous workflows — research a prospect, pull their deal history, draft a customized proposal, and route it for approval — require more architecture than a connector provides. That's where the gap between a template and a system becomes real.

## The practical split

Think of Claude for Small Business as covering the first 60 percent of what's possible. The connectors eliminate the setup friction and give you immediate productivity gains on routine tasks. For a business that hasn't used Claude at all, that 60 percent is a significant upgrade worth capturing quickly.

The remaining 40 percent — the workflows specific to your business, the multi-step automations, the institutional knowledge that makes output actually useful rather than just correct — requires implementation work. That's not a knock on the product. It's just the nature of custom software.

The question for any small business is whether the 60 percent is enough, or whether the processes you most need to automate are in the 40 percent. In my experience, the highest-value targets usually are.

## What this means if you're evaluating it now

Start with the prebuilt connectors and use them. The Anthropic onboarding path is well-designed and the time-to-value is fast. Document what you're doing manually that Claude doesn't handle well — those are your Phase 2 targets.

If you get to Phase 2 and find yourself looking at workflows that need customization, that's where a structured implementation helps. Not because the technology is hard, but because figuring out which workflows to build, in what order, with what context is a design problem as much as a technical one.

The launch is good news for small businesses. The prebuilt layer is a real floor, not a ceiling. Most operators will find they want to go higher.

---

*Darren Hamilton is the founder of NexHam, an AI consulting firm focused on Claude implementations for small and mid-size operators. [Book a session](https://nexhamcorp.com/#contact) if you want help designing what's past the prebuilt layer.*
