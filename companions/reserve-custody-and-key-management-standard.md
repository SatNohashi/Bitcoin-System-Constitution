# Reserve Custody and Key Management Standard of Bitcoin System Constitution

**Author:** Satoshi Nohashi  
**License:** CC0 1.0 Universal (Public Domain Dedication)  
**Website:** [bitcoinsystemconstitution.org](https://bitcoinsystemconstitution.org)  
**Type:** Binding 
**Supports:** Article XIV (Reserve Custody Independence, Non-Unilateral Control, and Open Participation), Section 3 
**Definitions:** Uses Article I definitions exclusively, particularly: custody structure, independent control domain, provisional custody, materially weakens, non-unilateral, reserve, liability, direct Bitcoin claim, Bitcoin transactional balance 
**Status:** Draft 

---

## Purpose

This companion standard defines the exact custody thresholds and operational requirements referenced by Article XIV of the Bitcoin System Constitution.

It exists because reserve truth is not enough if the reserves are held under weak custody. A reserve that is visible but one key, one signer cluster, one jurisdiction, or one infrastructure provider away from loss is not constitutionally sound.

This standard defines:

- minimum signer counts and threshold requirements
- minimum independent jurisdiction distribution
- single-jurisdiction concentration limits
- key ceremony requirements
- hardware security requirements
- signer rotation cadences
- recovery quorum rules
- anti-sybil requirements for signer admission
- signer removal procedures and conditions
- concentration limits and threshold bands
- when custody concentration becomes non-compliant
- caps and constraints during provisional custody
- recovery behavior if many signers disappear
- auditability of signer changes
- effects of signer addition on custody safety
- proof that operator admission requirements are objective

This standard is binding. It does not weaken, blur, or contradict Article XIV of the constitution.

---

## Governing Principles

1. No reserve backing direct Bitcoin claims or Layer 2 transactional balances may be subject to unilateral control.
2. Apparent signer count is not enough. Real independence matters more than headline diversity.
3. A custody structure must be secure against:
   - single-key failure
   - single-operator compromise
   - small-clique collusion
   - single-jurisdiction coercion
   - infrastructure monoculture
   - silent signer substitution
4. Provisional custody is allowed only as a disclosed, bounded, capped transition. It is not full compliance.
5. Signer growth must reduce concentrated control, not merely expand the appearance of decentralization.
6. If a custody threshold or requirement is not explicitly met, the more conservative compliance reading applies.

---

## Section 1. Scope and Applicability

### 1.1 In-scope reserves

This standard applies to all reserves backing:

- direct Bitcoin claims
- Bitcoin transactional balances on Layer 2
- any other balance that the system presents as reserve-backed Bitcoin access

### 1.2 Out of scope

This standard does not directly govern:

- purely optional Layer 3 credit instruments
- unbacked utility balances
- speculative balances not presented as reserve-backed Bitcoin

However, if any such system is marketed or functionally presented as reserve-backed Bitcoin access, this standard applies.

### 1.3 Measurement basis

Where thresholds depend on reserve exposure, exposure shall be measured as the **highest daily reserve-backed balance** observed during the trailing **30-day** window, denominated in BTC.

---

## Section 2. Custody Bands and Minimum Threshold Requirements

### 2.1 Principle

Thresholds scale with reserve exposure. Lower exposure does not excuse unsafe custody forever, but higher exposure demands materially stronger custody.

### 2.2 Minimum operational signer bands

| Reserve-backed exposure (BTC) | Minimum active operational signers (N) | Minimum spend threshold (T) | Minimum independent jurisdictions |
|---|---:|---:|---:|
| >0 to 250 BTC | 3 | 2 | 2 |
| >250 to 2,500 BTC | 5 | 3 | 3 |
| >2,500 to 25,000 BTC | 7 | 5 | 4 |
| >25,000 BTC | 9 | 6 | 5 |

### 2.3 Higher bands allowed

A system may voluntarily adopt the thresholds of a higher band than required by current exposure. Doing so is constitutionally favored.

### 2.4 Full-compliance floor

A system meeting only the minimum of the lowest band is not automatically fully compliant if other independence, concentration, or provisional-custody conditions are not met.

### 2.5 Threshold rule

For any operational signer set:

1. The spend threshold must always be greater than one.
2. The spend threshold must always exceed one half of the active signer count once N is 7 or greater.
3. No single signer and no subset below the threshold may unilaterally move, steal, or encumber reserves.

---

## Section 3. Jurisdiction, Entity, and Infrastructure Distribution

### 3.1 Single-jurisdiction limit

No single jurisdiction may control, host, or legally compel enough operational signers to satisfy the spend threshold by itself.

### 3.1A Jurisdiction definition for custody purposes

For purposes of this standard, a jurisdiction means a distinct legal and regulatory compulsion domain in which a single legal order could compel all signers located within it simultaneously.

Jurisdictional independence is measured by practical compulsion risk, not by superficial geographic labeling.

Different subdivisions within the same sovereign legal order do not automatically count as separate jurisdictions if the same legal or regulatory process could compel them together.

### 3.2 Jurisdiction concentration rule

For fully compliant custody:

- no single jurisdiction may contain more than **T - 2** active operational signers
- and no single jurisdiction may contain more than **one third** of active operational signers, whichever is stricter

### 3.3 Corporate-family limit

No single legal entity or corporate family may control more than:

- **1** operational signer in any band
- **2** recovery quorum members in any band

This limit applies regardless of provisional status.

Provisional custody may relax exposure band requirements and maturity timing only where explicitly allowed by this standard. It does not relax independence requirements.

### 3.4 Infrastructure concentration limit

No single cloud provider, hosting cluster, datacenter family, managed key provider, or equivalent infrastructure concentration point may support more than:

- **one third** of active operational signers for bands at or above 7 signers
- **one half** of active operational signers for bands below 7 signers

### 3.5 Client implementation concentration

For bands at or above 7 operational signers:

- no single signing software implementation may support more than **two thirds** of active operational signers

For exposures above 25,000 BTC:

- no single signing software implementation may support more than **one half** of active operational signers

### 3.6 Correlated domains

Where several signers share the same effective control, failure domain, or compromise path, they shall be measured together.

---

## Section 4. Key Ceremony Requirements

### 4.1 Required public ceremony record

Every initial key ceremony and every full re-ceremony must generate a durable public record sufficient to verify:

- ceremony date
- signer count
- threshold
- participating jurisdictions
- hardware or HSM class used
- software versions or signing stack versions
- cryptographic identifiers or fingerprints of resulting public keys
- whether the ceremony was initial, replacement, or emergency

### 4.2 Secret handling

Private key material must not be transmitted in plaintext or reconstructed outside the declared secure ceremony process.

### 4.3 Witnessing and attestation

Each ceremony must produce signed attestations from participating custody operators that:

- the declared process was followed
- the stated threshold and signer distribution are accurate
- no undeclared shared control exists to the best of the attestors' knowledge

For reserve-backed exposure above **2,500 BTC**, at least one independent non-signer witness must attest to ceremony conduct. That attestation must be published alongside participant attestations and must identify whether the witness observed any deviation from the declared ceremony process.

### 4.4 Emergency ceremonies

Emergency re-ceremonies are allowed, but must be publicly disclosed within **24 hours** of completion unless disclosure would itself materially endanger funds. In that case, disclosure must occur as soon as the acute danger has passed.

---

## Section 5. Hardware Security Requirements

### 5.1 Core requirement

Operational and recovery signing material must be generated, stored, and used in hardware-isolated environments appropriate to their role.

### 5.2 Prohibited practices

The following are prohibited for reserve-backed custody:

- storing reserve-signing keys in general-purpose hot wallets
- using browser-managed key storage for reserve movement authority
- exporting plaintext private key material after generation except where constitutionally required for a separately protected archival recovery process
- relying on ordinary cloud VM memory as the primary long-term home of reserve-signing keys

### 5.3 Acceptable control environments

Reserve-signing material must use one or more of:

- dedicated HSMs
- hardware wallets or signing devices with verified firmware paths
- air-gapped signing environments
- secure enclaves with public attestation, where constitutionally appropriate
- functionally equivalent secure hardware architectures

### 5.4 Recovery hardware

Recovery quorum material must be held in colder and materially more isolated environments than routine operational signers.

---

## Section 6. Rotation, Review, and Signer Changes

### 6.1 Regular review cadence

All signer assignments, jurisdictions, infrastructure dependencies, and software stacks must be reviewed at least every **180 days**.

### 6.2 Rotation cadence

Operational signing material must be rotated or re-attested no less often than every **24 months**, unless the system publishes a stronger security justification for a longer interval and that interval does not exceed **36 months**.

### 6.3 Immediate rotation triggers

Immediate rotation or removal action is required upon:

- suspected key compromise
- confirmed signer compromise
- undisclosed shared control discovered
- critical software compromise in the signing stack
- signer legal capture that materially changes coercion risk
- signer insolvency
- signer regulatory shutdown, dissolution, or equivalent forced cessation
- material violation of this standard by a signer

Upon a mandatory immediate rotation trigger, the affected signer's authority must be suspended as soon as constitutionally and operationally possible pending completion of rotation or replacement. It is not sufficient merely to schedule rotation while the compromised or constitutionally impaired signer remains active.

### 6.4 Public disclosure of signer changes

Planned signer addition, removal, or replacement must be publicly disclosed at least **7 days** before taking effect.

Emergency changes may occur faster, but must be disclosed within **24 hours** unless acute risk temporarily prevents disclosure.

### 6.5 Auditability

A durable public record of signer additions, removals, replacements, and threshold changes must be maintained.

---

## Section 7. Recovery Quorum Rules

### 7.1 Independent recovery requirement

A reserve-backed custody system must maintain a recovery quorum independent from the daily operational signer path.

### 7.2 Minimum recovery quorum

| Reserve-backed exposure (BTC) | Minimum recovery quorum members | Minimum recovery threshold | Minimum independent jurisdictions |
|---|---:|---:|---:|
| >0 to 2,500 BTC | 5 | 3 | 3 |
| >2,500 to 25,000 BTC | 5 | 4 | 3 |
| >25,000 BTC | 7 | 5 | 4 |

### 7.3 Overlap limit

No more than **40 percent** of recovery quorum members may also be active operational signers.

In addition:
- overlap members must not by themselves be sufficient to satisfy both the operational spend threshold and the recovery threshold
- the overlap set must not create a practical path for the same small coordinated group to dominate both ordinary reserve movement and recovery reconstitution

If a band-specific configuration would allow such dual domination despite numerical compliance, the custody structure is non-compliant.

### 7.4 Recovery quorum strength

A recovery quorum must not be materially easier to compromise than the operational custody path. If a lower threshold is used for recovery, the system must justify why the colder environment and stronger isolation offset the lower numerical threshold.

### 7.5 Recovery trigger

Recovery quorum authority may be used only for:

- reconstituting the operational signer set
- restoring user control after operator disappearance or refusal
- replacing compromised signers
- preserving funds when operational quorum is no longer reliable

It must not be used as a convenience shortcut for ordinary reserve movement.

---

## Section 8. Anti-Sybil Admission Requirements

### 8.1 Objective criteria

Signer admission criteria must be:

- public
- rule-based
- specific
- measurable

### 8.2 Independence proof

A candidate signer must demonstrate independent control domain status through one or more of:

- public disclosure
- cryptographic attestation
- legal separation evidence
- operational separation evidence
- jurisdictional separation evidence
- privacy-preserving but reviewable independence attestations that can be evaluated under the Constitutional Dispute and Review Standard process, with evidence made available to that process under appropriate confidentiality protections

Self-assertion alone is insufficient.

### 8.3 No arbitrary incumbent veto

Incumbent signers may reject applicants only for failure to meet published criteria, not for competitive, political, or social preference.

### 8.4 Anti-sybil aggregation

Candidates with shared beneficial control, shared coercion path, or shared infrastructure dependency may be counted as one effective control domain for compliance purposes.

---

## Section 9. Signer Removal Procedures and Conditions

### 9.1 Mandatory removal or suspension triggers

A signer must be suspended or removed when:

- compromise is confirmed
- prolonged unavailability exceeds published maximum tolerance
- false independence claims are proven
- required rotation or re-attestation is refused
- the signer becomes part of an unconstitutional concentration cluster
- the signer materially violates this standard

### 9.2 Emergency suspension

Emergency suspension may occur before full investigation where credible risk to reserves exists. Such suspension must be followed by public disclosure and review.

### 9.3 No silent removal

Signer removal must not occur silently.

### 9.4 Replacement safety

Adding or replacing signers must not:
- lower threshold protections
- worsen jurisdiction concentration
- worsen operator concentration
- worsen infrastructure monoculture
- make recovery weaker

For planned changes, a post-change concentration analysis must be published at least **7 days** before the change takes effect.

That analysis must be publicly reviewable and sufficiently detailed for independent evaluators to assess whether concentration, independence, and recovery posture are materially weakened.

Emergency changes may occur faster, but the same analysis must be published within **24 hours** after the change unless acute risk temporarily prevents disclosure.

---

## Section 10. Provisional Custody Rules

### 10.1 Principle

Provisional custody is a transitional state only. It is not fully compliant custody.

### 10.2 Minimum provisional requirements

A system claiming provisional custody must, at minimum:

- satisfy the lowest exposure band thresholds
- disclose its provisional status publicly
- publish a reserve cap
- publish a maturity plan
- publish deadlines and milestones
- disclose the precise ways in which it is not yet fully compliant

### 10.3 Duration limit

Provisional custody may not continue beyond **12 months** from activation of the reserve-bearing component unless a stricter project-specific deadline has already been declared.

### 10.4 Reserve cap

A provisional system must hard-cap reserve-backed exposure at a publicly declared amount before accepting user funds.

That cap:
- must be technically enforceable or publicly auditable
- must not be raised without **30 days** prior public notice
- must not be raised if prior maturity milestones have been missed
- may be raised only after the immediately preceding maturity milestone has been publicly verified as complete

Being merely not-yet-late is not sufficient to justify a cap increase.

### 10.5 No full compliance claim

A provisionally custodied system must not claim:
- full constitutional compliance
- full compliance with Article XIV
- full reserve-custody compliance

It may only claim provisional or partial compliance, with explicit disclosure.

### 10.6 Failure to mature

Failure to meet the published maturity path or deadline constitutes a compliance issue under the constitution and may escalate under the Breach and Restoration Standard.

---

## Section 11. Recovery if Many Signers Disappear

### 11.1 Operational quorum loss

If operational signer availability falls below threshold:

1. ordinary reserve movement must halt unless constitutionally necessary for user protection
2. recovery quorum procedures must begin under published rules
3. public disclosure must occur within **24 hours**

Such a halt must not block users from initiating normal downward exit through the recovery quorum path or any other constitutionally valid alternative path that remains available.

### 11.2 Recovery quorum degradation

If recovery quorum availability also falls below threshold:

- the system must publicly disclose that reserve recovery is at risk
- affected balances must not continue to be represented as normally secure
- constitutional breach evaluation may be triggered

### 11.3 Reconstitution

Reconstitution of signer sets must preserve or improve:
- threshold security
- independence
- jurisdictional spread
- concentration posture

It must not be used as a pretext to consolidate power.

---

## Section 12. Concentration Limits and Compliance Zones

### 12.1 Green

Custody is Green only if:
- all applicable band thresholds are met
- no concentration limit is exceeded
- no provisional-custody status remains
- recovery quorum requirements are met
- signer changes are fully auditable

### 12.2 Yellow / Warning

Yellow applies where:
- a concentration limit is approached or slightly exceeded
- a required rotation is overdue but not dangerously so
- independence evidence is incomplete
- a signer cluster has become temporarily too correlated

Yellow requires:
- public warning within **7 days**
- corrective action plan within **30 days**

### 12.3 Red / Failure

Red applies where:
- a required threshold or distribution rule is materially violated
- provisional custody overstays its deadline
- one operator cluster or jurisdiction materially dominates reserve movement
- recovery quorum requirements fail but no actual loss or rewrite has yet occurred

Red is non-compliant and should be classified under the Breach and Restoration Standard.

### 12.4 Critical

Critical applies where:
- unilateral or near-unilateral reserve movement becomes possible
- a single coercion domain can practically compel reserve movement
- reserve recovery is plausibly impossible under current conditions
- signer concentration makes immediate user loss realistically likely

Critical conditions may constitute continuity-threatening breach.

### 12.5 Return to Green

A system that has entered Yellow, Red, or Critical custody status may return to Green only after:

- meeting Green requirements for all applicable custody metrics
- maintaining those conditions for **two consecutive reporting periods**
- publicly disclosing the return-to-Green claim with supporting evidence

A temporary single-period improvement is not sufficient to re-establish Green status.

---

## Section 13. Relationship to Other Standards

### 13.1 Constitution

This standard operationalizes Article XIV of the Bitcoin System Constitution.

### 13.2 Operational Independence Standard

Where custody concentration overlaps broader operator concentration, this standard works together with [Operational Independence Standard](operational-independence-standard.md).

### 13.3 Breach and Restoration Standard

Violations of this standard are classified under [Breach and Restoration Standard](breach-and-restoration-standard.md).

### 13.4 Verification Checklist

[Verification Checklist](../reference/verification-checklist.md) may assist evaluators in applying this standard consistently, but does not override this standard.

### 13.5 UX Constitution

User-facing disclosure of custody structure, custody-zone status, provisional custody status, and material custody-zone changes is governed jointly by this standard and [UX Constitution](ux-constitution.md).

Where custody status changes materially affect user trust assumptions, users must be informed through constitutionally compliant interface disclosure.

---

## Final Rule

A reserve backing Bitcoin access is constitutionally sound only when:

- it is real
- it is current
- it is unencumbered
- and no single person, operator cluster, jurisdiction, or hidden clique can quietly take it away
