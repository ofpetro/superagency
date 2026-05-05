build on any result from [[online data preprocessing]] that elucidates _the principles and limits_ of effective outlier detection
### acute misalignment
decision making uncertainty def
let's just see a simple stat effect: you have sg like a bandwidth limit due to 
- sampling
- sensitivity
you also have noise
you have a basis of functions to create a best fit with
would a trained model correctly find simplest fitting function if it requires extrapolating with very high error to unobserved region? 
is this how no free lunch theorems are "violated"?
toy model: with the purpose to illustrate [[theory core#uncertainties in decision-making]]
- [ ] we want to solve a problem with any kind of learning: fit a smooth function to D(x)=sin(e(x)/x) where e(x) is low-frequency noise, the error is i=(g(x-x_0)|f(x)-D(x))|x with standard inner product over x and g bell-shaped function centered at an unknown x_0
- [ ] sampling is limited by shannon-nyquist which is circumvented by composability

### No current quantification or qualificaton
of misalignment (1) because
- [ ] misunderstanding geometry of polynomials, or basis functions in general
- [ ] fractal structure?
- [ ] ai still remains a stat tool that can't capture single, almost-outlier-but-not-quite, high-information encoding specific processes

2. Recall how representation of [concepts](10.md) is sought in AI but the current best attempt at it in humans using quantum probability theory is yet to be applied to that, in addition it is proven that the estimation of quantum states with the lowest expected error is with one that reproduces measurements to the observation level and has the highest entropy beyond that, hinting that the best conceptual interpretation of agent state may be expressed using observation levels and estimating *the maximal entropy over concepts not probed for.*  
	1. Informally that hypothesis states that the new piece of information we gain in conceptually interpreting the agent state is the most unexpected, therefore if some assumption of integrity of the *external* world model is correct, then some corresponding concept acquisition[^18] should necessitate a far-reaching update to the incomplete internal world model.  
	2. Natural language does poorly at encoding concepts but well at frames, which is what LM’s are being optimized for, and it has been shown that this produces some capabilities in predicting true statements in a formal system intended to capture concepts.[^19]  
	3. If agents have acquired different concepts (or structured them differently) and they are being conceptually interpreted, possibly by each other, in the more detail their concepts are compared, the likelier it is to find misalignment (this is an effective way to elicit human conflict, even using natural language).   
(2) here you go

3. a qualitative distinction of policies that is not specified prior to testing, e. g. 
4. undesirable and unpredicted behavior of a specific agent
5. a training setup that is prone to create #2
6. (a combination of) evaluation and training that exposes #2 and/or #3
7. the expectation that #4 is a generic property of ML independent of specific models
8. the self-reinforcing cultural prevalence (meme) of #5
9. the broader cultural context in which #6 is closely related to evil
### Must learn reward learning x info theory
