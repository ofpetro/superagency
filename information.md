to critique, select and synthesize multiple ideas
- negative log-likelihood $i$ seems equivalent to probability as a starting point to build (an) information theory:
	- $p=\exp(-i), H=ip$ etc.
	- we wish to capture that these are problems:
		- the notion of probability assumes an universal or potentially omniscient view on events, esp. over the time horizon
		- time-ordering-dependent probabilities are cumbersome in quantum systems
		- the notion of conditioning and time ordering stick together
	- the envisioned solution enriches inference to include time-ordering-free sequential steps, e. g. "near-future predictions based on certainty about far-future events"
- $p$ may be natural for simple systems like elementary particles, but only $i$ can be such for complex, e. g. cognitive systems
- in "perceptive" systems, events and perceptions become interdependent
	- the gesture is that e. g. neurons, sensitive single-particle detectors etc. enter a dynamical regime, or a transient state, in which they lose sensitivity
	- abstractly: in systems with instantaneous interactions $i$ evolves towards an equilibrium, and quick succession of possible interactions with different objects is appropriately described by an evolving out-of-equilibrium model
- some series of events can have wildly varying $i$ not just in time ordering but actual time differences between them
- unclear whether the entropy of high-information-density simple systems and low-info-density ensembles should be identically defined (AFAIK there's only a large ensemble correspondence)
- causality needs to be eliminated from models with many variables but "influence" may give a good intuition
more on acausality and non-causality
- optimizing a policy for a reward is an example where repetitive and reliable reward assignment is crucial, and the optimization process builds (as in stepwise gradually increases in accuracy of) the actions -- or program generating the actions -- of the approximate optimal policy _backwards in time_
- probably this is the only order in which accurate credit assignment is feasible
- (possible nonsense alert: attempting to formalize "near-future predictions based on certainty about far-future events" here) if some constraints are known on the hypothesis class and there is strong evidence for bayesian update, then actions to be taken and new hypothesis to be selected (+ possibly prior to be updated) become deterministic (at least highly constrained in distribution) so there is an indirect prediction that could be built into the prior to make better predictions 