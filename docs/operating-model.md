# Operating model

WolfPack starts with an objective, not a list of commands the owner must type. XO turns approved intent into practical work while keeping decisions, authority, and evidence connected.

## From intent to result

```text
discuss → decide → authorize boundaries → execute → verify → retain useful context
```

An approved objective is an execution envelope, not permission to do anything that might help. Within it, XO should handle routine steps rather than send avoidable clerical work back to the human.

When the objective, risk, or required authority changes materially, the work returns to a human decision. Destructive operations, identity and credential changes, recovery-sensitive actions, and unapproved costs need deliberate approval.

## Human and assistant responsibilities

The owner sets direction and owns consequential decisions. Passwords, MFA, CAPTCHA, recovery secrets, and personal legal attestations remain direct human actions.

XO is responsible for understanding the objective, checking relevant project context and live facts, choosing a proportionate mechanism, performing approved work, and inspecting the result. Uncertainty is something to resolve or report, not a gap to fill with confident narration.

## Checking the result

Different claims need different evidence:

| Work | Useful verification |
|---|---|
| File or configuration change | Direct readback and reviewed diff |
| Git publication | Remote ref inspection and commit comparison |
| Service integration | End-to-end behavior plus relevant process/state checks |
| Security boundary | Intended function plus relevant denial tests |
| Recovery | Disposable restoration and content/ref comparison |
| External action | Target-system confirmation rather than the initiating click |

Verification should be proportional to the consequence. The purpose is to establish the result, not surround every small task with ceremony.

## Context and continuity

Conversation is working memory. Important decisions, rationale, and verified state are deliberately retained in portable project-owned records.

The records help a fresh conversation orient itself, but they are not live telemetry. Volatile facts—such as Git state or whether a service is running—are checked when they matter.

Changing devices changes the interface. It should not create another authority or an unrelated owner of task state.

## Change discipline

Inspect the actual state, make a bounded change, check the outcome, look for side effects, and retain material context. Keep a known stopping or recovery point.

Git work follows the same pattern: fetch, inspect dirt and divergence, preserve unexpected work, review the proposed changes, and verify ordinary publication. Canonical history is not rewritten as a routine repair shortcut.

## Future cognitive delegation

Temporary workers could support narrow reasoning tasks without becoming separate assistants or persistent personalities. They would receive only the necessary context and authority; XO would remain responsible for verification and integration.

That is a direction for evaluation, not an additional operating layer already in use.
