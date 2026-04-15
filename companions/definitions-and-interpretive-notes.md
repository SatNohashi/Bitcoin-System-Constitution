# Definitions and Interpretive Notes

**Author:** Satoshi Nohashi  
**License:** CC0 1.0 Universal (Public Domain Dedication)  
**Website:** [bitcoinsystemconstitution.org](https://bitcoinsystemconstitution.org)  
**Type:** Interpretive 
**Supports:** Article I (Definitions) of the Bitcoin System Constitution 
**Definitions:** This document IS the interpretive extension of Article I definitions 
**Status:** Draft 

## Purpose

Article I of the constitution contains formal definitions for the load-bearing terms used throughout the Bitcoin System Constitution. This companion document extends those definitions with:

- **Interpretive notes** that clarify edge cases and boundary conditions.
- **Usage guidance** that explains how terms work together across articles.
- **Examples** that show what falls inside and outside each definition.
- **Anti-gaming notes** that identify common ways adversarial actors may try to twist language.

This document does not override Article I. It clarifies, illustrates, and protects the intended meaning of Article I.

The spirit of these notes is simple:

- If there is doubt, interpret terms in the direction that best preserves user freedom, honest risk disclosure, current proof, meaningful exit, and resistance to hidden capture.
- If a system relies on ambiguity to justify behavior, that ambiguity should generally be resolved against the actor seeking extra power.

---

## Reading Rule

Where a term could reasonably be interpreted in more than one way, the preferred interpretation is the one that best protects:

1. Bitcoin as root money.
2. Honest separation between money, claims, utility balances, and credit.
3. Non-discretionary downward exit.
4. Current reserve and liability truth.
5. Resistance to capture through semantics, architecture, or operational concentration.

If a later companion standard does not yet exist, interpretation should default to the most conservative reading consistent with these principles.

---

## 1. Core Structure Terms

### Bitcoin
**Interpretive note:** 
The definition of Bitcoin is intentionally narrow. It refers to the Bitcoin network and its native monetary unit, not to any wrapped, represented, bridged, or synthetic form of Bitcoin on another layer or system.

**Inside the definition:**
- Bitcoin held directly on Layer 1.
- Bitcoin UTXOs controlled under Bitcoin consensus rules.

**Outside the definition:**
- A wrapped BTC token on another network.
- A custodial IOU denominated in BTC.
- A Layer 2 balance, even if fully backed and redeemable.

**Anti-gaming note:** 
Actors may try to exploit branding by saying "this is Bitcoin" when they mean "this is a Bitcoin-linked asset." The constitution requires stricter classification than common marketing language.

---

### Layer 1
**Interpretive note:** 
Layer 1 is not merely the oldest chain in a stack. It is the final monetary truth layer recognized by the constitution.

**Inside the definition:**
- Final settlement.
- Long-term self-custody.
- Bitcoin-native consensus truth.

**Outside the definition:**
- A fast settlement network that periodically checkpoints to Bitcoin.
- A sidechain or rollup that derives security from Bitcoin but has its own operational rules.

**Usage guidance:** 
If a system offers convenience but still depends on another system for final truth, it is not Layer 1 under this constitution.

---

### Layer 2
**Interpretive note:** 
Layer 2 is defined by its role, not by one technical pattern. It is the cash rail and support layer for real economic life.

**Inside the definition:**
- Fast Bitcoin-denominated transfer systems.
- Payment-oriented systems with finer accounting and lower fees than Layer 1.
- Systems designed to be safer and more conservative than Layer 3.

**Outside the definition:**
- A generic smart contract chain with a BTC token.
- A speculative execution layer that happens to support Bitcoin.

**Anti-gaming note:** 
Calling something "Layer 2" does not make it a constitutional Layer 2. It must function as the transactional support layer described by the constitution.

---

### Layer 3
**Interpretive note:** 
Layer 3 is the place for programmability, experimentation, and optional higher risk. It is constitutionally downstream from both Layer 1 and Layer 2 in trust.

**Inside the definition:**
- Smart contract environments.
- App layers.
- Tokenized systems and optional risk-bearing execution environments.

**Outside the definition:**
- Core transactional Bitcoin rail functions that should belong to Layer 2.
- Systems marketed as fast but expected to function as final money.

**Usage guidance:** 
If a system is designed to be the place where users build, automate, speculate, or take app-level risk, it is likely Layer 3.

---

### Constitutional layer
**Interpretive note:** 
This is a functional category, not a physical topology requirement. A constitutional layer may be composed of many technical parts.

**Anti-gaming note:** 
A project may not avoid constitutional duties by saying, "This is only a subsystem, not the layer itself," if that subsystem performs core constitutional functions of the layer.

---

### Component, sublayer, module, support system

#### When does a support system become a component with constitutional duties
A support system becomes a component with constitutional duties when failure, capture, concentration, or misbehavior in that system can materially affect:

- reserve truth
- liability truth
- custody safety
- normal downward exit
- transaction inclusion
- constitutional timekeeping
- user ability to distinguish what they hold

**Examples:**
- A read-only public dashboard showing proof data is likely a support system.
- A relayer network that users must rely on to exit is no longer a harmless support system. It has constitutional significance.
- An indexer used only for convenience may be a support system.
- An indexer whose failure makes balances undiscoverable becomes constitutional in effect.

#### Is an indexer a support system
Usually yes at first. 
No, if users cannot meaningfully discover or prove balances without it.

#### Is a fee market a module
Yes, if it is a distinct functional unit governing transaction ordering, inclusion, or exit economics.

#### How to evaluate whether internal decomposition weakens, obscures, or evades protections
Ask four questions:

1. Did the decomposition make risk harder for users to see.
2. Did it reduce practical exit rights.
3. Did it move a core duty into a supposedly non-critical subsystem.
4. Did it create a new choke point while keeping the old constitutional label.

If the answer to any is yes, constitutional concern exists.

---

## 2. Monetary Asset Classes

### Direct Bitcoin claim
**Interpretive note:** 
A direct Bitcoin claim is stronger than a Bitcoin-denominated balance, but weaker than actual Layer 1 Bitcoin. It is redeemable against Bitcoin reserves through a non-discretionary published process.

**Inside the definition:**
- A claim backed by publicly verifiable reserves and liabilities with a non-discretionary redemption path.
- A BTC representation whose reserve and claim set can be independently verified.

**Outside the definition:**
- A balance redeemable only by committee approval.
- A BTC IOU issued by a company without proof of liabilities.
- A wrapped token with no enforceable or visible reserve process.

**Usage guidance:** 
A direct claim is still a claim. It should never be confused with Layer 1 Bitcoin itself.

**Anti-gaming note:** 
A project may try to say "redeemable under normal conditions" while reserving emergency discretion. That is not non-discretionary redemption.

---

### Bitcoin transactional balance
**Interpretive note:** 
A Bitcoin transactional balance is for use on Layer 2 as money in motion. It may be backed, but it is not defined primarily by reserve marketing. It is defined by its role in ordinary transfer and economic life.

**Inside the definition:**
- A Layer 2 payment balance.
- A cash-like BTC-denominated balance used for normal transfers and commerce.

**Outside the definition:**
- A credit position.
- A time-locked application-specific position on Layer 3.
- A balance that can only move through complex contracts by default.

**How to distinguish from a direct Bitcoin claim in practice** 
A direct Bitcoin claim emphasizes redemption against reserve. 
A Bitcoin transactional balance emphasizes everyday movement under Layer 2 rules.

A system can have both features, but the constitutional classification depends on the actual role and user-facing trust model.

---

### Bitcoin utility balance
**Interpretive note:** 
A Bitcoin utility balance is a Bitcoin-denominated balance used inside Layer 3 rules and risk. It is not ordinary money unless the user is fully informed that it remains subject to Layer 3 conditions.

**Inside the definition:**
- A BTC-denominated balance used in a Layer 3 smart contract environment.
- A balance used as app collateral, execution fuel substitute, or contract-side asset.

**Outside the definition:**
- A plain Layer 2 cash balance.
- A direct Bitcoin claim marketed as current reserve-backed exit money.
- A credit instrument paying yield from reserve use.

#### When does a Bitcoin utility balance cross into being a credit instrument
It crosses over when the holder's position depends on:
- lending
- rehypothecation
- maturity transformation
- discretionary repayment
- reserve usage for yield

If the balance earns yield because the underlying reserve is being put to work, the balance or associated position has become credit-like.

---

### Native gas token
**Interpretive note:** 
A native gas token is not automatically speculative, but it is not Bitcoin unless it truly is Bitcoin. Clear separation matters.

**Anti-gaming note:** 
Systems often try to create emotional equivalence between a native token and Bitcoin utility balances. The constitution rejects that blur.

---

### Governance token
**Interpretive note:** 
A governance token is defined by authority, not branding. If a token materially influences protocol decision making, it is governance-like even if called something softer.

---

### Credit instrument
**Interpretive note:** 
This definition is intentionally broad because history shows that money-substitute fraud often begins with narrow loopholes.

**Examples inside the definition:**
- BTC lending receipts.
- Yield-bearing wrapped balances whose reserves are deployed.
- Rehypothecated custody positions.
- Maturity-mismatched liabilities presented as stable value.

**Examples outside the definition:**
- A plain transactional balance with no lending or discretionary repayment risk.
- A direct Bitcoin claim backed by unencumbered reserve.

---

### Reserve, liability, encumbered reserve, unencumbered reserve

#### Examples of encumbered reserve
- Reserve BTC lent out to earn yield.
- Reserve pledged as collateral.
- Reserve committed into staking or bonded control.
- Reserve subject to third-party lien or claim.

#### Examples of unencumbered reserve
- Reserve held solely to back its claims.
- Reserve not lent, pledged, or committed elsewhere.

#### Edge case: staking rewards
If "staking rewards" arise because reserve assets are being committed into another protocol or risk-bearing arrangement, then the reserve is encumbered and the resulting structure creates either:
- a credit instrument
- a new liability
- or both

It does not remain constitutionally clean reserve merely because the system calls the yield "efficiency."

---

## 3. Trust and Movement

### Canonical interlayer path
**Interpretive note:** 
A canonical path is the constitutionally recognized normal route or routes for moving balances between layers under the system's core safety promises.

**Usage guidance:** 
A system may have more than one canonical path if each is published, standard, and covered by the claimed protections.

**Anti-gaming note:** 
A team may try to treat a weak path as canonical when convenient and as "just optional" when criticized. The classification must be stable and public.

---

### Trust-minimized
**Interpretive note:** 
Trust-minimized does not mean magical or risk-free. It means bounded, visible, rule-based trust assumptions that do not depend on a specific party's discretion.

**Who evaluates "honestly"** 
No single actor gets to define this unilaterally. Honest evaluation should be based on:
- published threat model
- available alternatives
- disclosed tradeoffs
- later companion standards when they exist

**Anti-gaming note:** 
Calling something trust-minimized because it uses signatures or smart contracts is not enough. The real question is whether users still depend on specific actors' judgment or favor.

---

### Strongest available security model
**Interpretive note:** 
This is not a license for self-serving marketing. It is a discipline of public justification.

A credible claim should be able to answer:
- What stronger alternative was considered.
- Why it was rejected.
- What trust assumptions remain.
- Why those assumptions were unavoidable at the time.

Until a later standard exists, the conservative reading applies.

#### Examples of insufficient justifications
The following are generally not enough on their own:
- "This was easier to ship."
- "This was what our team knew how to build."
- "No one else had shipped the stronger option yet."
- "We used a trusted multisig because coordination was simpler."
- "We call this strongest available because it is the strongest version we personally implemented."

#### Examples that may count as stronger justification
- A published explanation of why a stronger design was technically infeasible at launch.
- A clear statement of what stronger model was considered and what concrete dependency blocked it.
- Honest disclosure that the current design is transitional rather than ideal.

---

### Trusted path
**Interpretive note:** 
A trusted path depends on trust in specific actors, even if it uses good software or cryptography around that trust.

**Examples:**
- A company-controlled redemption path.
- A bridge where a signer council can halt or selectively approve movement.

---

### Contractual path
**Interpretive note:** 
A contractual path depends on law, terms of service, business process, or signed agreements rather than protocol-enforced outcome.

**Examples:**
- Redemption guaranteed by legal contract only.
- A business-operated withdrawal path governed by customer account terms.

---

### Non-discretionary
**Interpretive note:** 
Non-discretionary means rule-based operation. It does not mean every human role disappears. It means rights and outcomes do not depend on case-by-case favoritism or politics.

**Inside the definition:**
- deterministic queues
- published timeout rules
- fixed challenge processes

**Outside the definition:**
- manual review boards
- emergency committee approval
- selective compliance judgments

---

### Downward exit
**Interpretive note:** 
Downward exit is movement toward a harder, more sovereign layer. It is not merely "moving somewhere else."

---

### Normal downward movement
**Interpretive note:** 
Normal downward movement means ordinary use of a standard exit path under standard conditions, not a one-off rescue by operator grace.

---

### Functional exit blocking vs structural exit blocking

#### Functional exit blocking examples
- Exit is "allowed" but only through KYC intermediaries.
- Fees make ordinary exit economically impossible.
- Delay is so extreme that exit is practically unusable.
- Operators refuse to route specific users.

#### Legitimate operational limits
- Congestion with uniform published rules.
- Fee pressure that is neutral and not strategically exclusionary.
- Timeouts required by known challenge windows.
- Invalid or malformed transactions being rejected.

#### When does fee-based difficulty become exit interference
When the system is intentionally structured or operated so that ordinary users cannot realistically exercise exit, especially if insiders or institutions retain easier access.

---

### Exit interference
**Interpretive note:** 
Exit interference includes more than formal prohibition. Delay, fees, dependency, or operator favoritism can all count if they materially impair ordinary movement.

---

### Plain transferability
**Interpretive note:** 
Plain transferability protects the idea that money should be movable without mandatory policy wrappers.

**Examples inside the definition:**
- sending a Layer 2 balance directly to another user
- receiving a Layer 3 base utility balance without forced contract mediation

**Examples outside the definition:**
- a transfer that can only occur through a mandatory permission contract
- a balance that cannot move unless identity data is provided

---

### Voluntary encumbrance

#### Edge case: time-locked contracts
A time-locked contract is a voluntary encumbrance if:
- the holder explicitly opted in
- the terms were visible
- the lock is part of a known contract condition

It becomes a structural problem if:
- users are forced into such contracts to use ordinary money functions
- the lock is hidden or unavoidable
- the lock cannot unwind into plain transferability on known terms

---

### Bridge
**Interpretive note:** 
A bridge is defined by function, not branding or implementation style. If a mechanism moves value across systems or trust boundaries by locking, wrapping, custodian release, message-mediated release, or equivalent logic, it is a bridge.

#### When does a bridge become a component with constitutional duties
A bridge becomes a constitutional component when its failure, capture, or discretion can materially affect:
- reserve truth
- movement between systems
- normal downward exit
- user asset classification
- practical access to Bitcoin-denominated balances

A bridge that merely observes or reports is not usually a constitutional component. A bridge that holds, locks, wraps, releases, or intermediates value usually is.

#### Is a smart contract automatically a bridge
Not automatically. A smart contract is a bridge when it performs bridge behavior, such as:
- locking funds in one system and causing release in another
- issuing wrapped balances against locked assets
- coordinating cross-system redemption or claims

A contract that only automates internal L3 behavior is not a bridge merely because it is a contract.

#### Does a bridge between two systems inside the same broader constitutional stack still count
Yes, if it crosses a distinct trust boundary, movement boundary, or asset-class boundary. The fact that two systems are within the same broad stack does not erase bridge risk.

**Anti-gaming note:** 
Teams may try to say "this is not really a bridge, it is just internal routing." If the mechanism introduces bridge-like custody, wrapping, release logic, or trust assumptions, it should be evaluated as a bridge.

---

## 4. Governance and Change

### Constitutional genesis
**Interpretive note:** 
Constitutional genesis is fixed to stop timeline games. It is not a marketing date. It is the earliest durable public publication date.

---

### Activation
**Interpretive note:** 
Activation is about real exposure, not labels.

**Examples of activation:**
- real users deposit value
- real users rely on the component for transfer
- funds are at risk in production

**Examples that may not count:**
- closed internal testing with no user reliance
- public testnets with no meaningful production value

**Anti-gaming note:** 
"Beta" does not save a system from activation if real users are already depending on it.

---

### Constitutional amendment vs protocol-level change
A constitutional amendment changes:
- the text
- the meaning
- or the operative effect of constitutional protections

A protocol-level change changes:
- implementation behavior
- parameters
- routing
- features
- operational rules

A technical change becomes constitutional if it materially changes:
- exit rights
- reserve truth
- custody safety
- governance reach
- the meaning of core protected terms

---

### Governance authority
**Interpretive note:** 
Governance authority is broader than token voting. Any mechanism that can make binding protocol decisions is governance authority, even if it uses:
- multisigs
- councils
- operator committees
- foundations
- delegated roles

---

### Protocol-level decision and protocol-level change
**Interpretive note:** 
These terms exist so governance cannot hide behind wording like "operational adjustment" or "technical housekeeping" when the change really affects users.

---

### Final implementation
**Interpretive note:** 
Final implementation means the approved change is actually deployed and active, not merely coded, proposed, or announced.

---

### Governance sunset
**Interpretive note:** 
Governance sunset is meant to be real, not ceremonial. After sunset, governance cannot continue by renaming itself, wrapping itself, or acting through new intermediaries.

**Examples of violation:**
- replacing token governance with a council that keeps the same practical authority
- creating an "advisory" vote that all operators are expected to obey
- introducing a new governance token after sunset within the same claimed compliant system

---

### Constitutional continuity
**Interpretive note:** 
Constitutional continuity means no material break in compliance since public adoption of the constitution by that system.

A short-lived issue does not automatically preserve continuity simply because it was brief. What matters is:
- whether the breach was material
- whether user rights were impaired
- whether system truth was broken
- whether continuity-breaking categories in the constitution were triggered

A system may be currently compliant but still lack uninterrupted constitutional continuity.

**Anti-gaming note:** 
Teams may argue that a breach was "too short to count." Duration matters, but materiality matters more.

---

### Successor system
**Interpretive note:** 
A successor system is not defined by branding alone. It is defined by meaningful discontinuity in trust model, rights structure, migration consent, or core operating assumptions.

#### When does an upgrade become a successor system
A change increasingly looks like a successor system when it:
- changes the trust model materially
- changes the constitutional rights users rely on
- changes the meaning of core asset classes
- changes governance authority or sunset structure
- requires users to accept a new dependency or custody model
- migrates balances or assumptions in a way that goes beyond normal protocol evolution

A large technical upgrade is not automatically a successor. But when users are effectively being asked to trust a different constitutional system, successor logic should apply.

---

### Pre-declared authority
**Interpretive note:** 
Pre-declared authority means authority that was:
- published publicly
- durably recorded
- sufficiently specific to identify the governed subject matter
- published before the constitutional amendment window closed

Vague statements like "governance may act as needed for protocol health" do not count.

**Examples of governance scope expansion disguised as technical change**
- adding new emergency powers while calling it "resilience tooling"
- moving a reserve function under governance by labeling it "parameter tuning"
- giving governance authority over new domains through a generic upgrade module

---

### Parallel implementation right
**Interpretive note:** 
The right to build alternative implementations is meaningless if incumbents can suppress it through legal mechanisms while claiming the protocol is open. Article XXIII.7 closes this gap.

**What counts as legal blocking:**
- Patent threats or litigation against interoperable implementations.
- API licensing that requires permission, payment, or identity disclosure to access constitutional functions.
- Trademark enforcement against accurate, non-deceptive compatibility claims (e.g., "compatible with X protocol").
- Certification or compliance programs that gate access to core protocol features.
- Terms of service that prohibit reverse engineering, interoperability, or independent tooling.
- Legal threats designed to make independent implementation economically unviable even if technically permitted.

**What does NOT violate this right:**
- Enforcing trademark against actually deceptive branding (e.g., claiming to BE the official implementation when you are not).
- Protecting trade secrets that are not necessary for constitutional function implementation.
- Requiring accurate disclosure of non-affiliation.
- Standard open-source license compliance (e.g., attribution, copyleft obligations).

**Anti-gaming note:** 
The test is whether the legal structure makes truthful independent implementation practically possible for an independent party with ordinary legal resources. A system that says "anyone can implement" while maintaining a patent portfolio aimed at implementers, or requiring expensive licensing for API access, fails this test.

**Relationship to protocol openness:**
Protocol-level openness (published specs, open code) is necessary but not sufficient. Legal openness is also required. A system with open code but closed legal posture is not compliant with Article XXIII.

---

## 5. Custody and Control

### Custody structure
**Interpretive note:** 
Custody structure is not just key count. It includes who can coordinate, who can compel, who can replace signers, and what real-world chokepoints exist.

---

### Unilateral control
**Interpretive note:** 
Unilateral control includes practical unilateral control, not just formal single-key control. One person controlling several nominally different signers may still create unilateral control in substance.

---

### Signer
**Interpretive note:** 
A signer is any actor with real reserve-moving authority, even if the technical role is called guardian, operator, validator, committee member, or shard holder.

---

### Independent control domain
**Interpretive note:** 
Independence must be real, not cosmetic. Different shells under one real controller are not independent domains.

---

### Custody concentration
**Interpretive note:** 
Custody concentration exists when reserve control is too dependent on too few real-world control points.

**Examples:**
- Many signers hosted by one company.
- Signers spread across legal entities but controlled by one parent group.
- Signers in several countries but all vulnerable to one practical coordination channel.
- A threshold that looks large but can still be satisfied by one hidden clique.

**Anti-gaming note:** 
Apparent signer count is not enough. Real independence matters more than headline diversity.

---

### Provisional custody
**Interpretive note:** 
Provisional custody is a transitional state, not a rhetorical excuse. It must be:
- publicly disclosed
- bounded
- capped
- and directed toward constitutional maturity

A mere statement of intent is not enough.

#### What provisional custody should include
At minimum:
- a public explanation of why full compliant custody is not yet in place
- a bounded timeline or declared review/expiry point
- a cap on reserve size while provisional custody remains
- clear statement that the custody model is not fully compliant
- a path or criteria for maturation

#### What provisional custody must not become
- a permanent excuse
- a vague "we are still growing" status
- a marketing label used to imply near-compliance without real progress

---

## 6. Breach and Compliance

### Compliant and non-compliant
**Interpretive note:** 
Compliance is about actual behavior, not branding, affiliation, aspiration, or code comments.

---

### Restored compliance
**Interpretive note:** 
Restored compliance is not amnesia.

#### How much disclosure is enough
At minimum:
- what happened
- when it happened
- what users were affected
- what was fixed
- whether continuity was broken
- whether the system is currently compliant but historically breached

If that is not disclosed, "restored compliance" is not honest.

#### Timing of restored compliance claims
A system should not claim restored compliance merely because it has published a patch. At minimum:
- the breach must be disclosed
- the remediation must actually be active
- users must have had a meaningful opportunity to understand the breach and, where relevant, exit after disclosure

This document does not set a fixed universal number of days. But immediate next-day "restored compliance" claims after a material breach should generally be viewed skeptically.

---

### Material breach
**Interpretive note:** 
A material breach is one that strikes the constitution where it actually protects users.

**Examples:**
- freezing exit
- hiding reserve encumbrance
- disguising credit as money
- using governance after sunset
- silent migration to a successor system

---

### Materially weakens
**Threshold guidance** 
A change materially weakens a protection if it reduces the real-world ability of ordinary users to rely on that protection, even if the text remains untouched.

This includes weakening by:
- ambiguity
- cumulative drift
- concentration
- stale proof
- fee pressure
- discretionary operation
- hidden dependency

#### Examples
- **Ambiguity:** redefining "ordinary transaction" so politically disfavored transactions are no longer treated as ordinary.
- **Cumulative drift:** several small fee increases, queue changes, and operator exceptions that together make ordinary exit unrealistic.
- **Concentration:** shifting more and more choke functions to one company while keeping protocol rules unchanged.
- **Stale proof:** continuing to market balances as backed while proof cadence is missed.
- **Fee pressure:** structuring costs so only large users can exit normally.
- **Hidden dependency:** making all practical exit rely on a legally controlled intermediary.

---

### Misrepresentation
**Examples in naming, branding, and marketing**
- calling a BTC IOU "Bitcoin"
- calling stale proof "verified backing"
- calling a discretionary bridge "trust-minimized"
- using constitutional branding while materially violating the articles

---

## 7. Transaction and Inclusion Terms

### Ordinary transaction
**Interpretive note:** 
An ordinary transaction is a standard, technically valid, publicly supported request to move value or execute a supported operation through the normal rules of the system. It is defined by rule-conforming behavior and use of published pathways, not by the identity, intent, politics, reputation, or social standing of the sender.

**Inside the definition:**
- A correctly formatted transfer request using supported transaction types.
- A redemption request that follows published rules.
- A Layer 2 payment using documented parameters.
- An exit transaction within published size, fee, and formatting bounds.
- Any transaction that would be processed the same way if the sender were anonymous and unknown.

**Outside the definition:**
- A malformed or technically invalid request.
- A request that violates explicit published protocol or policy limits.
- A request that depends on unsupported behavior, exceptional privileges, or unpublished operator discretion.
- A request that triggers a publicly predeclared exploit-mitigation or emergency invalidity rule that existed before the request was submitted.

**Anti-gaming note:** 
The key test is whether the transaction would be treated the same way if the sender's identity, politics, and relationships were unknown. Systems may not redefine "ordinary" to exclude transactions based on:
- sender identity
- political context
- regulatory pressure on specific users
- transaction destination
- perceived purpose of funds

An ordinary transaction remains ordinary regardless of who sends it or why, so long as it uses a supported path under the published rules.

**Usage guidance:** 
When the constitution protects ordinary transactions from censorship, it means technically valid requests using supported public paths. A system cannot claim compliance while selectively refusing transactions that are rule-conforming but politically inconvenient.

---

### Valid transaction
**Interpretive note:** 
For constitutional purposes, a valid transaction is one that satisfies all published, neutral, identity-blind technical and policy requirements for inclusion under the relevant path. Validity is not merely whatever an operator says it is, and it is not limited to raw consensus validity if the system also relies on published inclusion rules.

**Inside the definition:**
- A transaction with correct cryptographic signatures.
- A transaction meeting the published minimum fee or fee rule, where applicable.
- A transaction referencing real, usable state or inputs, where applicable.
- A transaction within published size, complexity, and format limits.
- A transaction that passes the same automated validation checks applied to comparable transactions.

**Outside the definition:**
- A transaction with invalid or missing signatures.
- A transaction referencing unusable or nonexistent state or inputs.
- A transaction that violates hard protocol rules.
- A transaction that fails published neutral validation or anti-spam rules.
- A transaction rejected under a rule that is unpublished, selectively applied, or identity-dependent.

**Anti-gaming note:** 
Validity is objective and rule-bound. A system may not declare a transaction invalid because:
- it dislikes the sender
- it faces pressure regarding the recipient
- external parties flagged the transaction
- the amount or pattern is politically inconvenient
- an operator wants to suppress the use case

If a transaction passes the same published checks that other comparable transactions pass, it is valid. Selective invalidity claims based on identity, politics, or pressure are censorship, not validation.

**Relationship to ordinary transaction:** 
Most ordinary transactions are valid transactions submitted through normal supported paths. Some technically valid edge-case transactions may be unusual without losing constitutional protection. The constitution's baseline test is whether valid public use remains available to ordinary users without special privilege.

---

### Practical path to inclusion
**Interpretive note:** 
A practical path to inclusion is a route by which an ordinary user can get a valid transaction processed within reasonable time and cost bounds, using documented tools and public procedures, without needing special access, insider relationships, exceptional capital, or extraordinary technical measures.

**Inside the definition:**
- A public mempool or submission path that accepts transactions from any user under published rules.
- A standard endpoint with documented, neutral acceptance criteria.
- A fee market where paying the generally applicable rate provides inclusion without identity checks.
- A queue system that processes requests in published order without favoritism.
- More than one route to inclusion, where at least one remains practical to ordinary users.

**Outside the definition:**
- A path that requires KYC or identity verification for basic inclusion.
- A path that requires a relationship with specific operators.
- A path where insiders or large players have systematically faster or cheaper access to the same constitutional function.
- A path that is technically open but practically inaccessible due to extreme fees, extreme delays, hidden requirements, or undocumented steps.
- A path that exists on paper but is not actually operational for ordinary users.

**Threshold guidance:** 
"Practical" means achievable by an ordinary user with ordinary resources, ordinary technical knowledge, and the documented public tools of the system. The test is not whether inclusion is theoretically possible. The test is whether a typical user can actually achieve it without extraordinary effort or privilege.

Factors that may make a path impractical include:
- materially elevated fees without neutral, generally applicable justification
- materially elevated delays relative to comparable transactions under comparable conditions
- requirements for specialized infrastructure, relationships, or insider knowledge
- undocumented queues, hidden approval layers, or informal gatekeeping

Exact operational thresholds should be defined in a later operational standard. Until then, the conservative reading applies.

**Anti-gaming note:** 
A system may claim "anyone can submit transactions" while structuring the actual path so that only insiders, wealthy actors, or specialists can realistically use it. This is functional censorship even if formal censorship does not exist.

The constitutional test is whether ordinary users actually have practical access, not whether documentation claims they do.

---

### Ordinary user
**Interpretive note:** 
An ordinary user is a person or entity using the system through the public, documented, non-privileged path, with ordinary resources, ordinary technical skill, and no special insider access. This term sets the minimum accessibility floor for constitutional protection. It does not reduce protections for users who are more sophisticated, wealthier, or more technically capable.

**Inside the definition:**
- A user with standard technical literacy who can use a wallet and follow documented procedures.
- A user with typical financial resources who does not require institutional-scale capital to participate.
- A user without special relationships to operators, developers, governance participants, or service providers.
- A user relying on published interfaces and documented processes.
- A user who expects the system to work as publicly represented.

**Outside the definition:**
- A user relying on private, undocumented, privileged pathways unavailable to the public.
- A user receiving preferential treatment through operator relationships, legal arrangements, or insider coordination.
- A user whose success depends on exceptional infrastructure or informal access that the system does not publicly promise to ordinary users.

**Important clarification:** 
A sophisticated user, wealthy user, expert, institution, or developer is not excluded from constitutional protection merely because they are sophisticated. The question is whether the right being evaluated is available through the ordinary public path, not whether some protected user is unusually capable.

**Usage guidance:** 
When the constitution refers to rights that must be available to users, the ordinary-user standard is the baseline test. A system cannot claim compliance by saying:
- sophisticated users can still exit
- large holders can still transact
- experts can still recover funds

If ordinary users cannot do the same through the public path, the system is constitutionally weak.

**Anti-gaming note:** 
Systems may try to define their real user base narrowly to exclude the users they find inconvenient. The constitutional test is this: would a reasonable person, seeing the system's public positioning and documented flows, expect to be able to use it through the normal path? If yes, that person counts as an ordinary user for constitutional evaluation.

**Relationship to other terms:**
- Ordinary users submit ordinary transactions.
- Ordinary users need practical paths to inclusion.
- Ordinary users must be able to exercise exit rights without extraordinary measures.
- The constitution's protections are not limited to ordinary users, but ordinary-user accessibility is the minimum test for whether those protections are real.

---

### Constitutional breach from transaction suppression
If valid ordinary transactions are suppressed by coercion and no practical neutral path to inclusion exists, the system is in constitutional breach — except where the restriction arises from a voluntary, explicit, user-chosen encumbrance whose terms were known in advance and are being enforced as written.

---

## Final Interpretive Principle

When a disputed interpretation arises, the preferred reading is the one that best prevents:

- hidden credit becoming money
- stale proof becoming acceptable truth
- temporary governance becoming permanent control
- dependence becoming captivity
- centralization becoming the only door
- constitutional language becoming branding theater

The constitution exists to keep systems honest under pressure, not merely elegant on paper.
