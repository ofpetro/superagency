 Keywords that should guide attention (cf. Iliad curriculum...), look these up and:
- high leverage points
- high entropy, low mutual information points
- ergodicity
- point permutation
- edge of stability
- phase transitions, susceptibilities
- quantum state identification
awareness of situation at the edge of aligned training?
- the idea that any outlier is likely in the mode of another possibly unknown distribution leads us to think that specialization for relaying responsibility is vital
- so is limit recognition as in "my policy has performed sub-optimally in this situation, deflect from training trajectory"
- susceptibilities + systemic shifts == overhang + criticality == sudden great disruption by noise, are these metastable regions in the loss landscape
- how does this translate to extra-agentic level? design & execute simulations
- address near-pt susceptibility that defeats the applicability of stats
- train to detect outliers in deployment by detecting them in training
- the interesting thing about susceptibilities being understood in some way is that in network science they have a rich theory history
- is there "de-seeding" in pt?
- ID where potential outcomes are defined by implicitly lumping together potentially independently-evaluated criteria
- if a component is unknown then the knowledge of other components sticks to it & is converted to uncertainty
- this can be alleviated by re-specifying without the unknowns
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
(2) here you go

1. a qualitative distinction of policies that is not specified prior to testing, e. g. 
2. undesirable and unpredicted behavior of a specific agent
3. a training setup that is prone to create #2
4. (a combination of) evaluation and training that exposes #2 and/or #3
5. the expectation that #4 is a generic property of ML independent of specific models
6. the self-reinforcing cultural prevalence (meme) of #5
7. the broader cultural context in which #6 is closely related to evil
### Must learn reward learning x info theory
