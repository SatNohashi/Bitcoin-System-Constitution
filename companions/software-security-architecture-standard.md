# Software and Security Architecture Standard of Bitcoin System Constitution

**Author:** Satoshi Nohashi  
**License:** CC0 1.0 Universal (Public Domain Dedication)  
**Website:** [bitcoinsystemconstitution.org](https://bitcoinsystemconstitution.org)  
**Type:** Binding 
**Supports:** Article XXV (Long-Term Recoverability and Compatibility Continuity), Article XXVI (Dependence Must Remain Escapable) 
**Definitions:** Uses Article I definitions exclusively, particularly: constitutional layer, custody structure, independent control domain, non-discretionary, materially weakens, compliance, provisional custody, strongest available security model, public durable repository 
**Status:** Draft 

---

## Purpose

This standard defines required implementation behaviors for software and security architecture that support constitutional protections around custody, recovery, delegation, revocation, and long-term system integrity.

It exists because constitutional protections can be undermined even when the protocol rules remain sound if:

- delegated control silently becomes ownership
- recovery depends on the same operators who run daily operations
- updates change recovery semantics without user consent
- archival recovery becomes impossible without live vendor infrastructure
- operational keys remain too powerful, too long-lived, or too opaque
- users cannot meaningfully escape dependence once they have entered it

This standard therefore defines required architectural properties for:

- delegated, revocable, rotating capability structures
- separation of operational and ultimate control
- revocability of delegation
- recovery independence from daily operators
- archival offline recovery environments
- hash-pinned reference implementations
- frozen recovery profiles

This standard is binding. It does not require one exact technical stack, but any alternative construction must be **functionally equivalent** to the protections defined here. Equivalent form is allowed. Equivalent protection is mandatory.

### Functional equivalence test

An alternative construction is functionally equivalent only if it can publicly demonstrate, under the same or stricter failure assumptions used in this standard, that it preserves all of the following properties:

- revocability of delegation without delegate cooperation
- separation of operational and ultimate control
- recovery independence from daily operators
- archival recoverability without vendor dependence
- stability of recovery-critical semantics over time
- verifiable integrity of recovery-critical software

At minimum, the alternative construction must remain effective under the failure assumptions listed in Section 4.3:
- operator disappearance
- operator capture
- operator refusal of service
- legal restraint
- prolonged outage
- operator malice

A claim of functional equivalence without such public demonstration is insufficient.

---

## Governing Principles

1. The constitution remains primary. This standard operationalizes, but does not override, Articles XXV and XXVI.
2. Operational control must never silently become ultimate ownership control.
3. Delegation is permitted. Irrevocable dependence is not.
4. Recovery must remain possible even if daily operators disappear, are captured, are offline, or refuse service.
5. Recovery-critical semantics must remain stable across time.
6. Recovery-critical software must be verifiable, preservable, and not silently mutable.
7. Any implementation choice that weakens revocability, separation, archival recoverability, or user escape is non-compliant unless explicitly authorized by the constitution.
8. This standard uses definitions from Article I exclusively. Any undefined technical term used here is descriptive only and does not override constitutional definitions.

---

## Section 1. Delegated, Revocable, Rotating Capability Trees

### 1.1 Required model

Where a system supports delegated control, it must implement delegation through a capability structure anchored in a colder, harder-to-compromise root authority or a functionally equivalent control model.

A compliant delegation architecture must ensure that delegated authority is:

- scoped
- revocable
- time-bounded or rotation-bounded
- distinguishable from ownership
- incapable of silently overriding recovery rights

Literal tree data structures are not mandatory, but the implemented architecture must provide equivalent guarantees.

### 1.2 Capability scope

Delegated capabilities must be limited by one or more of the following:

- action type
- value range
- asset class
- time window
- layer or context
- destination policy
- frequency or rate limit

Open-ended delegation without scope is prohibited for any authority that can materially affect user funds.

### 1.3 Cold roots

Any architecture using delegation must anchor ultimate recovery or revocation power in a colder control domain than the one used for routine operations.

Cold roots must not be:

- permanently online by default
- required for routine daily operation
- silently replaced or bypassed by operator convenience paths

### 1.4 Recovery quorums

Where recovery quorums are used, they must be independent of the day-to-day operational key path.

A recovery quorum must not be reducible to the same operator set that controls ordinary operations.

### 1.5 Rotation

Delegated operational authority must rotate on a declared schedule or under a declared rotation policy.

Long-lived operational keys are permissible only if:

- they remain clearly subordinate to root and recovery control
- they are revocable without delegate cooperation
- they cannot trap or irreversibly transfer ownership

### 1.6 No hidden broadening of delegated authority

No software update, operator intervention, or policy change may silently broaden the scope of an existing delegated capability.

Any broadening of capability scope must be explicit, visible, and separately consented to by the delegator.

---

## Section 2. Separation of Operational and Ultimate Control

### 2.1 Core requirement

Day-to-day operational keys and ultimate ownership or recovery keys must remain meaningfully distinct.

### 2.2 Prohibited control collapse

No operational key, hot key, operator key, session key, API credential, or delegated capability may by itself:

- irreversibly transfer ownership
- permanently disable recovery
- permanently change the recovery profile
- rebind a user into a new trust model without explicit higher-authority consent

### 2.3 Ownership transfer vs convenience delegation

The system must clearly distinguish between:

- convenience delegation
- temporary authority
- operational authorization
- ownership transfer

Routine use of a delegated path must not be treated as implied transfer of ownership.

### 2.4 Location and environment separation

Where possible, ultimate control and operational control must be held in materially different control environments.

Operational convenience is not a sufficient reason to collapse all control into the same device, service, or operator path if doing so would eliminate meaningful recovery independence.

### 2.5 Replacement and succession rules

Changes to operational control must not automatically affect ultimate control.

Changes to ultimate control must require a stronger consent path than changes to operational control.

---

## Section 3. Revocability of Delegation

### 3.1 Core requirement

All delegation must be revocable by the delegator or by a constitutionally valid recovery path.

### 3.2 No delegate cooperation requirement

Revocation must not require cooperation, approval, availability, or good behavior from the delegate.

A delegate must not be able to hold the delegator hostage by refusing to participate in revocation.

### 3.3 Time-bounded delegation

Time-bounded delegation is preferred over open-ended delegation wherever practical.

If delegation is open-ended, the system must justify why a bounded model was not used and must still preserve immediate or bounded revocation.

### 3.4 Revocation path independence

The revocation path must be available even if:

- the delegate is offline
- the delegate is hostile
- the delegate has been captured
- the operator service is unavailable
- the software vendor has disappeared

### 3.5 Declared revocation latency

If revocation is not immediate, the system must declare the maximum revocation latency.

For delegation that materially affects normal downward exit, user withdrawal capability, or restoration of independent control over reserve-backed or Bitcoin-denominated balances, the declared revocation latency must not exceed the constitutional maximum downward movement delay.

For other forms of delegation, the declared revocation latency must be specifically disclosed, technically justified, and bounded strongly enough that escape does not become practically illusory.

Any declared revocation latency that renders escape, exit, or independent control practically unavailable to ordinary users may constitute a breach under the constitution and [Breach and Restoration Standard](breach-and-restoration-standard.md).

### 3.6 Revocation must not weaken funds recoverability

A revocation process must not force the user into a worse trust model merely to revoke a delegate.

---

## Section 4. Recovery Independence from Daily Operators

### 4.1 Core requirement

Recovery must not depend on the same actors, infrastructure, or control path that run the system's ordinary daily operations.

### 4.2 Independent recovery path

A compliant system must provide an independent recovery capability sufficient to restore user control under the conditions contemplated by Article XXVI.6.

### 4.3 Required failure assumptions

Recovery must remain possible if the ordinary operator:

- disappears
- is captured
- refuses service
- is legally restrained
- experiences prolonged outage
- becomes malicious

### 4.4 No single-operator recovery choke point

No single operator, company, hosted API, or centralized service may be the only path by which a user can recover from dependence.

### 4.5 Recovery documentation

The system must document, in technically accurate but user-legible form:

- how recovery works
- what prerequisites are needed
- what happens if the operator disappears
- what happens if the user loses routine access but still holds ultimate recovery material
- what conditions, delays, or thresholds apply

### 4.6 Distinction from normal use

Recovery architecture is not required to be convenient for daily use.

It is required to be real, independent, and durable.

### 4.6A Partial recovery quorum failure

The system must document the recovery path where one or more recovery quorum participants become unavailable, hostile, seized, or uncooperative during the recovery process.

That path must not require the cooperation of the hostile or unavailable party to complete, provided the remaining constitutionally sufficient recovery authority still exists.

If quorum loss below the required threshold would make recovery impossible, that condition must be explicitly disclosed as part of the recovery model.

### 4.7 External data dependency

Recovery, revocation, and restoration of independent control must not depend on external data sources whose unavailability, compromise, or manipulation would block or indefinitely delay recovery.

This includes, where relevant:
- oracles
- price feeds
- attestation services
- external state proofs
- third-party API responses

If an external data source is used, the architecture must preserve a bounded, non-discretionary fallback path that allows the user to recover, unwind, or otherwise regain control without waiting indefinitely for that source to return.

---

## Section 5. Archival Offline Recovery Environments

### 5.1 Core requirement

Recovery must be possible from archival offline materials without dependency on operator-controlled live servers for key interpretation, address discovery semantics, or fundamental recovery logic.

### 5.2 What offline recovery must preserve

An archival offline recovery environment must preserve, at minimum:

- recovery-critical software behavior
- recovery profile semantics
- key and metadata interpretation
- address derivation semantics
- descriptor or script interpretation, where relevant
- documentation sufficient to perform recovery

### 5.3 Allowed online dependencies

Network access may still be required to:

- fetch blockchain data
- broadcast transactions
- synchronize chain state

But operator-controlled live services must not be required for any step of the recovery process beyond standard blockchain data access and transaction broadcast.

A recovery path that depends on operator-controlled live services for interpretation, authorization, execution, or completion of recovery is non-compliant.

### 5.4 Offline recovery package

A compliant system must provide, directly or through verifiable archival means, a recovery package or equivalent recoverability set containing:

- recovery documentation
- recovery-critical software or source
- cryptographic hashes
- version identifiers
- recovery profile data
- metadata needed to reconstruct ownership and discovery logic

### 5.5 Longevity requirement

The archival recovery path must be designed for long-term viability, not merely short-term backup convenience.

### 5.6 No archive bait-and-switch

A system must not publish archival recovery materials and later render them useless through silent semantic drift.

---

## Section 6. Hash-Pinned Reference Implementations

### 6.1 Core requirement

Recovery-critical software versions must be cryptographically identifiable and verifiable.

### 6.2 Hash pinning

A compliant system must publish cryptographic hashes for recovery-critical software, including where relevant:

- binaries
- scripts
- deterministic build outputs
- source references
- manifests

### 6.3 No silent updates

Recovery-critical software must not be silently updated.

Any update affecting recovery semantics, key handling, profile interpretation, descriptor interpretation, or discovery logic must be:

- visible
- documented
- versioned
- opt-in where constitutionally required

Any change to recovery-critical software or recovery-profile semantics must result in active notification to affected users through the system's primary user-facing interface, where such an interface exists. Publication in a changelog or technical note alone is insufficient.

### 6.4 Known-good verification

Users must be able to verify that they are running a known-good reference implementation or a functionally equivalent implementation.

### 6.5 Public release record

A durable public record of recovery-critical releases must be maintained.

Recovery-critical release records must be maintained for the longer of:
- the life of the system
- or 10 years from the last active use of the relevant recovery profile

### 6.6 Reproducibility where reasonably achievable

Where reasonably achievable, recovery-critical reference implementations should support reproducible verification paths. If not, the system must document what substitute integrity guarantees exist.

---

## Section 7. Frozen Recovery Profiles

### 7.1 Core requirement

A compliant system must provide a defined recovery profile or set of recovery profiles whose semantics do not silently change over time.

### 7.2 Meaning of a recovery profile

A recovery profile includes, where relevant:

- derivation path
- descriptor structure
- script type
- address discovery logic
- profile version
- key interpretation rules
- required metadata

### 7.2A Activation timestamps and applicability record

Each recovery profile version must carry a publicly recorded activation timestamp or activation block reference.

The system must maintain a durable record of:
- which recovery profile version was in force
- during which time window
- and, where reasonably achievable, which balances or deposits were placed under that profile

This record must be sufficient to determine which recovery semantics applied at the time a user entered the system.

### 7.3 Profile stability

If a user follows the recovery procedure in force at the time funds were placed under that profile, the user must remain able to recover those funds later, provided the user still possesses the required secrets and the publicly documented chain data.

### 7.4 No silent derivation or mapping changes

No compliant implementation may silently change:

- derivation paths
- descriptor interpretation
- wallet mapping rules
- discovery behavior
- script interpretation

for existing balances.

### 7.5 Legacy discovery preservation

Legacy discovery must remain available for previously supported balances, either:

- natively in current software
- or through a fixed archival recovery path that preserves prior semantics

### 7.6 New profiles

New recovery profiles may be introduced prospectively, but the existence of a new profile must not make old profiles unreadable, undiscoverable, or unsupported for existing balances.

### 7.7 Profile export

Recovery profiles must be exportable in an open, durable, machine-readable form sufficient to support independent recovery.

Exported recovery profiles must:
- use publicly documented formats
- be free from IP restrictions that prevent independent parsing or implementation
- be interpretable without vendor-specific tooling
- contain enough information to reconstruct profile semantics independently

---

## Section 8. Relationship to Other Standards

### 8.1 Constitution

This standard operationalizes:

- Article XXV (Long-Term Recoverability and Compatibility Continuity)
- Article XXVI (Dependence Must Remain Escapable)

### 8.2 UX Constitution

The user-facing implications of this standard, including warnings, recovery walkthroughs, and continuity disclosures, are governed by [UX Constitution](ux-constitution.md).

### 8.3 Definitions and Interpretive Notes

Interpretation of edge cases, terminology, and anti-gaming guidance is informed by [Definitions and Interpretive Notes](definitions-and-interpretive-notes.md), but this document remains binding within its scope.

### 8.4 Breach and Restoration Standard

Violations of this standard may constitute breach conditions and are classified under [Breach and Restoration Standard](breach-and-restoration-standard.md).

### 8.5 Operational Independence and Concentration Standard

Where delegation, custody, revocation, or recovery architecture creates operational concentration in signers, operators, jurisdictions, infrastructure, or user access paths, this standard applies together with [Operational Independence Standard](operational-independence-standard.md).

A software architecture that is formally correct but operationally concentrated may still be constitutionally weak.

---

## Final Rule

A user who still possesses valid recovery authority must not lose control merely because:

- a hot key was compromised
- an operator disappeared
- a service was captured
- a vendor changed software
- a live server stopped functioning
- a delegated path failed

If the user can still prove rightful control under the constitution, the architecture must still provide a real path home.
