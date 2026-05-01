# When welfare measurement sets the budget: failure modes, gaming, and the paradox of better data

**whether measurement improvements reduce manipulability rather than merely increase precision.**
- empirical pattern is consistent: direct gaming of well-designed welfare measures is surprisingly rare
- political gaming of the *meta-rules* (formula construction, index weighting, pace-of-change policies) is pervasive
- Frankel-Kartik theoretical framework resolves what initially appears paradoxical — making measurement more consequential can *degrade* its informational value — by showing that [ideas/repec](https://ideas.repec.org/a/oup/jeurec/v20y2022i1p79-115..html), [oxford academic](https://academic.oup.com/jeea/article-abstract/20/1/79/6255435?redirectedFrom=fulltext&login=false) the two-tier structure itself functions as the recommended design: commit to under-utilising manipulable welfare data for fine-grained decisions [arxiv](https://arxiv.org/abs/1908.10330) while delegating detailed allocation to trusted experts.

---

## The NHS weighted capitation apparatus as structural benchmark

England has allocated health funding to local areas 
- now **36 Integrated Care Boards** 
- population health need determines each area's target share of the national budget
- local managers then allocate within that envelope.
- separates funding into components [ncbi](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7511896/) 
	- general and acute, 
	- mental health,
	- maternity,
	- prescribing,
	- primary care,
	- specialised services,
	- community services
- calculation [nhs](https://www.england.nhs.uk/wp-content/uploads/2025/12/allocations-2627-technical-guide-to-formulae-v2.pdf), [uk parliament](https://researchbriefings.files.parliament.uk/documents/CBP-10031/CBP-10031.pdf)
	- starts with registered GP practice population,
	- applies **age-sex cost weights**,
	- an **additional needs index**: deprivation and morbidity
	- **Market Forces Factor** for unavoidable cost variation
	- **Health Inequalities and Unmet Need adjustment** (currently **10%** of core allocation, **15%** of primary care)
- The formula determines each ICB's *target share*

**supply variable sterilisation** 
- general [nhs eng](https://www.england.nhs.uk/wp-content/uploads/2025/02/PRN01601-technical-guide-to-allocation-formulae-and-convergence-for-2025-to-2026-revenue-allocations.pdf)
	- distance to hospital, 
	- provider capacity
	- set to national average values so that areas with historically poor access are not penalised.
- Variables reset to zero on the normative judgment that they represent systematically unmet need rather than genuinely lower need. [hfma](https://www.hfma.org.uk/system/files?file=230703---nhs-allocations-to-icbs---slides.pdf) 


The two-tier trust structure
- The Advisory Committee on Resource Allocation (ACRA), established 1997, [nhs eng](https://www.england.nhs.uk/statistics/wp-content/uploads/2022/04/Update-of-the-general-and-acute-formula-for-2022-23-resource-allocations-final-v2.0.pdf) 
	- GPs,
	- public health experts,
	- NHS managers,
	- academics,
	- finance professionals.
- advises on target shares
- Local ICB leadership then decides how to spend the envelope

---

## Failure modes that measurement improvement alone cannot fix

The NHS formula's documented failures illuminate structural vulnerabilities that recur across all welfare-budget mechanisms.

**The pace-of-change problem is the formula's most consequential failure mode.** 
- under-target ICBs get relatively more and over-target ones relatively less. [uk parl](https://researchbriefings.files.parliament.uk/documents/CBP-10031/CBP-10031.pdf), [hfma-data](https://www.hfma.org.uk/system/files/2025-05/Allocations%20HCF%20June%2025.pdf) [hfma-anal](https://www.hfma.org.uk/articles/closing-gap)
	- As of 2025/26, ICB distances from **5% under-target to nearly 9% over-target** 
	- Surrey Heartlands sits 8.64% above
	- Bedfordshire, Luton and Milton Keynes falls roughly **£100 million short**. 
	- the pace of change is *politically* determined while the formula is *technically* determined — a divergence between formal and informal governance that chronically destabilises the allocation mechanism.

**The utilisation-needs circularity remains unresolved despite fifty years of refinement.**
- Despite supply variable sterilisation, critics including Asthana, Gibson, and Moon (2004, *Social Science & Medicine*) argued: areas that historically had more services appear to have more "need." [sciencedirect](https://www.sciencedirect.com/science/article/abs/pii/S027795360300217X)
- ACRA "understanding what drives utilisation currently gives the best insight into what drives need" — is an explicit pragmatic compromise rather than a technical solution. [hfma](https://www.hfma.org.uk/system/files?file=230703---nhs-allocations-to-icbs---slides.pdf) [nuffield](https://www.nuffieldtrust.org.uk/resource/fairer-funding-for-general-practice-in-england)

Barr et al. (2014, *BMJ*) found **halving** of absolute health inequalities from amenable mortality (from 95 to 54 deaths per 100,000 for males, 2001–2011), with NHS resource increases explaining **85% of the total reduction**. [nuffield](https://www.nuffieldtrust.org.uk/news-item/lesson-4-make-sure-the-funding-follows-the-plan) -- effectiveness is hostage to political choices about the meta-parameters -- poorly justified

---

## The measurement-gaming interaction is non-monotonic and mechanism-dependent
"Improving Information from Manipulable Data" (*JEEA*, 2022) shows the optimal response is to **commit to under-utilising manipulable data** [arxiv](https://arxiv.org/abs/1908.10330)

The Manheim-Garrabrant taxonomy of Goodhart's Law [arxiv](https://arxiv.org/pdf/1803.04585), [MIRI](https://intelligence.org/2018/03/27/categorizing-goodhart/)

- **Regressional Goodhart** (proxy-goal gap at tails): reduced by noise reduction — improvement helps
- **Extremal Goodhart** (model breakdown at extremes): reduced by better specification — improvement helps
- **Causal Goodhart** (intervening on the measure changes the causal structure): reduced by using root-cause measures rather than correlated proxies — improvement helps
- **Adversarial Goodhart** (strategic manipulation by agents with divergent goals): *persists regardless of accuracy* if agents can manipulate inputs — improvement redirects but does not eliminate gaming

Holmström and Milgrom's multitask theory (1991): **partial measurement improvement can amplify distortion**. If welfare has multiple dimensions but only some are measured, improving measurement on those dimensions diverts effort toward them, comprehensive measurement across all relevant dimensions avoids this trap. [duke](https://people.duke.edu/~qc2/BA532/1991%20JLEO%20Holmstrom%20Milgrom.pdf), [theac](https://www.theacpgroup.com/blog/Understanding%20Goodhart%E2%80%99s%20Law%20of%20Metrics)

**In the NHS context, direct gaming of the capitation formula is remarkably limited.**
- This contrasts sharply with payment-by-results, where individual episode coding (upcoding) is directly gameable.
- The formula's reliance on **exogenous, centrally administered data** is its primary anti-gaming defence 
- Ahmad-Thomas (1997) principle from intergovernmental fiscal transfer theory that allocation factors must be independent of recipient government actions.

indirect gaming channels
- GP list inflation through delayed removal of patients who have moved,
- variable diagnostic coding between practices that can affect person-based models.

---

## Formula funding conflicts beyond health: the same architecture, the same fractures

Revenue Support Grant [^1]
- needs-based formulae until 2013 [Sm](https://www.english.sm.dk/media/14349/sarah-ponsford.pdf)
- formula baseline was locked in as part of the transition to business rates retention. **Allocations were frozen for over a decade** [IFG](https://www.instituteforgovernment.org.uk/explainer/local-government-funding-england)
- extreme case of pace-of-change failure (effectively zero).

Multiple Deprivation[^1]
- 2025 "formula bypasses" (£600 million Recovery Grant and floor protections) [gov.uk](https://www.gov.uk/government/publications/local-government-finance-policy-statement-2025-to-2026/local-government-finance-policy-statement-2025-to-2026)
- "the government's subjective judgement." [ifs](https://ifs.org.uk/articles/immediate-response-local-government-finance-policy-statement) 
- 2026/27 settlement delivered spending increases **2.4 times greater** for the most deprived areas versus least deprived, [ifg](https://www.instituteforgovernment.org.uk/explainer/local-government-funding-england)
- formula works directionally even when politically compromised.

**The Free School Meals auto-enrolment[^1]
- measurement improvement can directly increase resource flow.
- Pupil Premium requires FSM registration, but under-registration is substantial — especially in more deprived local authorities, paradoxically. [epo](https://epi.org.uk/publications-and-research/who-has-been-registered-for-free-school-meals-and-pupil-premium-in-the-national-pupil-database/)
- Sheffield pioneered auto-enrolment in 2022, using welfare datasets. By 2024, 74 local governments
- 17 areas with full implementation, reducing a measurement gap rather than gaming *per se*, but it demonstrates that removing friction from welfare measurement can dramatically improve targeting.

**Australia's Commonwealth Grants Commission: intergovernmental transfer formula[^1] 
- Western Australia's GST share fell [springer](https://link.springer.com/chapter/10.1007/978-3-031-53759-2_3) from ~0.72 to ~0.30 of population share (2011–2015, iron ore royalties surged), WA mounted a $1 million public campaign. The Morrison government legislated a GST floor in 2018 WA now receives ~$7.8 billion from GST versus ~$1.7 billion under full equalisation.

Goodhart's Law in UK public spending [hood, piotrowska](https://ora.ox.ac.uk/objects/uuid:e5fe165e-18aa-4d38-b4b3-a24287be19e1/files/sqf85nb34z)
- when spending categories are designated as "desirable" or "undesirable," creative reclassification follows.
- NHS ring-fencing -- reclassify spending to fall within protected categories.
- PFI shifted spending off-balance-sheet.
- The MoD: **35% of a reported transfer was attributed to "accounting changes contrived to show non-cash savings."**
- Their core conclusion: "Creating new spending categories to control public expenditure and limit gaming is a two-edged sword since it itself creates new opportunities for gaming."

---

## Corporate and organisational analogues: implicit trust asymmetries and the rarity of the stronger form

**German Social Plans (Sozialplan)
- if the works council and employer cannot agree, the conciliation board decides on **both the budget of the Social Plan and its distribution** — a direct case where measured worker welfare impact determines budget envelope
- Works Constitution Act (Betriebsverfassungsgesetz) formalises the trust asymmetry: workers have binding codetermination rights on social matters [deutschland](https://www.deutschland.de/en/topic/business/co-determination-in-german-companies-rules-and-laws) (§87), while management retains operational authority. [bbi](https://www.businesslocationcenter.de/en/labor-market/employment-law-and-collective-contracts-system/german-works-council-constitution-act)

**Mondragon
- 2012: ~75,000 worker-members agreed to a 3% salary cut across all cooperatives, worker-assessed crisis driving budget creation through democratic sovereignty. [dr. pop](https://drpop.org/mondragon-what-is-solidarity/)
- welfare body Lagun Aro distributes benefits based on assessed worker need (retirement, invalidity, widowhood). Gaming is disciplined by co-risk-bearing: worker-members who misrepresent need harm their own capital accounts (each member deposits €15,000). [corporate rebels](https://www.corporate-rebels.com/blog/lessons-from-the-mondragon-cooperative-movement) The Social Council mediates an emergent trust asymmetry where workers defer to management expertise for operational decisions while retaining sovereign democratic control over budget envelopes. [mx](https://www.managementexchange.com/story/mondragon-cooperative-experience-humanity-work) [participedia](https://participedia.net/case/82)

**UK Tenant Satisfaction Measures 
- April 2023: registered social housing providers must collect and publish 12 satisfaction measures from tenant perception surveys, 10 from management data.
- The Regulator of Social Housing: identify outliers and trigger interventions. [gov.uk](https://www.gov.uk/government/news/rsh-publishes-analysis-on-tenant-satisfaction-in-the-social-housing-sector)
- Poor TSM results -> regulatory pressure → mandated improvement plans → forced resource reallocation.
- indirect budget-driving mechanism through a regulator acting as a trust intermediary.
- First-year results: regulator "engaging with landlords where it has concerns about the quality of their data" [gov.uk](https://www.gov.uk/government/news/rsh-publishes-analysis-on-tenant-satisfaction-in-the-social-housing-sector) — suggesting measurement-gaming concerns from inception.

**The UK Teaching Excellence Framework
- TEF ratings (based partly on National Student Survey results, retention, and employment outcomes) determine whether universities can charge maximum tuition fees. [ofs](https://www.officeforstudents.org.uk/for-providers/quality-and-standards/about-the-tef/) [cug](https://www.thecompleteuniversityguide.co.uk/student-advice/where-to-study/teaching-excellence-framework-tef)
- welfare measurement → revenue envelope → expert allocation within the institution. 
- gaming response: **student unions organised NSS boycotts in 2017**, [researchgate](https://www.researchgate.net/publication/326400766_The_UK_Teaching_Excellence_Framework_TEF_The_Development_of_a_New_Transparency_Tool) with 12 institutions (including Cambridge and Oxford) achieving insufficient response rates.
- "innovative forms of teaching, which challenge pre-conceptions, often score low student satisfaction ratings despite being highly effective." [researchgate](https://www.researchgate.net/publication/326400766_The_UK_Teaching_Excellence_Framework_TEF_The_Development_of_a_New_Transparency_Tool) This case illustrates Adversarial Goodhart: agents with divergent goals (students wanting to undermine TEF) manipulated the measure directly.

**Formal-informal governance divergence tends to destabilise**
- German codetermination: Where informal practice erodes, the system becomes adversarial.
- Mondragon: the cooperative structure's implicit trust norms have persisted through multiple crises.
- Corporate wellbeing programmes: budgets shift annually based on management priorities with no structural anchoring.

---

## Participatory budgeting: the stronger instantiation exists only in partial form

The Platteau-Gaspart paradox:
- better information about target populations' needs can *increase* elite capture, because elites strategically propose projects that more closely match their own preferences when they know the funder can verify some claims but not all. [sciencedirect](https://www.sciencedirect.com/science/article/abs/pii/S0304387813001454) 
- consistent with Indonesia (Grillos, 2017), where sub-units with more poor people received *smaller* percentages of funding than their population share warranted, [repec](https://ideas.repec.org/a/eee/wdevel/v96y2017icp343-358.html)
- Kenya (Sheely), even when citizen mobilisation was high. [harvarfd](https://www.innovations.harvard.edu/blog/showing-enough-lessons-mobilizing-participatory-budgeting-rural-kenya)

---

## The theoretical resolution: why the two-tier structure is its own best defence

Frankel-Kartik: **commit to under-utilising manipulable data**. [arxiv]([Improving Information from Manipulable Data](https://arxiv.org/pdf/1908.10330)) The optimal policy sensitivity β* is strictly less than both the fixed-point sensitivity and the OLS coefficient. The designer should place *less* weight on the welfare signal than the data would justify, because this attenuates gaming and improves net information quality.

*implementing this optimal design*
- Tier 1: budget a relatively coarse function of welfare measures (low β* — the budget responds to need but not with high sensitivity). 
- Tier 2 delegates fine-grained allocation to trusted experts using richer local information. 
- Because experts are more trusted, the effective stake of their decisions can be higher without triggering Adversarial Goodhart. This interpretation explains
	- the NHS formula more resistant to direct gaming than payment-by-results or performance-based funding: the formula determines a coarse aggregate (area budget share) rather than fine-grained allocations, exactly as the theory recommends.

The Holmström-Milgrom multitask theory:
- **measurement improvement reduces gaming only when it is comprehensive across all welfare dimensions**. Partial improvement can amplify distortion by diverting strategic effort toward newly measured dimensions. 
- The Carr-Hill formula's failure illustrates this: 
	- measures workload but not deprivation, creating systematic underfunding of deprived-area practices. [nuffield](https://www.nuffieldtrust.org.uk/resource/fairer-funding-for-general-practice-in-england) [hfma](https://www.hfma.org.uk/system/files/2024-03/Leicester,%20Leicestershire%20&%20Rutland%20case%20study.pdf)
	- Improving it by adding deprivation variables would reduce one distortion, but only if the variables are genuinely less manipulable than self-reported workload indicators.

The synthesised conditions under which measurement improvement reduces gaming:

- **Reduced manipulability** (using exogenous, centrally administered data rather than self-reports) — the NHS formula's primary strength
- **Greater dimensionality** (measuring all welfare dimensions to prevent effort diversion) — the direction of PBRA's person-level linked data
- **More exogenous indicators** (demographics, geography, administrative records rather than behavioural proxies) — the Ahmad-Thomas principle from fiscal transfer theory
- **Maintained coarseness** of the budget response to measurement, even as measurement precision improves — the Frankel-Kartik optimal sensitivity result
- **Formal institutionalisation** of the trust asymmetry, so that expert allocation authority is protected from political erosion — German codetermination's legal framework versus corporate wellbeing programmes' discretionary instability

The counterintuitive design implication is that the optimal system invests in better measurement but deliberately *underweights* it in the allocation rule. The FSM auto-enrolment case — where improved measurement directly increased resource flow — succeeds precisely because it reduced a *friction* (non-registration) rather than increasing measurement *precision*, thereby operating on manipulability rather than accuracy.

---

## Conclusion: what the comparative evidence reveals


The hypothesis that measurement improvement reduces gaming receives **conditional support**: improvement works when it reduces manipulability or increases dimensionality, but fails when it merely increases precision while making the measure more consequential. The FSM auto-enrolment case (removing friction → £82 million additional funding nationally) [pubmed](https://pmc.ncbi.nlm.nih.gov/articles/PMC7617560/) and the NHS shift from area-based to person-based models (reducing ecological fallacy) are positive cases. The Australian GST floor (measurement excellence overwhelmed by political force) and the TEF NSS boycotts (measurement improvement provoking adversarial strategic responses) [researchgate](https://www.researchgate.net/publication/326400766_The_UK_Teaching_Excellence_Framework_TEF_The_Development_of_a_New_Transparency_Tool) are negative cases. The Frankel-Kartik paradox — that more consequential measurement degrades its informational value — explains both patterns and points toward the design principle that the most robust welfare-budget mechanisms are those that invest heavily in measurement quality while deliberately constraining how aggressively the budget responds to measured welfare.

The two-tier welfare-budget structure is **theoretically well-justified** by the Frankel-Kartik framework as an optimal mechanism design response to manipulable welfare data, but its practical resilience depends on institutional features that existing theory underspecifies — particularly the legal entrenchment of the trust asymmetry and the pace-of-change policy. Germany's codetermination law and Mondragon's cooperative constitution provide structural stability that discretionary corporate wellness programmes and politically contingent PB systems lack.

[^1]: This example fails on the criterion that the expert group should have a direct effect on their allocated budget based on their decision, unless an illegal, corrupt policy is followed by the respective institutions.
