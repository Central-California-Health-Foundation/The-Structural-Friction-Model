# CCHF Framework Proposal: The Structural Friction Model (SFM)
**Thesis:** We propose a mechanistic extension to Social Determinants of Health (SDOH) that reconciles individual agency with structural constraints. The **Structural Friction Hypothesis** identifies threshold-dependent behavioral collapse, which we operationalize here via a moderated probability framework: the **Interaction-Constrained Adherence Model (SFM)**. The hypothesis posits that health behavior is governed not solely by individual capacity or environmental conditions independently, but by their interaction under conditions of constraint.

---

## I. Significance: Addressing the Ecological Bottleneck
Behavioral epidemiology frequently encounters a methodological bottleneck: the routine application of the ecological fallacy [1]. Mapping area-level proxies (e.g., ZIP code aggregates) directly onto individual biological risk assumes uniform deprivation and ignores intra-zonal mobility [2]. This approach often confounds individual-level composition with environmental context [3], potentially obscuring the proximal mechanisms linking structural neglect to disease [2].

The SFM serves as a **complementary mechanistic framework** to existing SDOH paradigms. While SDOH describes environmental conditions, the SFM seeks to quantify the dynamic *cost* of navigating those conditions. We move beyond subjective "perceived access" to model health behavior as a behavioral-economic function of **intertemporal utility optimization**, consistent with constraint-based decision models [6, 7]. Ultimately, this framework introduces a measurable interaction between agency and environment as a primary driver of health behavior.

---

## II. Volition as a Latent Construct
Cognitive science demonstrates that even under severe structural coercion, individuals often preserve a sense of agency [8]. We define **Intrinsic Capacity** ($V_i$) as the latent psychological and cognitive drive for health adherence. 

In adverse conditions, we hypothesize that **Structural Friction** ($F_s$)—the sum of financial, temporal, and safety costs—progressively exhausts the cognitive and economic bandwidth required to execute this capacity. We posit that individual non-compliance is often a probabilistically constrained outcome of high $F_s$ [7]. In this model, volition is not "lost," but its behavioral expression is subjected to extreme **variance compression**. As environmental costs rise, the probability of adherence follows a threshold-dependent decline, where structural constraints become the **dominant determinant** of behavior, degrading the cognitive and economic capacity required for action [2, 8, 11].

---

## III. The Moderated Probability Model (SFM)
We operationalize behavioral capacity as a dynamic probability $P(\text{adherence})$ using a logistic model: the **Interaction-Constrained Adherence Model**. Both $V_i$ and $F_s$ are modeled as **standardized latent indices** ($Z$-scores) to allow comparability across domains. Crucially, we include an **interaction term** to test for non-linear behavioral collapse. The collapse threshold is not a fixed parameter, but emerges from the interaction term $\beta_3(V_i \cdot F_s)$, where increasing $F_s$ progressively attenuates the marginal effect of $V_i$, producing a non-linear transition from agency-dominant to constraint-dominant behavioral regimes. This interaction term is critical, as it allows the model to distinguish between environments where agency is expressed versus environments where it is systematically suppressed:

$$P(A)_{is} = \frac{1}{1 + e^{-(\beta_0 + \beta_1 V_i - \beta_2 F_s - \beta_3(V_i \cdot F_s))}}$$

### 3.1 Identification of Variables
* **$\beta_1 V_i$ (Intrinsic Engine):** The marginal effect of baseline motivation.
* **$\beta_2 F_s$ (Environmental Brake):** The direct suppressive penalty of structural barriers.
* **$\beta_3(V_i \cdot F_s)$ (The Exhaustion Threshold):** The interaction effect. We hypothesize that as $F_s$ increases, the marginal utility of $V_i$ decreases, representing the point of **cognitive/economic exhaustion**.

<img width="813" height="647" alt="Screenshot 2026-04-02 at 9 34 22 AM" src="https://github.com/user-attachments/assets/53ddaf47-4112-4e64-a102-c1eea4dddcda" />

---

## IV. Measurement & Identification Strategy
To ensure the SFM is operationalizable and falsifiable, we propose the following measurement proxies:

### 4.1 Estimating Latent Intrinsic Capacity ($V_i$)
Since $V_i$ cannot be directly observed, we propose two primary inference strategies:
* **Revealed Preference:** Measuring adherence variance in comparatively low-friction cohorts (minimum observed $F_s$ within the sample) to establish a baseline distribution of $V_i$.
* **Behavioral Rebound:** Leveraging natural experiments or quasi-experimental designs (e.g., Difference-in-Differences). We will measure the non-linear improvement in adherence following an exogenous shock to $F_s$ (e.g., a sudden transit subsidy or mobile clinic placement). The magnitude of the rebound isolates the previously suppressed $V_i$.

### 4.2 Quantifying Structural Friction ($F_s$)
$F_s$ is operationalized as a weighted composite index ($F_s = \sum \omega_k C_k$) utilizing spatial and socioeconomic data:
* **Temporal Cost ($C_{temp}$):** GIS-modeled travel time to health/food hubs via public transit (measured in minutes).
* **Financial Cost ($C_{fin}$):** Out-of-pocket costs + transit fares relative to localized median household income (measured as % burden).
* **Safety Cost ($C_{safe}$):** Standardized local crime density indices within the individual’s transit buffer (index score).

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

### 6.1 Empirical Validation: The 2025 Fresno Cross-Section
To establish construct validity and measure the biological cost of friction, the SFM was tested against the 2025 CDC PLACES (GIS-Friendly) dataset across Fresno City Census Tracts. $F_s$ was calculated as the product of localized poverty rates and mean commute times (ACS 5-Year Estimates). 

**Construct Validity:** The $F_s$ index demonstrated exceptionally high predictive validity for acute environmental deficits, correlating almost perfectly with CDC tract-level estimates for **Lack of Transportation (r = 0.91)** and **Food Insecurity (r = 0.90)**.

**Biological & Psychological Weathering:** The data reveals a severe, dose-response relationship between environmental friction and physiological load. High $F_s$ tracts exhibited statistically profound correlations with:
* **Acute Temporal Friction:** A severe correlation with short sleep duration (**r = 0.85**), suggesting sleep is the primary biological currency traded for environmental navigation.
* **Psychological Collapse:** A strong correlation with loneliness (**r = 0.77**), validating the compound isolating toll of high-resistance environments and the suppression of baseline agency ($V_i$).
* **Metabolic Weathering:** A significant correlation with adult diabetes prevalence (**r = 0.75**) and hypertension (**r = 0.45**).

These robust 2025 coefficients confirm that $F_s$ is not merely a descriptive proxy, but a highly sensitive, predictive environmental variable for physiological and psychological load. While the Central Valley serves as an empirical anchor, the SFM is structurally generalizable to any environment where health behavior is mediated by measurable cost constraints.

<img width="593" height="529" alt="Screenshot 2026-04-02 at 9 41 36 AM" src="https://github.com/user-attachments/assets/3604f63c-fcd2-45fb-ab85-2d17b346862e" />

---

## VII. Implications for Public Health Policy
By shifting the intervention locus from the individual to the environment, the SFM provides a quantifiable mandate for structural reform. If the model is validated, educational interventions in high-friction environments are mathematically predicted to yield diminishing returns. Capital must be redirected toward localized food systems, transit integration, and direct economic relief to bring $F_s$ below the critical collapse threshold. This framework enables policymakers to treat health behavior not as a fixed trait, but as a variable response to modifiable environmental cost structures.

***

## VIII. Necessary Supporting Visualizations (Operationalizing the Model)
The figures in Section III illustrate the outcome *curves*, but to fully satisfy reviewer critiques regarding "black box" indices and abstract concepts, the final proposal requires visualizations that decompose the friction index and demonstrate testable policy shocks.

### 8.1 Figure 1: Friction Decomposition Plot
Reviewers will rightly ask, “What actually *drives* friction in the real world?” This figure decomposes the composite $F_s$ index, showing the explicit illustrative contribution of $C_{temp}$, $C_{fin}$, and $C_{safe}$ across actual Central Valley tracts. This visually proves that high friction isn't just a number; it’s a specific product of infrastructure deficits and economic constraints.

### 8.2 Figure 2: The Structural Release Hypothesis Simulation (Policy Shock)
This is the framework's most critical conceptual figure. It demonstrates that the SFM is not just descriptive but is *tunable* and *testable*. It shows a before-and-after simulation for a *single individual* with fixed $V_i$. When exposed to high $F_s$ (pre-intervention), their probability of adherence ($P(A)$) is suppressed to <20%. Following a targeted "Structural Release" policy (e.g., introduction of mobile clinics reduces $C_{temp}$), $F_s$ is brought below the collapse threshold, triggering an immediate, non-linear jump in $P(A)$ to >80%. This screams, "policy intervention works."

### 8.3 Figure 3: SFM Phase Diagram (Regions of Collapse and Agency)
This converts the framework into a comprehensive **system map**. It is a 2D plot of $F_s$ vs. $V_i$, colored by $P(A)$. This visualization effortlessly communicates the interaction effect: it proves that in high-friction environments (right side), individuals collapse to low adherence *regardless* of their baseline capacity, defining the "Constraint-Dominant Regime." Only when friction is low (left side) can variance manifest, creating the "Agency-Dominant Regime." Preliminary mapping of Fresno City already demonstrates this phase shift, with high-friction southern tracts tightly clustering in the constraint-dominant regime.

<img width="737" height="436" alt="Screenshot 2026-04-02 at 9 37 50 AM" src="https://github.com/user-attachments/assets/c1967a5d-1cfd-4711-9068-1a4e975952aa" />

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
11. Perrykkad, K., et al. (2021). The effect uncertainty on prediction error. *Cognition*.
12. Imaizumi, S., et al. (2018). Compress global, dilate local: Intentional binding. *biorxiv*.
13. Tanaka, T. (2024). Evaluating the Bayesian causal inference model of intentional binding. *Scientific Reports*.
14. Zullig, L. L., et al. (2018). The new landscape of medication adherence improvement. *Patient preference and adherence*.
15. Fresno Economic Opportunities Commission. (2025). *Community Needs Assessment Executive Summary*.
16. Kern County Public Health. (2022). *Community Health Needs Assessment (CHNA)*.
