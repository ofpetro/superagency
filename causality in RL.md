A crucial part of the possibility of optimizing a policy is value estimation, itself involving discounting future values.[^1] Here we first investigate why that is crucial, i. e. what effect the discounting formula has.

Consider the following game: in one round the agent can take 3 actions $G, H, I$ and it is independently decided according to a random process which of 2 effects they take.

| actions \ effects | 1. probability $P(t)$                                                                                                 | 2. probability $1-P(t)$                                                                                 |
| ----------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| $G$               | $R$ finite reward                                                                                                     | end of both games                                                                                       |
| $H$               | $q(t)=Q(t)-Q(t-1)$ with $Q(t)$ a finite penalty, $Q(t-1)$ the penalty received so far from this effect and action $H$ | $\bar q=Q(\infty)-Q(t-1)$ with $Q(\infty)$ a finite total penalty that this effect yields on action $H$ |
| $I$               | a small finite penalty $Q_0\ll R$                                                                                     | a small finite penalty $Q_0$                                                                            |
Various cases emerge:
1. $R$ is known or not
2. $q$ is known or not
3. $Q(\infty)$ is known or not
4. the number of timesteps $N$
5. $N$ is known or not
6. $Q_0$ is known or not
7. $P(t)$ is known or not
8. the probabilities for all timesteps, $\forall t:p(t)$ are known or not
9. the probabilistic process (with possible hyperparameters $\theta$) that generates $p(t)$, i. e. $p_\theta(t)$ is known or not
I propose that this is the type of game by which we can reason about unexplored and unboundedly grave risk (e. g. from AI). On each potentially disruptive event (e. g. introduction of a revolutionary application or model) multiple individuals and communities decide to take one kind of action:
- $G$ (gamble): lean into using and supporting a technology, which may lead to material gain or the end of economic value (caveat: the material gain is far from constant and the alternative is far from being that drastic)
- $H$ (hard thing): forego the confident expectation of reward from using the technology at the cost of sacrificing resources and labor on safety preparations (caveat: the penalty of lost opportunity in safety preparations may not be integrable, i. e. possibly $Q(t)\rightarrow\infty$)
- $I$ (inaction): lose value by suspending economic activity (caveat: the devaluation is far from constant and inhomogeneous across agents, sectors)
Even with the caveats it may be worth quantitatively analyzing this game for a qualitative picture of the analogue from the real world that we may be interested in.

With this motivation in mind, consider the case of known $R, Q_0$, infinite $N$, unknown $q,\theta$ (but possibly known $p_\theta$). At timestep $t$ (losing the indices) we have a prior $\Theta$ on the value of $\theta$ to estimate $p\approx\tilde p=\max\int_\theta p_\theta\Theta(\theta)\mathrm d\theta$. The expected reward for the actions $A=(G,H,I)$ is thus $(\tilde pR, -\tilde pq-(1-\tilde p)\bar q,-Q_0)$. At each timestep taking $G$ yields the highest expected reward but given $N$ and the integrability of the expected reward for $H$ the discounting scheme sets a time horizon $\tau$ up to which consistently taking $H$ and then switching to $G$ is definitely higher in expected value. More importantly, if $q$ has a finite range, then the probability of not realizing the maximal reward with this switching policy drops to 0 at $T:Q(T)=Q(\infty)$.

**Claims**:
1. An optimizing agent follows the policy involving switching with non-zero probability.
2. If $T<\tau$ then an optimizing agent follows the switching policy with 1 probability.

The value of $\tau$ is the choice of the agent (via the discounting) and $T$ depends on the unknowns $q,\theta$, about which the agent can learn information during the game. 

**Claims**:
1. On the assumption that the agent can indeed learn information on $q,\theta$, i. e. the process yielding $T$ is stationary, the agent has increasing confidence about outcomes in future timesteps.
2. If the previous agent is an optimizer, it has to compute the optimal policy on future events.

**Corollary**: In this game the optimizer implements retroactive causation.

A case can be made that projecting current observed value-based decision theory to estimate future reward is not optimal. This suggests that if this case can be properly formalized in RL, then the optimal policy is approximated in a retrograde fashion starting with the best approximation for the final action. Indeed, prompting in [[back-rl]] suggests that there is some (but scarce) literature supporting this, pointing to a promising research area.

Go to [[information#more on acausality and non-causality]] for more.
### underlining the necessity
self-alignment is expected from a fractional agent for health and that involves resource consumption regulation as in [[theory core#training regimes]] and that involves backchaining and we do it and it works

### underlining observation-limited attribution correction
wrong reward attribution to the tasks you care about, should ref [[outliers#acute misalignment]]? yes and [[theory core#uncertainties in decision-making]]? yes

[^1]: By definition, future rewards. If we assume that the agent makes doesn't change its predictions starting with some future timestep, then this is equivalent to future value estimation for all but finitely many timesteps.
