There's a dual purpose to this document: establishing a fitting language to draw inspiration from philosophy for a descriptive theory of agent populations; create such a theory that is also quantitative, so it both successfully guides intuition and informs engineering.
### An alternative to the agent foundations framework

This section is deliberately philosophical, can be skipped for more mathematical rigor.

The value of action is a crucial question to be decided. It is a question related to
* economy: in what ways is value created in the economy?[^1] how can its dependence on material vs perceived attributes be quantified?[^2]
* ethics: this decision is inherently ethical, and if the object-level decision can be generalized as a normative, then moral.
Attempts at both quantification and generalization point towards an utilitarianist paradigm of agency. Also, we can promptly arrive at the conclusion that anything fitting the agent foundations framework necessarily takes on the responsibility of realizing those interactions of the environment with it which optimize what it perceives as higher (material or psychological) value.

Does this need to be the case? In particular, can a population that is a mixture of EUM's and unpredictable, preference-denying actors be more likely to thrive than an all-EUM one? If we assume the EUM's to be embedded in the same environment during training and deployment then any internal value function it has is incomplete, and the environment's participation in the process comes with accepting that there will be (material or psychological) effect on it by the agent. That effect, having originated from an imprecise approximative value function for the principal's intended one, will be perceived as suboptimal from the principal's perspective. The principal being part of the environment suffers these effects but also reconsiders training methods and goals.

The principal must accept (possibly a combination of) 2 situations:
1. the meta-level training interaction keeps ongoing[^3] and training (side-)effects keep increasing potentially proportionally in impact with capabilities
2. the training is accepted as complete at some point and will no longer adapt to shifts in the principal's updated knowledge of how it wants to use the agent.

We aim to investigate
1. can agents be non-EUM's, or only principals?
2. how do the effects hinted at above (propagating in the population) influence the population's fitness?
3. what is the difference between fitness and thriving? (is there one?)
### Resourceful agents

I want a working definition for an agent that is expected to discover communication channels towards the environment[^4], this will be "resourceful agent". To express hierarchy, I'll call another agent responsible for keeping the interaction of a specific resourceful agent $Q$ ongoing a principal $P$, itself a resourceful agent. From AIS's perspective the accurate picture contains a (human) $P$ that shares part of the environment, $E_S$ with $Q$.

My hypotheses to test:
- from $Q$'s perspective: environment $E_Q$ "embeds" $P$, with $E_P$ being its environment, $P$ "maintains a model of" $(E_P\setminus E_S)\triangleq D$ or a "principal part" of the environment; importantly the relations in quotation marks mean a possibility of resource and/or information flow that can be bidirectionally defined and do not mean containment or isolation
- compressed information goes from $D$ to $Q$
- and back, too
- $P$ has an estimate of the loss function that $Q$ optimizes for (again, slightly less importantly, we used to consider an accurate human-fed reward function and an inaccurate agent-internal reward model, which is flipped here!)
An important question to formalize: how is this estimate catastrophically erroneous? Of interest are classical misaligned behavior patterns like reward misspecification / gaming, goal misgeneralization etc. But, importantly
- here these are treated information theoretically without the need for the containment hierarchy of agents and environments
- communication channels suggest boundaries to divide agent and environment by, but these are expected to be ambiguous, polymorphic and/or unrecognized, as to be made more precise in [[theory core]] 
### Remarks about alignment
Inner and outer alignment
- In the present view, the agent in training is at least indirectly interacting with the principal as part of its environment from initialization.
- Information about the distinction of the 2 can (can we prove if it will?) be used to improve the agent policy.
- If that happens, the agent recognizes that it has the principal as another agent that it can train as part of its policy optimization
- There is no moment of distinction, recognition or starting to train the principal, in order to establish these, episodes that can be described as all 3 need to happen (and generate reward for the agent) first in an apparently unexpected way
- Note that with agents, principals, and resourceful agents in general we aim to account for ensembles thereof, too, as hinted at in [[collapse]]
[^1]:  For Marx, too, this is a starting point of inquiry. Most of the last >200 years of economic theory has been primarily informed by that body work. (It should be connected to the present work later.)

[^2]: I have not yet seen such a question reassuringly answered related to NFT's yet (as an illustrative example).

[^3]: I. e. the type of agent, if not the same agent, is repeatedly trained with an iteratively improved training method, and the update in iteration is determined by the principal's perceived value of the training success.

[^4]: Additionally, use those to model the environment as in https://arxiv.org/abs/2506.01622
