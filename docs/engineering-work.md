# Selected engineering work

WolfPack develops through practical use cases. These examples show how I approach integration, delegation, and implementation choices—and what working with machine cognition has taught me along the way.

## Continuing real work across interfaces

### The problem

A useful assistant should follow the work, not tie it to whichever screen happens to be open. Switching from phone to workstation should not create another assistant, lose the decisions already made, or repeat the research.

### The approach

I used a Job Search research task to exercise that idea. XO evaluated six public opportunities against existing private career context, retained source provenance, and produced recommendations. I started through mobile Telegram and continued on a portable workstation with two recommendations intact.

The continuation led to two decisions: one opportunity had a relevant skills gap; another was no longer accepting applications. Both were recorded in the project's private state.

Checks of the shared runtime and session supported the continuity result. More importantly, the task state survived the change of interface: we continued the work rather than merely resuming a greeting.

### What I learned

Continuity has several parts: access to the same runtime, preservation of useful context, and a result that still makes sense when the work resumes. Giving several interfaces the same assistant name does not establish any of those things by itself.

This example concerns research and decision support. Application preparation and submission are distinct workflows with their own approval boundaries.

## Messaging without a second assistant runtime

### The problem

Mobile text and files needed to reach the existing assistant without turning the messaging interface into a separate agent or handing it the assistant's broader privileges.

### The approach

A restricted transport connects Telegram to an extension inside the existing Pi process. The transport handles validated input and delivery; the extension manages incoming work and responses associated with the relevant request. The bot credential stays outside the assistant process.

Restart deduplication, busy queueing, and bounded failure handling are part of the integration. Tests and live interaction exercised delivery, response correlation, and the separation between transport and assistant authority.

### A useful failure

An attachment-handling defect exposed a conflict between directory creation and service hardening. Rather than relax the security boundary, the repair removed unnecessary per-update directory creation and used an already provisioned shared location. Fresh text and document delivery checks confirmed the repaired path.

### What I learned

Security restrictions are not always an obstacle to work around. Sometimes they reveal an operation the design did not need in the first place.

The value of this integration is not another chatbot. It is a convenient window into the existing assistant, with a deliberately narrower responsibility.

## Household: a simpler foundation for XO

### The problem

The household use case is straightforward: to-do and shopping lists, a calendar, and reminders. The original approach put a custom gateway, model-mediated tools, and deterministic local state at the center of the implementation.

### What changed

The custom work included source implementation, local tests, and a model qualification benchmark. The complete benchmark covered three candidates across 52 fixtures with three repetitions per candidate. None met the accepted reliability requirements; further focused work did not establish a qualified implementation.

That made the implementation path worth reconsidering—not the household objective or the wider WolfPack idea.

### The decision

I adopted **Home Assistant** as the native household foundation. It now supplies the lists, local calendar, reminder automation, and household dashboard. Browser workflows exercised list and calendar operations with reloads; mobile use and notification checks supported the practical usability work.

This reduced the amount of custom software between a household need and a useful result. It also gave the future XO connection a clearer purpose.

### Where XO fits next

The intended next layer is a language and coordination interface: interpreting requests, connecting relevant context, and organizing approved actions against a deterministic backend. Home Assistant would continue to own household state and scheduling.

That integration is future work. The change in foundation makes it easier to reason about what XO should contribute, rather than assuming cognition belongs inside every operation.

### What I learned

Keep the outcome stable while allowing the implementation to change. Choosing an existing platform is not a retreat from engineering; it can be the engineering decision that makes the larger system more useful.

## From use case to discussion

These are also the kinds of experiences I plan to bring into [**Signals**](https://signalsbyonursiper.substack.com/): what we wanted to achieve, what the implementation taught us, and which assumptions changed. The technical account and the broader discussion should support each other.

Public case studies describe the work and its reasoning. Detailed operational evidence and private records remain in the project's internal documentation.

[Back to WolfPack](../README.md)
