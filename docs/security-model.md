# Security model

WolfPack is a personal engineering environment, not a classified or safety-critical system. Its security model aims for practical least privilege, visible human control at sensitive boundaries, and recovery from realistic failures.

## Security objectives

- Keep credentials and authentication state out of Git and public documentation.
- Prevent an external transport from becoming an unrestricted shell.
- Keep machine reachability separate from modification authority.
- Limit delegated Git identities to their intended repository operations.
- Preserve human control over account recovery and strong authentication.
- Keep public, private operational, and local-only data deliberately separated.
- Make consequential actions and recovery outcomes observable.

## Trust boundaries

### Human authentication

Passwords, MFA, passkeys, hardware keys, recovery codes, CAPTCHA, and legal attestations remain Commander interactions. XO may navigate up to the boundary but must not request, inspect, copy, or retain those values.

### Machine authority

Bastion, Command, Overwatch, Scout, and Raider have different responsibilities. Connectivity does not imply authorization. Normal interaction identities are separated from broader administration paths where practical.

### Messaging

Messaging is an external transport. Accepted messages are allowlisted, validated, represented as bounded envelopes, and correlated with responses. Token custody is separated from the general assistant runtime. The transport does not expose a public webhook, general command execution, or a second XO.

### Browser control

Browser capability is visible and operator-started. It uses a dedicated profile and narrow temporary connection. Credentials and human-verification challenges stay with Commander. A click is not treated as proof of an external outcome.

### Git and publication

The operational repository remains private and locally authoritative. Its private GitHub mirror is non-authoritative. The public repository was initialized independently so sensitive operational ancestry was never imported and then “cleaned up.”

## Data classification

### Public

Public architecture, engineering rationale, honest status, safe diagrams, selected examples, limitations, and roadmap.

### Private

Operational configuration, detailed topology, internal runbooks, ordinary personal records, private logs, and evidence that does not belong in public.

### Local-only protected state

Passwords, tokens, private keys, session and cookie stores, recovery codes, authentication databases, and equivalent secrets. These do not leave their approved custody merely because a private repository exists.

## Verification approach

Security work uses both positive and negative checks. Examples include verifying that an intended operation succeeds while proving that the same identity cannot access unrelated credentials, administrative commands, runtime sessions, or repository modifications.

Repository publication adds content and reachable-history review, sensitive-pattern scanning, ref inspection, anonymous-access checks, and comparison of authoritative and mirrored commit IDs.

## Known limitations

- A sufficiently privileged host administrator can access local runtime state.
- Cloud model use means intentionally supplied content is processed outside the purely local machine boundary.
- GitHub Free does not provide every advanced private-repository security or branch-control feature.
- Pattern scanners reduce risk but cannot prove that arbitrary prose contains no sensitive information.
- Human judgment remains necessary for privacy classification and consequential external actions.

## Reporting a vulnerability

Please follow the instructions in [SECURITY.md](../SECURITY.md). Do not place credentials, private operational details, or exploit material in a public issue.
