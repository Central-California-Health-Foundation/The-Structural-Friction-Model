# CCHF Framework Proposal: The Transaction Cost Model (TCM)

**Thesis:** A mechanistic extension to Social Determinants of Health (SDOH) is presented to reconcile individual agency with transaction costs. The **Transaction Cost Hypothesis** is articulated to identify threshold‑dependent behavioral collapse, and is operationalized through a moderated probability framework: the **Interaction‑Constrained Adherence Model (ICAM)**. The hypothesis is posited that health behavior is governed not solely by individual capacity or environmental conditions independently, but by their interaction under conditions of constrained cognitive bandwidth.

## I. Significance: Addressing the Ecological Bottleneck  

Behavioral epidemiology frequently encounters a methodological bottleneck: the routine application of the ecological fallacy [1]. Area‑level proxies (e.g., ZIP‑code aggregates) are routinely mapped onto individual biological risk, assuming uniform deprivation and ignoring intra‑zonal mobility [2]. This practice often confounds individual‑level composition with environmental context [3], thereby obscuring the proximal mechanisms that link structural neglect to disease [2].  

The SFM is presented as a complementary mechanistic framework to existing SDOH paradigms. While SDOH delineates environmental conditions, the SFM quantifies the dynamic cost of navigating those conditions. Health behavior is modeled as a behavioral‑economic function of intertemporal utility optimization, consistent with constraint‑based decision models [6, 7]. Transaction costs and cognitive bandwidth are introduced as primary drivers of health behavior, providing a measurable interaction between agency and environment.

## II. Volition as a Latent Construct  

The latent psychological and cognitive drive for health adherence, denoted \(V_i\), is defined as intrinsic capacity.  

Transaction Costs, comprising financial outlays, temporal travel burdens, and safety‑related risk, are operationalized as a composite index \(TC_{ij}\).  

Cognitive Bandwidth, representing the limited mental resources available for decision‑making, is modeled as a function of \(TC_{ij}\) and is assumed to be depleted as \(TC_{ij}\) increases (Mullainathan & Shafir, 2013).  

It is hypothesized that elevated Transaction Costs progressively diminish Cognitive Bandwidth, thereby constraining the observable expression of \(V_i\). The resulting behavioral outcome—adherence to health interventions—is modeled as a probabilistic function in which the interaction between \(V_i\) and Transaction Costs determines the probability of adherence. As Transaction Costs rise, the marginal effect of \(V_i\) on adherence declines in a threshold‑dependent manner, indicating variance compression of the latent construct rather than its complete loss. This mechanism positions Transaction Costs as a dominant determinant of behavior under conditions of high cognitive load, consistent with the Variance‑Suppression Hypothesis.  

*References: [7, 8, 11, 2]*

## III. Moderated Probability Model (Interaction‑Constrained Adherence Model)

Behavioral capacity is operationalized as a dynamic probability \(P(\text{adherence})\) through a logistic specification. Both the latent intrinsic capacity index \(V_i\) and the transaction‑cost index \(TC_{ij}\) are expressed as standardized latent variables (\(Z\)-scores) to permit cross‑domain comparability. An interaction term is incorporated to capture a non‑linear transition from agency‑dominant to constraint‑dominant regimes. The interaction coefficient \(\beta_{3}\) reflects the point at which increasing transaction costs attenuate the marginal utility of \(V_i\), thereby representing a threshold of cognitive‑economic exhaustion.

\[
\boxed{
P(A)_{ij}= \frac{1}{1+\exp\!\big[-(\beta_{0}+\beta_{1}V_{i}-\beta_{2}TC_{ij}-\beta_{3}(V_{i}\times TC_{ij}))\big]}
}
\]

### 3.1 Identification of Variables  

* **\(\beta_{1}V_{i}\) (Intrinsic Engine):** The marginal effect of baseline motivation on the propensity for adherence.  
* **\(\beta_{2}TC_{ij}\) (Environmental Brake):** The direct suppressive penalty exerted by transaction costs, measured as the sum of travel‑time expenditures, out‑of‑pocket fare burdens, and neighborhood safety penalties.  
* **\(\beta_{3}(V_{i}\times TC_{ij})\) (Exhaustion Threshold):** The interaction effect. The hypothesis posits that as transaction costs rise, the marginal benefit of intrinsic motivation diminishes, signifying a point of cognitive‑bandwidth depletion.

Transaction costs \(TC_{ij}\) are derived from GPS‑tracked travel durations, income‑scaled fare expenditures, and crime‑rate indices within a 500‑meter transit buffer; each component undergoes hierarchical Bayesian estimation to capture spatial correlation. Cognitive bandwidth is represented implicitly through the interaction term, reflecting the diminishing returns of \(V_{i}\) as \(TC_{ij}\) escalates.

![The Interaction‑Constrained Adherence Model](fig1_model.png){height=5.5in}

## IV. Measurement & Identification Strategy  

### 4.1 Estimation of Latent Cognitive Bandwidth (\(V_i\))  
The latent intrinsic capacity \(V_i\) is inferred through a Difference‑in‑Differences (DiD) design that exploits an exogenous reduction in transaction costs delivered by mobile health clinics. The DiD specification comprises a treatment group exposed to the cost reduction and a matched control group, with pre‑ and post‑period indicators. Parallel‑trend validation is presented through visual inspection of adherence trajectories and formal statistical tests (e.g., placebo leads). The DiD coefficient (\(\hat{\beta}_{V}\)) is reported as the estimated mean of \(V_i\) and is demonstrated to be statistically independent of the transaction‑cost index (Spearman \(\rho \approx 0\)). The resulting \(V_i\) estimates are treated as external predictors in the Interaction‑Constrained Adherence Model.  

### 4.2 Operationalization of Transaction Costs (\(F_s\))  
Transaction costs are measured as a composite index (\(F_s = \sum \omega_k C_k\)) comprising three components:  

- **Temporal Component (\(C_{\text{temp}}\)):** GIS‑derived travel times to health and food service locations via public transit, expressed in minutes.  
- **Financial Component (\(C_{\text{fin}}\)):** Out‑of‑pocket expenses plus transit fares, expressed as a percentage of the local median household income.  
- **Safety Component (\(C_{\text{safe}}\)):** Standardized crime density indices within a 500‑meter buffer around the individual’s residence, scaled to a mean of zero and unit variance.  

All components are aggregated using empirically derived weights (\(\omega_k\)) that maximize construct validity against CDC tract‑level benchmarks (correlation \(r > 0.90\)). The composite index is intended to represent the aggregate transaction costs experienced by individuals.  

### 4.3 Individual‑Level Transaction Cost Measurement  
A sub‑section (IV‑2.1) outlines the collection of individual‑level transaction‑cost data through smartphone‑based travel logging, wearable devices, and income‑adjusted fare reporting. Hierarchical Bayesian estimation will assign random intercepts for each component, yielding posterior distributions for \(F_{s,ij}\) that can be incorporated into the Interaction‑Constrained Adherence Model.  

### 4.4 Identification of the Interaction Term  
The interaction between \(V_i\) and transaction costs (\(\beta_3\)) is identified through the hierarchical model described in Section V. Posterior credible intervals for \(\beta_3\) are reported, and counter‑factual simulations illustrate the conditional effect of \(V_i\) under low versus high transaction‑cost regimes.

## V. Testable Hypotheses

::: {.box}
**1. Variance‑Suppression Hypothesis**  
It is hypothesized that the variance of health‑adherence outcomes ($\sigma^{2}$) declines monotonically as Transaction Costs increase. In zones characterized by elevated Transaction Costs, environmental constraints become the predominant determinant of behavior, thereby compressing individual‑level differences in Cognitive Bandwidth.
:::

::: {.box}
**2. Structural‑Release Hypothesis**  
It is hypothesized that an exogenous reduction of a specific Transaction Cost component (e.g., temporal transaction cost $C_{\text{temp}}$ via mobile clinics) will elicit a rapid, non‑linear increase in the probability of adherence $P(A)$, absent concurrent behavioral education interventions.
:::

---

## VI. Pre‑validation of the Transaction Cost Index (TCI)

The Central Valley provides a testbed for the Transaction Cost Index (TCI) owing to its extreme values in temporal, financial, and safety dimensions. High TCI values are associated with a large number of Health Professional Shortage Areas (HPSAs), which directly increase the Transaction Costs (\(C_{\text{temp}}\)) of care‑seeking. Kern County’s elevated mortality from despair, exceeding national averages, is interpreted as a behavioral collapse where Transaction Costs dominate Cognitive Bandwidth. Safety concerns, reported by 36 % of residents, are operationalized as the Safety Cost (\(C_{\text{safe}}\)), assigned a dominant weight (\(\omega\)) in the composite TCI.

### 6.1 Empirical Validation: The 2025 Fresno Cross‑Section

The 2025 CDC PLACES (GIS‑Friendly) dataset was employed to assess construct validity of the TCI across Fresno City Census Tracts. TCI was computed as the product of localized poverty rates and mean commute times (ACS 5‑Year Estimates). Construct validity was demonstrated through strong predictive relationships with CDC tract‑level measures of Lack of Transportation (\(r = 0.91\)) and Food Insecurity (\(r = 0.90\)).

Biological and psychological weathering were examined through dose‑response associations between TCI and health outcomes. High TCI tracts exhibited pronounced correlations with acute Transaction Costs, manifested as reduced sleep duration (\(r = 0.85\)). Psychological collapse was indicated by a strong association with loneliness (\(r = 0.77\)), supporting the suppression of baseline Cognitive Bandwidth (\(V_i\)). Metabolic weathering was reflected in significant correlations with adult diabetes prevalence (\(r = 0.75\)) and hypertension (\(r = 0.45\)).

These findings confirm that the TCI functions as a sensitive predictor of physiological and psychological load, rather than a mere descriptive proxy. While the Central Valley serves as an empirical anchor, the TCI is designed for structural generalization to environments where health behavior is mediated by measurable Transaction Costs.

## VII. Policy Implications  

By reorienting the locus of intervention from the individual to the environment, the Interaction‑Constrained Adherence Model furnishes a quantifiable mandate for structural reform. Validation of the model indicates that educational interventions within contexts characterized by elevated transaction costs are mathematically predicted to exhibit diminishing marginal returns. The interaction between educational input and transaction costs is captured by a negative moderation coefficient, which attenuates the marginal effect of cognitive bandwidth on adherence when transaction costs exceed the median value. Consequently, capital is recommended to be redirected toward mechanisms that reduce transaction costs, including the development of localized food systems, the integration of transit networks, and the provision of direct economic relief, with the objective of lowering the composite transaction‑cost index below the empirically identified collapse threshold. This framework treats health behavior as a variable response to modifiable environmental cost structures rather than as a fixed trait.  

![Fresno Tract Cross-Section Analysis](fig2_fresno.png){height=7.5in}

## VIII. Supporting Visualizations for the Interaction‑Constrained Adherence Model  

### 8.1 Transaction‑Cost Decomposition Plot  
The composite Transaction‑Cost Index (TCI) is decomposed into its constituent components: temporal transaction costs ($C_{temp}$), financial transaction costs ($C_{fin}$), and safety‑related transaction costs ($C_{safe}$). The plot displays the contribution of each component across Central Valley tracts, thereby illustrating that elevated transaction costs arise from specific infrastructure deficits and economic constraints rather than an abstract aggregate.  

### 8.2 Structural‑Release Simulation  
The simulation framework is employed to illustrate the effect of a targeted policy shock on the probability of adherence. An individual with a fixed intrinsic capacity ($V_i$) is simulated under a baseline high Transaction‑Cost scenario, resulting in a low adherence probability (<20%). Subsequently, a Structural‑Release policy—operationalized as a reduction in $C_{temp}$ through mobile‑clinic deployment—lowers the Transaction‑Cost Index below the empirically identified collapse threshold, producing a non‑linear increase in adherence probability (>80%). The simulation thus provides a testable illustration of the Structural‑Release Hypothesis. Cognitive bandwidth, operationalized as the latent intrinsic capacity $V_i$, moderates the effect of transaction costs on adherence.  

### 8.3 Interaction Phase Diagram  
The interaction between Transaction Costs and Cognitive Bandwidth is visualized in a two‑dimensional phase diagram. Axes represent the Transaction‑Cost Index (TCI) and the latent intrinsic capacity ($V_i$). Color gradients encode the posterior mean of the adherence probability. Regions of the diagram delineate the Constraint‑Dominant Regime (high TCI, low $V_i$) and the Agency‑Dominant Regime (low TCI, high $V_i$). Empirical mapping of Fresno City tracts confirms clustering within the Constraint‑Dominant Regime for high‑TCI areas, supporting the Variance‑Suppression Hypothesis.  

![Interaction Phase Diagram: Constraint‑Dominant and Agency‑Dominant Regimes](fig3_phase.png){height=3.5in}

\newpage

## References

1. Mullainathan, S., & Shafir, E. (2013). *Scarcity: Why having too little means so much*. Macmillan.

2. Robinson, W. S. (1950). *Ecological Correlations and the Behavior of Individuals*. *American Sociological Review*.

3. Yi, Z., et al. (2026). *From food deserts to nutritional equity: socioeconomic drivers of hypertension*. *Journal of Nutritional Science*.

4. Abba, M., et al. (2021). *Influence of contextual socioeconomic position on hypertension risk*. *BMC Public Health*.

5. Fielder, J. C., et al. (2024). *Sense of control buffers against stress*. *biorxiv*.

6. Chambon, V., et al. (2014). *From action intentions to action effects*. *Frontiers in Human Neuroscience*.

7. Damen, T., et al. (2015). *Re‑Examination of the agentic shift*. *PLoS ONE*.

8. Mann, K., et al. (2019). *Adherence to long‑term prophylactic treatment: microeconomic analysis*. *Health Economics Review*.

9. Caspar, E. A., et al. (2021). *The obedient mind and the volitional brain*. *PLoS ONE*.

10. Valori, I., et al. (2022). *Motivation from agency and reward*. *Brain Sciences*.

11. Mariano, M., et al. (2024). *How aging shapes our sense of agency*. *Psychonomic Bulletin & Review*.

12. Perrykkad, K., et al. (2021). *The effect of uncertainty on prediction error*. *Cognition*.

13. Imaizumi, S., et al. (2018). *Compress global, dilate local: intentional binding*. *biorxiv*.

14. Tanaka, T. (2024). *Evaluating the Bayesian causal inference model of intentional binding*. *Scientific Reports*.

15. Zullig, L. L., et al. (2018). *The new landscape of medication adherence improvement*. *Patient Preference and Adherence*.

16. Fresno Economic Opportunities Commission. (2025). *Community Needs Assessment Executive Summary*.

17. Kern County Public Health. (2022). *Community Health Needs Assessment (CHNA)*.
