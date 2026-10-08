<p align="center">
  <img src="assets/WolfPack_Header.png" alt="WolfPack — One XO, many windows. Human direction, machine cognition, checked outcomes." width="100%">
</p>

# WolfPack

**One XO, many windows.**

[In practice](#the-project-in-practice) · [Architecture](docs/architecture.md) · [Selected work](docs/engineering-work.md) · [Roadmap](docs/roadmap.md)

WolfPack is my personal AI and automation project: an operating environment for getting useful work done with machine cognition across computers, tools, and interfaces.

I'm [Onur Siper](https://github.com/siperonur). My background in technical delivery, application management, and service ownership shapes how I approach the project: make responsibilities clear, understand dependencies, control unnecessary complexity, and follow through until the work is actually complete.

> **Minimal mechanism. Explicit context. Observable outcomes.**

## The idea

Useful work rarely fits inside one conversation. It moves between devices, documents, applications, and decisions. WolfPack explores how an assistant can follow that work without losing its context—or acquiring unlimited authority along the way.

At its center is **XO**, short for **Executive Officer**. The name borrows from the relationship between a commander who sets the mission and an executive officer who organizes its execution. In WolfPack, I define the objectives and boundaries; XO translates them into practical steps, carries out approved work, and checks the result.

XO is the supervisory role, not a particular model or chat window. Models provide cognition; the agent harness provides execution; project-owned context preserves decisions and operating knowledge between conversations.

## The project in practice

The operating foundation brings together:

- **Desktop, mobile, and messaging access** to the same assistant runtime, so changing an interface does not mean starting the work again.
- **Text and file interaction through Telegram**, with a restricted transport and responses tied to the relevant conversation.
- **Visible, operator-started browser workflows** for approved research and interaction, leaving authentication and personal attestations with the human.
- **Git-backed project context and recovery**, using versioned decisions, runbooks, and tested repository restoration rather than relying on conversation history alone.

A Job Search research workflow put these pieces together: I started from mobile messaging, XO evaluated public opportunities against private career context, and I continued on a portable workstation with the recommendations intact. A skills gap and a closed advertisement became recorded decisions rather than reasons to repeat the research.

[Explore the engineering work →](docs/engineering-work.md)

## How the pieces fit

![Functional architecture: human direction sets scope; interfaces connect to XO; permitted tools, cognitive resources, and durable context support the work.](assets/WolfPack_Architecture.svg)

These are functional roles, not a map of the deployment. The important distinction is between talking to the assistant, giving it authority, and maintaining the state it needs to work responsibly.

Persistence comes from deliberately maintained context. It does not depend on pretending that one conversation can remember everything forever.

[Architecture](docs/architecture.md) · [Operating model](docs/operating-model.md)

## Engineering, not reinvention

WolfPack uses **Pi** as its current agent harness, existing models for cognition, **Telegram** for messaging, and standard operating-system, connectivity, and **Git** primitives for the surrounding environment.

The project-specific work sits around those foundations: the operating contract, small integrations, privilege boundaries, context discipline, and verification procedures. Choosing what not to build is part of the engineering.

The Household use case illustrates this. An early custom approach did not meet the project's reliability requirements. I adopted **Home Assistant** as the native household foundation, simplifying the implementation while preserving the intention to connect XO later as a language and coordination interface.

That division lets the native platform own lists, calendar state, and reminder mechanics. The intended contribution of XO is interpretation and coordination—not rebuilding those mechanics around a model.

[Household: a simpler foundation for XO](docs/engineering-work.md#household-a-simpler-foundation-for-xo)

## What I'm exploring next

The next questions are practical: how to connect XO to useful native systems, improve durable context, and select cognitive resources without increasing operating cost and complexity unnecessarily.

Temporary cognitive workers and automated resource selection remain possible directions. They should earn their place through a useful task, not through an elaborate agent roster.

I also plan to discuss selected use cases through [**Signals**](https://signalsbyonursiper.substack.com/)—connecting opinions about machine cognition to actual decisions, implementations, and lessons. GitHub will hold the technical reference; the writing can explore why a choice mattered.

## Explore further

- [Selected engineering work](docs/engineering-work.md)
- [Architecture](docs/architecture.md)
- [Operating model](docs/operating-model.md)
- [Design principles](docs/design-principles.md)
- [Security model](docs/security-model.md)
- [Roadmap](docs/roadmap.md)
- [Professional portfolio](https://portfolio.onursiper.chatgpt.site/)

This repository contains curated public documentation and case studies. The private operational environment is maintained separately; this is not a packaged installation of WolfPack.

## Project information

Created and maintained by **Onur Siper**, with XO carrying out authorized implementation and verification work.

For security concerns, see [SECURITY.md](SECURITY.md).

No open-source license has been selected. Copyright remains with the repository owner; absence of a license does not grant permission for unrestricted reuse, modification, or redistribution.
