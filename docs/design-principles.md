# Design principles

## 1. Minimal mechanism

Use the smallest mechanism that solves a demonstrated problem. New services, databases, frameworks, and layers are liabilities until their value exceeds their operational and removal cost.

## 2. Explicit context

Machines, repositories, identities, data classes, and authority boundaries are named explicitly. “The server,” “the agent,” or “the repo” is insufficient when several exist.

## 3. Observable outcomes

AI narration is not evidence. Filesystem state, Git refs, configuration reads, process inspection, protocol responses, checksums, tests, and target-system confirmations are evidence.

## 4. Bounded autonomy

Commander authorizes objectives and boundaries; XO performs routine in-scope execution. Escalation is reserved for ambiguity, destructive action, identity or credential changes, material risk, authority gaps, or changed intent.

Bounded autonomy is intended to reduce human clerical work without erasing human authority.

## 5. One XO, many windows

Interfaces are access paths to one supervisory identity. A new device, transport, session, or model must not silently create another authority or competing memory owner.

## 6. Replaceable cognition

Models and providers are selected resources. Model identity must not become XO identity. Cost, quota, latency, privacy, tool support, task difficulty, reliability, and reversibility are engineering inputs.

## 7. Least necessary privilege

Reachability is not authorization. Each identity receives only the machine, repository, command, data, or transport access needed for its function. Authentication boundaries remain with the human where automation would create disproportionate risk.

## 8. Durable state is deliberate

Context windows are volatile working memory. Decisions, verified state, rationale, and provenance are promoted intentionally into portable project-owned state. Saving everything indiscriminately is not a memory architecture.

## 9. Verification proportional to risk

Low-risk claims can use lightweight checks. Security changes, repository publication, recovery, and externally consequential actions require stronger and preferably independent evidence.

## 10. Recovery is part of design

Important state must have an understood loss consequence and a tested recovery path. Easily reconstructed state does not need ceremonial redundancy; irreplaceable state should not rely on one failure domain.

## 11. Economics are architecture

Money, quota, compute, storage, latency, attention, privacy exposure, and reasoning effort are resources. The strongest or most expensive option is not automatically the correct default.

## 12. Removal pain matters

Before admitting a component, ask how it is removed, replaced, migrated, or rebuilt. Opaque state, proprietary coupling, credential sprawl, and unclear exit paths are design costs even when initial setup is easy.

## Component admission questions

A proposed component should answer:

1. What demonstrated problem does it solve?
2. Which WolfPack asset owns it?
3. Must it run continuously?
4. What data does it own?
5. How is that data backed up or reconstructed?
6. How does XO access it?
7. What permissions does it require?
8. How is correct operation proved?
9. What does it cost?
10. Does Pi or an existing component already solve the need?
11. Does it reduce Commander workload?
12. How painful is it to remove or replace?
