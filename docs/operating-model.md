# Operating model

WolfPack combines natural-language intent with explicit authority and evidence requirements.

## Mission lifecycle

```mermaid
flowchart LR
    A[Commander intent] --> B[Orient on durable context]
    B --> C[Verify live facts]
    C --> D{Authority and scope clear?}
    D -- No --> E[Clarify or escalate]
    D -- Yes --> F[Execute smallest bounded step]
    F --> G[Verify resulting state]
    G --> H{Outcome proved?}
    H -- No --> I[Investigate, retry safely, or stop]
    H -- Yes --> J[Reconcile durable state]
    J --> K[Report evidence]
```

## Commander authority

Commander defines the outcome and risk envelope. Explicit approval is required when work materially changes scope, creates destructive or difficult-to-reverse effects, changes credentials or identity, threatens recovery, incurs unapproved cost, or crosses a trust boundary without existing authority.

Commander directly handles passwords, MFA, passkeys, security keys, CAPTCHA, recovery secrets, and legal attestations.

## XO responsibility

Within an approved mission, XO should not return avoidable clerical work to Commander. XO is responsible for:

- translating the request into bounded steps;
- selecting proportionate tools and reasoning effort;
- checking authoritative project context;
- distinguishing documented state from live telemetry;
- preserving unexpected local work;
- making and validating ordinary in-scope changes;
- reporting uncertainty rather than filling gaps with assumptions;
- maintaining a known stopping or rollback point.

## Evidence hierarchy

Evidence depends on the claim:

| Claim | Suitable evidence |
|---|---|
| File changed | direct read, metadata, checksum, and reviewed diff |
| Git publication succeeded | remote ref inspection and commit equality |
| Service works | process/service state plus an end-to-end behavior check |
| Recovery works | restoration into a disposable target and content/ref comparison |
| External action completed | target-system confirmation, not the initiating click |
| Security boundary holds | positive function test plus relevant denial tests |

Documentation is authoritative project context but not live runtime telemetry. A remembered success is historical evidence, not proof of current operation.

## Git discipline

Operational Git work begins by fetching the authoritative remote and inspecting the working tree, local branch, remote branch, and divergence. Dirty or divergent state is preserved and investigated rather than silently reset.

Before publication, XO reviews the diff, reruns relevant verification, fetches current canonical state, and proves the update is a normal fast-forward. Force-pushing canonical history is outside routine authority.

## Context and continuity

Conversation context is temporary cognition. Material decisions and verified state are promoted into concise durable files. Session handoffs transfer context and constraints; they do not grant new mission authority by themselves.

## Cognitive delegation

WolfPack may later let XO commission ephemeral workers for narrowly described tasks. A worker would receive only the necessary objective, context, tools, data, authority, budget, and evidence requirements. Its output would be input to XO—not proof—and XO would remain responsible for verification and integration.

This capability is not currently implemented as a WolfPack component.
