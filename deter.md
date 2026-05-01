In a view agnostic of whether a set of agents is natural or artificial, the specific challenge in alignment that we wish to address looks like this
- deterrence or obstruction of accessing necessary (non-AI) resources for an activity, imposed on subset B of agents by subset A of agents, if A suffers consequences of it
- put more concretely, cooperation of A and B to be ensured
	- B: a more trusted group tasked with solving a complex problem
	- A: a less trusted group whose own perception of well-being determines the amount of resources the trusted group may use.
- possible but definitely secondary normative priority is optimality of the technical solution
Perplexity content:
>A stylised way to capture the situation is as follows.
>- Citizens each have a perceived well-being level $w_i$ or a preference ranking $\succ_i$ over outcomes (or projects), which they can report.
>- A social or institutional rule aggregates these perceptions into a resource level $R = g((w_i)_i)$ or into a budget constraint $B = g((\succ_i)_i)$.
>- Experts observe $R$ or $B$ and then choose an action or allocation $x$ in a feasible set $X(R)$ that reflects technical, legal, or physical constraints.
>- The quality of $x$ according to some efficiency criterion (e.g. cost-effectiveness, aggregate output) is not lexicographically prior; the key requirement is that $R$ or $B$ is determined by the citizens’ perceived needs or welfare.

### preexisting examples and failure modes in particular

Many real-world institutions can be understood as instantiations of this template. Let's investigate them following this blueprint
1. collecting the examples
	1. critically analyzing their fit to the model
	2. collecting policy disfunction cases
	3. statistically analyzing frequency and severity (only)
2. selecting prominent shortcomings
3. specifying the model to quantify them
The intended outcome is that we can formulate them according to the network specifications in [[theory core]].

The examples are (shortened, edited versions of LLM artifacts) in [[research-0]], awaiting review in [[research-1]] and [[research-2]]. These are interim results roughly at the 1.1. sage, and work is in progress on refining them, see the unedited artifact [[research-0.1]].

An even stronger and strongly-held assumption here is that the social structures described therein translate readily to the same dynamics involving AI experts.

### inherent alignment of RL-performing fractional agent constituents
AI-specific key observations
- there is a collective human decision to involve AI into the economy
- existential reward, cf. [[scale-free]], connects to the livelihoods of humans whose lifestyle and living space interfaces robustly with AI
- opportunity in AI is to collectively steer its development in the direction where at the level of human involvement reward is artificially deflated
	- e. g. for the _same end state_, higher reward is given if human involvement is less extensive and more indirect throughout a series of actions
	- interchangeability of natural and artificial quality means humans should be dissuaded from solving a task with AI if it can be done without -- e. g. create virtual credit score for how essential your AI-use is, and require this credit for later access to it

Supporting claim: fractional agent can be designed so that
- it has a better internal model of its environment than most (or any) of its constituents
- it can simulate its actions and the environment and minimize its resource needs or damages
- it pursues convergent instrumental goals, notably self-preservation
- constituents get to control their well-being 
- they supply each other with vital resources

Main claim: if the design in the supporting claim persists (approximately) over many fractional agent definitions, alignment is achieved.

See also [[theory core#Work in progress as of last update]] and [[causality in RL]].

### within aligned training regime
See [[theory core#training regimes]] for training regime definition.

(is this even important?)