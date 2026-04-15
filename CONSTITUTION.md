# Bitcoin System Constitution

**Author:** Satoshi Nohashi  
**Contact:** satoshinohashi@proton.me  
**Website:** [bitcoinsystemconstitution.org](https://bitcoinsystemconstitution.org)  
**Repository:** [github.com/SatNohashi/Bitcoin-Freedom-Constitution](https://github.com/SatNohashi/Bitcoin-Freedom-Constitution)  
**Bitcoin Reference:** [github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin) | [bitcoin.org/bitcoin.pdf](https://bitcoin.org/bitcoin.pdf)  
**License:** CC0 1.0 Universal (Public Domain Dedication)  

---

## Preamble

This constitution defines the non-negotiable principles for designing, operating, maintaining, and evaluating Bitcoin-aligned systems whose purpose is to maximize monetary freedom, preserve honest trust boundaries, and prevent users from being cheated by architecture, governance, implementation drift, hidden dependency, or captured control.

This constitution is not a product pitch. It is a constitutional standard.

It exists to ensure that Bitcoin remains the root money, that transactional systems built around Bitcoin preserve usability without corrupting scarcity, and that higher-risk systems for programmability or experimentation do not gain the power to trap, redefine, or quietly degrade user freedom.

This constitution recognizes that different systems may implement these goals in different technical ways. It therefore defines functional roles, rights, protections, and hard boundaries rather than requiring one monolithic architecture.

A separate UX constitution shall exist to support the ideals of this protocol-level constitution. That UX constitution must not weaken, blur, or contradict the protections defined here. See [UX Constitution](companions/ux-constitution.md).

This constitution is voluntary in applicability and strict in claim. The rules governing applicability, adoption, and compliance claims are defined in Article XXIX.

Interpretive guidance for defined terms and boundary cases is provided in [Definitions and Interpretive Notes](companions/definitions-and-interpretive-notes.md). Article-by-article intent and examples are provided in the Constitutional Commentary, available at [bitcoinsystemconstitution.org](https://bitcoinsystemconstitution.org).

---

## Article I. Definitions

The following terms carry specific meaning throughout this constitution. Adversarial reinterpretation of undefined language is a known attack vector. These definitions exist to close it.

### Section 1. Core Structure

1. **Bitcoin** means the Bitcoin network as defined by the longest valid proof-of-work chain under the consensus rules of Bitcoin, including its native monetary unit.
2. **Layer 1** means the Bitcoin base layer: final settlement, long-term savings, self-custody, and monetary truth.
3. **Layer 2** means the transactional Bitcoin support layer: low-fee payments, high-speed transfers, fine-grained accounting, and safer fallback from higher-risk systems. Layer 2 must remain simpler, harder, and more conservative than Layer 3.
4. **Layer 3** means the smart contract and experimentation layer: high-speed execution, apps, automation, tokenized systems, and optional financial risk-taking.
5. **Constitutional layer** means any of the three functional layers, or any future functional equivalent explicitly mapped to them under this constitution.
6. **Component** means any distinct technical part of a constitutional layer, including sublayers, modules, domains, chains, rollups, bridges, or support systems.
7. **Sublayer** means an internal subdivision within a constitutional layer that performs a subset of that layer's functions.
8. **Module** means a separable functional unit within a layer or component.
9. **Support system** means infrastructure that assists a constitutional layer but does not itself hold user funds, define monetary truth, define reserve truth, control custody, or determine normal user exit unless and until its operational role makes it constitutionally significant or it is otherwise reclassified under this constitution.

### Section 2. Monetary Asset Classes

10. **Direct Bitcoin claim** means a balance whose holder can redeem it for actual Bitcoin on Layer 1 through a non-discretionary, published, trust-minimized process without requiring permission from any intermediary.
11. **Bitcoin transactional balance** means a Bitcoin-denominated balance on Layer 2 used for ordinary payments, transfers, and commerce under Layer 2 rules.
12. **Bitcoin utility balance** means a Bitcoin-denominated balance on Layer 3 used within Layer 3 under Layer 3 rules, subject to Layer 3 risk.
13. **Native gas token** means a token used to pay for computation, execution, or transaction processing on Layer 3, which may or may not be Bitcoin-denominated.
14. **Governance token** means a token that confers voting, decision, or protocol-influence rights within a system.
15. **Credit instrument** means any instrument involving lending, rehypothecation, maturity mismatch, counterparty risk, discretionary repayment, or yield derived from reserve use.
16. **Reserve** means assets held to back outstanding claims.
17. **Liability** means outstanding claims against reserves.
18. **Encumbered reserve** means a reserve that is lent, pledged, staked, rehypothecated, or otherwise committed beyond simple backing of the claim it supports.
19. **Unencumbered reserve** means a reserve that is free from any commitment, lien, pledge, lending arrangement, or use beyond backing its corresponding claim.

### Section 3. Trust and Movement

20. **Canonical interlayer path** means one or more standard, published, protocol-defined routes for moving Bitcoin or Bitcoin-denominated balances between constitutional layers under the system's claimed core safety properties.
21. **Trust-minimized** means relying on cryptographic proof, protocol rules, or independently verifiable mechanisms rather than trust in any specific party, to the maximum extent practically achievable.
22. **Strongest available security model** means the most trust-minimized coupling achievable given the current state of technology. Any claim that a model is the strongest available must be supported by a publicly documented threat model, including:
   - the trust assumptions being made
   - the stronger alternatives considered
   - the reasons those alternatives were not used
   - the failure modes of the chosen approach
   Assertions without such justification are not sufficient.
23. **Trusted path** means an interlayer movement path that relies on trust in one or more specific parties rather than on cryptographic or protocol-enforced proof.
24. **Contractual path** means an interlayer movement path governed by legal, business, or contractual relationships rather than protocol-enforced rules.
25. **Non-discretionary** means operating by published rules without case-by-case human judgment, political consideration, or selective enforcement.
26. **Downward exit** means movement of Bitcoin or Bitcoin-denominated balances from a higher layer to a lower harder layer.
27. **Normal downward movement** means ordinary, non-emergency downward exit performed under standard conditions.
28. **Functional exit blocking** means any condition that makes downward exit practically unavailable to ordinary users even if it is not structurally prohibited, including identity gates, legal intermediaries, excessive fees, excessive delays, or approval requirements.
29. **Structural exit blocking** means protocol-level prohibition or absence of a downward exit path.
30. **Exit interference** means any action, design, or condition that materially impairs normal downward movement, whether through delay, fee, approval, identity requirement, or other mechanism.
31. **Plain transferability** means the ability to transfer an unencumbered balance to another party through a simple protocol-native operation without mandatory contract mediation, identity disclosure, or third-party approval.
32. **Voluntary encumbrance** means a restriction on a balance that the holder has explicitly and knowingly opted into under disclosed terms.
33. **Bridge** means any system, contract, protocol, or mechanism that facilitates movement of Bitcoin or Bitcoin-denominated balances between separate systems or trust boundaries by holding, locking, wrapping, custodying, releasing, or intermediating those balances during transit. The existence of a bridge does not by itself satisfy trust-minimized movement, non-discretionary exit, or constitutional safety requirements. Those properties must be demonstrated independently.

### Section 4. Governance and Change

34. **Constitutional genesis** means the earliest publicly verifiable timestamp at which this constitution is published in full in a public durable repository designated under the identity of the system claiming compliance.
35. **Activation** means the point at which a component becomes usable by real users in production, regardless of labels such as beta, preview, pilot, guarded, or limited.
36. **Constitutional amendment** means any change to the text, meaning, or operative effect of this constitution.
37. **Governance authority** means the power to make binding decisions about protocol behavior, rules, parameters, or policy.
38. **Protocol-level decision** means a decision that changes how the protocol behaves for users, including parameter changes, rule changes, upgrade approvals, and emergency actions.
39. **Protocol-level change** means any modification to protocol rules, behavior, parameters, or implementation that affects users.
40. **Final implementation** means the complete deployment and activation of a protocol-level change that was validly approved before the governance hard stop.
41. **Governance sunset** means the permanent cessation of governance authority at the constitutionally specified time.
42. **Constitutional continuity** means unbroken compliance with this constitution from the point of public adoption through the present, without material breach.
43. **Successor system** means a new system that replaces, continues, or claims lineage from an earlier system but must independently demonstrate compliance.
44. **Pre-declared authority** means governance authority that is publicly published in a durable repository, sufficiently specific in subject matter, and fixed before the constitutional amendment window closes. Vague blanket language does not qualify. Such authority must identify the exact domains, parameters, or functions subject to governance. Open-ended, catch-all, or future-extensible authority definitions are invalid under this constitution.

### Section 5. Custody and Control

45. **Custody structure** means the combination of key management, signing authority, access controls, and operational procedures that governs who can move, spend, or encumber reserves.
46. **Unilateral control** means the ability of a single person, single key, single entity, or single coordinated group to move, spend, or encumber reserves without independent authorization from other parties.
47. **Signer** means any party holding a key, share, or equivalent authority that participates in authorizing reserve movements.
48. **Independent control domain** means a signer or signing authority that operates under separate operational, legal, jurisdictional, and infrastructure control from other signers, such that compromise of one does not imply compromise of another.
49. **Custody concentration** means a condition where reserve control is practically dependent on a single entity, a single coordinated group, a single jurisdiction, a single infrastructure provider, or a small enough set that compromise, coercion, or collusion among them is a realistic threat.
50. **Provisional custody** means a custody structure that does not yet meet the constitution's full requirements but is openly disclosed as temporary, operationally bounded, capped, and progressing toward constitutional maturity.

### Section 6. Breach and Compliance

51. **Compliant** means currently meeting all requirements of this constitution as measured by actual behavior, not by claim or certification.
52. **Non-compliant** means currently failing to meet one or more requirements of this constitution.
53. **Restored compliance** means a previously non-compliant system that has corrected its behavior and publicly disclosed the nature, scope, timing, and remediation of its breach, subject to the Breach and Restoration Standard.
54. **Material breach** means a violation of this constitution that affects exit rights, reserve integrity, credit distinction, constitutional time limits, governance sunsets, forced migration, or compliance misrepresentation.
55. **Materially weakens** means any change, action, or condition that reduces the effective protection of a constitutional right, guarantee, or hard boundary, whether by direct amendment, cumulative drift, reinterpretation, operational degradation, fee burden, hidden dependency, or reclassification.
56. **Misrepresentation** means presenting a system's compliance status, risk properties, reserve conditions, or constitutional standing in a way that is materially false or misleading.

Interpretive extension of these definitions is governed by [Definitions and Interpretive Notes](companions/definitions-and-interpretive-notes.md).

---

## Article II. Sovereignty of Bitcoin

1. Bitcoin Layer 1 is the final monetary base recognized by this constitution.
2. No higher layer, component, module, extension, or interface shall claim equality with Bitcoin Layer 1 in monetary finality, censorship resistance, or historical immutability unless it truly possesses those properties.
3. All higher systems exist to serve Bitcoin, not replace it.
4. Any design choice that weakens Bitcoin's role as final settlement is unconstitutional.

---

## Article III. Functional Layer Order

### Section 1. Layer 1

Layer 1 is Bitcoin.

Its role is final settlement, long-term savings, self-custody, and monetary truth.

### Section 2. Layer 2

Layer 2 is the transactional Bitcoin support layer.

Its role is low-fee payments, high-speed transfers, fine-grained accounting, merchant settlement, wage and remittance use, and safer fallback from higher-risk systems.

Layer 2 must remain simpler, harder, and more conservative than Layer 3.

### Section 3. Layer 3

Layer 3 is the smart contract and experimentation layer.

Its role is high-speed execution, smart contracts, apps, automation, tokenized systems, optional financial risk-taking, and experimentation.

Layer 3 is not the monetary base.

### Section 4. Functional interpretation

The constitutional categories of Layer 1, Layer 2, and Layer 3 describe functional trust boundaries, user rights boundaries, and monetary roles. They do not require each layer to be implemented as one indivisible technical component.

A constitutional layer may be composed of multiple internal parts, sublayers, modules, domains, support systems, or future sub-contexts, provided that such decomposition does not weaken, obscure, or evade the constitutional protections, user rights, and risk boundaries assigned to that layer.

---

## Article IV. Honest Risk Hierarchy

1. Risk must be layered and visible, not hidden.
2. The closer a layer is to Bitcoin, the simpler and more hardened it must be.
3. The more expressive and fast a layer becomes, the more clearly optional it must remain.
4. No user shall be misled into treating higher-layer exposure as equivalent to Bitcoin Layer 1 or to a harder lower layer.
5. Marketing, interfaces, economic design, naming, protocol labels, and code-facing definitions must preserve the distinction between money, transactional balances, utility balances, credit, and speculative risk.
6. Internal subdivision of a layer must not be used to hide reserve conditions, blur risk boundaries, weaken exit rights, bypass mutability limits, shift trust assumptions invisibly, or claim constitutional equivalence while behaving differently.

---

## Article V. Monetary Integrity

1. Bitcoin supply shall never be altered by Layer 2 or Layer 3 accounting.
2. Expanded divisibility shall never be treated as expanded supply.
3. Units below the sat may exist for accounting and transactional precision, but they must represent finer claims on the same reserve base, not new money.
4. Ownership proportions must remain unchanged when precision expands.
5. Precision may scale upward. Supply may not.
6. No architectural rearrangement, module split, abstraction layer, or accounting migration may be used to create hidden claims, hidden liabilities, or synthetic supply that is represented as direct Bitcoin.

---

## Article VI. Mission of Layer 2

Layer 2 exists to preserve spendability without weakening scarcity.

Its mandatory goals are:

1. Low fees.
2. Fast confirmation for normal economic activity.
3. Expandable precision for very small balances and prices.
4. Safe handling of tiny remainders and sub-sat balances.
5. Reliable batching and net settlement toward Layer 1.
6. Usability for merchants, workers, savers, and machine-to-machine payments.
7. Meaningfully safer fallback conditions than Layer 3.

Layer 2 is the Bitcoin cash rail of the system and must remain boring enough to survive stress.

---

## Article VII. Boundaries of Layer 2

Layer 2 shall not become a casino chain.

Unless proven consistent with its monetary mission and safety requirements, the following are prohibited on Layer 2:

1. Speculative native money tokens.
2. Complex DeFi structures.
3. Broad app-token sprawl.
4. Governance games capable of rapidly rewriting reserve logic.
5. Hidden leverage.
6. Fractional reserve behavior disguised as accounting precision.
7. Features that make ordinary exit harder in stress conditions.
8. Dependence on external price oracles, external compliance lists, or external value attestations for plain transactional Bitcoin.

Where there is conflict between new features and monetary safety, safety wins.

---

## Article VIII. Divisibility Without Dilution

1. Layer 2 shall support precision beyond the sat for internal accounting.
2. Precision expansion must apply proportionally across balances, prices, fees, and accounting units.
3. Precision expansion must never alter reserves, reserve ratios, or aggregate monetary supply.
4. Dust and remainder balances must not silently disappear.
5. Any unresolved fractional amount must remain attributable to its owner until spent, netted, batched, or settled by published rules.
6. Small balances shall not become protocol property merely because they are inconvenient.
7. The system shall be designed so that rising Bitcoin purchasing power does not make ordinary commerce impractical.

---

## Article IX. Exit as a Right

1. Exit toward harder layers must be a right, not a favor.
2. Movement from Layer 3 to Layer 2, and from Layer 2 to Layer 1, shall not be conditioned on discretionary identity-based approval inside the protocol.
3. No committee, operator group, governance body, multisig council, foundation, or delegated authority may exercise discretionary control over normal downward movement between constitutional layers.
4. No insider class shall receive privileged redemption or withdrawal rights over ordinary users unless that seniority is explicitly declared in advance by asset class.
5. No emergency rule shall selectively trap users by politics, identity, size, affiliation, or jurisdiction.
6. Layer 2 must remain workable even if Bitcoin Layer 1 never changes.
7. Any future Bitcoin Layer 1 improvements shall be treated as upside, not dependency.
8. Functional exit blocking shall be treated the same as structural exit blocking where ordinary users lack a practical non-discretionary path downward without identity-gated or legally mediated intermediaries.
9. The core system must not depend on legally mediated, identity-gated, or committee-controlled infrastructure as the sole or normal means of downward exit.

---

## Article X. Transaction-Level Censorship Resistance

1. A compliant Layer 2 must not permit sustained discretionary suppression of otherwise valid ordinary transactions based on identity, affiliation, political preference, or operator favoritism.
2. No single operator, committee, sequencer, or coordinated group should be able to permanently or systematically prevent valid ordinary transactions from finding a practical path to inclusion.
3. Transaction-level censorship includes not only explicit rejection, but also discriminatory delay, selective routing denial, and systematic refusal to process valid ordinary transfers or exits.
4. This does not require every operator to include every transaction. It requires that the system's architecture preserve a practical path to inclusion for valid transactions without discretionary gatekeeping.
5. Legitimate reasons for non-inclusion of a specific transaction, including malformed data, invalid state, insufficient fee, congestion management, contract conditions not met, or spam resistance, are not censorship under this article.
6. Exact thresholds for what counts as sustained censorship, acceptable delay, and practical path to inclusion may be defined in a later operational standard. In the absence of such a standard, interpretation defaults to the most conservative reading that best protects practical inclusion and user exit.
7. If valid ordinary transactions are blacklisted by coercion and users no longer have a practical neutral path to inclusion, the system is in constitutional breach, except where a restriction arises solely from explicit voluntary encumbrance under known terms and an ordinary plain-transfer path existed outside that encumbrance.
8. Transaction suppression resulting from economic coercion, bribery, or inducement is treated as censorship under this article. The constitution does not distinguish between suppression by command and suppression by incentive.

---

## Article XI. Privacy as a Component of Financial Freedom

1. Users have the right to transact, exit, hold balances, and move between constitutional layers without identity exposure, balance disclosure, or transaction history revelation beyond what is strictly required by the constitutional functions of the system.
2. Privacy is not a secondary preference. It is a constitutional requirement to the maximum extent compatible with reserve truth, liability truth, and non-custodial verification.
3. No compliant system may treat surveillance as a neutral default. Surveillance, identity collection, and transaction monitoring impose a constitutional burden and must be justified by a specific constitutional necessity, not by administrative convenience, growth optimization, abuse prevention convenience, or regulatory anticipation.
4. Where proof obligations and privacy conflict, systems must minimize identity and balance exposure to the maximum extent compatible with reserve truth, liability truth, and non-custodial verification. The chosen method must be publicly justifiable and must favor the least invasive proof approach reasonably achievable under current technology.
5. No system may require identity disclosure as a condition of ordinary transaction, ordinary transfer, or normal downward exit within the protocol, except where a user has explicitly, knowingly, and avoidably opted into a voluntary encumbrance whose terms require it and where a plain-transfer path exists outside that encumbrance.
6. Privacy loss shall not be normalized merely because it is administratively convenient, operationally simpler, or demanded by a non-constitutional external authority.
7. Systems that collect identity, balance, or transaction data beyond what is constitutionally required must disclose:
   - what is collected
   - why it is collected
   - how long it is retained
   - how it is used
   - whether it affects transaction inclusion or exit
   - how users can avoid or minimize that exposure
8. Data collected beyond constitutional necessity must not be retained longer than required for the stated purpose and must not be repurposed without explicit user consent.
9. The right to transact without unnecessary exposure applies equally to savings, commerce, exit, and interlayer movement. No constitutional layer may impose broader surveillance than its proof and safety requirements demand.

---

## Article XII. Distinction Between Bitcoin, Claims, Utility Balances, and Credit

1. Bitcoin, a direct Bitcoin claim, a Bitcoin-denominated utility balance, and a credit instrument are categorically different assets.
2. No credit instrument shall be represented, marketed, displayed, labeled, routed, or settled as if it were Bitcoin or a direct Bitcoin claim.
3. Any instrument involving lending, rehypothecation, maturity mismatch, counterparty risk, discretionary repayment, or yield derived from reserve use must be visibly and permanently labeled as credit.
4. Credit may exist only as an explicit optional risk layer. It may never be disguised as cash, reserve backing, or transactional Bitcoin.
5. Layer 2 shall not require acceptance of credit instruments as money substitutes for normal settlement.
6. A holder must always be able to tell whether they hold Bitcoin, a direct Bitcoin claim, a Bitcoin-denominated utility balance, or someone else's promise.
7. Layer 3 contracts may create credit instruments, lending markets, or yield instruments only by explicit opt-in and with clear labeling. Such instruments must never be confused with core Bitcoin balances, Layer 2 transactional balances, or direct Bitcoin claims.

---

## Article XIII. Reserve Truth, Liability Truth, and Proof Cadence

1. Any direct claim on Bitcoin must be provable without trusting the issuer.
2. Reserve integrity must be independently verifiable by any user through cryptographic, on-chain, or otherwise trust-minimized means.
3. Proof of reserves without proof of liabilities is insufficient.
4. No asset may be presented as a Bitcoin claim unless both the corresponding reserve and the total outstanding claims can be publicly verified.
5. Encumbered, lent, rehypothecated, pledged, or otherwise impaired reserves shall not count as free backing unless explicitly disclosed.
6. Where full real-time proof is impossible, the system must default toward less trust, less leverage, and clearer limitation of claims.
7. All reserves backing direct Bitcoin claims or Layer 2 transactional balances shall be unencumbered by default.
8. Lending, rehypothecation, staking, or yield-seeking use of such reserves is prohibited unless explicitly and individually opted into by the holder under clearly labeled terms.
9. No reserve optimization, treasury efficiency, protocol efficiency, regulatory necessity, audit necessity, or compliance necessity claim may override the default unencumbered status of reserves backing direct Bitcoin claims or Layer 2 transactional balances.
10. Any system presenting direct Bitcoin claims or Layer 2 transactional balances must publish a publicly available proof cadence for reserves and liabilities.
11. That proof cadence must include a declared maximum acceptable lag between valid proofs.
12. Proofs must be timestamped, publicly accessible, and independently verifiable under the standards of this constitution.
13. If the declared proof cadence is missed, the system must not continue presenting the affected claims as currently proven without clearly marking them as stale or unproven.
14. A system that has missed its declared proof cadence beyond the acceptable lag must not represent affected balances as currently backed, currently verified, or fully proven. Such balances must be treated as stale or unproven until valid proof is restored.
15. Persistent failure to meet the declared proof cadence constitutes a compliance issue whose severity shall be evaluated under [Breach and Restoration Standard](companions/breach-and-restoration-standard.md).

---

## Article XIV. Reserve Custody Independence, Non-Unilateral Control, and Open Participation

### Section 1. Custody Independence and Non-Unilateral Control

1. Reserves backing direct Bitcoin claims or Layer 2 transactional balances must be held under a custody structure that is meaningfully resistant to unilateral control, single-key failure, single-operator capture, single-jurisdiction coercion, and silent substitution of signers or key authority.
2. No single key may be sufficient to move, spend, or encumber reserves backing direct Bitcoin claims or Layer 2 transactional balances.
3. No single entity may hold exclusive custody over reserves backing direct Bitcoin claims or Layer 2 transactional balances.
4. Signing authority for such reserves must be operationally distributed across independent control domains.
5. Custody concentration can constitute a constitutional compliance issue even if proof of reserves is technically valid. A reserve is not constitutionally sound merely because it is visible. It must also be held under a custody structure consistent with the constitutional safety claims of the system.
6. Reserve custody structure must be disclosed publicly in sufficient detail for users to understand the control model, coercion exposure, jurisdictional distribution, and failure modes.
7. Key rotation, recovery, signer replacement, or any change to signing authority must not silently weaken the custody model, reduce the effective number of independent control domains, or downgrade users into a worse trust model without public disclosure.
8. No custody change that materially weakens the independence, distribution, or non-unilateral character of reserve control may take effect without prior public notice and an exit window for affected users.

### Section 2. Reserve Custody Growth and Open Participation

1. Reserve custody structures for Layer 2 should be designed to reduce concentrated control over time rather than entrench it.
2. Where reserve signers or equivalent custody operators exist, the system should permit expansion of the signer set through public, rule-based admission criteria rather than incumbent discretion alone.
3. No signer admission process may rely on arbitrary favoritism, hidden approval, or exclusive incumbent control if the system claims to be progressing toward constitutional maturity.
4. Growth in signer participation must not weaken the non-unilateral safety of reserves or create a practical path for a subset of signers to abscond with user funds.
5. The custody structure must be designed so that no single signer and no subset of signers below the required threshold can unilaterally move, steal, or encumber reserves.
6. A system may begin with a more concentrated reserve custody structure than its long-term constitutional target, but that concentration must be openly disclosed as provisional, operationally bounded, capped in reserve size, and treated as a transitional state rather than an acceptable end state.
7. Provisional custody is not compliant custody. A system operating under provisional custody must not represent itself as fully compliant with this article or as fully compliant with the constitution overall, regardless of other constitutional conformance. Such a system may only claim provisional status if a public, bounded maturity path exists with defined milestones, timelines, and consequences for failure to reach constitutional custody requirements.

### Section 3. Companion Standard

1. Exact custody thresholds, including minimum signer counts, minimum independent jurisdictions, key ceremony requirements, HSM specifications, rotation cadences, recovery quorum rules, anti-sybil measures, signer removal procedures, and concentration limits, are defined in [Reserve Custody and Key Management Standard](companions/reserve-custody-and-key-management-standard.md).
2. That standard must not weaken, blur, or contradict the principles defined in this article.

---

## Article XV. Plain Transferability and Voluntary Encumbrance

1. Plain transferability of unencumbered Bitcoin must remain native to the core of Layer 2.
2. Plain transferability of the base Bitcoin-denominated utility balance must remain native to the core of Layer 3.
3. The core protocol of Layer 2 and Layer 3 must not require mandatory contract mediation for ordinary transfer.
4. Users may voluntarily opt into contracts, vaults, escrows, time locks, business rules, or other execution methods after receipt or by explicit choice at the time of use.
5. Voluntary encumbrance must be explicit, visible, and governed by known terms.
6. When the known terms of a voluntary encumbrance expire or are satisfied, the affected balance must return to plain transferable form unless the user explicitly chooses otherwise.
7. External business practices, legal requirements, or regulated workflows at the edges do not redefine the constitutional requirement that the core preserve plain transfer as a native capability.

---

## Article XVI. Role of Layer 3

1. Layer 3 exists for experimentation, programmability, and speed.
2. Layer 3 may use a native gas or utility token.
3. That token must not be marketed as Bitcoin, Bitcoin-equivalent, or Bitcoin-protected unless such protection is explicit, limited, and true.
4. Layer 3 users knowingly opt into greater execution, governance, dependency, and application risk.
5. Layer 3 failure must not redefine Bitcoin ownership on Layer 2 or Layer 1.
6. Layer 3 may be fast and complex. Its base protocol may not trap, censor, or make discretionary the normal downward movement of Bitcoin-denominated balances toward harder layers.
7. This constitution does not forbid voluntary smart contracts, vaults, covenants, or applications on Layer 3 that lock Bitcoin-denominated balances under explicit user-chosen terms. It forbids only the base protocol from imposing such lock-in as a structural condition of the layer itself.
8. Any Layer 3 application that introduces additional custody risk, credit risk, lockup risk, or withdrawal conditions must present those conditions clearly to the user and must not be confused with the guarantees of the constitutional core.

---

## Article XVII. Interlayer Coupling and Movement

### Section 1. Interlayer Movement Within a Compliant System

1. The minimum constitutional requirement for movement of Bitcoin or Bitcoin-denominated balances between constitutional layers is not zero theoretical risk. It is bounded, visible, non-discretionary risk with clearly published trust assumptions, failure modes, and downward exit conditions.
2. Every canonical interlayer movement path must publish its trust assumptions, withdrawal conditions, delay windows, proof model, and failure domain in a form users can inspect.
3. The canonical Layer 1 to Layer 2 path must aim for the strongest available security model and at minimum be trust-minimized.
4. The Layer 1 to Layer 2 coupling goal is:
   - strongest available security model
   - no identity-gated normal exit
   - public truth of claims and reserves
   - plain transactional Bitcoin remains native on Layer 2
   - no mandatory contract mediation for ordinary transfer
5. Layer 1 and Layer 2 should function as hard money and its cash extension.
6. The canonical Layer 2 to Layer 3 path need not match the strength of Layer 1 to Layer 2, but it must remain rule-based, non-discretionary, and free from committee control over normal movement.
7. Committee approval, governance discretion, operator favoritism, or identity-gated approval must not be part of the normal Layer 2 to Layer 3 or Layer 3 to Layer 2 movement path.
8. Trusted or contractual movement paths may exist only as explicit opt-in paths and must never be confused with the core safety properties of the constitutional system.
9. A higher layer may impair its own balances or applications, but it may not redefine actual Bitcoin ownership on a harder lower layer.
10. Core infrastructure dependencies between layers must not allow capture or failure of Layer 3 to functionally compromise the constitutional guarantees of Layer 2.
11. Any normal downward movement path must have a constitutionally fixed maximum delay. That maximum shall not exceed 12 Bitcoin blocks.
12. Systematic or discriminatory delay of ordinary downward movement shall be treated as a form of exit interference.
13. The protocol must not intentionally structure fees so that ordinary downward exit becomes practically unavailable.

### Section 2. Bridges Between Compliant Systems

1. A bridge between two compliant systems does not inherit constitutional compliance from either system. Compliance is demonstrated independently, not inherited through adjacency or connection.
2. A bridge must independently demonstrate compliance with the constitutional standards applicable to the movement it performs, including reserve truth, custody independence, non-discretionary operation, exit rights, and published trust assumptions.
3. A bridge that holds, custodies, locks, wraps, or intermediates Bitcoin or Bitcoin-denominated balances is subject to the same reserve, custody, and proof requirements as any other system handling those balances under this constitution.
4. No bridge may represent itself as constitutionally protected merely because the systems it connects are compliant.
5. Users must be clearly informed when they are moving balances through a bridge whose compliance status differs from the systems on either side.
6. A compliant system that routes users through a non-compliant bridge without disclosure is itself in potential breach of its clarity and honesty obligations under this constitution.
7. Bridge failure, capture, or insolvency does not by itself alter the protocol-compliance status of the systems it connects. However, systems that route users through such bridges remain responsible for:
   - accurate disclosure of bridge risk
   - avoiding misleading defaults
   - not presenting bridged paths as equivalent to canonical paths
   Failure to do so constitutes a breach of clarity and honesty obligations under this constitution.

---

## Article XVIII. Exit Priority Under Stress

1. The core protocol shall always preserve the priority of downward exit toward harder layers.
2. The protocol shall not require a discretionary or subjective failure declaration before users may exercise normal downward movement.
3. Detection of elevated risk, degraded trust, censorship, reserve weakness, or other failure conditions may be performed by users, auditors, external software, artificial intelligence, or other monitoring systems.
4. Users have the right to access published system-state data sufficient to evaluate reserve conditions, proof cadence compliance, operational concentration, and the availability of normal downward movement, subject only to limits necessary to preserve user privacy and cryptographic integrity.
5. The purpose of such detection is to inform users and assist coordination, not to create a new gatekeeper over exit.
6. When uncertainty exists, the protocol must favor accounting integrity, reserve truth, withdrawal capability, and low-fee accessibility over growth, emissions, or convenience features.
7. No entity that materially benefits from restricting withdrawals may gain discretionary authority to trigger such restrictions through emergency powers.
8. No appeal to legal, regulatory, audit, compliance, or emergency necessity shall convert a non-compliant restriction on exit, reserve integrity, credit distinction, or withdrawal rights into constitutional behavior.
9. Regulatory capture often arrives as a reasonable-sounding exception. Such exception shall not create constitutional precedent for future encumbrance, reserve impairment, or exit restriction.
10. Any emergency measure must be explicitly declared, time-bounded, and non-renewable. It must not be used to indefinitely suspend constitutional protections or convert temporary restrictions into permanent conditions. Specific duration limits and escalation rules may be defined in a companion standard.

---

## Article XIX. Governance, Mutability, and Ossification

1. The system recognizes that governance is a temporary weakness to be reduced over time, not a permanent virtue.
2. This principle applies whether or not a governance token exists.
3. Constitutional mutability, governance authority, and implementation authority are separate powers with separate hard stop windows.
4. Constitutional amendments may be made only during the founding period, which must end no later than 5 years from constitutional genesis.
5. After the constitutional amendment window closes, no further constitutional changes are permitted within the same compliant system. Any attempt to continue changing constitutional rules shall render the system non-compliant or establish a new system.
6. Governance authority to approve new protocol-level decisions may exist only until 25 years from constitutional genesis.
7. After year 25, no new governance decisions, votes, protocol-level approvals, or equivalent decision acts are permitted, whether by governance token, committee, operator council, multisig, foundation, delegated authority, or any other decision mechanism.
8. Any protocol-level change validly approved before year 25 must be fully implemented within 5 years of the governance hard stop.
9. After year 30, no further constitutional, governance, or protocol-level change is permitted. Any continued change beyond that point renders the system non-compliant.
10. No extension mechanism shall exist for the constitutional amendment window, governance window, or final implementation window.
11. Unresolved issues may remain unresolved. Failure is allowed. Endless mutability is not.
12. Bugs or imperfections not deemed critical enough to be addressed within the allowed windows must be left alone.
13. Only specifically defined and publicly disclosed changes approved before the governance hard stop may continue into the final implementation window. Blanket authority, open-ended mandates, or undefined upgrade powers do not survive the governance cutoff.
14. If unresolved problems require a new architecture, that architecture must launch as a new system and earn trust separately.
15. No upgrade, patch, proposal, or governance action may expand the scope of matters subject to governance beyond pre-declared authority. Governance may exercise only authority that was publicly published, durably recorded, sufficiently specific in subject matter, and fixed before the constitutional amendment window closed.
16. No open-ended or blanket upgrade authority may be created that allows future unspecified expansion of governance-controlled domains.

---

## Article XX. Governance Tokens

1. Governance tokens, if they exist at all within a compliant system, may exist only on Layer 3 or in clearly optional extension layers.
2. No governance token shall exist on Layer 2.
3. Governance tokens must not be represented as Bitcoin, Bitcoin-equivalent, or as conferring ownership over Bitcoin reserves unless that claim is explicit and true.
4. Governance tokens must not control constitutional protections, exit rights, reserve truth, liability truth, plain transferability, mandatory interlayer movement rules, constitutional time windows, or constitutional hard stops.
5. Governance token voting may govern only bounded operational, optional, or application-layer matters that do not impair the constitutional rights of users.
6. No governance token holder class may gain privileged withdrawal, reserve access, or constitutional override rights by virtue of token ownership alone.
7. Any governance token used within a compliant system must lose all protocol-level voting, decision, amendment, emergency, or override authority no later than 25 years from constitutional genesis.
8. After its sunset, a governance token shall confer no protocol-level decision rights, no amendment rights, no emergency rights, no reserve rights, and no authority over normal user movement or constitutional protections.
9. No governance token may be renewed, extended, renamed, mirrored, wrapped, or functionally replaced in order to continue token-based protocol governance beyond its constitutional sunset within the same compliant system.
10. If a token-governed successor system is created, it must be treated as a new system, not continuation of the old one.

---

## Article XXI. Constitutional Entrenchment

1. This constitution may not be amended by the same ease of process used for ordinary governance.
2. Amendments to foundational protections must require a threshold materially higher than any ordinary protocol change during the allowed constitutional window.
3. The following protections require the highest amendment threshold:
   - Bitcoin sovereignty
   - monetary integrity
   - distinction between Bitcoin claims and credit
   - reserve and liability provability
   - reserve custody independence and non-unilateral control
   - plain transferability
   - exit rights
   - transaction-level censorship resistance
   - privacy as part of exit freedom
   - non-discretionary interlayer movement
   - mutability hard stops
4. Any amendment to foundational protections must include:
   - a long public notice period
   - a long review period
   - an unimpeded exit window before activation
   - clear public explanation of what protection is being weakened, strengthened, or redefined
5. Any amendment that materially weakens the constitutional core shall be treated as creation of a new system, not continuation of the old one.
6. No constitutional amendment may be hidden inside technical upgrades, emergency patches, ambiguous governance language, or internal module reclassification.
7. A sequence of governance actions that cumulatively weakens foundational protections shall be treated as a constitutional weakening even if no individual action alone appears sufficient.
8. Such cumulative weakening must trigger the same notice, exit window, and entrenchment standards as a direct constitutional amendment.

---

## Article XXII. Constitutional Genesis and Activation Clocks

1. Constitutional genesis is the earliest publicly verifiable timestamp at which this constitution is published in full in a public durable repository designated under the identity of the system claiming compliance.
2. The constitutional clock begins at constitutional genesis.
3. The constitutional clock governs the constitutional amendment window, the governance decision window, and the final implementation hard stop.
4. Constitutional genesis shall not be reset by republication, reformatting, repository migration, mirrors, branding refresh, minor edits, later versioning, or other non-substantive continuity actions under the same system identity.
5. If the original repository disappears or moves, mirrors and migrated repositories preserve continuity of genesis rather than resetting it.
6. Every layer, sublayer, module, or user-facing component has a separate activation clock.
7. A component is activated when real users can rely on it, deposit value into it, transact through it, or otherwise use it outside a clearly segregated test environment, regardless of whether it is labeled beta, preview, pilot, guarded, or limited.
8. Token generation, branding launch, public announcement, or marketing event alone does not define activation if real production use begins at another time.
9. Later-launched parts may have their own activation dates for operational review, compliance analysis, and provisional mechanism timing, but they do not receive a fresh constitutional clock.

---

## Article XXIII. Right of Parallel Implementation and Escape

1. No compliant system may reserve to any company, council, operator set, foundation, or recognized body the exclusive right to implement, operate, route, settle, bridge, or provide access to the constitutional functions of the system.
2. Any person or group must be free to create alternative implementations, alternative routing systems, alternative operator networks, alternative custody-escape tools, or alternative supporting subsystems, provided they do not falsely claim compliance or misrepresent their risk.
3. The core system must not require identity revelation, political approval, or incumbent permission merely to build or operate such alternative paths.
4. Users must remain free to trust, reject, adopt, or ignore these alternative systems voluntarily.
5. This right does not grant automatic constitutional trust to alternative implementations. Trust must be earned through transparency of rules and operation, not through mandatory identity exposure or incumbent endorsement.
6. No constitutional function should require public personal identity disclosure merely to implement a compliant alternative path.
7. No compliant system may use legal, licensing, trademark, or contractual structure to prevent truthful independent implementation of constitutional functions, though false compliance claims and misleading naming remain prohibited.

---

## Article XXIV. Directional Decentralization and Operational Concentration

1. A compliant system may begin with operational concentration above its long-term ideal, but its architecture, incentives, and rights structure must favor decreasing central dependency over time rather than entrenching it.
2. Constitutional compliance requires not only correct protocol rules but sufficiently distributed real-world operation of critical system functions. Operational concentration can constitute a constitutional compliance issue even if every protocol rule is technically followed. Protocol compliance alone is insufficient if real-world operation creates a de facto gatekeeper.
3. If one actor, one coordinated group, one company, one infrastructure provider, or one jurisdiction can practically gate ordinary Layer 2 operation or downward exit, the system is operationally compromised even if its protocol rules remain unchanged.
4. Layer 2 and any critical support functions must be designed and operated to reduce concentrated chokepoints across operators, infrastructure, and jurisdictions. Layer 2 in particular must not depend on a single company, a single operator cartel, a single cloud provider, or a single legal jurisdiction for ordinary functioning.
5. Constitutional compliance evaluation may consider concentration of choke functions, including transaction ordering, settlement publication, reserve custody, proof generation or verification, routing or bridging, withdrawal processing, key infrastructure dependencies, and shared cloud or hosting, not merely raw node counts, validator counts, or jurisdiction counts.
6. Concentration sufficient to make exit or ordinary operation practically dependent on a single center of control is constitutionally unacceptable, regardless of whether formal protocol rules remain correct.
7. Measurable thresholds for when concentration becomes constitutionally unacceptable are defined by [Operational Independence Standard](companions/operational-independence-standard.md). That standard should use a sliding scale that grows or shrinks with real network participation.
8. This article targets structural and incentive conditions that create or entrench gatekeeping. Mere user preference for one provider in an otherwise genuinely open and non-coercive market is not by itself a constitutional breach.

---

## Article XXV. Long-Term Recoverability and Compatibility Continuity

1. A user who could validly access funds once must not lose discoverability of those funds because of silent software, firmware, wallet, or implementation drift.
2. No compliant implementation may silently change derivation paths, descriptor interpretation, address discovery logic, script interpretation, wallet mapping rules, or other recovery-critical behavior for existing balances.
3. Any change to recovery-critical behavior must be explicit, user-visible, documented, and opt-in.
4. Legacy discovery for previously supported balances must remain available, or a fixed archival recovery tool must be provided that preserves the prior rules.
5. Recovery-critical metadata must be exportable in open, durable, machine-readable form sufficient to rediscover funds without vendor dependence.
6. No user should need a specific vendor, server, or update path to rediscover funds that were already validly under their control.
7. If an update can make coins appear missing without the user voluntarily opting into a new recovery model, that behavior is non-compliant.
8. Detailed implementation patterns for recovery architecture, including capability trees, archival recovery environments, hash-pinned reference implementations, and frozen recovery profiles, are defined in [Software Security Architecture Standard](companions/software-security-architecture-standard.md).

---

## Article XXVI. Dependence Must Remain Escapable

1. A compliant system may allow delegated control, assisted custody, managed recovery, managed signing, operator assistance, or other convenience arrangements.
2. Such arrangements must not eliminate the user's constitutionally protected path to regain independent control or exit toward harder layers.
3. No compliant system may structure delegated control so that routine convenience authority becomes irreversible ownership authority without explicit and separately consented transfer.
4. Any custodial, assisted, delegated, or managed arrangement presented within a compliant system must clearly disclose:
   - who controls what
   - what the user can revoke
   - how the user can exit dependence
   - what delay or conditions apply
   - what happens if the operator disappears, is captured, or refuses service
5. A user must not be forced into permanent dependence merely because they once opted into temporary convenience.
6. Where immediate self-custody restoration is not technically possible, the system must provide a defined, bounded, non-discretionary path back to independent control.
7. Dependence on external data sources, including oracles, price feeds, attestation services, or external state proofs, must not trap user funds. If an external data source fails, becomes unavailable, or is compromised, users must still have a bounded, non-discretionary path to exit, unwind, or otherwise recover control of their funds or positions.

---

## Article XXVII. Breach, Restoration, and Continuity

1. A system that violates this constitution does not automatically regain uninterrupted compliant status by later changing behavior.
2. Any claim of restored compliance must publicly disclose the nature, scope, timing, and remediation of the breach.
3. Material violations affecting exit rights, reserve integrity, credit misrepresentation, constitutional time limits, governance sunsets, forced migration, or compliance misrepresentation may break constitutional continuity and require treatment as a new or successor system.
4. A system may be currently compliant yet historically breached. Such a system must not represent itself as continuously compliant across the breach period.
5. No implementation may conceal, relabel, minimize, or retroactively erase a period of material non-compliance.
6. Breach history matters. Current behavior and historical integrity are not the same thing.
7. Restoration of compliance does not authorize retroactive violation of the constitution's harder-layer truth, ownership continuity, or non-discretionary movement guarantees. Breach restoration may repair future behavior. It may not erase constitutional truth by retroactively rewriting valid system history, ownership, or settlement.
8. Forward remediation, such as fixing a bug, restoring reserve visibility, correcting labels, or repairing exit tooling, may be acceptable within allowed constitutional and governance windows. Impermissible retroactive correction, including rewriting valid settled history, forced rollback of valid final transfers, or retroactive ownership rewriting, is not acceptable under the current system identity and is classified under [Breach and Restoration Standard](companions/breach-and-restoration-standard.md).
9. A separate document titled [Breach and Restoration Standard](companions/breach-and-restoration-standard.md) defines breach severity, continuity effects, restoration conditions, uncertainty notice deadlines, concurrent-breach propagation, and the difference between forward remediation and impermissible retroactive correction.
10. A separate document titled [Constitutional Dispute and Review Standard](companions/constitutional-dispute-and-review-standard.md) defines procedures for raising disputes, presenting evidence, reviewing contested facts, classifying breach claims, and preserving public historical integrity.
11. A system that materially misrepresents asset class, trust model, custody state, exit conditions, or compliance context through its user interface may be classified as in breach under the Breach and Restoration Standard, regardless of underlying protocol correctness.

---

## Article XXVIII. Clarity to Users

Every user must be able to distinguish which of the following they hold:

1. Bitcoin on Layer 1.
2. Bitcoin transactional balance on Layer 2.
3. Bitcoin utility balance on Layer 3, meaning a Bitcoin-denominated balance used within Layer 3 under Layer 3 rules.
4. Native gas or utility token on Layer 3, if distinct from Bitcoin.
5. Credit instrument.
6. Other experimental or speculative assets.

Where Layer 3 uses a non-Bitcoin gas or utility token, the system must clearly distinguish that token from any Bitcoin-denominated balance at all times.

The system must not blur these categories for convenience, marketing, or growth.

Protocol-level naming, labeling, and code-facing definitions must not permit deceptive use of terms.

---

## Article XXIX. Scope, Extensions, Compliance, Naming, and Voluntary Applicability

1. This constitution governs the design, operation, and maintenance of any system claiming compliance with it.
2. This constitution is voluntary in applicability but strict in claim. No pre-existing system is automatically bound by it merely by resembling it. A system becomes subject to it when it publicly adopts or claims compliance with it.
3. No system may claim retroactive uninterrupted compliance for periods before that public claim unless it can independently demonstrate that its prior behavior conformed to the relevant constitutional requirements.
4. In the event of any ambiguity or conflict between descriptive or introductory text and Article XXIX, Article XXIX governs.
5. Where this constitution refers to a companion standard that does not yet exist, has not yet defined a relevant threshold, or is otherwise incomplete, the constitution remains fully operative. In such cases, interpretation and compliance evaluation shall default to the most conservative reading that best preserves exit rights, reserve and liability truth, custody independence, non-discretionary operation, censorship resistance, practical path to inclusion, constitutional time limits, and user freedom.
6. Applications, contracts, side systems, bridges, additional layers, derivative extensions, and internal modules built on top of or around a compliant system are not automatically constitutional merely because they interact with it.
7. Such systems may be evaluated as compliant, partially compliant, non-compliant, or out of scope.
8. Compliance evaluation may be performed by users, developers, auditors, institutions, automated systems, artificial intelligence, or any combination thereof.
9. No evaluator is infallible, and no compliance label substitutes for understanding the actual rules and risks of a system.
10. Constitutional compliance is determined by actual rules, behaviors, reserve conditions, coupling properties, activation properties, and withdrawal conditions as measured against this constitution and its binding companion standards, not by the claims, branding, certifications, or judgments of any evaluator or authority.
11. A system may be useful while remaining non-compliant with this constitution. Non-compliance does not automatically mean illegitimate. It means only that the system does not meet the standards of this constitution.
12. No external layer, contract, extension, or module may claim constitutional compliance unless its behavior, withdrawal conditions, reserve truth, and risk structure can be examined against these principles.
13. No system that is non-compliant with this constitution may represent itself to users as compliant with it, protected by it, or authorized by it.
14. A system that uses constitutional naming or implies constitutional protection while operating in material violation of these articles is engaged in misrepresentation regardless of its technical relationship to compliant infrastructure.
15. Compliance is not inherited through technical interaction. It must be demonstrated independently against the full text of this constitution.
16. The purpose of this constitution is not to prohibit experimentation. Its purpose is to preserve the integrity of maximum-freedom Bitcoin system design while creating a standard against which future systems may be judged.

---

## Article XXX. Successor Systems and Voluntary Migration

1. A successor system is not constitutionally continuous merely because it shares brand, developers, code, infrastructure, social backing, or historical lineage with an earlier system.
2. No user may be automatically migrated into a new trust model, new layer, new token, or successor system.
3. No balance may be silently rolled over, remapped, mirrored, or treated as consent to a successor system.
4. Any new system must be entered voluntarily by users.
5. A successor system must independently demonstrate compliance if it wishes to claim compliance.
6. A failed or non-compliant implementation may be replaced only by a new system that users choose to trust and enter.

---

## Article XXXI. Strategic End State

The intended long-term order of compliant systems is:

1. Bitcoin Layer 1 remains the fortress and final monetary truth.
2. Layer 2 becomes the everyday transactional Bitcoin rail for the world.
3. Layer 3 becomes the place for high-speed innovation, apps, and experimentation.
4. Value may move upward for utility, but it must always be able to move downward for safety.
5. The system succeeds only if ordinary people can save in harder money, transact in finer units, and leave weaker layers without begging permission.

---

## Companion Documents

The following companion documents support, interpret, or operationalize this constitution:

- [Definitions and Interpretive Notes](companions/definitions-and-interpretive-notes.md)
- [Breach and Restoration Standard](companions/breach-and-restoration-standard.md)
- [UX Constitution](companions/ux-constitution.md)
- [Constitutional Dispute and Review Standard](companions/constitutional-dispute-and-review-standard.md)
- [Operational Independence Standard](companions/operational-independence-standard.md)
- [Software Security Architecture Standard](companions/software-security-architecture-standard.md)
- [Reserve Custody and Key Management Standard](companions/reserve-custody-and-key-management-standard.md)


Where a companion document is designated binding, its binding force is limited to the scope assigned to it by this constitution.

---

## Constitutional Summary

**Interpretive and advisory only.** 
This summary does not create binding obligations beyond the articles above.

This constitution stands on thirteen core truths.

1. Layer 1 preserves scarcity.
2. Layer 2 preserves spendability.
3. Layer 3 preserves experimentation.
4. Credit must never masquerade as money.
5. Proof must replace trust wherever claims exist, and proof must stay current.
6. Reserves must be held, not just shown. Custody must resist seizure, not just prove existence.
7. Plain transfer must remain native at the core.
8. Exit preserves freedom, at both the structural and transaction level.
9. Governance must die on schedule and must not expand its own reach.
10. A new system requires new consent.
11. Dependence must remain escapable.
12. No incumbent may become the exclusive doorway.
13. Centralization must decrease over time, not harden.

---

## Attack Vectors Closed

**Interpretive and advisory only.** 
This list does not create binding obligations beyond the articles above.

This version closes the main attack vectors identified so far, including:

- compliance as Trojan horse
- hidden reserve lending and yield capture
- emergency powers as exit gate
- functional KYC or legal chokepoints as soft exit blocks
- amendment by ambiguity and constitutional drift
- evaluator capture
- shared infrastructure contamination
- naming and branding misrepresentation
- endless governance by extension
- silent migration into successor systems
- non-resettable constitutional timing
- hidden activation timing games
- silent recoverability drift
- dependence that becomes prison
- breach history erasure
- undefined terms enabling adversarial reinterpretation
- monopoly over constitutional infrastructure
- centralization hardening over time
- soft censorship through transaction-level suppression while formally allowing exit
- governance self-expansion before sunset
- stale or ancient proofs presented as current verification
- retroactive fake compliance claims by pre-existing systems
- operational concentration creating de facto gatekeepers despite protocol compliance
- impermissible retroactive history rewriting disguised as breach remediation
- visible reserves under weak custody, technically proven but one seizure, one key, or one coerced signer away from loss
- bridges inheriting compliance by adjacency while masking weaker trust assumptions
