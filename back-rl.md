# Backward-from-optimality tractability arguments across the alignment and RL-theory literature

**Bottom line.**
- **three contain** small-perturbation / benign-landscape tractability that are formal and trajectory-level:
	- RLSP, classical trust-region reasoning?
	- the Off-Switch Game classical trust-region reasoning?
	- the HJ-reachability family (Fisac 2019, Hsu 2021, Bajcsy 2021) — finite-horizon backward DP + discount-induced contraction.
- Two candidates are best read as _refutations_
	- MIRI tiling
	- ELK
- formal tractability infrastructure in the **pure RL-theory citation neighborhood** 
	- Kakade–Langford CPI,
	- TRPO Theorem 1,
	- Agarwal–Kakade–Lee–Mahajan,
	- Cen et al.,
	- Rashidinejad et al.
- **single-policy concentrability** — the cleanest formal embodiment of "how close the current data/policy distribution is to π*" — which directly formalizes backward-from-optimality reasoning.

## How the 13 candidates split on tractability

The clearest organizing axis is **whether the paper formally relies on the current state (policy, reward belief, demonstrator) being a small perturbation of the optimum**. Four distinct patterns emerge.

**Pattern A — load-bearing Sense-2 (small perturbation as a theorem assumption).**
- RLSP (Shah et al. 2019)
	- Appendix A is exact only under a triad of assumptions that together constitute a Sense-2 tractability stance: **finite simulation horizon T**, **linear-in-features reward**, and **Boltzmann-rational human** π(a|s) ∝ exp(βQ_θ).
	- Boltzmann softness makes the log-likelihood locally quadratic around the optimum (the standard MaxCausalEnt convexity trick from Ziebart 2010)
	- the finite T bounds the backward trajectory length — exactly the backward-from-endpoint structure of the fixed-point framework.
- PAC bound: **CIRL (Hadfield-Menell et al. 2016)** 
	- reduces to a single-agent POMDP, an exponential complexity reduction
	- **Zhou, Bloem, Bambos 2017** upgrade the MaxCausalEnt objective to a convex program in the ∞-horizon case.
	- Off-Switch Game (Hadfield-Menell et al. 2017
		- **Theorems 1–2 are formal**, showing that the robot's deferral incentive Δ = σ² · 𝔼[π̇ᴴ] − |μ|·Pr(C) trades R's uncertainty σ against H's suboptimality β, with Δ changing sign as H approaches random behavior.
		- Corollary 1 makes this explicit — optimality of w(a) requires H rational.
		- one-shot value-of-information argument that **requires H to be a small perturbation of optimal**;
	- (Milli et al. 2017, Carey & Everitt 2024) confirms the guarantee breaks under irrationality.

**Pattern B — Sense-2 assumption present but informal.** IRD, ICRL, T-REX/Bayesian REX, and IDA/HCH all silently inherit a Boltzmann-rational or small-step assumption without making it the target of a theorem. **IRD** Assumption 1 ("proxy rewards are likely to the extent they produce high true utility in the training environment") and Equation 1 (β-Boltzmann designer) encode Sense-2 at the designer level, but the only formal result is a linear-feature invariance proposition. **ICRL** (Malik et al. 2021; Scobee–Sastry 2020) inherits the MaxEnt-IRL Boltzmann-rational expert silently; neither paper gives sample-complexity bounds (those appear only later, in Anwar et al. 2024). **T-REX** abandons demonstrator near-optimality but replaces it with a Boltzmann-rational _ranker_ assumption via the Bradley-Terry likelihood — the Sense-2 premise just moves up one abstraction level. **Bayesian REX** adds a final-policy high-confidence policy evaluation bound — the closest thing to a Sense-1 statement in this quartet — but it is a Bayesian posterior quantile over evaluation policies, not a training-trajectory PAC bound. **IDA/HCH** (Christiano et al. 2018) makes the central intuitive argument of the whole fixed-point framework: _each amplification step A_n → A_{n+1} is a small local improvement auditable by the previous overseer_. This is pure Sense-2 conceptually and explicitly trajectory-level, but the paper is empirical and contains no convergence theorem. Yudkowsky's 2018 "Challenges to Christiano's capability amplification" is the canonical adversarial steelman: errors in D-imitations of DD-imitations compound, and the Sense-2 smallness assumption may not survive iteration. The weak-to-strong generalization literature (Burns et al. 2023) provides empirical gap measurements but still no formal Sense-1 bound over training.

**Pattern C — tractability via a mechanism other than small perturbation.** The HJ-reachability family is the surprise here. **Bajcsy, Siththaranjan, Tomlin, Dragan 2021** is structurally the paper closest to the fixed-point framework — it literally defines a target set ℒ = {z : ‖θ̂ − θ*‖ ≤ ε} around a near-optimal belief and runs backward dynamic programming (Eq. 5) to compute Time-To-Learn (Eq. 7). Crucially, **no trust-region, no linearization, and no Bayesian-update contraction assumption** is invoked. Tractability rests entirely on (i) low state dimension and (ii) finite horizon T — a geometric analogue of Sense-2 at the PDE-solving level rather than the RL level. The authors explicitly flag dimensionality as the practical limit. **Bansal et al. 2017** (the HJ survey) is explicit that "computational complexity scales poorly with state dimension"; the curse of dimensionality is the binding constraint, not policy-space geometry. Two alternative tractability levers appear: **Hopf–Lax for linear dynamics** gives pointwise PDE solutions (Sense-2 at the PDE level via linearity), and **decomposition methods** (Mitchell-Tomlin, Chen et al.) trade conservatism for lower effective dimension. **Fisac et al. 2019** and **Hsu et al. 2021** achieve a different, Sense-1 tractability: by introducing a discount γ into the safety or reach-avoid Bellman equation (Hsu Eq. 15), the operator becomes a sup-norm contraction with rate γ (Hsu Proposition 1), Q-learning converges w.p. 1 (Proposition 2), and the γ-discounted set converges in Hausdorff distance to the true reach-avoid set as γ→1 (Theorem 1). **This is a formal, trajectory-level convergence guarantee on Bellman iterates**, but it does not require the current policy to be near optimal — only the discount to be strictly less than one. These are pure Sense-1 contraction-mapping arguments. **PEVI (Jin, Yang, Wang 2021)** belongs in the same Pattern C slot: Theorem 4.4 gives minimax-optimal suboptimality bounds on linear MDPs under a _single-policy coverage assumption_ — the dataset only needs to cover π*'s trajectory, not the full state-action space. This is a Sense-1 PAC bound whose _key assumption_ is ideologically Sense-2 (topology of the data distribution around π*).

**Pattern D — Sense-2 intuition is refuted.** **MIRI's tiling agents** (Yudkowsky-Herreshoff 2013; Fallenstein-Soares 2014–2015) is framed precisely around the Sense-2 hope that a parent agent can audit a near-identical successor, and the Löbian obstacle is presented as the **formal refutation**: even identity-like self-modification is not soundness-tractable in standard formal systems. The partial patches — descending trust, Herreshoff's waterfall, model polymorphism (§6.3) — all weaken the Sense-2 demand: model polymorphism's κ-step parameter is the closest thing to a positive Sense-1 finite-step bound, but only by dropping all-time soundness. Reflective oracles (Fallenstein–Taylor–Christiano 2015) and Demski's HCH/logical-induction bridge are the fixed-point-theoretic contributions in the neighborhood. **ELK** (Christiano, Xu, Cotra 2021) is similarly a catalog of negative results: every Sense-2-flavored regularizer (complexity penalties, continuity requirements, "sequence of reporters for successively more powerful predictors") is explicitly broken by counterexamples. The direct translator and the human simulator are _close_ on the training distribution — that's precisely what makes them indistinguishable, not what makes the problem tractable. ELK's lesson for the fixed-point framework is adversarial: structural closeness of alternatives does not imply audit-tractability.

## Decision Transformer family and control-as-inference

**Decision Transformer, Trajectory Transformer, and RvS** are directly relevant because they condition on returns-to-go or goal states — effectively treating near-optimal trajectories as fixed-point inputs and predicting actions backward. Yet none provides a formal Sense-2 or Sense-1 convergence guarantee. The most informative work is **Emmons et al. 2022 (RvS)**, which empirically dissects _when_ return-conditioned or goal-conditioned supervised learning suffices: a 2-layer MLP with dropout matches Decision Transformer, so **the transformer architecture is not the essential ingredient**. RvS performs poorly on purely random-data regimes (where TD methods dominate), cannot interpolate between dataset behavior modes (Fig. 6), and validation loss is an unreliable proxy for return — these are practical _anti_-tractability findings. Neither DT nor RvS nor Trajectory Transformer proves that coverage of near-optimal trajectories is sufficient; it is conjectured empirically. **Levine 2018 (Control as Inference)** is structurally the most Sense-2-relevant: the KL-regularized optimal-policy derivation (SAC, soft Q-learning, MPO) _is_ a local-perturbation argument — the optimal policy under a KL constraint to a reference is a small reweighting of that reference. TRPO and PPO inherit this framework. But Levine 2018 is a tutorial, not a theorem paper; the formal content is in the RL-theory neighborhood below.

## Where the real formal tractability lives — the RL-theory neighborhood

The fixed-point framework's formal infrastructure is almost entirely in papers cited by but not belonging to the alignment candidates. **Kakade–Langford 2002 (CPI)** is the foundational Sense-2 paper: the Performance Difference Lemma η(π̃) − η(π) = (1/(1−γ))·𝔼_{s∼d^{π̃},a∼π̃}[A^π(s,a)] translates policy-space distance into value-gap bounds, and the mixture-update bound η(π_new) ≥ L_{π_old}(π_new) − (2εγ)/(1−γ)²·α² is the exact per-iteration improvement guarantee the fixed-point framework wants. **TRPO (Schulman et al. 2015) Theorem 1** is the direct generalization — η(π') ≥ L_π(π') − (4εγ/(1−γ)²)·α² with α the max-state TV distance, and its KL form via Pinsker. This is **the canonical Sense-2 formal bound**: quadratic in policy distance, with a 1/(1−γ)² horizon prefactor that explodes as γ→1 (a warning sign for long-horizon alignment settings). **CPO (Achiam et al. 2017)** extends TRPO to constraint satisfaction at every iterate — the natural template for trust-region-based auditing.

**Agarwal, Kakade, Lee, Mahajan (JMLR 2021)** provides the modern NPG global convergence theory. The tabular NPG achieves a dimension-free rate V*(ρ) − V_t(ρ) ≤ 2/((1−γ)²t), and the function-approximation version depends on the __distribution mismatch coefficient M(π_, ρ; μ) = max_s d^{π_}_ρ(s)/μ(s)** — a quantity that is precisely "how well the sampling distribution covers the optimal policy's occupancy." **This is the cleanest formalization of backward-from-π* reasoning available.** **Rashidinejad, Zhu, Ma, Jiao, Russell (2021)** strengthens this with the **single-policy concentrability coefficient** C^{π*} = max ‖d^{π*}/μ‖_∞, proving LCB achieves Õ(√(C·|S|·H³/N)) suboptimality — minimax optimal, and adaptively interpolating between imitation (near-expert data) and full offline RL. **PEVI inherits this insight.** The framework should adopt single-policy concentrability as its primary topological constant.

**Local quadratic convergence near π*** appears explicitly in **Cen, Cheng, Chen, Wei, Chi 2022**: entropy-regularized NPG achieves linear global convergence ‖Q__τ − Q^(t)_τ‖_∞ ≤ C₁(1 − ητ/(1−γ))^t, and becomes **quadratic once the iterate enters a local neighborhood of π*** (inexact-Newton behavior). **Mei et al. 2020** shows softmax PG obeys a non-uniform Łojasiewicz inequality whose constant depends on π(a_|s) at initialization — formally making "near-optimal initialization" mandatory, not cosmetic. **Bhandari & Russo 2024** and **Fazel, Ge, Kakade, Mesbahi 2018 (LQR)** establish the **benign landscape** paradigm: PG satisfies a PL/gradient-dominance inequality C(K) − C(K*) ≤ const·‖∇C(K)‖² despite non-convexity, so there are no spurious stationary points. These are the rigorous versions of "local convexity of the value landscape near π*."

Pure Sense-1 structural tractability (linear and low-rank MDPs) is covered by **Jin–Yang–Wang–Jordan 2020** (LSVI-UCB regret Õ(√(d³H³T))), **Zanette et al. 2020** (low inherent Bellman error), and **Jiang et al. 2017** (Bellman rank). These give trajectory-level PAC bounds, but the assumption is structural (linear-in-features, low rank) rather than small-perturbation. **DAgger (Ross et al. 2011)** bridges imitation and RL with a trajectory-level bound J(π̂) ≤ J(π*) + u·T·ε_N + O(1), giving linear horizon-dependence provided the Q-gap u is bounded — a direct warm-start-from-π* result.

## Summary table

|Candidate|Sense-1 formal|Sense-2 formal|Sense-2 conceptual|Trajectory|Stance|
|---|---|---|---|---|---|
|MIRI tiling / VR|κ-step model polymorphism only|no|proof-theoretic small-modification|yes|**refutation** via Löb|
|Bajcsy et al. 2021|finite-time reach certificate|no|no|yes|neutral — dim+horizon are the limits|
|IRD|no|no|β-Boltzmann designer, training-env coverage|no|Sense-2 informal|
|Off-Switch Game|no|**Thm 1–2**|ε-rational H|no (one-shot)|canonical Sense-2 formal|
|ICRL (Malik/Scobee)|no|no|inherited MaxEnt|no|Sense-2 silent|
|T-REX / Bayesian REX|HCPE-IL final-policy bound|no|Boltzmann-rational _ranker_|no|partial Sense-1 final-policy|
|ELK|no|no|continuity, complexity priors — **all refuted**|no|**refutation**|
|IDA / HCH|no|no|each amplification step small|yes|central intuition, unformalized|
|DT / RvS / TT|no|no|conditioning on near-optimal trajectories|weak|empirical, not formal|
|Levine 2018 CaI|no|KL-regularization derivations|trust-region foundation|framework|supplies scaffolding|
|HJ reach. (Bansal/Fisac/Hsu)|**Hsu Prop. 1–2**: γ-contraction|no|short horizon, linear dynamics (Hopf-Lax)|yes|Sense-1 via contraction|
|RLSP|no|MaxCausalEnt convexity|finite T + linear reward + Boltzmann|yes|**most aligned with framework**|
|PEVI|**Thm 4.4** minimax-optimal|no|single-policy coverage|yes|Sense-1 with Sense-2-flavored assumption|

## What this means for the fixed-point framework

1. rarely formalized Sense-2 intuitions — IDA's "small step per amplification" and IRD's "proxy close to true reward" are exactly the arguments the framework needs, but they are stated as motivating assumptions, not theorems. The framework's contribution is therefore to _supply the formalism these papers implicitly rely on_, by importing from the RL-theory neighborhood.
2. reason about single-policy concentrability (Rashidinejad et al.) or the distribution mismatch coefficient M(π*, ρ; μ) (Agarwal et al.) — both capture backward-from-π* topology without requiring uniform coverage. 
3. RLSP combined with HJ-reachability-over-learning-dynamics (Bajcsy 2021)**: RLSP supplies the finite-horizon backward trajectory with a Boltzmann-linear-reward tractability triad, and Bajcsy supplies the HJ machinery without requiring contraction or linearization of the belief update.

## More

1. The Off-Switch Game provides the cleanest formal Sense-2 theorem in the alignment literature.
2. HJ-reach-avoid (Hsu 2021) gives the cleanest Sense-1 contraction-based iterate convergence bound. 
3. Performance Difference Lemma, TRPO Theorem 1, NPG rates with distribution-mismatch coefficients, local quadratic convergence in entropy-regularized NPG, single-policy concentrability, PL/gradient-dominance for LQR** — all lives in the pure RL
4. the Kakade–Langford–TRPO inequality quantifies per-step perturbation from π*, Cen et al. show that near π* the dynamics become inexact-Newton, Rashidinejad's single-policy concentrability formalizes "closeness of data to π*" without demanding uniform coverage, and HJ reachability provides the backward-induction PDE technology.