### Turning concerns with autonomous machines into operational relief
Continuous alignment comes in many forms and the essence of the idea is to keep finding opportunities for identifying them in different application areas. To both illustrate that and seed execution of exemplary agendas for it, this repo documents several closely connected research activities following this pattern:
- An AI risk can be identified in this shape
	- Some resource is being committed to ML of a model that performs impressively enough to be perceived advantageous over alternatives. [^2] [^3]
	- Evaluators identify a specific task (or class of tasks) that are conducive to harming living beings and attempt to use the trained model efficiently for that.
	- They succeed, and they (or others) may suggest measures to prevent the effectiveness of the released model on that task.
- Crucially, note that at least one of these lacks guarantees:
	- the adoption of these measures, 
	- their predisposition to circumvention
	- the scope of the dangerous tasks covered by them being significant among all possibilities.
- From a security perspective this amounts to a failure to prevent an AI-enabled dangerous activity, the only remaining improvements to the situation are:
	- deterrence from the specific dangerous activity or obstruction of accessing necessary (non-AI) resources for it
	- infrastructure to be able to locate and defuse the activity as someone makes preparations for it
- Suppose (however rudimentary) an existing theoretic framework that can describe the context and the activity _equivalently_ whether 0, 1 or more AI instances interact, and investigate some of its predictions in the 0 AI case.[^4]
- Make the specific difference in outcome for the $\neq0$ AI case quantitative.
- Iterate.
This is intended to establish an engineering approach to the 2 highlighted security improvements that aims to dimension them and refine them, as well as the underlying theory simultaneously over iterations.[^5][^6][^7] During the process, LLM's should be intentionally leveraged and regular reflection on methods, especially in AI use, practiced.

The rest of the content of the repo belongs to examples of the research pattern, i. e. continuous alignment, in use.
### A possible entry point for reading
I want this repo to go through 3 very fuzzily distinguishable stages
1. collection philosophical, conceptual texts, mathematical notations, programming infrastructure choices; with many links to guide reading in a non-linear way[^8]
2. appearance of actionable points, phrased as prompts; encouraged interaction from readers is to tweak them until response from LLM's seems genuinely helpful
3. a self-modifying application with increasingly more complex and higher impact features; it has to contain guidelines to social experiments to test their features (here reader engagement is external to the product)

The main normative is to be concise, precise, evocative, interesting and time-consuming, even if only for a specific type of reader.

Beware that the text is intentionally trying to use an everyday linguistic style but not such vocabulary, and some jargon is chosen after very thorough deliberation to be consistent and connective to quantitative science\! To be informed about the lingo, see the [glossary](3.md) (“quotation”, unless clearly used differently, marks an entry in the glossary).

[[theory core]] lays out the basics of the current, better informed version. Clicking through inline links all named (as in not numbered) files may momentarily not be possible, you're welcome to look at the file tree to see everything.

To go through the remains of an early version, go to the [summary](4.md).
### Status
a read-through is timely to remove old and unclear or plain wrong bits
files to work on (immediately: checked, near-term: unchecked)
- [ ] [[deter]]
- [ ] [[defuse]]
- [ ] [[theory core]]
- [x] [[scale-free]]
- [ ] [[information]]
- [ ] [[22]]
- [x] [[12]]
- [ ] [[collapse]]
- [ ] [[embedding autonomous machines]]
- [x] [[outliers]]
- [x] [[causality in RL]]
### Calling for collaboration
These days, although I have prepared notes, I have little time to write them down properly, I'm happy to be contacted about them anyway. 

[^2]: Advantage is defined as: constrained by a budget allocation bracket to the class of tasks to carry out, which model is expected to consume the least in preference-weighted collateral cost, also discounting opportunities.

[^3]: This is a vague definition, but concrete enough to expose that class-specific expectation and opportunity discounting formulae are unreliable due to a low consensus on usage best practices and narrow capabilities status and projections.

[^4]: Also, for a more fruitful investigation, the class of dangerous activities can be relaxed.

[^5]: The validation of the model for the AI case need not come from experiment, it can be simulated or analytically derived if the quantitative difference of introducing AI is well understood in the theory.

[^6]: The cases and theories should come from a diverse set of fields, as we shall see, the gamut from social sciences through natural sciences to mathematics and liberal arts is all relevant.

[^7]: The optimistic position that the relevant theory has actually been discovered is assumed throughout.

[^8]: Can a wiki be a good format?
