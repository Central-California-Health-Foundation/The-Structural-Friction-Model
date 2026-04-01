# CCHF Framework Proposal: The Structural Friction Model (SFM)
**Thesis:** We propose a mechanistic extension to Social Determinants of Health (SDOH) that reconciles individual agency with structural constraints, identifying threshold-dependent behavioral collapse via a moderated probability model.

---

## I. Significance: Addressing the Ecological Bottleneck
Behavioral epidemiology frequently encounters a methodological bottleneck: the routine application of the ecological fallacy [1]. Mapping area-level proxies (e.g., ZIP code aggregates) directly onto individual biological risk assumes uniform deprivation and ignores intra-zonal mobility [2]. This approach often confounds individual-level composition with environmental context [3], potentially obscuring the proximal mechanisms linking structural neglect to disease [2].

The SFM serves as a **complementary mechanistic framework** to existing SDOH paradigms. While SDOH describes environmental conditions, the SFM seeks to quantify the dynamic *cost* of navigating those conditions. We move beyond subjective "perceived access" to model health behavior as a behavioral-economic function of **intertemporal utility optimization** [6, 7].

---

## II. Volition as a Latent Construct
Cognitive science demonstrates that even under severe structural coercion, individuals often preserve a sense of agency [8]. We define **Intrinsic Capacity** ($V_i$) as the latent psychological and cognitive drive for health adherence. 


In adverse conditions, we hypothesize that **Structural Friction** ($F_s$)—the sum of financial, temporal, and safety costs—actively exhausts the cognitive bandwidth required to execute this capacity. We posit that individual non-compliance is often a probabilistically constrained outcome of high $F_s$ [7]. In this model, volition is not "lost," but its behavioral expression is suppressed. As environmental costs rise, the probability of adherence follows a threshold-dependent function, where the environment fails to support the necessary cognitive mechanisms for action [2, 8, 11].

---

## III. The Moderated Probability Model (SFM)
We operationalize behavioral capacity as a dynamic probability $P(\text{adherence})$ using a logistic model. Crucially, we include an **interaction term** to test for non-linear behavioral collapse:

$$P(A)_{is} = \frac{1}{1 + e^{-(\beta_0 + \beta_1 V_i - \beta_2 F_s - \beta_3(V_i \cdot F_s))}}$$

### 3.1 Identification of Variables
* **$\beta_1 V_i$ (Intrinsic Engine):** The marginal effect of baseline motivation.
* **$\beta_2 F_s$ (Environmental Brake):** The direct suppressive penalty of structural barriers.
* **$\beta_3(V_i \cdot F_s)$ (The Exhaustion Threshold):** The interaction effect. We hypothesize that as $F_s$ increases, the marginal utility of $V_i$ decreases, representing the point of **cognitive/economic exhaustion**.

---

## IV. Measurement & Identification Strategy
To ensure the SFM is operationalizable and falsifiable, we propose the following measurement proxies:

### 4.1 Estimating Latent Intrinsic Capacity ($V_i$)
Since $V_i$ cannot be directly observed, we propose two primary inference strategies:
* **Revealed Preference:** Measuring adherence variance in "Low-Friction" control cohorts (where $F_s \approx 0$) to establish a baseline distribution of $V_i$.
* **Behavioral Rebound:** Measuring the non-linear improvement in adherence following a discrete reduction in $F_s$ (e.g., a transit subsidy). The magnitude of the rebound serves as a proxy for the previously suppressed $V_i$.

### 4.2 Quantifying Structural Friction ($F_s$)
$F_s$ is operationalized as a weighted composite index ($F_s = \sum \omega_k C_k$) utilizing spatial and socioeconomic data:
* **Temporal Cost ($C_{temp}$):** GIS-modeled travel time to health/food hubs via public transit.
* **Financial Cost ($C_{fin}$):** Out-of-pocket costs relative to localized median household income.
* **Safety Cost ($C_{safe}$):** Standardized crime and perceived safety indices within the individual’s transit buffer.

---

## V. Testable Hypotheses
1. **The Variance Suppression Hypothesis:** We hypothesize that the variance of health adherence ($\sigma^2$) will decrease monotonically as $F_s$ increases. In high-friction zones, environmental constraints become the primary determinant of behavior, statistically compressing individual-level differences in $V_i$.
2. **The Structural Release Hypothesis:** Exogenously reducing a specific friction component (e.g., $C_{temp}$ via mobile clinics) will trigger a rapid, non-linear improvement in $P(A)$ without concurrent behavioral education.

---

## VI. Empirical Anchor: The Central Valley
The Central Valley serves as a critical testbed for the SFM due to its intersectional extremes:
* **High $F_s$ (Infrastructure):** 176 identified Health Professional Shortage Areas (HPSAs) directly scale the **Temporal Cost** ($C_{temp}$) of care-seeking [15].
* **Behavioral Collapse:** Kern County’s "Deaths of Despair" rate (>50% above national average) serves as a potential indicator of the tipping point where $F_s$ overrides $V_i$ [16].
* **Safety Barriers:** With 36% of residents prioritizing safety [15], we identify **Safety Cost** ($C_{safe}$) as a dominant weight ($\omega$) in the local friction index.

---

## VII. Implications for Public Health Policy
By shifting the intervention locus from the individual to the environment, the SFM provides a quantifiable mandate for structural reform. If the model is validated, educational interventions in high-friction environments are mathematically predicted to yield diminishing returns. Capital must be redirected toward localized food systems, transit integration, and direct economic relief to bring $F_s$ below the critical collapse threshold.

***

## Strictly Cited References
1. Robinson, W. S. (1950). Ecological Correlations and the Behavior of Individuals. *American Sociological Review*.
2. Yi, Z., et al. (2026). From food deserts to nutritional equity: socioeconomic drivers of hypertension. *Journal of Nutritional Science*.
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
15. Fresno Economic Opportunities Commission. (2025). *Community Needs Assessment Executive Summary*.
16. Kern County Public Health. (2022). *Community Health Needs Assessment (CHNA)*.
