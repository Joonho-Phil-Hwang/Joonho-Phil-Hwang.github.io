## Research interests

- Panel data & network econometrics
- Causal inference

## Working papers

### Fixed-Effect Regression with Link Misclassification

{{< links >}}

{{< abstract >}}
Fixed-effect regressions on network data estimate node effects from outcomes on links. We study these regressions when links are misclassified. False negatives (links that are not reported) alone cause no distortion. False positives (nonlinks that are reported as links) do: apart from sampling variation, they pull particular linear combinations of the estimated effects toward zero when nonlinks have mean outcome zero, and nonzero means add a shift. This attenuation need not vanish in large networks. We therefore adjust the regression for the false positives. When nodes have many links, the adjusted estimator is consistent, and a bias-adjusted estimator of a contrast of the effects (e.g., the difference between two groups of nodes) is asymptotically normal. When nodes have few links, the adjusted estimator is unreliable, because it magnifies the noise in the reports and its bias does not vanish. In this case, we propose an alternative method that splits the sample, tests each candidate value of the contrast, and keeps the values that are not rejected. Under suitable conditions, the resulting confidence set is valid for the linear combination of the effects that the test measures, which need not equal the contrast. In an application to gifts between households in a Tanzanian village, the unadjusted regression finds that gifts flow from richer to poorer households, but the confidence set that allows for link misclassification contains zero.
{{< /abstract >}} 

### Fixed-Effects Estimation and Cluster-Robust Inference for Streaming Panel Data

with [Seojeong Lee](https://sites.google.com/site/misspecifiedjay/)

{{< links >}}

{{< abstract >}}
Panel datasets grow over time: a new unit enters, an existing unit reports an observation for a missed period, or a new period begins. Re-estimating a fixed-effects regression after each arrival is costly for a large panel and impossible once the earlier observations are gone. We derive recursive formulas for the least-squares coefficient and the unit-clustered covariance that reproduce the full-sample estimates after each arrival, allowing for the change in a returning unit’s within transformation and for the time effect added in a two-way model. The exact covariance recursion stores two matrices whose size grows with the fourth power of the number of regressors. Our approximation instead stores one score vector per unit and keeps the coefficient exact. It is unbiased for the variance of the coefficient estimator under homoskedastic and serially uncorrelated errors, and asymptotically equivalent to the exact covariance as the number of units grows. We apply the updates to the staggered rollout of Community Health Centers, adding one year of data at a time.

***Note:*** This paper supersedes “Online Updating for Linear Panel Regressions”

**Award:** Best Third-Year Paper, Department of Economics, Seoul National University.

**Presentations:** SNU Econometrics Workshop, SETA 2025 (University of Macau), University of Sydney, KERIC 2025 (SNU), SNU Workshop on Recent Advances in Econometrics, SETA 2026 (University of Tokyo).
{{< /abstract >}}

## Publications

### On the Bracketing Relationship in Staggered Treatment Designs

*Economics Letters* (2026) 268, 113208

{{< links pdf="https://drive.google.com/file/d/1H5jOOK2tXjx_i2RRKmk9e-bi_uRfIGsz/view?usp=share_link" ssrn="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6683845" journal="https://doi.org/10.1016/j.econlet.2026.113208" journalname="Economics Letters" journallabel="DOI" >}}

{{< abstract >}}
Researchers often use fixed-effects and lagged-dependent-variable (LDV) estimates as upper and lower bounds on a treatment effect. This paper studies this comparison in staggered-treatment designs and shows that the conventional ordering of the two estimates is not generally preserved. The direction of the difference depends on cohort- and event-time-specific treatment effects, outcome persistence, and the alignment of treatment timing with unit and time heterogeneity. Thus, either estimator may serve as the lower or upper bound, and the ordering may vary across group-time cells. Monte Carlo simulations further show that the interval formed by the two realized point estimates frequently fails to contain the true group-time average treatment effect in finite samples. The results suggest that fixed-effects and LDV estimates should be viewed as a descriptive comparison rather than as guaranteed bounds.
{{< /abstract >}}

## Work in progress

### Neural-Augmented Mixed-Frequency Panel Quantile Forecasting

with [Chencheng Fang](https://ccfang2.github.io/) and [Gayeon Hong](https://sites.google.com/view/gayeon-hong/)

<!-- ### Synthetic Difference-in-Differences with Missing Post-Treatment Outcomes-->

<!-- with [Chencheng Fang](https://ccfang2.github.io/) -->
