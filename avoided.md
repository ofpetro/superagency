### Goal
A type of story was identified as a likely candidate for a narrative that humans have picked up on, and which connects an initial sense of danger and a final sense of complete deescalation. The hypothesis to be tested is that there exists a common narrative thread that humans could internalize and follow in cases where deescalation of (partially) obscured -- and potentially grave -- danger is necessary, including taking preventive action and making correct decisions in acute situations. With LLM use (mostly) historical examples were found for the story type. As part of testing, subjectively extracted features of the exemplars were sought across all of the relevant corpus.

Work on this is ongoing and see below how you can contribute!
### Prompting
Claude Sonnet 4.6, responses marked as
> quotes.

A shortened, edited version of the transcript is presented.[^1] For an overview and qualitative evaluation, see [[#Discussion]]
#### Seed
We wish to focus on the early stages, as the unexpected events start to unfold, e. g. the circumstances of the first steps to conflict deescalation. We expect that these are hard to disentangle causally, can involve haphazard or serendipitous incidents, in as much as the initially predicted scenarios are likely. Therefore let's explore a wider selection of reports that give more insight into this. Formal requirements: 
1. Start by collecting a substantial list of (at least 10) stories in the narrative type. 
2. These may be real-life accounts but fictional ones are acceptable, too, as long as not all are fictional.
3. In each story, identify key events. Start at the final moment, which is clearly identifiable. Work backwards in building possible causal connections between episodes. 
4. For simplicity, the list of episodes of each story should be referred to by keywords, the summary given in bullet points. 
5. As the list of episodes is built, and we progress earlier in time, we arrive at a situation where the actual trajectory of episodes is deemed unlikely. That can be considered the starting point. We stop there. As this is an exploratory research, the conclusion is too early to be drawn, let's omit that.
> Q: For fictional examples, what medium do you prefer? 

A: Novels / short fiction

> Q: For the causal chain per story, how long should it be?

A: Natural depth per story

[[batch-1-3.pdf]]

[[prompt-3]] gathers characteristic features into 4 distinct categories (under 4 headings), some of which are more readily identified with plot points, some of which may be convoluted or unclear. In each category, the features are given in keywords in a main list and corresponding details are given in sub-lists. Let's go through all features and score them against each story example on a scale where 0 corresponds to unclear or unobserved feature and 3 to a conspicuous one. As a conclusion, the scores can be aggregated across stories.

[...]
#### Seeking new examples interleaved with scoring updates
Let's look at 10-20 more stories that fit the category of "non-firing guns" [...]. If a significant amount of the found examples is fictional, that can still be used, but they should be evaluated in a separate matrix. 

> Q: For the new batch, should we prioritise any particular domain, or cast the net wide again (Cold War, science, legal investigations, peace processes, expeditions, fiction)?

A: Cast wide — best examples wherever they fall

> Q: The previous matrix used 15 stories. Should the new batch aim for the full 20, or is 10–12 sufficient if the examples are strong?

A: 10–12 strong examples is fine

> Q: For fictional examples — should they be kept entirely separate, or mixed into the main batch and then split only at the matrix stage?

A: Find them mixed, split only at matrix stage

[[batch-2-3.pdf]]

[...]

Interesting insights. Now I would like you to reflect: given the total of 25 non-fictional cases and the analysis framework, how adequate is the feature identification? I suggest multiple possible approaches:

1. Investigate each feature description -- are they clear, detailed enough to discern them? Are they clearly distinct? Or are some too close? Do some contain tension such that they could be split into more?
2. Is the list complete? Are some features missing? Are some not particularly fit for such analysis?
3. Investigate scoring matrices -- Within a row, considering stories corresponding to different entries, especially differences of 2 or 3, are those indeed so different stories to justify the different scores? Within a row, if the entries are consistently 2 or 3, is the corresponding feature indeed omnipresent?
4. Research other analyses of the concept. Is this an existent approach in literary aesthetics? These suggestions are not equally valuable. Some may not lead to a substantial answer. A different, 5. approach may be needed. Complete the reflection in 2 passes: write up a shorter form draft to each approach first, then evaluate them for content originality, then on a second pass pursue the 2 best ones. Due to the complexity of the suggested approaches, the first pass requires at least as much thinking as the second.

[...]

Now let's find 8 additional real-life stories. It may turn out that these are rare and they become increasingly ill-fitting to the non-firing gun narrative type. As the stories are accumulated, check after the 4th, 6th and 7th for precision in characterization as such a narrative. If the precision seems to significantly decrease, the search does not need to be completed.

[[batch-4.pdf]]

Let's keep a list of the historical examples. Write a list entry with the title of the stories in each batch, for every batch, in a markdown file.

[...]

Now let's find 8 additional real-life stories. It may turn out that these are rare and they become increasingly ill-fitting to the non-firing gun narrative type. As the stories are accumulated, check after the 4th, 6th and 7th for precision in characterization as such a narrative. If the precision seems to significantly decrease, the search does not need to be completed. Append their titles to [[nfg_stories]]

[[batch-5.pdf]]
#### Compiling results
[[nfg_stories]] -- examples
[[nfg_framework_v3_c]] -- the scoring framework document

[...] which will hopefully disambiguate some cases and help us better discern which feature the stories represent more prominently. Within categories A, B, C and D, if multiple features score similarly, some extra thought should be given to whether one stands out or is significantly weaker, and that one should get +1 or -1 point (unless that results in a score >3 or <0). Let's assess the historical example stories according to these guidelines and the attached document. If applying a certain directive is uncertain, interrupt the task to ask a clarifying question.

> Q: On the tiebreaker: when multiple features score similarly, should the adjustment go one way only (the standout or the weakest), or both ways?

A: Both: +1 to the standout and -1 to the weakest if both are discernible

> Q: On scope: does the tiebreaker apply within each category independently, and is category E confirmed as excluded?

A: Within each category independently — and yes, E is excluded

[scoring matrix](nfg_v3_scoring_matrix_all44.html)

> **Tiebreaker logic applied.** Within each category, wherever two or more features scored identically, the clearest standout received +1 and the weakest −1 (capped at 0–3). Tiebreaker-adjusted cells appear in italic. The most frequent adjustments were in category C, which has six features and frequently produces near-ties — particularly between C2 (Noise) and C4 (Misguided Resistance), which tend to co-present and required careful differentiation.
> **Notable scoring decisions across the new C features:**
> - C3 (Doubt) scores high in stories where a key agent's inhibition was emergent and unplanned — Petrov, Schabowski/Berlin Wall, Tsipras/Greek debt. It scores 0 wherever the decisive agent followed protocol (Heroic Judiciousness) or was simply absent.
> - C5 (Heroic Judiciousness) dominates in the technological cases — Apollo 13's tested reentry sequence, TMI's containment vessel, Flash Crash's circuit breaker, Black Monday's Fed statement — all pre-designed responses executing correctly.
> - C6 (Flinching) is most prominent in Sadat (the speech), Iran-Contra (North's televised performance paradoxically flinching the committee), Berlin Wall (Schabowski's saturation), and Cold Fusion (Pons' premature announcement).
> - C2 (Noise) is highest in the nuclear near-misses where systemic false signals or command-structure accidents place agents in decisive positions without their knowledge.
> The batch and story filters allow focused comparison. Hovering over any cell shows the story, feature ID, score, and whether a tiebreaker was applied.
### Discussion
LLM usage was targeted at the following (not all presented above):
1. scraping stories
2. iterating on the story type description while scraping new stories
3. presenting text summaries (with citations) in a retrograde chronology so that stages of deescalation are better highlighted
4. identifying and quantifying (scoring) narrative features in summaries
#### To do -- where you can easily help!
A few steps of quality assurance are in order (checked if in progress):
- [ ] verify the fidelity and source credibility of stories
- [x] cross-examine the scoring 
I had the strongest doubts in the latter, less so because the LLM might not appreciate the nuance of the scoring directives or the stories, but simply because it might mix up tokens for the digits that symbolize the scores. When I started scoring myself, I initially had the impression that this doubt is justified and the scoring is off. Then upon further reflection I realized I should correct my scoring to the LLM's.

Of course, this is a soft and highly subjective task. Just as human variance, the LLM persona likely skews the results in one way, possibly one that my prompting style influenced. It is instructive to
- try the scoring task possibly with multiple LLM's and optimally with base model access
- gather scores from humans

Another potential shortcoming is the incompleteness of the scoring system, to be further investigated, but --

#### Initial exploration of feature statistics -- prompting again, responses only
##### baseline check
**The top correlation cluster: Good Friday × South Africa (r ≈ 0.97+)**

These two are the highest-correlated pair in the corpus — barely distinguishable by score. Both are long-armed peace transitions where armed insurrection had been operative for decades, both feature simultaneous symbolic disarmament by two sides, both are driven by small groups of key negotiators (C1 conspicuous), and both deploy de-escalation ladders as the primary resolution mechanism. The single meaningful divergence is C2 (Noise): South Africa scores slightly higher because the transition was surrounded by more unpredictable violence from third parties (right-wing Afrikaner factions, Inkatha) that didn't reach the negotiating principals — a cleaner instance of noise below the veto-point level. What the high correlation reveals structurally is a distinct sub-type: _the choreographed bilateral unloading_, where both parties must simultaneously reduce tension through a sequence of publicly witnessed symbolic acts. The gun doesn't misfire — it is formally disassembled in a ceremony.

---

**The nuclear machine-error cluster: Petrov × Arkhipov × Norwegian Rocket**

These three form a tight sub-cluster (all pairwise r values high). All three share: extreme D1 (trigger specificity — the signal must look like a full-scale first strike to be actionable), high D4 (multi-channel confirmation — ground radar failing to corroborate satellite), high C1 (structural veto — an individual in the right architectural position), and near-zero D5/D7 (no de-escalation ladders needed; the non-firing is achieved before any negotiation becomes possible). The key distinguishing score in this cluster is C3 (Doubt): Petrov scores highest (his inaction was genuinely emergent and ambiguous — a protocol violation driven by engineering instinct), while Arkhipov scores on C2 (Noise — his presence aboard B-59 was an accident of command structure), and the Norwegian Rocket scores on A2 (assumption failure — the filing error that meant the military didn't know about the launch). So even within this extremely tight cluster, the three stories pivot on different proximate mechanisms: systemic false alarm + individual doubt (Petrov), command structure accident + individual resistance (Arkhipov), bureaucratic noise + institutional veto (Norway). The high correlation captures the shared _environment_ (Cold War nuclear hair-trigger), while the divergences capture the specific _mechanism_ that prevented the firing.

---

**The scientific false-positive cluster: BICEP2 × Cold Fusion × N-rays × Polywater**

These four form a loose but consistent cluster with pairwise correlations in the 0.80–0.88 range. All share very high C2 (systemic noise below any individual level — contaminated samples, misread slides, loose cables), high D4 (peer replication as the multi-channel confirmation mechanism), and low or zero D5/D6/D7 (no temporal deceleration or de-escalation structure). The key structural difference within the cluster: Cold Fusion and N-rays score high on C6 (Flinching) — Pons' premature announcement and Blondlot's nationalistic investment represent agents becoming saturated or predictably susceptible — while BICEP2 and Polywater score this feature lower because the flaw was more purely instrumental (a loose cable, contaminated glass). This is an analytically useful distinction: _flaw in the person_ versus _flaw in the instrument_, even though both produce the same narrative arc.

---

**The economic mechanism cluster: LTCM × Black Monday × Flash Crash × Draghi**

A less tight cluster (correlations 0.72–0.83) united by zero or near-zero C3/C6 (no individual doubt or flinching), high C5 (Heroic Judiciousness — the Fed statement, the circuit breaker, the OMT announcement), and high E4 (systematic confidence challenges across the market ensemble). The structural contrast within the cluster is between _passive_ and _active_ heroic judiciousness: Black Monday and Flash Crash involve pre-designed mechanisms executing automatically (Greenspan's statement, the CME circuit breaker), while LTCM and Draghi involve individuals deliberately deploying a pre-existing structural capacity (the Fed's convening authority, the ECB's unlimited mandate) in a way that required personal judgment about timing and framing. The scores cannot distinguish these — C5 captures both — but the narrative difference is real and may suggest a future sub-feature.

---

**The most analytically interesting pair: Checkpoint Charlie × Good Friday (r ≈ 0.84)**

This pair is the most structurally illuminating of all because it is _not_ obvious. The Berlin tank standoff (1961, 16 hours, resolved by a backchannel) and the Good Friday Agreement (28 years of armed conflict, resolved by years of negotiation) seem utterly different in scale and duration. What the correlation reveals: both score identically high on C1 (structural veto — both required one decisive actor to act, Kennedy/Khrushchev in the first, the small negotiating groups in the second), D5 (de-escalation ladders — choreographed reciprocal withdrawal vs. sequenced decommissioning), and D7 (polarization disruption — the US backchannel disrupts the Soviet-American polarity; external actors including the US and Irish diaspora disrupt the IRA-British polarity). The key divergence is time: Checkpoint Charlie scores near-zero on D6 (temporal deceleration) because the crisis was compressed into one night, while Good Friday scores high because the multi-year process was built on deliberate temporal structure. This suggests a structural insight: de-escalation ladders (D5) and polarization disruption (D7) are the _mechanism-invariant_ features of bilateral standoff resolution, while temporal deceleration (D6) is the _context-variable_ feature that determines whether the resolution is acute or chronic.

---

**Cross-cutting observation**

The ten highest correlations fall into four distinguishable structural sub-types, each with a characteristic feature signature:

|Sub-type|Defining features|Representative pairs|
|---|---|---|
|Choreographed bilateral unloading|C1+D5+D7 high; D6 high; C2–C6 low|Good Friday × South Africa; Checkpoint × Good Friday|
|Nuclear machine error|D1+D4 high; C1 high; C3 or C2 differentiates|Petrov × Arkhipov × Norwegian|
|Scientific false positive|C2 high; D4 high; D5–D7 low; C6 differentiates|BICEP2 × Cold Fusion × N-rays × Polywater|
|Economic mechanism|C5 high; E4 high; C3/C6 low|LTCM × Black Monday × Flash Crash × Draghi|

The high correlations are therefore genuinely reflective of deep structural similarity — not just surface domain overlap — while the residual divergences reliably point to the specific mechanism that differentiates two otherwise near-identical narratives.

---
##### evaluation stress-testing
**What the lowest-correlated pairs share — and what that tells us**

The most striking finding is that even the most structurally dissimilar pairs in this corpus share 8–11 features out of 20 within the diff < 2 threshold. That floor is telling: it means the non-firing gun category imposes a genuine minimum structural signature — certain features are present at similar levels across essentially all cases regardless of domain, mechanism, or era. The shared features across nearly every low-correlation pair are:

- **C3 (Doubt) = 0** in both stories of almost every low-correlation pair. This is not because C3 is unimportant — it scores high in several individual stories — but because it is rarely present in the _same pair of stories simultaneously_. When one story features emergent inhibition in a decisive agent, the other typically does not.
- **E1 (Macro-state vs conflict)** and **E3 (Asymmetric propagation)** are near-universally shared — both stories in almost every pair score 2 or 3 — which confirms these are baseline category-defining properties rather than discriminating variables, consistent with Flag C.
- **E4 (Confidence challenges)** is similarly shared at 2+ in almost all pairs, for the same reason.

---

**The specific character of each low-correlation pair**

The ten pairs cluster into a recognisable pattern: in each case, one story is dominated by the _individual/machine agency_ cluster (C1–C6 and D1/D4 high) while the other is dominated by the _systemic/structural_ cluster (D5/D6/D7 high, C features mostly absent or inverted). The lowest-correlation pairs are precisely those where one story's non-firing mechanism operates through a decisive individual or mechanism resisting a cascade, and the other's operates through structural and negotiated de-escalation unfolding over extended time.

The pair that exemplifies this most cleanly is **Apollo 13 × Good Friday Agreement**. Apollo 13 is almost entirely a C5 (Heroic Judiciousness) and E4 (confidence challenge across the system) story with near-zero D5/D6/D7 — the gun didn't fire because pre-designed procedures executed correctly in an acute crisis over four days. Good Friday is almost entirely a D5/D6/D7 story — the gun didn't fire because a choreographed multi-year de-escalation ladder was constructed and walked down — with near-zero C5. Their shared features are exactly the E-category universals plus the moderate A-category scores.

Similarly, **Franklin's Expedition × Swine Flu 1976** are both stories of spectacular failure of preparation (A1 maximal in both) and asymmetric observation level (B2 high in both), but Franklin's is a story of pure structural silence — there is no agent-level mechanism, no de-escalation, nothing — while Swine Flu is driven by institutional confidence challenges and misguided resistance cascading through a bureaucratic system.

---

**The invariant residue**

Across all ten lowest-correlation pairs, the features that consistently score similarly (diff < 2 in 9 or 10 of the 10 pairs) are:

|Feature|Why it survives even across uncorrelated pairs|
|---|---|
|C3 = 0|Emergent decisive-agent doubt is rare — most stories lack it; both stories in a pair typically agree on its absence|
|E1 ≥ 2|The macro-state disposed against conflict is a category prerequisite|
|E3 ≥ 2|Information asymmetry at population level is similarly universal|
|E4 ≥ 2|Systematic confidence challenges pervade the category|
|C6 low|Flinching is episodic; most stories don't feature it; pairs agree on its absence|

This suggests the analytical framework has a two-tier structure that the low-correlation analysis makes visible: a **universal floor** (E1/E3/E4 and the near-zero C3/C6 baseline) that all non-firing guns share regardless of mechanism, and a **discriminating superstructure** (C1–C5, D1/D4/D5/D6/D7) where the actual differences between story types reside. The low-correlation pairs diverge maximally on exactly the discriminating superstructure and agree only on the universal floor — making them the ideal test cases for validating the framework's internal architecture.

[^1]: This should contain all and only necessary context.
