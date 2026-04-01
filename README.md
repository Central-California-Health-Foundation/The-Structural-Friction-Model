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

## III. The Structural Friction Model (SFM)
Unlike static Social Determinants of Health (SDOH) models, the **Structural Friction Model** mechanistically quantifies the dynamic *cost* of navigating environmental conditions.

### 3.1 The Moderated Probability Model
We operationalize behavioral capacity as a dynamic probability $P(\text{adherence})$ using a logistic model with an interaction term to account for non-linear behavioral collapse:

$$P(A)_{is} = \frac{1}{1 + e^{-(\beta_0 + \beta_1 V_i - \beta_2 F_s - \beta_3(V_i \cdot F_s))}}$$

### 3.2 Defining the Weighted Friction Index
**Structural Friction** ($F_s$) is not treated as a monolithic variable, but as a composite index of environmental barriers weighted by regional relevance ($\omega$):

$$F_s = \sum_{k=1}^{n} \omega_k C_k = (\omega_1 \cdot \text{Cost}_{\text{financial}} + \omega_2 \cdot \text{Cost}_{\text{temporal}} + \omega_3 \cdot \text{Cost}_{\text{safety}})$$

### 3.3 Variable Definitions and Functional Roles
* **$\beta_0$**: **The Baseline.** Represents the baseline log-odds of adherence in a zero-friction vacuum.
* **$\beta_1 V_i$**: **The Intrinsic Engine.** The positive marginal effect of baseline individual volition.
* **$\beta_2 F_s$**: **The Environmental Brake.** The direct suppressive penalty of environmental costs.
* **$\beta_3(V_i \cdot F_s)$**: **The Critical Interaction.** The rate at which environmental friction modulates and suppresses the efficacy of individual agency. This represents the **Cognitive Exhaustion Threshold**.

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

Public health capital requires massive redirection toward structural subsidies—localized food systems, transit integration, and direct economic relief. By targeting the *cost* of adherence [7], we move past the moralization of "lifestyle choices." Public health becomes the engineering of structural support for latent human will.

***

## Strictly Cited References
1. Robinson, W. S. (1950). Ecological Correlations and the Behavior of Individuals. *American Sociological Review*.
2. Yi, Z., et al. (2026). From food deserts to nutritional equity: exposing socioeconomic drivers of hypertension. *Journal of Nutritional Science*.
3. Abba, M., et al. (2021). Influence of contextual socioeconomic position on hypertension risk. *BMC Public Health*.
4. Fielder, J. C., et al. (2024). Sense of control buffers against stress. *biorxiv*.
5. Chambon, V., et al. (2014). From action intentions to action effects. *Frontiers in Human Neuroscience*.
6. Damen, T., et al. (2015). Re-Examining the Agentic Shift. *PLoS ONE*.
7. Mann, K., et al. (2019). Adherence to long-term prophylactic treatment: microeconomic analysis. *Health Economics Review*.
8. Caspar, E. A., et al. (2021). The obedient mind and the volitional brain. *PLoS ONE*.
9. Valori, I., et al. (2022). Motivation from Agency and Reward. *Brain Sciences*.
10. Mariano, M., et al. (2024). How aging shapes our sense of agency. *Psychonomic Bulletin & Review*.
11. Perrykkad, K., et al. (2021). The effect of uncertainty on prediction error. *Cognition*.
12. Imaizumi, S., et al. (2018). Compress global, dilate local: Intentional binding. *biorxiv*.
13. Tanaka, T. (2024). Evaluating the Bayesian causal inference model of intentional binding. *Scientific Reports*.
14. Zullig, L. L., et al. (2018). The new landscape of medication adherence improvement. *Patient preference and adherence*.
