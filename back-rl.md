The content of this note will require some improved wording, clarification and expansion.

In order to do that, first the missing citations need to be identified.

Only do this: search for instances in the text where authors or recurrent topics are mentioned and identify the publication (or the most likely candidates) of which the citation is missing from the text.

- **Kakade–Langford 2002 (CPI)** is the foundational paper: the Performance Difference Lemma η(π̃) − η(π) = (1/(1−γ))·𝔼_{s∼d^{π̃},a∼π̃}[A^π(s,a)] translates policy-space distance into value-gap bounds, and the mixture-update bound η(π_new) ≥ L_{π_old}(π_new) − (2εγ)/(1−γ)²·α² is the exact per-iteration improvement guarantee the fixed-point framework wants. 
- **DAgger (Ross et al. 2011)** bridges imitation and RL with a trajectory-level bound J(π̂) ≤ J(π*) + u·T·ε_N + O(1), giving linear horizon-dependence provided the Q-gap u is bounded — a direct warm-start-from-π* result.
- **TRPO (Schulman et al. 2015) Theorem 1** is the direct generalization — η(π') ≥ L_π(π') − (4εγ/(1−γ)²)·α² with α the max-state TV distance, and its KL form via Pinsker. This is **the canonical formal bound**: quadratic in policy distance, with a 1/(1−γ)² horizon prefactor that explodes as γ→1 (a warning sign for long-horizon alignment settings). 
- **CPO (Achiam et al. 2017)** extends TRPO to constraint satisfaction at every iterate — the natural template for trust-region-based auditing.
- **Levine 2018 (Control as Inference)** is structurally the most Sense-2-relevant: the KL-regularized optimal-policy derivation (SAC, soft Q-learning, MPO) _is_ a local-perturbation argument — the optimal policy under a KL constraint to a reference is a small reweighting of that reference. TRPO and PPO inherit this framework. But Levine 2018 is a tutorial, not a theorem paper; the formal content is in the RL-theory.
- **Mei et al. 2020** shows softmax PG obeys a non-uniform Łojasiewicz inequality whose constant depends on π(a_|s) at initialization — formally making "near-optimal initialization" mandatory, not cosmetic.
- **Agarwal, Kakade, Lee, Mahajan (JMLR 2021)** provides the modern NPG global convergence theory. The tabular NPG achieves a dimension-free rate V*(ρ) − V_t(ρ) ≤ 2/((1−γ)²t), and the function-approximation version depends on the __distribution mismatch coefficient M(π_, ρ; μ) = max_s d^{π_}_ρ(s)/μ(s)** — a quantity that is precisely "how well the sampling distribution covers the optimal policy's occupancy." **This is the cleanest formalization of backward-from-π* reasoning available.** 
- **Rashidinejad, Zhu, Ma, Jiao, Russell (2021)** strengthens this with the **single-policy concentrability coefficient** C^{π*} = max ‖d^{π*}/μ‖_∞, proving LCB achieves Õ(√(C·|S|·H³/N)) suboptimality — minimax optimal, and adaptively interpolating between imitation (near-expert data) and full offline RL. **PEVI inherits this insight.** The framework should adopt single-policy concentrability as its primary topological constant.
- **Local quadratic convergence near π*** appears explicitly in **Cen, Cheng, Chen, Wei, Chi 2022**: entropy-regularized NPG achieves linear global convergence ‖Q__τ − Q^(t)_τ‖_∞ ≤ C₁(1 − ητ/(1−γ))^t, and becomes **quadratic once the iterate enters a local neighborhood of π*** (inexact-Newton behavior).
- **Bhandari & Russo 2024** and **Fazel, Ge, Kakade, Mesbahi 2018 (LQR)** establish the **benign landscape** paradigm: PG satisfies a PL/gradient-dominance inequality C(K) − C(K*) ≤ const·‖∇C(K)‖² despite non-convexity, so there are no spurious stationary points. These are the rigorous versions of "local convexity of the value landscape near π*."
 
## How the candidates to extend with split on tractability

The clearest organizing axis is **whether the paper formally relies on the current state (policy, reward belief, demonstrator) being a small perturbation of the optimum**. Four distinct patterns emerge.

**Pattern A — small perturbation as a theorem assumption.**
- RLSP (Shah et al. 2019)
	- Appendix A is exact only under a triad of assumptions: **finite simulation horizon T**, **linear-in-features reward**, and **Boltzmann-rational human** π(a|s) ∝ exp(βQ_θ).
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

**Pattern B — **Bayesian REX** 
- a final-policy high-confidence policy evaluation bound 
- but it is a Bayesian posterior quantile over evaluation policies, not a training-trajectory PAC bound. 
**Pattern C — tractability via a mechanism other than small perturbation.** 
- **Bajcsy, Siththaranjan, Tomlin, Dragan 2021**
	- target set ℒ = {z : ‖θ̂ − θ*‖ ≤ ε} around a near-optimal belief 
	- backward dynamic programming (Eq. 5) to compute Time-To-Learn (Eq. 7). 
	- **no trust-region, no linearization, and no Bayesian-update contraction assumption** is invoked but 
		- low state dimension
		- finite horizon T 
	- dimensionality as the practical limit. **Bansal et al. 2017** (the HJ survey) is explicit that "computational complexity scales poorly with state dimension"
- **PEVI (Jin, Yang, Wang 2021)** 
	- Theorem 4.4 gives minimax-optimal suboptimality bounds on linear MDPs under a _single-policy coverage assumption_ 
	- the dataset only needs to cover π*'s trajectory, not the full state-action space.
	- PAC bound whose _key assumption_ is on the topology of the data distribution around π*.

**Pattern D — refute
- **MIRI's tiling agents** (Yudkowsky-Herreshoff 2013; Fallenstein-Soares 2014–2015) 
	- model polymorphism's κ-step parameter is the closest thing to a positive finite-step bound, but only by dropping all-time soundness.
	- Reflective oracles (Fallenstein–Taylor–Christiano 2015) and Demski's HCH/logical-induction bridge are the fixed-point-theoretic contributions

## What this means for the fixed-point framework

1. rarely formalized intuitions — IDA's "small step per amplification" and IRD's "proxy close to true reward" are exactly the arguments the framework needs, but they are stated as motivating assumptions, not theorems. Supply the formalism these papers implicitly rely on, by importing from RL-theory.
2. reason about single-policy concentrability (Rashidinejad et al.) or the distribution mismatch coefficient M(π*, ρ; μ) (Agarwal et al.) — both capture backward-from-π* topology without requiring uniform coverage. 
3. combine RLSP with HJ-reachability-over-learning-dynamics (Bajcsy 2021)**: RLSP supplies the finite-horizon backward trajectory with a Boltzmann-linear-reward tractability triad, and Bajcsy supplies the HJ machinery without requiring contraction or linearization of the belief update.