# Operational Independence and Concentration Standard of Bitcoin System Constitution

**Author:** Satoshi Nohashi  
**License:** CC0 1.0 Universal (Public Domain Dedication)  
**Website:** [bitcoinsystemconstitution.org](https://bitcoinsystemconstitution.org)  
**Type:** Binding 
**Supports:** Article XXIV (Directional Decentralization and Operational Concentration), clause 7; Article X (Transaction-Level Censorship Resistance), clause 6 
**Definitions:** Uses Article I definitions exclusively, particularly: constitutional layer, support system, component, independent control domain, ordinary transaction, ordinary user, practical path to inclusion, non-discretionary, strongest available security model, compliance, provisional custody 
**Status:** Draft 

---

## Purpose

This standard defines the measurable thresholds and tests for when operational concentration becomes constitutionally unacceptable.

It exists because protocol compliance alone is not enough. A system can follow every rule in code and still become a de facto gatekeeper if too much practical control sits with one operator, one company, one cloud provider, one client implementation, one jurisdiction, or one coordinated cluster.

This standard therefore defines:

- a sliding-scale anti-concentration framework
- choke-function analysis
- operational concentration measurement
- censorship-resistance thresholds
- directional decentralization measurement
- phase-based expectations
- compliance zones and transitions

This standard is binding. It does not replace the constitution. It operationalizes the concentration and censorship-resistance duties imposed by the constitution.

---

## Governing Principles

1. The constitution protects users from practical gatekeeping, not merely from formal rule violations.
2. Concentration is evaluated by **control over choke functions**, not by raw node counts alone.
3. Thresholds must scale with real operational participation and real user dependence.
4. A small network and a large network are not judged by the same raw numbers, but both remain bound by minimum floor expectations.
5. "We are still early" is never a permanent excuse for dangerous concentration.
6. User preference for one provider in an otherwise genuinely open market is not by itself a constitutional breach. Structural chokepoints, incentive lock-in, or dependency traps are.
7. Where uncertainty exists, measurements and classifications shall default to the more conservative reading that best protects exit, inclusion, reserve truth, and user freedom.

---

## Section 1. Sliding-Scale Anti-Concentration Framework

### 1.1 Measurement window

Unless otherwise specified, concentration shall be measured over a trailing **90-day** window. 
If the system or relevant component is younger than 90 days, measurement uses the full lifetime of the live system to date.

### 1.2 Independent control domains

For each choke function, the system must identify the set of **independent control domains** actively participating in that function during the measurement window.

Let:

- **N** = number of independent control domains actively performing the choke function during the measurement window.

For this standard, N is used only to compute dynamic thresholds. It is not a constitutional validator-count requirement.

### 1.3 Dynamic threshold functions

For any choke function with active participation count **N**, the following thresholds apply.

#### Single-cluster thresholds
Used for:
- largest operator share
- largest jurisdiction share
- largest infrastructure-provider share
- largest client-implementation share
- largest exit-dependency share

**Green threshold:**
- `SG(N) = max(0.15, min(0.50, 1.25 / N))`

**Yellow threshold:**
- `SY(N) = max(0.25, min(0.67, 1.75 / N))`

**Red threshold:**
- `SR(N) = max(0.35, min(0.80, 2.25 / N))`

If a measured single-cluster share exceeds **SR(N)**, that metric is in the **Critical** zone.

#### Top-three concentration thresholds
Used for:
- top-three operator share
- top-three coordinated-cluster share

**Green threshold:**
- `TG(N) = max(0.45, min(0.90, 3.25 / N))`

**Yellow threshold:**
- `TY(N) = max(0.60, min(0.95, 4.25 / N))`

**Red threshold:**
- `TR(N) = max(0.75, min(0.98, 5.25 / N))`

If a measured top-three share exceeds **TR(N)**, that metric is in the **Critical** zone.

### 1.3A Design intent of threshold constants

The constants used in the threshold functions are not arbitrary. They are chosen to create three properties at once:

1. A small network is not judged by the same raw counts as a larger network.
2. Early networks are not permanently excused from meaningful distribution.
3. As the number of active independent control domains grows, acceptable concentration tightens rather than remaining flat.

The constants are calibrated so that, for small and mid-sized live systems, Green status requires visibly meaningful distribution across independent domains, Yellow status warns before concentration becomes constitutionally dangerous, and Red status captures concentration severe enough to threaten ordinary operation or exit.

These functions are binding unless amended through the constitutionally valid process. Disagreement with the constants is not by itself grounds to suspend their application.

### 1.4 Floor expectation

Regardless of formula output:

1. A core choke function with only **one** active independent control domain cannot be Green.
2. A core choke function with only **one** active independent control domain is **Red at minimum**, and may be **Critical** if it controls ordinary operation, reserve custody, or normal downward exit.
3. A core choke function with fewer than **three** active independent control domains cannot be Green unless the system is in a declared provisional phase with public caps, deadlines, and decentralization milestones.

### 1.5 No permanent bootstrap excuse

A system may begin above its long-term concentration target, but:
- that concentration must be publicly disclosed
- its reduction path must be published
- it must have deadlines
- failure to reduce concentration on that path has constitutional consequences

---

## Section 2. Choke Function Analysis

### 2.1 Choke-function principle

A **choke function** is any operational function whose failure, capture, concentration, or coordination can materially affect:

- transaction inclusion
- normal downward exit
- reserve truth
- reserve custody
- proof publication
- settlement publication
- bridge release or redemption
- protocol mutability
- practical user access to constitutional rights

### 2.2 Core choke functions

The following are core choke functions:

1. Transaction ordering or sequencing.
2. Block production, validation, or equivalent acceptance of state updates where those functions affect ordinary inclusion.
3. Canonical bridge operation or release where a canonical path depends on it.
4. Normal downward exit processing.
5. Reserve custody for direct Bitcoin claims or Layer 2 transactional balances.
6. Proof generation, proof publication, or authoritative reserve-state publication for reserve-backed claims.
7. Upgrade deployment while protocol mutability still exists.

### 2.3 Auxiliary choke functions

The following may be auxiliary choke functions, but become core if practical user dependence is high:

1. Fee setting, where operator-controlled.
2. Routing and mempool access.
3. Settlement publication if ordinary users materially depend on it.
4. Withdrawal batching or release services.
5. Shared relayer systems.
6. Common attestation pipelines.

An auxiliary choke function becomes a **core choke function** when either of the following is true:

1. More than **50 percent** of ordinary users depend on it for normal operation or normal downward exit.
2. Its failure, capture, or concentration would delay normal downward exit beyond the constitutional maximum or materially impair practical path to inclusion.

Once an auxiliary choke function becomes core, it must be measured and zoned under the same rules as any other core choke function.

### 2.4 What matters more than node count

A system must not rely on raw node count as its primary concentration defense if practical control of choke functions remains concentrated elsewhere.

---

## Section 3. Concentration Measurement

### 3.1 Unit of measurement

Concentration must be measured by **effective control**, not merely by nominal participation.

Effective control may include aggregation across:

- the same legal entity
- the same corporate family
- the same operator cartel
- the same funding controller
- the same infrastructure cluster
- the same jurisdictional capture domain
- the same code implementation if a common failure or exploit would disable all of them together

### 3.2 Required concentration measures

For each core choke function, the system must publish, at minimum:

1. **Largest operator share** 
 The share of the choke function controlled by the single largest independent control domain.

2. **Top-three operator share** 
 The cumulative share controlled by the three largest independent control domains.

3. **Largest jurisdiction share** 
 The share capturable by one legal or regulatory jurisdiction.

4. **Largest infrastructure-provider share** 
 The share dependent on the same cloud provider, datacenter family, or equivalent infrastructure cluster.

5. **Largest client-implementation share** 
 The share dependent on the same codebase or client implementation for that choke function.

6. **Largest exit-dependency share** 
 The share of users whose normal downward exit depends on the same operational cluster.

### 3.3 Correlated failure domains

Operators that would likely fail together under the same stress event shall be measured together where constitutionally relevant.

Examples include:
- same corporate parent
- same major cloud dependency
- same jurisdictional seizure path
- same client monoculture
- same signer-hosting provider

### 3.4 Reserve custody overlap

Where reserve custody exists, this standard measures operational concentration of custody clusters. Exact signer requirements remain governed by [Reserve Custody and Key Management Standard](reserve-custody-and-key-management-standard.md).

### 3.5 Materiality floor

For this standard:

1. A change is presumptively **material** if a measured concentration, delay, dependency, or resilience metric worsens by more than **5 percent relative deterioration** within a single reporting period, unless a publicly documented and constitutionally neutral justification is provided.
2. A comparison is **materially comparable** only where the transactions, users, or operational conditions being compared are similar in type, fee conditions, network conditions, and constitutional function.
3. Comparisons that mix unlike conditions in order to dilute concentration, delay, or censorship findings are invalid.

### 3.6 Anti-gaming measurement rule

Trailing-window averages do not excuse short periods of constitutionally dangerous concentration.

If any concentration metric exceeds the applicable **Red** threshold for more than **7 consecutive days** within the reporting window, that metric shall be treated as Red for the reporting period unless the system proves that the excursion was caused solely by a neutral and temporary failure outside operator control.

If any concentration metric exceeds the applicable **Critical** threshold for more than **72 consecutive hours**, that metric shall be treated as Critical for the reporting period unless the system proves that the excursion was caused solely by a neutral and temporary failure outside operator control.

Temporary cosmetic expansion of nominal participants that does not create durable independent control domains does not reduce concentration for purposes of this standard.

---

## Section 4. Censorship Resistance Thresholds

### 4.1 Practical path to inclusion

A practical path to inclusion exists only if an ordinary user can submit a valid ordinary transaction through a public, documented, and non-discretionary path without:

- special relationships
- identity-gated access
- insider-only routing
- extraordinary technical effort
- extraordinary fee burden

### 4.2 Acceptable delay

Under normal conditions, a valid ordinary transaction is considered within acceptable delay if it is included within:

- the greater of **3 times** the rolling median inclusion time for comparable transactions under comparable fee conditions, or
- **12 blocks** where the transaction is part of normal downward movement

This threshold may be refined by later review, but not weakened without public justification.

### 4.3 Sustained censorship

Sustained censorship is presumed where valid ordinary transactions, or a specific affected class of such transactions, are:

- delayed beyond **2 times** the acceptable-delay threshold for more than **24 hours**, or
- repeatedly subjected to materially worse inclusion than comparable transactions across **three or more distinct 24-hour windows** in a rolling **30-day** period, without neutral justification

### 4.4 No practical path to inclusion

A practical path to inclusion is presumed absent where:

1. All public submission paths are identity-gated, relationship-gated, or practically inaccessible to ordinary users.
2. Fees required for inclusion exceed materially comparable neutral market fees without publicly justified and generally applied reasons.
3. The only paths require insider coordination or extraordinary infrastructure.
4. A single operator or coordinated cluster can indefinitely refuse inclusion for valid ordinary transactions.

### 4.5 Neutral reasons that do not count as censorship

The following do not by themselves constitute censorship, provided they are published, identity-blind, and generally applied:

- malformed transaction rejection
- invalid state rejection
- minimum fee rules applied consistently
- temporary congestion management
- anti-spam rules applied neutrally
- contract terms that the user explicitly and voluntarily accepted

### 4.6 Economic coercion and incentive-based suppression

Where there is credible evidence that financial incentives, bribery, side payments, induced coordination, or other economic coercion are being used to systematically exclude, delay, or disadvantage a class of valid ordinary transactions, that pattern shall be evaluated as censorship under this standard.

The standard does not distinguish between suppression by formal command and suppression by economic inducement.

Such a pattern may qualify as sustained censorship even if no written rule prohibits inclusion.

---

## Section 5. Directional Decentralization Measurement

### 5.1 Progress, stagnation, regression

Directional decentralization is measured across reporting periods.

A system is **progressing** if:
- at least three core concentration metrics improve over two consecutive reporting periods, and
- no core concentration metric materially worsens

A system is **stagnating** if:
- concentration remains materially unchanged across two consecutive reporting periods, and
- network participation, user reliance, or value under operation has grown materially

A system is **regressing** if:
- a core metric worsens by more than **10 percent relative deterioration** across a reporting period, or
- operator or governance decisions entrench existing chokepoints

If a system crosses into a worse compliance zone under Section 7, the zone transition governs current compliance status immediately, regardless of whether the directional deterioration threshold in this section has been crossed.

### 5.2 Entrenching centralization

A system is presumed to be entrenching centralization if it:

- keeps a provisional structure open-ended
- preserves incumbent privilege in operator admission
- resists addition of independent control domains without public justification
- allows concentration to worsen as participation or value grows
- shifts more choke functions under the same actor set

### 5.3 Required reporting cadence

A system must publish concentration and decentralization reports at least every **90 days**, and additionally within **7 days** of entering a worse compliance zone.

Such reports must be published in a public, durable, and reasonably discoverable location. Reports published only in obscure technical channels, private dashboards, or inaccessible API outputs do not satisfy this requirement.

---

## Section 6. Phase-Based Expectations

### 6.1 Principle

The sliding scale must not become a permanent excuse for dangerous concentration because the network is still small.

### 6.2 Provisional phase

A system may be treated as in a provisional decentralization phase only if all of the following are true:

1. The concentration is publicly disclosed.
2. The affected choke functions are named.
3. The system publishes a public decentralization plan.
4. The plan includes deadlines and measurable milestones.
5. Reserve size or operational exposure is bounded where constitutionally relevant.
6. The system does not present provisional operation as mature compliance.

### 6.3 Required decentralization plan

A constitutional decentralization plan must publish:

- the current concentration state
- the target state
- measurable milestones
- deadlines
- blocker explanations
- consequences if milestones are missed

### 6.4 No permanent early-phase excuse

No system may rely indefinitely on claims such as:
- "we are still early"
- "we are still decentralizing"
- "this is temporary"

without measurable progress.

Persistent failure to progress converts provisional concentration into a compliance problem.

### 6.5 Exit from provisional status

A system exits provisional decentralization status only when:

1. it has met its published decentralization milestones
2. it satisfies the applicable Green-zone requirements for all core choke functions
3. it has remained outside provisional caps and exception logic for at least **two consecutive reporting periods**
4. no material concentration exception remains undisclosed or unresolved

A system may not remain labeled provisional after these conditions are satisfied, nor may it claim mature compliance before they are satisfied.

---

## Section 7. Compliance Zones

### 7.1 Zone definitions

| Zone | Status | Meaning |
|---|---|---|
| Green | Compliant | Concentration within acceptable bounds for current network size and structure |
| Yellow / Warning | At risk | Concentration approaching constitutional concern; corrective action required |
| Red / Failure | Non-compliant | Concentration too high to call the system compliant |
| Critical | Continuity-threatening | Concentration so severe it may break constitutional continuity |

### 7.2 Zone assignment

For each core choke function, assign a zone based on the worst applicable measured metric:

- **Green** if all measured metrics are within Green thresholds
- **Yellow** if any metric exceeds Green but none exceeds Yellow
- **Red** if any metric exceeds Yellow but none exceeds Red
- **Critical** if any metric exceeds Red

The system-wide zone is the worst zone among its core choke functions, adjusted upward where cross-function dependence materially compounds risk.

### 7.3 Zone consequences

#### Green
- compliant with this standard

#### Yellow / Warning
- mandatory public disclosure within **7 days**
- corrective action plan within **30 days**
- no claim that concentration is safely resolved

#### Red / Failure
- current non-compliance under this standard
- presumptive material breach under [Breach and Restoration Standard](breach-and-restoration-standard.md)
- public disclosure within **72 hours**
- corrective action plan within **14 days**

#### Critical
- presumptive continuity-breaking breach
- may trigger successor logic if sustained, concealed, or combined with other core breaches
- immediate disclosure required under the Breach and Restoration Standard
- in addition to immediate public disclosure, Critical zone status requires active notification to users through the system's primary user-facing interface within the same disclosure timeframe, where such an interface exists

### 7.4 Transition rules

A system enters a worse zone immediately upon crossing the threshold.

A system returns to a better zone only after:
- two consecutive reporting periods at the better level, and
- public disclosure of the transition

### 7.5 User preference safeguard

A system is not in breach merely because many users prefer one provider, wallet, or interface, so long as:
- alternatives remain genuinely open
- alternatives remain practical for ordinary users
- the protocol and incentives do not structurally entrench one chokepoint

---

## Section 8. Interaction with Other Standards

### 8.1 Constitution

This standard operationalizes:
- Article XXIV (Directional Decentralization and Operational Concentration)
- Article X (Transaction-Level Censorship Resistance)

### 8.2 Breach and Restoration Standard

Red and Critical zone conditions may trigger classification under [Breach and Restoration Standard](breach-and-restoration-standard.md).

### 8.3 Reserve Custody and Key Management Standard

Where concentration concerns reserve custody specifically, this standard works together with [Reserve Custody and Key Management Standard](reserve-custody-and-key-management-standard.md).

### 8.4 Verification Checklist

[Verification Checklist](../reference/verification-checklist.md) may assist evaluators in applying this standard consistently, but does not override this standard.

### 8.5 UX Constitution

Where concentration manifests through user-facing access paths to constitutional functions, including wallet dominance, interface routing dominance, or practical monopoly over visible exit paths, this standard applies together with [UX Constitution](ux-constitution.md).

A chokepoint in user-facing access may constitute operational concentration even where alternative paths exist in theory, if ordinary users are not given a practical and visible way to use them.

---

## Final Rule

The real question is not:

**"How many validators or operators do we have?"**

The real question is:

**"How easy is it for one pressure point to control meaningful operation or exit right now?"**

If that answer becomes dangerously favorable to one pressure point, the system is in constitutional danger, no matter how good the code looks.
