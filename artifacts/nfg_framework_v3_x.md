! DISREGARD! This artifact is a directive that I updated [[nfg_framework_v3_c]] to but then Claude compared the 2 and rejected the update due to being negligible. I disagree but I'm not confident that this makes a difference in the end product. See more in [[avoided#Discussion]] 
# Non-firing guns — analytical framework
## Version 3

*Based on analysis of 41 real-life and 5 fiction cases. Supersedes version 2.*

---

## Overview of changes from version 2

The principal structural changes in version 3 are:

1. **Category C renamed** from "Individual agency" to **"Agent-level mechanisms"** to better reflect the inclusion of non-individual agents (groups, institutions, machines) and of features that concern the environment around agents rather than the agents themselves.

2. **C2 (occupant disposition: temperament and state of mind) and C3 (occupant disposition: experience and ideology) dropped.** Their territory is redistributed across five new features (C2–C6) that make finer and more analytically useful distinctions.

3. **D2 (exogenous uncertainty injection) and D3 (endogenous confidence erosion) dropped.** Their territory is likewise redistributed across the same five new features.

4. **Five new agent-level features introduced** (C2–C6): Noise, Doubt, Misguided Resistance, Heroic Judiciousness, and Flinching. Each is defined as the intersection of two or more of the dropped features, but with additional precision about *where* the disruption occurs relative to the decisive agent.

5. **E2 (stable sub-ensemble) refined** to explicitly exclude the single-agent case: if a single agent's non-criticality is significant, it must be captured by one of the five agent-level features rather than by E2.

6. **D5 (de-escalation ladders) and D7 (polarization disruption) reworded** to remove domain-specificity. Both features now express abstract structural transitions rather than Cold War or diplomatic examples.

---

## Summary table

| ID | Feature | Category | Status |
|----|---------|----------|--------|
| A1 | Built-in preparation failure | A. Indicators | Carried over |
| A2 | Built-in assumption failure | A. Indicators | Carried over |
| A3 | Divergent group reasoning | A. Indicators | Carried over |
| B1 | Asymmetric information propagation | B. Observation & information | Carried over |
| B2 | Asymmetric observation level | B. Observation & information | Carried over |
| C1 | Structural veto point | C. Agent-level mechanisms | Carried over |
| C2 | Noise | C. Agent-level mechanisms | **New** |
| C3 | Doubt | C. Agent-level mechanisms | **New** |
| C4 | Misguided resistance | C. Agent-level mechanisms | **New** |
| C5 | Heroic judiciousness | C. Agent-level mechanisms | **New** |
| C6 | Flinching | C. Agent-level mechanisms | **New** |
| D1 | Trigger specificity and understated escalation threshold | D. Technical & structural | Carried over |
| D4 | Mandatory multi-channel confirmation | D. Technical & structural | Carried over |
| D5 | De-escalation ladders | D. Technical & structural | Rewording |
| D6 | Temporal deceleration | D. Technical & structural | Carried over |
| D7 | Polarization disruption | D. Technical & structural | Rewording |
| E1 | Initial macro-state disposed against conflict | E. Population dynamics | Carried over |
| E2 | Stable sub-ensemble (small critical mass, ≥ 2 agents) | E. Population dynamics | Refined |
| E3 | Asymmetric information propagation (population level) | E. Population dynamics | Carried over |
| E4 | Systematic confidence challenges | E. Population dynamics | Carried over |

*Note: D2 and D3 are retired. C2 and C3 (old) are retired. New C2–C6 take their combined number range.*

---

## A. Indicators of applicability

*Circumstances along the arc that help identify the narrative as it plays out — ideally earlier than naively expected.*

---

### A1 — Built-in preparation failure

The predicted sequence depends on actions that were poorly designed, resourced, or executed from the start. The failure is latent in the preparation itself, not merely in circumstances.

**Sub-items:**
- Actors commit resources or reputation before validating assumptions
- Operational plans rest on untested or incompatible components
- Visible at the pivot point as a gap between declared capability and actual capability

> **Flag A:** May correlate with B2 (asymmetric observation level) — agents with limited observation access are more likely to commit to poorly-grounded preparations. Review after re-scoring.

---

### A2 — Built-in assumption failure

The predicted sequence depends on a background premise about how the world works that is false, even if the preparation itself is technically adequate. The execution is correct; the model is wrong.

**Sub-items:**
- A paradigm, protocol, or strategic doctrine assumes a state of affairs that does not hold
- The error is only detectable in retrospect or by an outsider who does not share the paradigm
- Examples: aether wind (Michelson–Morley), Soviet first-strike logic (Able Archer), Bretton Woods dollar support (Suez)

> **Flag A:** May correlate with B2. Review after re-scoring.

---

### A3 — Divergent group reasoning

Different groups forward-chain from their respective observations toward incompatible projected outcomes. The less-informed group tends toward panic, escalation, or premature closure; the better-informed group remains more measured. The divergence is primarily cognitive: two groups hold incompatible models, not merely different facts.

**Sub-items:**
- Causally downstream of asymmetric observation level (B2), but separable: groups can diverge in reasoning while holding identical facts if interpretive frameworks differ
- Less-informed groups are the ones exhibiting more tendency to escalate
- Epistemic divergence can be intentional (deception) or structural (access barriers)
- Example of purely interpretive divergence with same facts: BICEP2, where astrophysicists and cosmologists drew incompatible inferences from the same signal

---

## B. Observation and information structure

*Structural features of how agents access, accumulate, and transmit information.*

---

### B1 — Asymmetric information propagation

The rate at which information can be transmitted and received differs systematically across agents or groups. This is a flow-rate property: it concerns the speed and bandwidth of information movement, independent of how much information any agent currently holds.

**Sub-items:**
- Pertains to the dynamics of information exchange: who can send to whom, how fast, with what fidelity
- Can defend or dismantle a scheme depending on which actor benefits from faster propagation
- Distinct from B2 (which concerns total quantity/quality of information held, not its movement rate)
- Example: ARD broadcast of Schabowski's announcement propagated to citizens faster than correction could reach border guards

---

### B2 — Asymmetric observation level

The total quantity and quality of information available to an agent — what they can observe, measure, or access — differs systematically across groups. This is a stock property: how much situationally relevant information an agent can in principle acquire, regardless of how fast it travels.

**Sub-items:**
- Constraints may be physical (geography, instruments), institutional (classification, clearance), or cognitive (paradigm blindness)
- Agents with lower observation levels are structurally more likely to rely on projection and worst-case reasoning
- Feeds into divergent group reasoning (A3) as a causal antecedent
- Feeds into preparation and assumption failure (A1, A2) when low-observation agents commit to plans
- Distinct from B1: observation level is a stock (how much you can know); propagation rate is a flow (how fast it moves)

> **Flag A:** May correlate with A1, A2.

---

## C. Agent-level mechanisms

*Features concerning how specific agents — individual, collective, institutional, or mechanical — behave at decisive moments. Covers both the structural positions agents occupy and the various ways in which uncertainty, information, disposition, or circumstance shape their actions. The category encompasses disruptions that operate below the level of the decisive agent as well as disruptions within that agent.*

---

### C1 — Structural veto point

A position in the decision chain whose refusal or inaction is sufficient to prevent cascade — whether placed there by design, accident of command hierarchy, or bureaucratic contingency. The veto is architectural: it exists independently of who occupies it.

**Sub-items:**
- The position may be formally recognised (e.g. second authorisation officer) or accidental (e.g. Arkhipov aboard B-59 as flotilla chief of staff, which happened to require three signatures rather than two)
- Structural veto points can be designed in (multi-channel confirmation, D4) or arise by circumstance
- High-impact cases often combine an accidental veto point with a resistant occupant (see C3–C6)
- When the veto point exists but is occupied by an escalation-prone agent, the non-firing story does not occur — the veto point is necessary but not sufficient

---

### C2 — Noise

Uncertainty, confusion, or disruption exists in the broader system or information environment but does not directly influence the decisive agent's actions. The key veto-point mechanism is insulated from the noise, operates before it arrives, is placed into its decisive position as an indirect result of it, or is simply unaffected by it even when it is present.

**Sub-items:**
- The decisive agent acts *before* noise enters the system: their disposition or position is fixed prior to the disturbance, which then perturbs other actors around them.
- An agent is *placed into* the decisive position as a consequence of noise or systemic accident, but their subsequent actions are not themselves a response to the noise (e.g. Arkhipov's presence on B-59 was an accidental result of flotilla command assignments — the "noise" of command structure — but his veto was his own deliberate act)
- Noise reaches the agent but does not change their behaviour — the agent's response is determined by prior training, commitment, or structural role rather than by the noisy input
- Contrast with C3 (Doubt) and C4 (Misguided Resistance), where noise *does* affect agent behaviour

---

### C3 — Doubt

Unexpected or unclearly originated inaction, paralysis, or malfunction arises in the decisive agent or veto-power mechanism. Something prevents the expected action from being taken, and the source of this inhibition is ambiguous, emergent, or not fully traceable to a deliberate prior decision.

**Sub-items:**
- The agent may be a person, group, institution, or automated system
- The inhibition may arise from psychological reticence under pressure, physical failure, structural ambiguity about authority, or emergent hesitation that was not anticipated
- The decisive quality is *unexpectedness* — Doubt is not the planned deployment of a veto but its unplanned emergence
- Example: Petrov's refusal to escalate the 1983 satellite alert — he violated protocol rather than following it, and the inhibition arose from a combination of engineering skepticism and situational reticence that no protocol had anticipated
- Distinct from C5 (Heroic Judiciousness), where the agent does follow a protocol or pre-designed procedure

---

### C4 — Misguided resistance

The decisive agent or veto-power mechanism lacks precise information, or is overwhelmed with information, either way leading it to resist taking action. This resistance may be directed against the initially predicted (escalatory) narrative — helping defuse it — or, in a more ambiguous variant, against the resolving (de-escalatory) narrative, or obstructing both sides.

**Sub-items:**
- The agent resists action because it cannot adequately process the signals available to it, not because it has made a deliberate choice
- Information poverty and information overload are both sub-cases: the agent either lacks what it needs to act or has too much to act coherently
- The resistance may work in the narrative's favour (resisting escalation) or produce unpredictable lateral effects
- Example: Soviet commanders during Able Archer 83 who received ambiguous NATO signals and chose not to act — resistance arising from genuine uncertainty about whether the exercise was real
- Example: LTCM counterparty banks that resisted liquidation because they lacked full visibility into the fund's positions, inadvertently stabilising the situation long enough for the Fed to organise the rescue
- Distinct from C3 (Doubt), where the inhibition is emergent and ambiguous in origin, rather than traceable to information poverty or overload

---

### C5 — Heroic judiciousness

A complicated or unusual situation arises, but a prescribed protocol, pre-designed response, or previously instituted mechanism exists, and an agent — human, group, institution, or machine — enacts it in the way it was previously intended. The agent does not improvise; it executes a pre-existing plan correctly under conditions that were anticipated in its design.

**Sub-items:**
- The agent may be a person following a safety procedure, an automated circuit breaker, a treaty mechanism, or an institutional rule
- The "heroism" lies not in invention but in correct execution under pressure or in circumstances that test the procedure's robustness
- The pre-designed response need not have been designed specifically for this crisis — it may be a general protocol that happens to apply
- Example: Flash Crash's CME Stop Logic Functionality — an automated five-second pause, pre-designed for exactly this scenario, activating at the critical moment
- Example: Ken Mattingly's reentry power-up sequence — tested in advance under strict constraints, executed correctly with frozen systems
- Example: The Berlin Airlift's three air-corridor guarantees — a pre-existing legal right whose existence Truman could invoke, transforming an apparently blocked path into a viable route
- Distinct from C3 (Doubt), where the inhibition is unplanned; distinct from C4 (Misguided Resistance), where the agent is information-impaired; distinct from C6 (Flinching), where the agent fails to perform as expected

---

### C6 — Flinching

An agent — who would be expected, under normal circumstances, to take a particular action — becomes saturated or overwhelmed by external noise (insufficient, conflicting, or excessive information flooding intake capacity) or, possibly predictably given their character, becomes susceptible to inaction or incorrect action under the pressure of the situation. This may either make the initial narrative (escalation, catastrophe) appear more likely, or contribute to deflecting events toward the actual resolution.

**Sub-items:**
- Saturation sub-case: the agent is overwhelmed by the sheer volume, speed, or contradictory nature of incoming signals, causing degraded performance relative to their own prior or anticipated standard
- Susceptibility sub-case: the agent's character, training history, or psychological profile renders them predictably likely to freeze or act incorrectly under this specific type of pressure — the flinch is in some sense foreseeable
- Flinching can cut either way: a key escalatory actor flinching prevents catastrophe; a key de-escalatory actor flinching allows it
- Example: Von Koren's flinch at the duel (Chekhov) — the decisive shooter flinches at the moment of firing, deflecting the bullet; a predictable susceptibility under the specific pressure of the duel's moral weight
- Example: Schabowski's unprepared improvisations at the press conference — saturation by an unexpected situation producing incorrect outputs
- Distinct from C3 (Doubt), which concerns emergent, ambiguous inhibition; Flinching implies some degree of predictability or recognisable pattern to the failure
- Distinct from C5 (Heroic Judiciousness), which is correct execution; Flinching is degraded or incorrect execution

---

## D. Technical and structural aspects

*Features of policy, infrastructure, machine design, or procedural architecture that contribute to non-firing.*

---

### D1 — Trigger specificity and understated escalation threshold

The signature required to identify a genuine threat — or to cross the threshold at which a perceived adversary would commit to action — is defined so precisely or set so high that most real signals fall below it. Whether by explicit design or tacit convention, weak signals are dismissed rather than acted upon.

**Sub-items:**
- A required trigger event must present a specific, complex pattern before it is treated as actionable — accidental matches are structurally rare
- Adversaries (real or imagined) signal ambiguously or with deliberately understated intensity, making first-move attribution uncertain
- Neither party can easily confirm whether the other has crossed the threshold, creating a zone of mutual ambiguity
- Example: Soviet doctrine required hundreds of simultaneous ICBM launches to constitute a credible first strike — a single missile alert fell below the threshold
- Note: the "understating escalation" dimension is identifiable only by inference from threshold design and post-hoc disclosure, since these stories are defined by a lack of escalation

---

### D4 — Mandatory multi-channel confirmation

Action requires agreement across multiple independent detection or authorisation systems, so that any single false alarm, erroneous reading, or individual decision is insufficient to trigger cascade.

**Sub-items:**
- Multiple physical sensors must confirm a signal before it is reported up the chain
- Multiple human authorisations are required before an irreversible action can be taken
- Cross-checking between independent systems creates friction that absorbs false positives
- Example: Soviet nuclear launch required corroboration between satellite early warning and ground-based radar — Petrov's instinct not to escalate was structurally supported by the absence of ground radar confirmation
- Example: Cuban Missile Crisis — U.S. ExComm deliberative process required consensus among multiple senior advisors before action

---

### D5 — De-escalation ladders

A structural shift in a situation from a binary, opposed, or deadlocked configuration toward one in which multiple resolution pathways become available, or in which one party's action opens a space the other can enter without loss of face. The feature is not specific to military or diplomatic standoffs; it describes any mechanism — procedural, institutional, legal, informational, or economic — by which a two-sided impasse is dissolved by the introduction of asymmetric options, lateral moves, or sequenced reciprocal steps.

What makes a situation a candidate for this feature is the prior absence of such options: the gun was loaded partly because both parties perceived only two outcomes (fire or capitulate). The ladder's appearance reframes this as a false binary.

**Sub-items:**
- Any protocol, channel, or convention that allows parties in a standstill to signal willingness to disengage without surrendering their position
- Opportunity for reciprocal action — one side's small step is matched, breaking symmetry without requiring either side to act first unconditionally
- Alternative resolution steps revealed in a timely and clear fashion, offering a path that neither side had initially projected
- In contexts without literal adversaries: any structured mechanism by which a deadlock is resolved without one party's unconditional defeat — including market mechanisms that dissolve regulatory impasses, scientific norm violations that break a paradigm stalemate, or institutional innovations that offer a new category of action
- The feature can manifest as a *deus ex machina* in fictional terms — a previously invisible possibility that suddenly restructures the available moves — but in real cases it is always traceable to a prior structural condition or agent action that created the option

---

### D6 — Temporal deceleration

Structural or procedural constraints slow the interval between detection and response, creating windows in which error can be identified, information can propagate, or agents can reconsider. The deceleration is not a deliberate choice by any single actor but a property of the system's architecture or physical environment.

**Sub-items:**
- Logistical constraints on escalation pace (supply lines, mobilisation timelines, weather, geography)
- Procedural requirements that impose waiting periods before action is authorised
- Physical constraints that create natural pauses (distance, communication lag, instrument cycle time)
- The window created by deceleration is what allows other non-firing mechanisms to operate: without it, multi-channel confirmation, heroic judiciousness, and structural veto points have no time to act
- Contrast with its absence: Petrov (9-minute window), Arkhipov (hours underwater with no surface contact) — temporal deceleration was near-zero, making agent-level mechanisms the only operative pathway

---

### D7 — Polarization disruption

A shift from a closed, binary, or mutually reinforcing opposition toward a more open configuration in which the original polarity loses its structuring force. The feature is not specific to political or military confrontation; it describes any event or mechanism that introduces a new element — a third agent, an unexpected development, a redefined interest, or an asymmetric revelation — that dissolves the self-reinforcing logic of a two-sided impasse.

The key structural property is that the original polarity was itself part of what kept the gun loaded: each side's stance was partly constituted by its opposition to the other. When that polarity is disrupted, both parties' options change simultaneously without either having to act first.

**Sub-items:**
- By an external third agent whose interests do not align with either party's preferred outcome, who thereby changes the strategic calculus for both without being captured by either
- By an internal defection, public revelation, or unexpected development that reframes what each party is actually contesting
- By an asymmetric information event that causes one party to discover that the stakes are different from what they believed, making continued opposition irrational
- By a reframing of the situation's identity — what the parties discover they are *really* fighting about — that makes the original polarity irrelevant
- The feature can appear in contexts without literal adversaries: a scientific community whose two factions are disrupted by an outsider's experiment; an economic standoff dissolved by a market signal that redefines what "winning" means

---

## E. Abstract population dynamics

*More fundamental features drawn from physics, statistics, and network science — qualitative ideas that could be turned into falsifiable hypotheses.*

---

### E1 — Initial macro-state disposed against conflict

The aggregate state of the ensemble represents a disposition against the escalatory outcome, even if individual sub-ensembles are at or near criticality. The macro-state reflects the weighted sum of all sub-ensemble states.

**Sub-items:**
- Individuals take simple actions with a finite number of degrees of freedom and interact weakly in most regions
- The idea of a macro-state describes (near-)total cooperation within one or more sub-ensembles, e.g. a group making preparations for conflict
- A sub-ensemble can be at criticality, where correlation functions are divergent and susceptibility is singular — small perturbations can produce large-scale changes
- Unexpected events add noise to a system at criticality; the macro-state is not observable on a local, low-scale level except at criticality

> **Flag C:** Near-universal across the corpus (22/25 real-life stories score ≥ 2). Review for reclassification as a necessary condition rather than a discriminating variable, once a control group of "fired guns" is available.

---

### E2 — Stable sub-ensemble (small critical mass, ≥ 2 agents)

One or more sub-ensembles within the broader system remain in a stable, non-critical state and thereby resist the cascade. The feature is most diagnostically valuable when the stable sub-ensemble is very small — a group of two to a handful of agents constitutes the entire resistance. **Single-agent cases are explicitly excluded**: if a single individual's stability is the decisive mechanism, that belongs in one of the C-category features.

**Sub-items:**
- Local regions where criticality is not achieved — combat preparedness, institutional compliance, or group panic do not reach the level sufficient to trigger cascade
- A series of checks and balances decelerates propagation of any decision into action
- The smaller the stable sub-ensemble relative to the critical one, the more contingent the non-firing outcome appears in retrospect
- The most structurally striking instances: a tiny group (Suárez's inner circle, the Fed's overnight team) constitutes the entire stable sub-ensemble
- Unexpected events cannot seed a phase transition if they occur within such a stable region
- The lower bound is two agents: two people who refuse to escalate together, two institutions whose combined resistance is sufficient

> **Flag C:** Near-universal across the corpus (23/25 real-life stories score ≥ 2). Refined definition (minimum two agents) should increase discriminating power by separating individual-agent cases to category C. Review for reclassification after control-case analysis.

---

### E3 — Asymmetric information propagation (population level)

At the population or network level, information propagates asymmetrically: escalation-seeking agents receive or transmit information at different rates than skeptics or holdouts. This asymmetry can work in either direction — sometimes faster propagation to skeptics allows them to act before escalators complete their preparations; sometimes slower propagation to escalators prevents coordination.

**Sub-items:**
- Between perpetrators of repression and a weak majority
- Between escalation-seeking agents and skeptics
- Cross-reference with B1 (individual/group level) — same underlying phenomenon at different scales

> **Flag C:** Near-universal (22/25 real-life stories score ≥ 2). Review for reclassification as a necessary condition.

---

### E4 — Systematic confidence challenges

Increased randomness in agents' policies — whether from noise in the environment, information overload, or structural sources — significantly muddles the execution of a scheme and contributes to the narrative arc of non-firing. At the population level this feature aggregates individual-level effects across the ensemble.

**Sub-items:**
- A scheme requires coordinated, confident execution across multiple agents; randomness in any agent's policy breaks that coordination
- Most useful at the population level when the challenge is systemic — affecting a class of agents rather than a single individual
- Example: N-rays — subjective measurement methodology systematically introduced randomness into all observers' readings, not just one
- Example: Y2K — uncertainty about actual risk levels produced highly variable remediation responses across organisations

> **Flag C:** Near-universal (20/25 real-life stories score ≥ 2). Review for reclassification as a necessary condition.

---

## Consolidated flags

| Flag | Features | Description | Trigger for revision |
|------|----------|-------------|----------------------|
| A | A1, A2 ↔ B2 | Preparation and assumption failure may correlate highly with asymmetric observation level | If re-scoring shows r > 0.7 between A1/A2 and B2 across all stories, consider merging or treating B2 as causal antecedent |
| B | C3 ↔ C6 | Doubt and Flinching share a family resemblance — both involve degraded or unplanned agent behaviour. The distinction (emergent/ambiguous vs. predictable/saturation-driven) may prove too fine for consistent scoring | If inter-rater reliability on C3 vs. C6 is low, consider merging with a richer sub-item structure |
| B | C4 ↔ B2 | Misguided Resistance is partly a consequence of asymmetric observation level at the individual agent level. The two features may be redundant for the decisive agent specifically | If C4 and B2 co-score identically across most stories, consider collapsing C4 into B2 with an agent-specific sub-item |
| C | E1, E3, E4 | Three population-dynamics features score ≥ 2 in 80–92% of real-life stories | After extending corpus to 50+ stories or introducing "gun that fired" control cases, test whether these features retain discriminating power or should become definitional prerequisites |

---

## Scoring guidance

- **Scale:** 0 = absent or inapplicable; 1 = weakly present or inferrable; 2 = clearly present; 3 = conspicuous and central to the story's non-firing mechanism
- **On the five agent-level features (C2–C6):** These are not mutually exclusive per story. Multiple features can score highly in the same story if the same situation involves both Noise (disruption below the decisive agent) and Doubt (emergent inhibition in the decisive agent), for example. Score each independently.
- **On C1 vs. C2–C6:** C1 asks whether the structural position exists; C2–C6 ask about the agent occupying or affected by that position. All can score simultaneously.
- **On E2:** Do not score E2 for cases where the sole mechanism is a single individual. Route those to C3, C4, C5, or C6 as appropriate. E2 requires at least two agents acting in concert.
- **On D5 and D7:** These features now apply across all domains. Do not score 0 simply because the story is not military or political — ask instead whether any mechanism introduced a lateral move, a new category of action, or dissolved a binary opposition.
- **On flagged near-universal features (E1, E3, E4):** Score normally for now. Do not reclassify until control cases are available.
