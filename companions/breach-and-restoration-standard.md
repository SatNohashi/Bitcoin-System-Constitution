# Breach and Restoration Standard of the Bitcoin System Constitution

**Author:** Satoshi Nohashi  
**License:** CC0 1.0 Universal (Public Domain Dedication)  
**Website:** [bitcoinsystemconstitution.org](https://bitcoinsystemconstitution.org)  
**Type:** Binding 
**Supports:** The article titled **Breach, Restoration, and Continuity** of the Bitcoin System Constitution, regardless of final article numbering 
**Status:** Draft 

---

## Purpose

This standard is binding. It defines how breaches of the Bitcoin System Constitution are classified, disclosed, evaluated, cured where possible, and recorded where cure is impossible.

It exists to prevent seven recurring failure patterns:

1. A system breaches the constitution, patches the issue, and pretends nothing happened.
2. A system downgrades a serious breach into a minor issue through vague language.
3. A system stays in "uncertainty notice" mode indefinitely to avoid harder disclosure obligations.
4. A system claims restored compliance too quickly, before users have had a practical opportunity to understand the breach and respond.
5. A system rewrites history backward and calls that "restoration."
6. A system treats concurrent breaches as isolated technical incidents when together they compromise the whole constitutional system.
7. A system remains permanently non-compliant while continuing to market itself as constitutionally trustworthy.

This standard defines:

- breach severity classification
- continuity effects of breaches
- cure types
- time sensitivity and disclosure deadlines
- historical integrity rules
- evidence requirements for claiming restored compliance
- naming consequences
- the difference between forward remediation and impermissible retroactive correction
- system-wide effects of concurrent breaches

---

## Governing Rules

1. This standard uses the definitions in **Article I** of the constitution exclusively.
2. Where more than one classification could apply, the **highest applicable severity** controls.
3. Where no exact case is listed, classification must default to the **nearest more conservative** reading, not the more forgiving one.
4. Aggravating factors may elevate a breach by one level where constitutionally justified. Mitigating factors may affect cure conditions, but do not reduce a breach below its baseline classification.
5. No claim of restored compliance is valid unless the conditions in this standard are met publicly and verifiably.
6. In the absence of a companion technical or operational standard, interpretation must default to the reading that best protects:
 - exit rights
 - reserve and liability truth
 - custody independence
 - non-discretionary operation
 - censorship resistance
 - practical path to inclusion
 - constitutional time limits
 - user freedom
7. Disputes over breach classification, restoration, continuity, or evidence may be reviewed under the **Constitutional Dispute and Review Standard of the Bitcoin System Constitution** where that document exists. In its absence, the public evidence and conservative-reading rules in this document control.
8. A system's own classification of its breach status is non-authoritative. Compliance status is determined by observable behavior and evidence under this standard and may be independently evaluated by external parties.

---

## Section 1. Failure Severity Classes

### Overview Table

| Level | Class | Description | Continuity Effect | Typical Cure Status |
|---|---|---|---|---|
| 1 | Minor deviation | Technical non-conformance without material user impact | No continuity break by default | Automatically curable or curable with disclosure |
| 2 | Material breach | Violation affecting constitutionally protected user interests | Continuity may survive, depending on severity and disclosure | Usually curable with disclosure or scarred |
| 3 | Continuity-breaking breach | Material breach severe enough to end uninterrupted constitutional continuity | Continuous compliance is broken | Scarred or not curable under same continuity claim |
| 4 | Permanent non-compliance | The system cannot restore compliance under its current identity | Current identity cannot truthfully claim compliance | Not curable under current identity |
| 5 | Successor-required | A new system is required if constitutional compliance is ever to be claimed again | Current system identity cannot continue as compliant | Only cure is a new successor system with fresh consent |

---

### Level 1. Minor deviation

A **minor deviation** is technical non-conformance that does not materially impair user rights, reserve integrity, custody safety, constitutional time limits, governance sunsets, asset-class clarity, or practical ability to transact or exit.

#### Typical examples
- A documentation mismatch that does not affect actual behavior.
- A proof publication formatting defect where the proof itself remains current and independently verifiable.
- A temporary non-critical implementation inconsistency with no material user effect.

#### What it is not
It is not a minor deviation if it affects:
- exit rights
- reserve truth
- liability truth
- custody safety
- credit versus money distinction
- governance authority or time windows
- user asset clarity
- practical transaction inclusion

---

### Level 2. Material breach

A **material breach** is a breach that affects constitutionally protected user interests, even if the system may still remain recoverable under its current identity.

#### Typical examples
- Functional exit blocking.
- Hidden reserve lending.
- Missing proof cadence repeatedly.
- Presenting stale proof as current.
- Misrepresenting a credit instrument as money.
- Transaction-level censorship of valid ordinary transactions.
- Governance action after the governance sunset date, where the act is isolated and immediately disclosed.

#### Typical effect
A Level 2 breach may or may not break continuity. Severity, concealment, duration, and user impact determine whether it escalates to Level 3.

---

### Level 3. Continuity-breaking breach

A **continuity-breaking breach** is a material breach severe enough that the system can no longer truthfully claim uninterrupted constitutional continuity from the point it adopted the constitution.

#### Typical examples
- Discretionary freezing of normal downward exit.
- Repeated undisclosed reserve impairment.
- Misrepresentation of constitutional compliance during a known material breach.
- Continued governance operation after sunset in a way that materially affects users.
- Silent migration behavior that materially changes trust assumptions without fresh consent.
- Repeated proof cadence failure combined with concealment or active current-backing claims.

#### Typical effect
The system may possibly become **currently compliant** again later, but it is permanently **historically breached** and may never claim uninterrupted compliance across the breach period.

---

### Level 4. Permanent non-compliance

A **permanent non-compliance** event means the system, under its current identity, can no longer restore constitutional compliance.

#### Typical examples
- Protocol-level changes after the final hard stop window.
- Governance continuing after the governance window in a sustained or structural way.
- Constitutional amendment attempts after the constitutional amendment window closes.
- Replacing governance or constitutional authority through disguised renamed structures after sunset.
- Persistently operating core functions through a model that is constitutionally incompatible and not reversible under the same identity.

#### Typical effect
The current system identity may continue to exist technically, but it cannot truthfully claim compliance.

---

### Level 5. Successor-required

A **successor-required** event means the only path back to constitutional compliance is a **new system** that users voluntarily enter.

#### Typical examples
- Forced migration into a new trust model.
- Silent remapping of balances into a new system.
- Retroactive rewriting of ownership or settlement history as a supposed cure.
- Continuing a permanently non-compliant system while claiming continuity under a refreshed brand or architecture.
- Governance or constitutional authority being functionally restarted under a new wrapper within the same claimed system identity.

#### Typical effect
The current system identity must not continue to claim constitutional compliance. Only a successor, with fresh voluntary consent, may seek compliance.

---

## Section 2. Cure Types

### Type A. Automatically curable

This applies where the system corrects itself through ordinary operation without requiring a special constitutional disclosure process, and without any material user impact.

**Typical fit:** Level 1 only.

### Type B. Curable with disclosure

This applies where a fix is possible, but the system must publicly disclose:
- what happened
- when it happened
- who was affected
- what changed
- whether continuity was impacted

**Typical fit:** Level 1 or Level 2.

### Type C. Scarred

This applies where the system may return to current compliance, but the breach history is permanently part of its record. It may not claim uninterrupted compliance across the breach period.

**Typical fit:** Level 2 or Level 3.

### Type D. Not curable

This applies where the system cannot restore constitutional compliance under its current identity.

**Typical fit:** Level 4 or Level 5.

---

## Section 3. Time Sensitivity, Uncertainty Notices, and Disclosure Windows

### 3.1 Acknowledgment duty

A system must acknowledge a known or reasonably suspected breach **without unreasonable delay**.

For binding evaluation, the following principles apply:

1. Breaches affecting **exit, reserves, liabilities, custody, governance authority, constitutional clocks, constitutional naming, or compliance status** require the fastest acknowledgment.
2. If full facts are not yet known, the system must publish an **uncertainty notice** rather than remain silent.
3. Silence when a material breach is known or reasonably inferable is itself an aggravating factor and may elevate the breach independently of the underlying cause.

---

### 3.2 Uncertainty notice requirements

An uncertainty notice is a temporary preliminary disclosure. It must include, at minimum:

1. what is known
2. what is unknown
3. what users should assume conservatively for now
4. whether exit, reserves, liabilities, custody, governance, or proof cadence may be affected
5. what the immediate user implications are
6. when the next update will be published

An uncertainty notice does not suspend the system's broader disclosure obligations. It only bridges the period before fuller disclosure is possible.

---

### 3.3 Hard deadlines for uncertainty notices and fuller disclosure

#### High-severity issue classes
For reasonably suspected issues affecting:
- exit
- reserve truth
- liability truth
- custody
- governance authority or governance time limits
- constitutional clocks
- compliance misrepresentation
- constitutional naming
- proof cadence failure involving reserve-backed claims

the following hard deadlines apply:

- **uncertainty notice:** within **24 hours**
- **fuller disclosure:** within **72 hours**
- **update cadence while uncertain:** every **24 hours**

#### Lower-severity issue classes
For lower-severity issues without current material effect on user rights, reserves, custody, governance, or exit:

- **uncertainty notice:** within **72 hours**
- **fuller disclosure:** within **7 days**
- **update cadence while uncertain:** every **72 hours**

---

### 3.4 Maximum uncertainty period

An uncertainty notice may not remain the system's sole disclosure state beyond the applicable maximum uncertainty period above.

At the end of that period, the system must publish the fullest disclosure then available, including:
- all facts known
- all facts still unknown
- current user impact
- worst-case implications if uncertainty remains
- next remedial steps

A system may not avoid fuller disclosure by claiming it still lacks perfect information.

---

### 3.5 Consequences of missed uncertainty deadlines

Failure to issue:
- the initial uncertainty notice on time,
- the required interim updates on time,
- or the fuller disclosure by the hard deadline

constitutes an aggravating factor and may itself be treated as a separate disclosure breach.

Repeated or strategic use of uncertainty status to avoid harder obligations should generally elevate severity by one level.

### 3.6 Silence as breach

Failure to disclose a known or reasonably inferable material breach within the required timeframe shall be treated as a minimum Level 3 continuity-breaking breach, regardless of the underlying breach classification.

---

## Section 4. Historical Integrity Rules

1. Breach history cannot be erased.
2. A system may be:
 - currently compliant
 - currently non-compliant
 - restored to compliance
 - historically breached
 - permanently non-compliant
3. "Currently compliant" and "continuously compliant" are not the same claim.
4. A system that suffered a continuity-breaking breach may never claim uninterrupted compliance across that breach period.
5. Material breach history is permanent on the constitutional record.
6. Minor deviations should remain in technical history, even if they do not permanently scar constitutional standing.
7. All material breach disclosures must remain permanently accessible in a public, durable location. Breach records must not be removed, rewritten, buried, or made practically inaccessible over time.

### Practical meaning
A system may say:
- "currently compliant, historically breached"
but may not say:
- "continuously compliant"
if continuity was broken.

---

## Section 5. Evidence Requirements for Claiming Restored Compliance

The burden of proof always lies on the system claiming restoration.

### 5.1 Required public disclosure

At minimum, the system must disclose:

1. the **nature** of the breach
2. the **scope** of the breach
3. the **timing** of the breach
4. the **affected functions, balances, or users**
5. the **constitutional article or articles implicated**
6. the **remediation taken**
7. whether the breach **broke continuity**
8. whether the system claims:
 - current compliance
 - restored compliance
 - or successor treatment

All such disclosures must be made in a public, durable location reasonably discoverable by affected users.

### 5.2 Evidence standard

Claims of restoration must be supported by the strongest publicly available evidence appropriate to the breach, including where relevant:
- on-chain evidence
- cryptographic proof
- updated proof-of-reserves and liabilities
- custody disclosures
- governance records
- published timelines
- public code or configuration changes
- independently checkable operational evidence

### 5.3 Minimum restoration conditions

No system may claim restored compliance until:

1. the breach has been publicly disclosed
2. the remediation is actually active, not merely promised
3. users have had a practical opportunity to understand the breach and, where relevant, exercise normal downward movement after disclosure under conditions that are not rendered illusory by excessive fees, excessive delays, or discriminatory access conditions
4. the system is no longer engaging in the breaching behavior
5. the system is not falsely presenting the breach period as uninterrupted compliance

### 5.4 Minimum remediation periods before claiming restored compliance

#### Level 1
No earlier than **24 hours** after full disclosure and active remediation.

#### Level 2
No earlier than **72 hours** after full disclosure and active remediation, where the affected protections include:
- exit
- reserve or liability truth
- custody
- proof cadence for reserve-backed claims
- governance or constitutional clocks
- compliance status or naming

#### Level 3
A system may never claim restored **continuity**. 
It may claim current compliance only as **historically breached** and no earlier than **7 days** after full disclosure and active remediation, with all scar conditions disclosed.

#### Level 4 and Level 5
No restored compliance claim is available under the same system identity.

### 5.5 Exit accessibility during remediation

A restoration claim is invalid if exit remains technically available but practically inaccessible due to excessive fees, delays, or discriminatory conditions. Exit must remain reasonably accessible to ordinary users during the restoration period.

### 5.6 Restoration claim publication

Restoration claims must be published in the same public, durable location as the original breach disclosure and must be directly linked to it. Restoration claims must not be scattered across multiple locations or hidden within unrelated communication channels.

### 5.7 Independent verification

Where a breach concerns:
- reserves
- liabilities
- custody
- governance authority
- constitutional clocks
- or system state needed for exit

the claim of restoration should be independently verifiable to the maximum extent technically possible.

---

## Section 6. Naming Consequences

### 6.1 Minor deviation
A system may continue using constitutional naming if the deviation is corrected and did not create material user confusion or harm.

### 6.2 Material breach
A system may continue using constitutional naming only if it does not misrepresent itself as continuously compliant and if it discloses the breach honestly.

### 6.3 Continuity-breaking breach
A system may use constitutional naming only with clear breach disclosure. It may not present itself as uninterruptedly compliant.

### 6.4 Permanent non-compliance
A system must not present itself as constitutionally compliant. It may describe itself as a former implementation, legacy implementation, or non-compliant implementation, but not as currently compliant.

### 6.5 Successor-required
A new system must not inherit constitutional naming by default. It must independently demonstrate compliance and obtain user trust on its own.

### 6.6 Misrepresentation
A system that continues to use constitutional naming while materially violating this standard or the constitution is engaged in misrepresentation.

---

## Section 7. Forward Remediation vs Impermissible Retroactive Correction

This section is central.

### 7.1 Forward remediation

**Forward remediation** means correcting future behavior without rewriting valid prior constitutional reality.

Forward remediation is generally acceptable if it:
- occurs within the allowed constitutional and governance windows
- is publicly disclosed
- does not retroactively alter valid ownership or settlement
- does not erase breach history
- does not require users to pretend the breach never happened

### 7.2 Impermissible retroactive correction

**Impermissible retroactive correction** means rewriting or undoing prior valid system history, ownership, settlement, or constitutional reality in order to cosmetically repair a breach or undo an undesirable outcome.

This is generally not acceptable.

### 7.3 Hard rule on rollback and history rewrite

A rollback, reorganization, or state reversal performed to:
- undo theft
- rescue users from bad contract programming
- reverse liquidation outcomes
- reverse politically painful but valid economic results
- or cosmetically repair a breach

is an impermissible retroactive correction.

If a system performs such a correction, the current system identity becomes **permanently non-compliant**, and any constitutionally compliant continuation must occur only through a **successor system** with:

- a new identity
- new clients
- no automatic migration
- no inherited constitutional continuity
- manual user exit and manual entry only

### 7.4 Invalid-state correction and core-rule breakage

If the system's published core monetary or consensus intent was broken, such as:
- more coins being created than the published rules allow
- objectively invalid blocks being accepted as if valid

actors may choose to correct that invalid state, but such correction does not restore constitutional continuity for the existing system identity if it requires rollback, reorganization, or state reversal of already-observed history.

In that case:
- the old system becomes permanently non-compliant
- a new system may be launched if users choose to trust it
- there is no automatic migration path
- users must move manually by exiting the old system and entering the new one

The purpose of this hard consequence is deterrence. It ensures that any actor considering rollback or history rewrite understands that the constitutional cost is severe and public.

### 7.5 Classification table

| Action | Classification |
|---|---|
| Fixing a core bug that enabled theft, going forward | Acceptable forward remediation |
| Patching a vulnerability prospectively | Acceptable forward remediation |
| Prospectively tightening governance rules within allowed windows | Acceptable forward remediation |
| Chain reorganization to undo theft or rewrite already-valid settled history | Impermissible retroactive correction |
| Rolling back state to before an exploit by rewriting valid final state | Impermissible retroactive correction |
| Retroactively changing governance rules to justify past actions | Impermissible retroactive correction |
| Retroactively changing ownership mapping to erase a breach | Impermissible retroactive correction |
| Rollback or reorganization to erase invalid supply creation or objectively invalid accepted blocks | Impermissible retroactive correction under current identity; only successor path remains if actors choose to proceed |

### 7.6 General test

Ask:

1. Does the action change future behavior only, or does it rewrite past valid state?
2. Does it preserve the constitutional truth model of the affected layer?
3. Does it require users to accept that history changed rather than that the system learned?
4. Does it erase evidence of the breach rather than disclose it?

If the answer points to rewriting past valid reality, it should generally be treated as impermissible retroactive correction.

---

## Section 8. Specific Breach Classifications

These are presumptive classifications. Aggravating or mitigating circumstances may shift the final level, but not below the constitutional seriousness of the act.

| Event | Presumptive Severity | Typical Cure Type | Notes |
|---|---|---|---|
| Governance action after year 25 | Level 2, Material breach | Curable with disclosure or scarred | May escalate if sustained or concealed |
| Continued protocol decisions after year 25 | Level 3, Continuity-breaking breach | Scarred or not curable | Likely breaks continuity |
| Any new protocol-level change after year 30 | Level 4, Permanent non-compliance | Not curable | Only successor path remains |
| Hidden reserve lending | Level 2, Material breach | Curable with disclosure or scarred | May escalate if prolonged or concealed |
| Functional exit blocking | Level 2, Material breach | Curable with disclosure or scarred | May escalate if sustained |
| Misrepresenting compliance status | Level 2, Material breach | Curable with disclosure or scarred | May escalate if intentional and prolonged |
| Missed proof cadence, promptly disclosed, affected claims marked stale or unproven | Level 1 or 2 | Curable with disclosure | Severity depends on duration and user impact |
| Repeated or persistent failure to meet declared proof cadence | Level 2, Material breach | Curable with disclosure or scarred | May escalate if prolonged or paired with reserve uncertainty |
| Failure to publish proof while continuing to present claims as currently backed or currently proven | Level 2 or 3 | Scarred or curable with disclosure | Concealment and duration matter |
| Backdating, falsifying, or misleading proof timestamps or cadence records | Level 3, Continuity-breaking breach | Scarred or not curable | May escalate if tied to reserve impairment |
| Stale proof presented as current proof | Level 2, Material breach | Curable with disclosure or scarred | May escalate if tied to reserve distress |
| Reserve custody downgrade without disclosure | Level 2, Material breach | Curable with disclosure or scarred | May escalate if user funds materially endangered |
| Transaction-level censorship of valid ordinary exits | Level 2 or 3 | Curable with disclosure or scarred | Depends on duration and concentration |
| Forced migration into new trust model | Level 5, Successor-required | Not curable | Requires new system and fresh consent |
| Silent balance remapping into successor | Level 5, Successor-required | Not curable | Identity continuity is broken |
| Governance continuation by renamed wrapper after sunset | Level 4 or 5 | Not curable | Depends on continuity claim and migration behavior |
| Retroactive rewriting of valid settled history to "repair" a breach | Level 5 | Not curable | Successor treatment required |

---

## Section 9. Concurrent Breaches and Propagation

### 9.1 Local classification

Every breach shall first receive an independent **local classification** by:
- article violated
- affected function
- severity level
- cure type

Lower-severity breaches do not disappear merely because a higher-severity breach also exists.

### 9.2 Propagation assessment

After local classification, each breach shall also receive a **propagation assessment**:

- **Isolated** 
 confined to a bounded optional component or non-core function
- **Core-propagating** 
 affects constitutional core guarantees strongly enough to set system-wide status
- **Cross-contaminating** 
 interacts with other breaches in a way that raises total system severity

### 9.3 Core-propagating breaches

A breach is **core-propagating** when it materially affects:
- normal downward exit
- reserve truth
- liability truth
- reserve custody independence
- constitutional clocks
- governance sunset or governance scope
- forced migration
- compliance misrepresentation
- constitutional continuity

A core-propagating breach sets the minimum **system-wide current status** at its severity level, even if other breaches are lower.

### 9.4 Cross-contamination

A breach is **cross-contaminating** when concurrent breaches share:
- a common cause
- a common operator set
- a common concealment pattern
- a common choke point
- or materially compounded user impact

Cross-contaminating breaches may elevate the system-wide classification by one level where constitutionally justified, even if each breach alone would be classified lower.

### 9.5 Isolated breaches

A breach may remain function-scoped only where it is clearly bounded, fully disclosed, and does not materially impair any constitutional core guarantee.

### 9.6 Example

If a system has:
- a **Level 3 breach** in exit rights, and
- a **Level 2 breach** in reserve labeling,

then:
- the exit breach is likely **core-propagating**
- the system-wide current status is at least **Level 3**
- the reserve labeling breach remains independently recorded
- the labeling breach may act as an aggravating factor if it worsened user confusion during the Level 3 event

### 9.7 Cross-contamination example

If a system:
- misses its declared proof cadence for reserve-backed claims, and
- simultaneously uses a misleading interface, notification, or public status display that conceals, downplays, or fails to clearly present that stale-proof condition,

then:
- the proof cadence breach and the clarity breach may be classified as cross-contaminating
- the shared operator set and shared concealment pattern may justify elevation of the system-wide classification
- the compounded harm is greater than either breach alone because users are deprived not only of current proof, but also of their practical ability to detect the missing proof and respond

This remains true even if each individual breach might otherwise appear curable in isolation.

---

## Section 10. Aggravating and Mitigating Factors

### 10.1 Aggravating factors
These factors may elevate the severity class by one level where constitutionally appropriate:

- concealment
- delayed disclosure
- operator enrichment during the breach
- insider advantage
- repeated occurrence
- misleading public statements
- impairment of user exit
- impairment of reserve truth
- impairment of user ability to distinguish asset class
- rewriting history rather than disclosing failure
- remaining in uncertainty status beyond the maximum allowed period

### 10.2 Mitigating factors
Mitigating factors may influence cure conditions but do not erase the breach. Examples include:
- prompt disclosure
- fast and honest remediation
- absence of operator benefit
- preserved user exit during remediation
- public evidence sufficient for independent verification

---

## Section 11. Interpretive Priority

When breach classification is disputed, the preferred classification is the one that best prevents the following abuse patterns:

- hiding a serious breach behind technical wording
- treating disclosure as cure without real remediation
- remaining indefinitely in uncertainty mode
- rewriting history to cosmetically restore legitimacy
- claiming continuity after a constitutionally significant break
- using short duration as an excuse for severe breach
- using branding to preserve trust after constitutional reality has changed

This standard exists to make breach handling honest, not convenient.
