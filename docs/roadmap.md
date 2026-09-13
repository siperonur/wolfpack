# Roadmap

WolfPack's roadmap is evidence-led. Items move from idea to experiment to accepted capability only after a demonstrated need and observable verification.

## Operational now

- One persistent XO role hosted through stock Pi on a dedicated runtime.
- Workstation, portable, mobile, and messaging access to the same XO.
- Explicit Commander/XO authority boundaries and bounded mission execution.
- Command-authoritative operational Git with tested independent recovery and a private off-machine mirror.
- Restricted, correlated messaging for text and files without a public inbound service.
- Visible, operator-started browser interaction with human-controlled authentication boundaries.
- Git-backed architecture, status, runbooks, evidence expectations, and historical checkpoints.
- Real cross-interface mission continuity demonstrated without creating a second XO runtime.

## Partially implemented or experimental

- Public documentation and architecture are established; safe implementation material will be selected deliberately rather than copied wholesale.
- Provider and model replaceability is an architectural requirement, but the current live resource pool is intentionally small.
- Durable state is Git-backed where appropriate, while broader memory requirements remain under study.
- Browser workflows are bounded and supervised rather than general unattended automation.
- Economic and reasoning-effort policy exists, but automatic routing has not been implemented.

## Near-term direction

1. Curate small implementation examples whose public value exceeds their privacy and maintenance cost.
2. Publish reproducible verification examples for bounded Git, transport, and recovery claims without exposing operational topology.
3. Improve continuity and provenance while keeping durable memory portable and understandable.
4. Evaluate a thin ephemeral-worker experiment using Pi primitives before building custom orchestration.
5. Continue using real missions as benchmarks, with explicit authority and outcome evidence.

## Longer-term questions

- What durable memory is actually useful beyond curated Git state?
- Which tasks benefit from temporary cognitive delegation rather than active XO model switching?
- How should cost, quota, latency, privacy, and risk influence cognitive-resource selection?
- Which capabilities should remain operator-started instead of becoming continuous services?
- What is the smallest recovery design that survives loss of the current runtime without creating secret sprawl?

## Explicit non-goals

- A persistent hierarchy of named autonomous agents.
- Unattended authority over credentials, account recovery, or destructive operations.
- Infrastructure introduced only to imitate an enterprise platform.
- Publishing sensitive operational configuration for the sake of reproducibility.
- Claiming general autonomy, production readiness, or guarantees the project has not demonstrated.
