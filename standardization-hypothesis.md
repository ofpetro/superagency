[[#Closing thoughts]] is where I give my (somewhat divergent, "bigger picture") conclusion to this post. [[#Seed prompt]] is to be run as part of a prompt with qualifications, an example (qualifying input, output) pair[^1] is ([[standardization-example]],[[Standardization-response-1.pdf]]). [[#Analysis]], a more important section comments on the latter document. Some highlights are quoted directly to make the analysis self-contained.

## Analysis

We wish to investigate the role of standardization in deescalating tension between competing labs or confrontative nation states and inciting cooperation on AI development. In particular, we look at what arguments could be convincing (or coercive) for labs to comply with standards, which eventually leads to their diminishing competitive advantages.

### Illustrative scenarios around potential standard adoption

The goal with these is not to prompt debate on the object level but to explore the relation between areas of standard applicability and corresponding private company motivations. Those can point to fragmentation _on multiple different points_ of an AI-assisted task lifecycle (even encompassing data collection, storage and training) with different levels of resistance to standard adoption at each point. The overarching claim to be supported in this analysis is that pushing sequentially for increasingly more resisted standards can amount to successful salami slicing tactics towards an eventual globally unified AI development.

The scenarios are not in this surmised ascending order. _Begin LLM quote._

### 1. "MCP-for-Provenance"
a mandatory routing-and-data-use disclosure schema

- _Description:_ A member-owned consortium of labs + cloud providers (SWIFT/ISO-20022 model) defines a structured, machine-readable manifest that every API response must carry: which model instance served the call, what system prompt/scaffolding was appended, and a flag for whether the call's data enters training. Adoption is voluntary-with-deadline, backstopped by EU AI Act transparency provisions.
- _Illustrative gesture (hypothetical):_ After a 2027 incident in which an enterprise discovers its confidential prompts were silently used to fine-tune a competitor-facing model, a coalition ships "AI-CBPR+" manifests; within 18 months 95% of API traffic carries provenance headers, but the "training-use" bit is only made mandatory by statute two years later.

### 2. "Compute-Safeguards Regime"
hardware-enabled verification as an IAEA-analog access standard

- _Description:_ Chip vendors ship governance-capable silicon (TEEs + location verification + offline licensing per FlexHEG/CNAS proposals); an international body verifies that above-threshold training runs occur only on licensed, attested compute, mirroring IAEA material accountancy but via cryptographic attestation rather than physical inspection.
- _Illustrative gesture (hypothetical):_ By 2028 a "Compute Safeguards Agency" convened by a US-China working group verifies attested training logs from three jurisdictions; a diverted cluster is caught by a failed location-ping, but enforcement stalls when the host state disputes jurisdiction, echoing New START verification disputes.

### 3. "Reactive Circuit-Breakers for Autonomous Agents"

- _Description:_ After an incident in which an autonomous agent (via MCP tool-calls) cascades a harmful action across services, regulators + an exchanges-analog (major clouds) impose uniform "kill-switch" and rate-limit standards on agentic execution, exactly as the SEC imposed uniform circuit breakers + the Market Access Rule after the Flash Crash.
- _Illustrative gesture (hypothetical):_ A runaway procurement agent places millions in erroneous orders across three SaaS platforms in minutes; within a quarter the major clouds adopt a common "agent limit-up/limit-down" API that pauses tool execution on anomalous velocity.

### 4. "Global Operating System for AI Access"
impartial aggregate manager/distributor

- _Description:_ Competing labs/nations establish an impartial aggregator that (a) obfuscates from users which lab/subnetwork serves their query (frustrating subnetwork-hijack attacks like the Hugging Face namespace/model-poisoning cases), (b) preserves per-session user tracking for intent-monitoring, (c) prevents single-lab lock-in, and (d) guarantees labs retain [some] customer base regardless of which lab's model carries a latent vulnerability. Grounded in IAEA dual-use governance and BGP/MANRS routing-security precedents.
- _Illustrative gesture (hypothetical):_ Following a 2028 automated attack that hijacks a popular open model to exfiltrate data at scale, a "Geneva-for-AI" summit stands up a neutral routing fabric; two frontier labs join for reputational cover but quietly keep their premium direct endpoints, and the fabric handles mostly commodity traffic — a partial MANRS-like honor-system equilibrium.

_End LLM quote._

### General remarks

With these scenarios I want to set up a space of "boring middle grounds", one where intervention proposals are not idealized silver bullets and ideation on them is just facilitated. I am aiming for those, respectively, because they sit between extremes that invite the counterarguments
1. "reality is always too complex and nuanced for simple cross-cutting solutions to be feasible" and "we need to concern ourselves with higher marginal impact and / or widely applicable policies (favoring them over rather specific and inconsequential ones)";
2. "the scope suggested here is too wide, the range of opportunities is overwhelming and disorientating and not inspiring at all" and "the level of specificity is so high, everything here is too rigid to survive realistic implementation".

If I take these scenarios at face value, the first impression is that towards long-overdue compromises, between AI industry players clinging to their competitive edge and public interests desperately needing to blunt that competition, we can take an approach from multiple angles,[^2] and it is not hard to make those approaches tangible. I believe that the bottleneck is not creativity to come up with strategies to win[^3] concessions from growth-obsessed economic actors, but _not wasting efforts by dismissing how our work weighs in the balance of surfacing the private-public conflict of interest vs bringing something else in focus._

Secondly, I can see a perspective worth maintaining while working with any concrete proposal: how are they likely to miss their target? Who is likely to circumvent standardization? How can they be detected? Who will care about the consequences? And above all, _in any suboptimal outcome, have we known precedents of similar failures that we managed somehow?_

Going forward, I shall move to the more abstract and less speculative sides of each scenario, with 2 questions to them:
- what is the relevant current economic and political scene like?
- how to envision outcomes up to mid-term?

Again, my point is not to claim accurate predictions or bulletproof arguments, but show a flavor of reasoning about these, which could be productive. _Begin LLM quote._

+++

1. "MCP-for-Provenance"

- _Evaluative answer:_ Providers adopt _disclosure of routing/model_ readily (a trust feature, like ISO 20022's richer data), but resist the _data-reuse flag_ (self-undermining — it exposes a monetization practice). Net: race-to-standardize on the transparency envelope, race-to-fragment on the sensitive field. Likely requires a legislative backstop (LIBOR-Act style) for the contested field.
- _Strength:_ direct analogy to ISO 20022 and MCP; clear mechanism; plausible adoption path via existing consortia.
- _Projected outcome category:_ persistent gap, then clear improvement once a triggering incident + legislative backstop arrive.

+++

+++

2. "Compute-Safeguards Regime"

- _Evaluative answer:_ Chip vendors adopt only if (a) it unlocks otherwise-blocked sales (the Nvidia location-verification cost-recovery logic) or (b) mandated (Chip Security Act-style). This is Montreal-Protocol logic: standardize once a substitute/benefit exists and defection is trade-penalized.
- _Strength_ on precedent: IAEA, Montreal trade-exclusion, export controls already de facto; on mechanism maturity: verification tech is proposed, not deployed; tamper-proofing evidence "limited" per RAND.
- _Projected outcome category:_ ongoing management, incremental improvement — verification asymmetry and great-power politicization limit it, as they do the IAEA.

+++

+++

3. "Reactive Circuit-Breakers for Autonomous Agents"

- _Evaluative answer:_ Post-incident, providers _want_ the uniform standard because disparate rules amplified the harm and the liability; a race-to-standardize triggered by a shared shock.
- _Strength:_ precise analogy to a documented case; mechanism (mandatory pre-trade-style risk checks) already exists in finance.
- _Projected outcome category:_ acute challenge, prompt effective resolution -- if the incident is salient and bounded; [persistent challenge without being addressed... for a period, but showing clear improvement, once addressed] -- if diffuse.

+++

+++

4. "Global Operating System for AI Access"

- _Evaluative answer:_ Requirement (c) "no lock-in" and requirement (d) "retain customer base regardless" are in direct competitive tension — an aggregator that dissolves brand attribution destroys the differentiation labs compete on, so each lab's dominant strategy is to defect (offer a superior direct API), exactly as BGPsec failed because unilateral adoption gave benefit only if universal and imposed a cost. It becomes adoptable only under (i) a catastrophic, attributable incident that makes fragmented access an existential shared liability (Montreal/Flash-Crash logic), or (ii) state coercion (export-control/IAEA logic). The obfuscation-plus-monitoring design also mirrors the confidential-routing vs. lawful-intercept tension.
- _Strength:_ The _motivation_ (mutual-risk cooperation after an infrastructure attack; US-China Schelling-point coordination) is well-grounded; the _mechanism_ is speculative and internally in tension.
- _Projected outcome category:_ diagnosis only in the near term — much proposed, little adopted — escalating to [acute governance challenge and prompt, effective resolution or persistent challenge without being addressed, later improvement, once addressed] only conditional on a forcing incident.

+++

_End LLM quote._

Indeed, the convincing strength, either based on the preexisting environment or on what the post-hoc management debt looks like, is mixed in this selection. Pro and contra arguments exist for each and their lists can go on. However, for each, I find them a potentially fruitful way for anchoring to middle ground between accelerationism and pause positions...

I am tempted to engage in object level discussions of the scenarios, yet realistically I highly doubt even my best informed opinions would further the case of any of them on this platform. So instead I shall stick to commenting on the base document.

+++

A note on using LLM input here

I take responsibility for this document written as-is, acknowledging that I lack the track record and formal education as credit to my judgement on whether the content is accurate or deep enough to be worth the attention of your possibly better informed person. If you inspect the base document, you will see the kind and extent of editing I am doing to assemble this one. I deem that (and my prompting) to be substantive enough to make the end result stand up to essays in the same realm of critique -- at least, of course, which I have seen -- and _that judgement_ is what drives the present work. If you can, I invite you to point out its -- my -- shortcomings (beyond "come on, quit feeding us slop"). 

+++

### A suggested structure for standardization prioritization

A key motivator for sharing this is the observation that through the evolution of the internet, there were pre-echoes of what has been said about AI: that it
- is the culmination of industrial revolutions, or a distinct, most-significant-yet new wave of them;
- unlocks the unprecedented economic value in low-latency and wide-band connection between endpoints;
- has the potential of becoming ubiquitous, not just technically, but driven by a real (initially latent) demand;
- will enable average citizens to improve their marketability, public presence, agency etc.;
- is expected to introduce a new species of security vulnerabilities and concerns;
- is maintained and developed in a separate (likely more powerful) network by the military;
- will cause self-stabilizing social transformation and entrenchment;
- in particular, divide the ontologies of subscribers and non-participants;
- lead a few particularly smart, well-positioned players to divide up the underlying physical infrastructure and essentially become landlords capitalizing on a generic user base.

There probably is more to this. The gist is that cyberspace was poised to become to the contemporary era what seas were to modernity. But building on the improved wisdom and common conscience from prior industrial revolutions, the benefits to standardization for more frictionless economic production as well as for equity have been also salient. We have by no means decisively sorted out those questions; not even whether standardization was relatively more effective for boosting production or for better distributing living standards improvement. Nevertheless, that process has been able to progress, hence the reason that I am treating it as a model for the _expected_ course of events with AI, for better or worse.

To me the most striking feature of standardization is OSI, an admittedly biased view, because it helps structure the "spheres of interest" related to the worldwide web. By that I mean that making the component stack for the operation of web apps explicit guides entrants to any market in setting up the scope of their business; also it has a defining role in supply chains. Evidently, AI apps are at least entangled with that layer stack, if not simply built on top of it.[^4] I propose considering layers following functional elements of how AI is used today, as an initial overview of standardization opportunities (see a provisory layer stack in the penultimate paragraph).[^5] Assessing scenarios following their classification, _begin LLM quote with liberal (unmarked) editing / rewriting_,
- On prompt/context/orchestration formats the market is converging (MCP, OpenAI-compatible API, OCI/K8s). As Linux Foundation is already doing for MCP, _codification_ of emergent standards through a neutral body is a means to create an intent-signaling, symbolic, easy-to-adopt conforming policy. In mediating negotiations between labs or nation states in a stale conflict these provide crucial moves in de-escalation; moves against these may be taken as warnings of preparation for aggression.
- According to the base document, the _technical_ side of governance that acts based on stocks and flows of physical (a) resources, (b) (ownership of) environmental impact, (c) infrastructure components (d) energy, is well prepared (if not directly for big data processing but established economic segments). What is lacking is stringency in enforcing it. If this is the case, it carries the chance for gradually increasing that, e. g. setting increasingly deterrent precedents in laws or court orders.
- Highlight: routing to a model instance
	- commercial aggregators (OpenRouter: 300–400+ models, 60+ providers; AWS Bedrock intelligent prompt routing) and academic benchmarks (RouterBench, RouteLLM, RouterEval) compete;
	- routing is deliberately proprietary/opaque [[ZenML](https://www.zenml.io/llmops-database/building-a-multi-model-llm-marketplace-and-routing-platform)];
	- a light-touch disclosure standard: an "ISO 20022 for AI routing/telemetry": a structured, mandatory schema for _what was appended, where the query was routed, and whether the call feeds training_;
	- a single high-profile "silent routing to an unsafe/compromised model" incident (cf. the Hugging Face namespace-hijacking and malicious-model attacks — 352,000 unsafe-model issues, 335 traced to one "ClawHavoc" operation) should launch a Flash-Crash-style reactive standardization push. [TNW | Security](https://thenextweb.com/news/hugging-face-clawhub-malware-ai-supply-chain)
- Possibly hard-to-regulate: API resellers, gray-market GPU clouds, state-affiliated users, jailbreak communities.

_End LLM quote._

### Caveats

I must admit, though, that because a few architectures, e. g. the transformer seem a reigning paradigm of commercial (and, actually, also access-restricted) AI implementations, there is a wide selection of design choices to steal instantly from competitors (thereby effectively standardizing but simultaneously closing competition gaps in certain aspects). And it is important to discern the tendency behind any standardization move, and not give too much optimism to superficial, apparent ones. One possibility is that all major labs covertly and gradually hand over AI improvement to AI, and an eventual cross-lab exfiltration incident synchronizes the present state of the art: while in effect that radically resets competition dynamics, it leaves competitive incentives intact (and may be a one-off, transient event).

Furthermore, one might argue that wide-spread and universal standardization carries the risk of a globally less resilient infrastructure or one designed to constantly absorb a series of patching attempts to the original standard (taken to the extreme, locking in fragmentation). The first example coming to mind is the state of IP addressing due to particularities of v4. To this, I posit that the further we push off the decisions, the less time we allow ourselves before technical and management debt starts accumulating and they become immediately needed -- then, the likelier it is that they will be botched.

To a wide market standard adherence has little meaning, moreover it may become a frustration when the entire market becomes divided into comparable sections dominated by slightly different ones. Still, AI is truly a product of a globalization age; or one could say the ambitions of leading labs are not far off from global market domination. In contrast, the aforementioned situation generally relies on some (geographical) isolation factor that deprioritizes unification across distinct areas with their peculiar standards (viz. power plugs). Therefore I do not see this a real threat to customer satisfaction here.

## Closing thoughts

The "race to AGI" is not the first narrative about society chasing the high of ever-increasing capture of dominated area or access to some resource, despite a seemingly unanimous understanding of it being finite and / or exhaustible. If we cannot bring ourselves to face the reality of how unpredictable (and grim) a future we are thus headed to, we may still _know_ and take the necessary action to cease progress in this direction.

I am making my present suggestion for the ethics of these circumstances with the end goal of spreading the practice of controlling economy. I deem standardization the branch where low-hanging fruit is to be found. 

## Seed prompt

The access and operation of computer resources to perform inference with, or training of, AI models is poorly (or not at all?) standardized, and although API's, e. g. to LLM's, provide a de facto specification of features available to consumers, the implementing business logic and side-effects, e. g. how interface providers collect and use API call data for subsequent training, is not subject to regulation or even practical mechanism patterns; not to mention UI's provided by developers, in which user-originating messages go through an entirely different pipeline compared to the API use case.

Sanity check: is this view actually due to being poorly informed on practical treatment of input from endpoints remotely accessing LLM capacity in the cloud? Or: is this overlooking a formal policy to handle such client-server communication that is evidently adhered to?

If the sanity check is passed, i. e. 2 decisive negative answers found: is there a substantive body of literature describing either benefits or drawbacks, or even both, of the diversity in the messaging business logic?

If the sanity check is not passed, i. e. at least one decisive positive answer found: is the coordination in messaging business logic organically emergent with no stated goal, or is there an explicit agreement on its origin or purpose?

Prioritize the sanity check for research and address at most one of the follow-up questions, if the sanity check is undecisive, skip both follow-up questions. Work with the thus accumulated result going forward.

In the following the core features of the hypothetical standardization scenarios is presented. First in order and priority, let's see the likely immediate impact of the described standardization effort, especially drawing on earlier similar governance instances. Second, evaluate each resulting case study by how confident or convincing the analogy between the inspiring regulatory example, or related narrative, is; create a class of stronger cases and one of weaker ones.

The main question to answer for each case: does this corroborate or refute that competing service providers (across the AI industry, e. g. datacenter construction suppliers, GPU manufacturers and vendors, data management companies, model developer labs, application developers etc.) will reduce the risk that their service (or products) falls behind in competition and they thusly worsen their market position?

Standardization scope:
- the format of the task handed over to AI, e. g. of the prompt in case of LLM's, the dataset in case of a finetuning
- what may be appended before handing over to a model, e. g. the system prompts, scaffoldings, model selection logic etc.
- the routing to a model instance
- the software stack supporting computation (inference or training) in the cloud
- the physical aspects of the computing infrastructure, e. g. network topology, security standards, location, ownership, monitoring access and switch-off privileges
- the datacenter site, surroundings, resource usage and other environmental impact (such as noise pollution)

A particularly strong element of the motivation behind the main question: it seems to increase in likelihood (considering the recent automated attack on Huggingface) that even despite customary safety protocols, human operators' negligence while running a powerful AI model can lead to destructive consequences that may only be resolved by proactive cooperation by entities with several competing interests -- like the nation states of China and the US. One national lab may have the AI to save another nation from such destruction, possibly impacting the existing international web infrastructures or applications, of the other nation's own AI, and vice versa, so they'd both benefit from an impartial aggregate manager and distributor of AI capabilities to consumers
- through a global operating system;
- that obfuscates for users where demand and queries are routed to complicate unsafe use by hijacking a subnetwork;
- but it allows for tracking specific users' sessions and monitoring their activity or intent;
- it doesn't let users be compelled by a specific lab's product;
- ensures labs' customer base regardless of any lab deploying a model, which contains manifest vulnerability, or can create one for an existing system.

[^1]: by Claude Sonnet 5

[^2]: like, a Swiss cheese approach in spirit -- but I would not think long about the analogy...

[^3]: I have to admit, I am partial here, something [I have elaborated](https://www.lesswrong.com/posts/9xqDFCLeYDtC3q362/growth-tax)

[^4]: I want to leave room for ambiguity here, entertaining the prospect of a separate (logical) web for AI.

[^5]: i. e. "Standardization scope", just above these footnotes
