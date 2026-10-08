# Security model

WolfPack's security approach is practical: limit unnecessary access, separate responsibilities, retain human control at sensitive boundaries, and understand how important state can be recovered.

Public explanations describe the design, not the operational deployment. Functional roles are enough to discuss the architecture without publishing machine identifiers, addresses, accounts, or access instructions.

## Separate interaction from authority

Access to an interface does not grant every capability of the host behind it. Conversational access, bounded browser interaction, Git publication, and deliberate administration have different responsibilities and should use appropriately scoped identities.

Network reachability is only connectivity. Modification authority depends on the identity and the approved work.

## Keep authentication human-controlled

Passwords, MFA, passkeys, recovery material, CAPTCHA, and personal attestations remain direct human actions. XO may prepare a workflow and navigate to a boundary without taking custody of authentication values.

Credentials and session state stay outside repositories and public evidence. A private repository is not automatically suitable custody for secrets.

## Give transports narrower responsibilities

Messaging validates allowlisted input, exchanges bounded envelopes, and associates responses with requests. Its token custody is separated from the assistant process; it does not receive the assistant's Git or session authority.

Browser interaction is visible and operator-started, using a dedicated environment. Authorization applies to the workflow, not to any account or page that happens to be reachable.

## Classify data deliberately

- **Public:** architecture, selected engineering material, and examples with explanatory value.
- **Private:** operational configuration, internal runbooks, personal work records, and detailed evidence.
- **Protected authentication state:** credentials, private keys, cookies, tokens, and recovery secrets in their appropriate custody.

Publication considers combinations of details, not just individual secret patterns. Screenshots, links, filenames, and prose can reveal more together than they do separately. `.gitignore` is a convenience, not a security boundary.

## Verify boundaries and recovery

Security checks exercise both the intended operation and relevant denied operations. Publication includes content review and repository-history considerations. Recovery uses standard formats and disposable restoration where appropriate.

Independent copies matter when they escape the original failure domain. Freshness and the scope of what was restored matter just as much as the existence of another copy.

## Practical trade-offs

Cloud cognition processes deliberately supplied content outside the purely local environment. External messaging and hosting providers introduce their own availability and account dependencies. Privileged host administration remains a powerful boundary.

Those trade-offs are evaluated in context rather than hidden behind a claim of perfect isolation. Access controls, sensible maintenance, protected custody, and recovery remain necessary even when public disclosure is careful.

## Reporting a concern

See [SECURITY.md](../SECURITY.md). Do not include credentials or private operational details in a public issue.
