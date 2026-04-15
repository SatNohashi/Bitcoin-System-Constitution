# UX Constitution of Bitcoin System Constitution

**Author:** Satoshi Nohashi  
**License:** CC0 1.0 Universal (Public Domain Dedication)  
**Website:** [bitcoinsystemconstitution.org](https://bitcoinsystemconstitution.org)  
**Type:** Binding 
**Supports:** The Preamble and the user-facing implications of the Bitcoin System Constitution, especially the articles titled:
- Honest Risk Hierarchy
- Exit as a Right
- Transaction-Level Censorship Resistance
- Privacy as a Component of Financial Freedom
- Distinction Between Bitcoin, Claims, Utility Balances, and Credit
- Reserve Truth, Liability Truth, and Proof Cadence
- Reserve Custody Independence, Non-Unilateral Control, and Open Participation
- Plain Transferability and Voluntary Encumbrance
- Role of Layer 3
- Interlayer Coupling and Movement
- Long-Term Recoverability and Compatibility Continuity
- Dependence Must Remain Escapable
- Clarity to Users
- Scope, Extensions, Compliance, Naming, and Voluntary Applicability

**Definitions:** Uses Article I definitions exclusively, particularly: constitutional layer, support system, bridge, canonical interlayer path, direct Bitcoin claim, credit instrument, plain transferability, voluntary encumbrance, strongest available security model, non-discretionary, ordinary transaction, ordinary user, custody structure, compliance, provisional custody, materially weakens 
**Status:** Draft 

## Purpose

This document defines required wallet-level, interface-level, and user-facing behavior for systems claiming compliance with the Bitcoin System Constitution.

Its purpose is simple.

**The protocol constitution protects the rules. 
The UX constitution protects the user's ability to see those rules clearly.**

A system that is technically compliant but hides risk, blurs layers, confuses asset classes, buries exits, changes core money workflows carelessly, or nudges users into weaker trust models is not compliant in spirit and should not be treated as compliant in user practice.

This document is binding. It does not replace the protocol constitution. It applies the protocol constitution to what the user actually sees and does.

## Governing Principles

1. User-facing design must not weaken, blur, or contradict protocol-level protections.
2. A user must always be able to tell:
 - where they are
 - what they hold
 - what trust model they are in
 - what changes if they move
3. Convenience must not silently become capture.
4. Risk must be visible before commitment, not discovered afterward.
5. Self-custody, plain transfer, and downward exit must remain intelligible and accessible.
6. If there is ambiguity, the UX must resolve it toward:
 - clearer user understanding
 - stronger protection of user freedom
 - more honest disclosure of risk
 - less chance of mistaking weaker layers for stronger ones
7. Innovation is allowed. Concealment is not.
8. Core truth must be visible without reveal. Deeper mechanics may be revealable. Credit must never be hidden.

---

## Section 1. Warning Language and Risk Presentation

**Supports:** Honest Risk Hierarchy, Exit as a Right, Distinction Between Bitcoin, Claims, Utility Balances, and Credit, Role of Layer 3

### Rules

1. Risk must be communicated in plain language before a user commits value to a new layer, asset class, contract context, bridge, custody model, or trust model.
2. No interface may describe a system, balance, bridge, or custody arrangement as "safe," "guaranteed," "fully secure," or equivalent unless that claim is literally and constitutionally true.
3. Risk gradients shown to the user must match the constitutional hierarchy:
 - Bitcoin on Layer 1 must not be visually equated with weaker higher-layer representations.
 - Transactional balances, utility balances, gas tokens, governance tokens, and credit instruments must not be presented as though they carry equal protections.
4. Warnings must identify the actual risk being taken, not generic caution language.
5. A warning must not be used as a substitute for clear system design. "Proceed at your own risk" does not cure deceptive UX.
6. If the user is entering a weaker trust context, the UX must say so plainly.

### Required minimum warning content when risk changes

At minimum, the UX must tell the user:
- what they are leaving
- what they are entering
- whether custody changes
- whether exit becomes weaker, delayed, or more conditional
- whether the asset changes class
- whether the move depends on a bridge, contract, operator, committee, or intermediary

---

## Section 2. Migration Prompts and Upgrade Confirmations

**Supports:** Governance, Mutability, and Ossification, Long-Term Recoverability and Compatibility Continuity, Successor Systems and Voluntary Migration

### Rules

1. Users must explicitly confirm before any change that alters:
 - trust model
 - custody model
 - recovery model
 - asset class
 - layer context
 - governance exposure
 - bridge dependency
2. No silent upgrade may change the effective risk properties of a user's balances or recovery assumptions.
3. Upgrade prompts must explain in plain language:
 - what is changing
 - why it is changing
 - whether the change is optional
 - whether the user may stay on the prior path
 - whether the change alters constitutional protections
4. No prompt may use artificial urgency, countdown pressure, fear-based manipulation, or "last chance" framing to push users into trust-model changes.
5. If a proposed upgrade would move the user into a successor system, that fact must be stated directly.
6. If an upgrade changes the process for sending, receiving, or moving between layers, the prompt must state whether the old process remains available.

### Forbidden patterns

- "Continue" buttons that mask a trust-model change.
- "Recommended" labels that steer users into weaker custody without equal disclosure.
- Hidden automatic migration to new contract logic, bridge paths, or recovery semantics.

---

## Section 3. Human-Readable Labels

**Supports:** Distinction Between Bitcoin, Claims, Utility Balances, and Credit, Clarity to Users

### Rules

1. All asset types must be labeled clearly and consistently.
2. Labels must distinguish at minimum:
 - Bitcoin on Layer 1
 - direct Bitcoin claim
 - Bitcoin transactional balance
 - Bitcoin utility balance
 - native gas or utility token
 - governance token
 - credit instrument
 - speculative asset
3. Protocol-level naming must match user-facing naming closely enough that the user is not misled by cosmetic rebranding.
4. No label may blur categories by using Bitcoin-like language for non-Bitcoin instruments without explicit qualification.
5. If a system uses non-standard layer names, the UX must still make the constitutional trust position understandable to a normal user.
6. Asset classification labels must persist across all screens where balances are displayed or actions may be initiated. Labels must be visible at the point of decision, including send, receive, bridge, stake, or any commitment action.

Labels must not:
- disappear after onboarding
- be reduced in visibility during normal use
- be replaced by ambiguous icons or branding

Asset classification is a permanent interface requirement, not an onboarding aid.

### Example

A system may call something:
- Settlement Rail
- Utility Zone
- Contract Context
- Layer 1.5
- Layer 4
- Layer 5

But the UX must still make clear:
- whether it is stronger, weaker, or simply different from the current context
- whether it is base-chain Bitcoin or not
- whether the user is holding money, claim, utility balance, gas token, governance token, or credit

---

## Section 4. Recovery Walkthroughs and Test Restore Flows

**Supports:** Long-Term Recoverability and Compatibility Continuity, Dependence Must Remain Escapable

### Rules

1. Self-custody systems must provide users with a way to verify that their recovery backup works without risking live funds.
2. Recovery procedures must be documented in plain language.
3. Recovery-critical metadata must be exportable in a way the user can actually understand and preserve.
4. No UX may imply that a seed phrase or backup is sufficient if additional hidden metadata is required to restore access.
5. No interface may rely on vendor lock-in as the normal or only recovery path.
6. If recovery assumptions change, the user must be explicitly informed before the change takes effect.

### Required recovery flow properties

- testable
- documented
- repeatable
- vendor-independent to the maximum extent possible
- honest about what is and is not backed up

---

## Section 5. Anti-Dark-Pattern Rules

**Supports:** Honest Risk Hierarchy, Clarity to Users, Dependence Must Remain Escapable

### Rules

1. No deceptive defaults.
2. No prechecked opt-ins for:
 - custody delegation
 - yield products
 - credit exposure
 - contract-based encumbrance
 - migration into weaker trust contexts
3. No visual manipulation that steers users toward riskier or more centralized options while hiding safer ones.
4. No burying of self-custody, plain transfer, or downward exit options.
5. No misleading color, icon, badge, or status system that suggests constitutional safety where it does not exist.
6. No "safety" language may be used merely because a product is popular, regulated, insured by a private party, or widely adopted.
7. No reveal control may be used to hide the fact that a user is entering credit, losing plain transferability, becoming custodial, or entering a weaker trust context.
8. Communications, including push notifications, emails, SMS messages, and in-app alerts, must adhere to the same anti-dark-pattern rules as the interface itself.

Such communications must not:
- use artificial urgency to pressure user action
- create fear-based decision-making
- steer users toward weaker trust models
- obscure the true nature of an action or change

Any communication prompting a user to:
- move funds
- change custody
- accept an upgrade
- enter a new context

must include clear disclosure of:
- the trust change involved
- the asset class implications
- whether the action weakens user control or exit rights

---

## Section 6. Context, Layer Position, and Relative Trust

**Supports:** Functional Layer Order, Honest Risk Hierarchy, Clarity to Users

### Rules

1. The user must always be able to see their current operational context.
2. The current context display must tell the user, at minimum:
 - what system or sub-system they are in
 - which constitutional layer or equivalent trust zone they are in
 - what asset class they currently hold
 - whether the current context is stronger, weaker, or simply different from the one below it
3. If a system uses more than three layers, sublayers, internal trust domains, or hybrid layer names, the UX must still present the current position clearly.
4. Developer naming is flexible. User-facing clarity is not.
5. Shared address formats, account metaphors, or reused wallet visuals must not be relied on as the sole indicator of where the user is.

### Special rule for same-address or same-identifier designs

If the same address format, account string, or receiving identifier is reused across multiple trust contexts, the UX must provide an explicit context marker strong enough that a normal user cannot reasonably confuse:
- base-chain Bitcoin
- claim balances
- utility balances
- custodial balances
- contract-governed balances

---

## Section 7. Cross-Layer and Cross-Context Confirmation

**Supports:** Exit as a Right, Interlayer Coupling and Movement, Plain Transferability and Voluntary Encumbrance

### Rules

1. Any action that changes:
 - layer
 - trust model
 - custody model
 - asset class
 - compliance context
 - contract status
must require explicit confirmation.
2. The confirmation must state in plain language:
 - what the user is moving out of
 - what they are moving into
 - what protections are lost, gained, or changed
 - whether the move is reversible
 - whether the move depends on a bridge, contract, or operator
3. No cross-context move may be hidden inside a generic send, deposit, bridge, stake, continue, or next flow.

### Required special confirmation cases

- Moving from Layer 1 Bitcoin into any claim-based or bridged context.
- Moving from a transactional balance into a utility balance.
- Moving from plain transferability into contract-governed state.
- Moving from self-custody into assisted, delegated, or custodial control.
- Entering a non-compliant, partially compliant, or out-of-scope component.

---

## Section 8. How Risk Is Shown on Screen

**Supports:** Honest Risk Hierarchy, Clarity to Users, Scope and Compliance

### Rules

1. The screen must always make visible:
 - current operational context
 - current asset class
 - custody status
 - compliance context, where relevant
2. Trust assumptions of the current context must be accessible directly from the primary balance or action screen without navigating away from that screen or entering secondary menus such as settings, profile, or configuration pages. Access must be clearly labeled and discoverable without requiring search, guesswork, or prior knowledge of the interface.
3. The UX must not blur:
 - self-custodial versus custodial state
 - compliant versus non-compliant context
 - plain transfer versus contract-governed state
 - money versus credit
4. If a user is about to take an action that weakens their current trust position, that weakening must be visible before commitment.
5. UX requirements must be satisfied across all device classes, including mobile, desktop, web, and embedded environments.

Where screen size or interface constraints limit simultaneous visibility, the following must remain persistently visible on the primary action screen:
- asset classification (money, claim, utility, credit)
- custody status (self-custodial, delegated, custodial)
- compliance context where relevant

Supporting detail may use progressive disclosure, provided that:
- first-level classification is always visible
- no core classification is hidden behind reveal controls
- reduced space is not used to omit or obscure constitutional disclosures

### Revealable detail rule

A compliant UX may use layered disclosure, including reveal controls, to present deeper implementation detail without overwhelming the user. However, the following must be visible without requiring reveal:
- asset classification
- current trust position
- custody status
- compliance context
- movement into credit
- movement into a weaker trust layer
- movement into custodial or delegated control
- movement into contract-governed state

Reveal mechanisms may deepen understanding but must not be required to determine the nature of the asset, trust model, custody state, or compliance context.

Core classifications must be represented by persistent visible text or clearly understandable symbols on the primary action screen. These classifications must not rely solely on:
- tap interactions
- hover states
- hidden panels
- expandable sections

Reveal controls are permitted only for additional detail, not for core classification.

### Minimum trust-assumption disclosure

At minimum, the user must be able to find:
- whether exit is permissionless or conditional
- whether reserves are direct, claimed, or absent
- whether a bridge or operator is involved
- whether governance or committee control exists
- whether the current balance is money, claim, utility balance, gas token, governance token, or credit

---

## Section 9. Compliance Context Disclosure

**Supports:** Scope, Extensions, Compliance, Naming, and Voluntary Applicability

### Rules

1. The interface must clearly disclose whether the current context is:
 - compliant
 - partially compliant
 - non-compliant
 - out of constitutional scope
2. A user must not be left assuming constitutional protection merely because the interface is inside a broader ecosystem that uses constitutional branding.
3. If a user is routed into a non-compliant, partially compliant, or less-proven context, that boundary must be disclosed before commitment.
4. Compliance status must not be hidden in documentation while the UI implies stronger protection.

### Examples

Allowed:
- "You are entering a non-compliant bridge path. Exit rights and proof standards may differ."

Forbidden:
- using the same visual trust signals for compliant and non-compliant components with only tiny footnote differences

---

## Section 10. Self-Custody Must Not Be Visually Discouraged

**Supports:** Dependence Must Remain Escapable, Long-Term Recoverability and Compatibility Continuity

### Rules

1. Where self-custody is available, it must be at least as visually accessible as custodial or delegated alternatives.
2. No interface may use asymmetrical warning language to portray self-custody as uniquely dangerous while presenting reliance on third parties as normal or safer by default.
3. No compliant UX may default users into custodial or delegated arrangements when a self-custodial path is available and practical.
4. No compliant UX may portray self-custody as merely "advanced" while portraying dependence on third parties as neutral baseline reality.
5. If a custodial or delegated path is offered, the UX must also explain the path back out.

### Important note

This section does not require every user to choose self-custody. 
It requires the system not to stack the deck against it.

---

## Section 11. Compliant Plus Designation

**Type within this document:** Optional higher UX designation 
**Purpose:** To recognize systems that not only remain honest, but also preserve long-term workflow continuity for routine money actions.

### Principle

A Compliant Plus system does not force users to relearn core money actions unnecessarily. It preserves confidence, habit, and operational continuity across upgrades.

### Qualifying rules

1. Routine money tasks must remain operationally stable across upgrades wherever reasonably possible.
2. Users must not be forced onto a new workflow for:
 - sending Bitcoin
 - receiving Bitcoin
 - moving up or down layers
 - checking custody state
 - confirming what asset they hold
 if the old workflow can still be preserved safely.
3. A system may introduce new workflows, new screens, new features, or safer processes, but must not force users to abandon prior core money paths without a safe continuity path.
4. The old process or a functionally equivalent compatibility path must remain available long enough for users to continue accessing their money without panic, retraining shock, or operational paralysis.
5. If an old process is genuinely unsafe and cannot remain, the system must preserve the old mental model as closely as possible through:
 - compatibility mode
 - legacy mode
 - guided safe bridge
 - functionally equivalent path
6. No upgrade may strand a user by radically changing the location, naming, or sequence of core money actions without a safe continuity path.
7. A system that repeatedly redesigns core money workflows for style, novelty, or product preference rather than necessity should not qualify for Compliant Plus.

### Evaluation and accountability

Compliant Plus status is not self-authoritative. Any system claiming Compliant Plus status is subject to the same evaluation, disclosure, and breach classification processes as base constitutional compliance.

Claims of Compliant Plus status must be:
- publicly stated
- supported by evidence of meeting the criteria defined in this section
- subject to independent evaluation by users, auditors, or other evaluators

Misrepresentation of Compliant Plus status constitutes a form of compliance misrepresentation under the constitution.

### Safety exception

If an old workflow is genuinely unsafe, Compliant Plus does not require preserving the dangerous behavior itself. It requires preserving the user's confidence path to the money as closely as safely possible.

### Practical examples

Allowed for Compliant Plus:
- adding a new send flow while keeping the old send flow available
- introducing a safer cross-layer confirmation while preserving the old action location and logic
- providing legacy mode for users trained on an earlier interface

Not allowed for Compliant Plus:
- moving send, receive, or exit into new locations with no legacy path
- requiring a new app for a routine action that users previously performed in the existing app
- repeatedly renaming basic actions in ways that force retraining

### Re-evaluation and erosion

8. Compliant Plus status requires periodic reaffirmation following major UX changes.

A system must be re-evaluated for Compliant Plus status:
- after any significant interface or workflow change affecting core monetary actions
- at reasonable periodic intervals if continuous changes occur

Incremental changes that individually appear minor but collectively degrade workflow continuity must be evaluated in aggregate.

A system may lose Compliant Plus status if cumulative changes materially violate the continuity principles defined in this section, even if no single change independently constitutes a breach.

---

## Section 12. Third-Party Interfaces

Third-party wallets, interfaces, and applications interacting with a compliant system must adhere to this UX Constitution when presenting or operating on constitutional functions.

A system must not:
- rely on third-party UX behavior to obscure or misrepresent constitutional properties
- outsource user-facing truth obligations to external interfaces

If third-party interfaces misrepresent constitutional properties:
- the system must not endorse, default to, or silently route users through such interfaces
- continued reliance on such interfaces may constitute a breach under [Breach and Restoration Standard](breach-and-restoration-standard.md)

---

## Section 13. Accessibility

All required disclosures, warnings, classifications, and confirmations must be accessible to ordinary users, including those with visual, cognitive, or language limitations.

Critical risk information must:
- not rely solely on color, icons, or small text
- be readable in plain language
- be accessible via screen readers and assistive technologies where applicable

Accessibility limitations must not be used as justification to omit required constitutional disclosures.

---

## Section 14. Relationship to the Protocol Constitution

### Rules

1. This document is binding on all user-facing behavior of systems claiming compliance.
2. No UX behavior may weaken, blur, or contradict protocol-level protections.
3. A system that materially misrepresents asset class, trust model, custody state, exit conditions, or compliance context through its user interface may be classified as in breach under [Breach and Restoration Standard](breach-and-restoration-standard.md), regardless of underlying protocol correctness.
4. If a conflict appears to exist between what is technically true and what the user is led to believe, the stronger requirement is:
 - truth in the protocol
 - honesty in the UX
5. Where this document is silent, interpretation should default toward:
 - clearer disclosure
 - stronger user understanding
 - easier self-custody
 - easier downward exit
 - less chance of mistaking weaker layers for stronger ones

---

## Final UX Principle

A compliant system must make it easy for a normal user to answer four questions at all times:

1. **Where am I?**
2. **What do I hold?**
3. **Who or what do I depend on right now?**
4. **What changes if I move from here?**

If the user cannot answer those questions quickly and honestly from the interface itself, the UX is not constitutionally sound.
