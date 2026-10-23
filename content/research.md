## Research interests

- Panel data & network econometrics
- Causal inference

## Working papers

### Fixed-Effect Regressions on Misclassified Networks

{{< links >}}

{{< abstract >}}
Network fixed effects regressions are widely used to control for unobserved heterogeneity across connected units, but their validity depends on observing the network accurately. This paper studies fixed effects regression when network links are misclassified. Misclassification happens when either some true links are missing or some recorded links are spurious. We show that the standard estimator is generally inconsistent, and that the two errors play very different roles: spurious links drive the bias. Because spurious links behave as if every pair of units were weakly connected, they attenuate broad, smooth variation in the fixed effects — differences at the level of regions, communities, or sectors — far more than localized variation, systematically washing out the large-scale heterogeneity that is typically of interest. We propose a bias-corrected estimator that removes the spurious-link component of the observed network and rescales for missing links. The corrected estimator is consistent when the true network is sufficiently well connected, supports asymptotically normal inference for the smooth functionals, and remains feasible because the misclassification rates can themselves be recovered from repeated measurements of the network.
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
