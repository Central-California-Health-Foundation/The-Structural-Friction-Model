# CCHF Framework Proposal: The Structural Friction Model: Inferring latent health volition and threshold-dependent behavioral collapse under structurally produced environmental constraints.

**Thesis:** We propose a mechanistic model that reconciles individual agency with structural constraints, revealing threshold-dependent behavioral collapse under high environmental friction.

---

## I. Significance: The Methodological Gap
Behavioral epidemiology faces a methodological bottleneck: across the field, researchers routinely commit the ecological fallacy [1], a flaw whose consequences are acute in regions like the Central Valley, where our Structural Friction Model offers a novel resolution. Researchers often map area-level proxies, like ZIP code aggregates, directly onto individual biological risk [2]. This assumes uniform deprivation and ignores intra-zonal mobility, confounding individual-level composition with environmental context [3] and obscuring the proximal mechanisms linking structural neglect to disease [2].

Current community assessments treat "perceived control" as a one-to-one proxy for objective capacity. This forces a reliance on retrospective inference, rendering these assessments predictive failures for establishing causal drivers. Consider local data: 55.0% of Fresno County respondents cite a "Lack of Access to Health Services" (Source: Fresno-EOC-CNA-Executive-Summary.pdf). This is rarely a verified physical impossibility; rather, it is a psychological perception filtered heavily through environmental cost. As noted in the literature, "access" frequently reduces to intertemporal utility optimization rather than simple geographic presence [6, 7].

---

## II. Volition as a Latent Construct
Escaping the "self-report fallacy" requires acknowledging the cognitive realities of agency without collapsing into behavioral determinism. Cognitive science demonstrates that even under severe structural coercion, individuals preserve a fundamental sense of agency [8]. Importantly, intrinsic motivation and immediate reward-seeking operate via distinct neural pathways [9].

The implication is critical: the **Intrinsic Capacity** for health adherence (conceptually aligned herein with **Latent Cognitive-Behavioral Capacity**) does not vanish in adverse conditions. Instead, **Structural Friction** actively exhausts the cognitive bandwidth and economic resources required to execute that agency. 

Capturing voluntary movements in an "ecologically relevant state" is notoriously difficult [2]. Consequently, laboratory proxies like "intentional binding" fall short [2, 10]. They simply lack the ecological validity to account for grinding, real-world environmental resistance. Individual non-compliance in the Central Valley is not a deficit of "grit." It is the probabilistically constrained outcome of high **Structural Friction** [7]. 

Volition cannot be directly observed. Instead, we infer it through constrained behavioral expression. When the environmental cost of adherence rises, adherence probability drops according to a threshold-dependent function [7]. The environment fundamentally fails to support the cognitive mechanisms of volition [2, 8, 11]. Treating "lifestyle choices" as an isolated independent variable is conceptually incomplete [4]. It ignores the relentless economic constraints dictating intertemporal utility [7].

---

## III. The Structural Friction Model
Unlike static Social Determinants of Health (SDOH) models, the **Structural Friction Model** mechanistically quantifies the dynamic *cost* of navigating environmental conditions.

We operationalize behavioral capacity as a dynamic probability $P(\text{adherence})$ using a logistic model with an interaction term:

$$P(\text{adherence}) = \frac{1}{1 + e^{-(\beta_0 + \beta_1 V_i - \beta_2 F_s - \beta_3(V_i \times F_s))}}$$

**Variable Definitions:**
* **$\beta_0$**: Baseline log-odds of adherence.
* **$\beta_1 V_i$**: The positive marginal effect of baseline individual volition ($V_i$).
* **$\beta_2 F_s$**: The direct suppressive penalty of **Structural Friction**.
* **$\beta_3(V_i \times F_s)$**: The critical interaction effect—the rate at which environmental friction modulates and suppresses the efficacy of individual agency.

This methodology allows for the precise identification of **threshold conditions**. Under low friction, behavioral variance directly reflects individual volition ($V_i$). However, as friction crosses a critical threshold, the interaction effect dominates, variance compresses, and the marginal influence of individual volition becomes statistically negligible.

---

## IV. Testable Propositions for Falsifiability
1.  **The Variance Suppression Hypothesis:** High **Structural Friction** ($F_s$) actively suppresses the behavioral expression of **Intrinsic Capacity** ($V_i$). Therefore, objective health adherence in high-friction populations will exhibit statistically lower variance than in low-friction cohorts.
2.  **The Structural Release Hypothesis:** Exogenously reducing $F_s$ (e.g., providing unconditional transit vouchers) in a high-friction group will trigger rapid, non-linear adherence improvements. No concurrent behavioral intervention is required; the previously suppressed $V_i$ simply emerges as opportunity increases.

---

## V. Empirical Testbed: The Central Valley
The Central Valley provides an ideal testbed where systemic constraints operate at the extremes of the population distribution:
* **Financial & Infrastructure Friction:** A 19.0% poverty rate meets 176 identified Health Professional Shortage Areas (HPSAs). The care-seeking environment is highly resistant (Source: Fresno-EOC-CNA-Executive-Summary.pdf).
* **The Collapse of Volition:** Kern County reports "Deaths of Despair" at rates exceeding the national average by more than 50% (Source: CentralValleyHealthEquityReport.pdf). This marks the tipping point where **Structural Friction** overrides **Intrinsic Capacity**.
* **Safety as Friction:** Residents prioritize safety (36.0%) and peace (32.0%) as primary components of $F_s$, actively suppressing feasible health behaviors (Source: Fresno-EOC-CNA-Executive-Summary.pdf).

---

## VI. Significance & Policy Implications
Shifting the intervention locus from the individual to the environment provides a quantifiable mandate for policy reform. Educational interventions in high-friction environments are mathematically constrained from reaching optimal outcomes. High cognitive load and resource exhaustion make this limitation inevitable.

Public health capital requires redirection toward structural subsidies—localized food systems, transit integration, and direct economic relief. By targeting the *cost* of adherence [7], we move past the moralization of "lifestyle choices." Public health becomes the engineering of structural support for latent human will.

***

## Strictly Cited References
1. W. S. Robinson (1950). Ecological Correlations and the Behavior of Individuals. *American Sociological Review*. https://doi.org/10.2307/2087176

2. Zihao Yi, Masoud Khani, Mohammad Assadi Shalmani, Amirsajjad Taleban, Jennifer T. Fink, Robert F. Frediani, Jake Luo (2026). From food deserts to nutritional equity: exposing socioeconomic drivers of hypertension. *Journal of Nutritional Science*. https://doi.org/10.1017/jns.2025.10067

3. Abba, M., Nduka, C., Anjorin, S., Mohamed, S., Agogo, E., Uthman, O. (2021). Influence of contextual socioeconomic position on hypertension risk in low- and middle-income countries: disentangling context from composition. *BMC Public Health*. https://doi.org/10.1186/s12889-021-12238-x

4. Fielder, J. C.; Shi, J.; McGlade, D.; Huys, Q. J.; Steinbeis, N. (2024). Sense of control buffers against stress. *biorxiv*. https://doi.org/10.1101/2024.12.05.626945

5. Valérian Chambon, Nura Sidarus, Patrick Haggard (2014). From action intentions to action effects: how does the sense of agency come about?. *Frontiers in Human Neuroscience*. https://doi.org/10.3389/fnhum.2014.00320

6. Damen, T., Müller, B., van Baaren, R., Dijksterhuis, A. (2015). Re-Examining the Agentic Shift: The Sense of Agency Influences the Effectiveness of (Self)Persuasion. *PLoS ONE*. https://doi.org/10.1371/journal.pone.0128635

7. Klaus Mann, Michael Möcker, Joachim Grosser (2019). Adherence to long-term prophylactic treatment: microeconomic analysis of patients’ behavior and the impact of financial incentives. *Health Economics Review*. https://doi.org/10.1186/s13561-019-0222-1

8. Emilie A. Caspar, Frederike Beyer, Axel Cleeremans, Patrick Haggard (2021). The obedient mind and the volitional brain: A neural basis for preserved sense of agency and sense of responsibility under coercion. *PLoS ONE*. https://doi.org/10.1371/journal.pone.0258884

9. Irene Valori, Laura Carnevali, Giulia Mantovani, Teresa Farroni (2022). Motivation from Agency and Reward in Typical Development and Autism: Narrative Review of Behavioral and Neural Evidence. *Brain Sciences*. https://doi.org/10.3390/brainsci12101411

10. Marika Mariano, Nicole Kuster, Matilde Tartufoli, Laura Zapparoli (2024). How aging shapes our sense of agency. *Psychonomic Bulletin & Review*. https://doi.org/10.3758/s13423-023-02449-1

11. Kelsey Perrykkad, Rebecca P. Lawson, Sharna Jamadar, Jakob Hohwy (2021). The effect of uncertainty on prediction error in the action perception loop. *Cognition*. https://doi.org/10.1016/j.cognition.2021.104598

12. Imaizumi, S.; Tanno, Y.; Imamizu, H. (2018). Compress global, dilate local: Intentional binding in action-outcome alternations. *biorxiv*. https://doi.org/10.1101/507582

13. Takumi Tanaka (2024). Evaluating the Bayesian causal inference model of intentional binding through computational modeling. *Scientific Reports*. https://doi.org/10.1038/s41598-024-53071-7

14. Leah L Zullig, Dan V Blalock, Samantha Dougherty, Rochelle Henderson, Carolyn C Ha, Megan M Oakes, Hayden B Bosworth (2018). The new landscape of medication adherence improvement: where population health science meets precision medicine. *Patient preference and adherence*. https://doi.org/10.2147/PPA.S165404
