<script>
  document.addEventListener("DOMContentLoaded", function () {
    document.title = "Joonho Phil Hwang";

    const headerLink = document.querySelector("header h1 a");
    if (headerLink && headerLink.parentElement) {
      const text = headerLink.textContent;
      const h1 = headerLink.parentElement;
      h1.textContent = text;   // <h1><a>...</a></h1>  →  <h1>...</h1>
    }
  });
</script>

<style>
.paper-title::before {
  counter-increment: paper-counter;
  content: "[" counter(paper-counter) "] ";
  font-weight: normal;
  margin-right: 0.25em;
}
</style>

<button id="theme-toggle" type="button" aria-label="Toggle color mode">🌙</button>

<script>
(function() {
  const storageKey = "color-theme";
  const body = document.body;

  function applyTheme(theme) {
    body.classList.remove("theme-light", "theme-dark");
    if (theme === "dark") {
      body.classList.add("theme-dark");
    } else {
      body.classList.add("theme-light");
    }
    const btn = document.getElementById("theme-toggle");
    if (btn) {
      btn.textContent = theme === "dark" ? "☀️" : "🌙";
    }
  }

  function initTheme() {
    const saved = localStorage.getItem(storageKey);
    if (saved === "light" || saved === "dark") {
      applyTheme(saved);
    } else {
      const prefersDark = window.matchMedia &&
        window.matchMedia("(prefers-color-scheme: dark)").matches;
      applyTheme(prefersDark ? "dark" : "light");
    }
  }

  document.addEventListener("DOMContentLoaded", function() {
    initTheme();

    const btn = document.getElementById("theme-toggle");
    if (!btn) return;

    btn.addEventListener("click", function() {
      const isDark = body.classList.contains("theme-dark");
      const nextTheme = isDark ? "light" : "dark";
      applyTheme(nextTheme);
      localStorage.setItem(storageKey, nextTheme);
    });
  });
})();
</script>

Hello. My name is Joonho Phil Hwang (황준호; 黃俊晧), and I am a fourth-year PhD student in economics at Seoul National University, where I am fortunate to be advised by Professor [Seojeong Lee](https://sites.google.com/site/misspecifiedjay/). My research interests are in econometrics, with a particular focus on
- panel data models
- causal inference


### Working papers
<div style="counter-reset: paper-counter;">
  <span class="paper-title">Online Updating for Linear Panel Regressions</span><br>  
  joint with <a href="https://sites.google.com/site/misspecifiedjay/">Seojeong Lee</a><br>

  <!-- 1. ABSTRACT 버튼 -->
  <details>
    <summary><span class="abs-pill">ABS</span></summary>
    <div style="font-size: 95%; margin-top: 10px; text-align: justify;">
      <span>
        In this paper, we develop online updating methods for linear panel regression models.
        Online updating refers to procedures for sequentially updating parameter estimates
        as new data become available. In practice, the potential size of the dataset or data
        confidentiality constraints may preclude researchers from storing or accessing the
        entire dataset. We propose an online updating procedure for widely used linear
        regression models in panel data, where data expansion can occur through either
        (1) the arrival of new units or (2) the arrival of additional time periods for
        existing units. The proposed procedure yields closed-form expressions for updating
        both the point estimates and associated standard errors in each scenario.
        <br><br>
        <em>What is online updating?</em>  See the example below:
      </span>
      <div style="text-align: center; margin-top: 10px;">
        <img src="https://github.com/Joonho-Phil-Hwang/Online_updating/blob/main/beta_path.gif?raw=true"
             alt="Online Updating Beta Path GIF"
             style="width: 70%; max-width: 600px; border: 1px solid #ccc;
                    box-shadow: 0 0 8px rgba(0,0,0,0.1);">
      </div>
      <div style="margin-top: 10px;">
        <span style="text-decoration: underline;">presented at:</span> 
        SNU Econometrics Workshop, SETA 2025, University of Sydney, KERIC 2025,
        SNU Workshop on Recent Advances in Econometrics
      </div>
    </div>
  </details>

  <!-- 2. SUMMARY 버튼 -->
  <details class="summary-section">
    <summary><span class="abs-pill">SUM</span></summary>
    <div class="summary-body">
      <p>
        <strong>Big picture.</strong>
        Many panel datasets grow over time as new units or new time periods are added.
        Re-estimating fixed effects regressions from scratch can be slow and memory-intensive,
        especially when the raw microdata cannot be permanently stored. This paper develops
        <em>online updating</em> methods for linear panel regressions that update the estimator
        sequentially using only low-dimensional summary statistics.
      </p>
      <p>
        <strong>Method.</strong>
        We study static fixed effects models and other linear panel regressions with
        unbalanced panels. We derive closed-form updating formulas for
        coefficients and cluster-robust variances when (i) new units arrive or (ii) additional time
        periods are appended for existing units. For TWFE with many time dummies, we adapt
        the incremental SVD algorithm of Brand (1999, 2006) to maintain an economy SVD of the
        normal matrix and recover the updated coefficients without direct inversion.
      </p>
      <p>
        <strong>Findings.</strong>
        In large simulated panels, the online SVD-based estimator matches the batch fixed effects
        estimator (from <code>plm</code>) up to machine precision, while using orders of
        magnitude less memory and much smaller per-unit update time. This makes recursive,
        numerically stable fixed effects estimation feasible even when the full panel cannot be
        stored.
      </p>
    </div>
  </details>

</div>

<div style="margin: 20px 0;"></div> <!-- 제목 사이 간격 -->

### Work in progress
<!--<div style="counter-reset: paper-counter;">
  <span class="paper-title">Revisiting the Weighting Scheme in Synthetic Difference-in-Differences</span><br>
  joint with <a href="https://www.econ.uni-bonn.de/en/department/doctoral-students/chencheng-fang">Chencheng Fang</a><br>
  <!--
  <details>
    <summary>
      <span style="font-weight: bold; color: gray;">abstract</span>
    </summary>
    <span style="font-size: 95%; margin-top: 10px; display: block; text-align: justify;">
      tbd
      <br>
    <span> presented at:</span> 3rd BCFM PhD conference (by coauthor)
    </span>
  </details>
  -->
<div style="counter-reset: paper-counter;">
<div style="margin: 10px 0;"></div> <!-- 간격 조정 -->
<div>
  <span class="paper-title">Disentangling Persistence from Treatment Effects in Staggered Event Studies</span><br>
  <details>
  <summary><span class="abs-pill">ABS</span></summary>
  <div style="font-size: 95%; margin-top: 10px; text-align: justify;">
      <span>
        Applied researchers often face a dilemma regarding whether to include lagged dependent variables. When the outcome exhibits state dependence but lagged terms are omitted, standard estimates can be biased. Following Angrist and Pischke (2009), many rely on a ``bracketing relationship'', treating specifications with and without lagged outcomes as bounds for the true causal effect. In this paper, we demonstrate that this heuristic breaks down in staggered two-way fixed effects settings. We propose a estimation strategy that explicitly accounts for the dynamic evolution of the outcome. By rigorously disentangling persistence from instantaneous treatment effects, our method ensures that intrinsic outcome dynamics are not mistaken for causal policy impacts.
      </span>
</div>

<div style="text-align: center; font-size: 90%; color: gray; margin-top: 40px;">
</div>
