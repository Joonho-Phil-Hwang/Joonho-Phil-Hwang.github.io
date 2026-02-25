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

Hello. My name is Joonho Phil Hwang (황준호; 黃俊晧), and I am a fifth-year PhD student in economics at Seoul National University, where I am fortunate to be advised by Professor [Seojeong Lee](https://sites.google.com/site/misspecifiedjay/). My research interests are in econometrics, with a particular focus on
- panel data models
- causal inference


<h3>Working papers</h3>

<div style="counter-reset: paper-counter;">

<div style="margin: 22px 0 30px 0;">
<span class="paper-title">Online Updating for Linear Panel Regressions</span><br>
joint with <a href="https://sites.google.com/site/misspecifiedjay/">Seojeong Lee</a><br>

<details style="margin-top: 10px;">
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
<em>What is online updating?</em> See the example below:
</span>

<div style="text-align: center; margin-top: 10px;">
<img src="https://github.com/Joonho-Phil-Hwang/Online_updating/blob/main/beta_path.gif?raw=true"
     alt="Online Updating Beta Path GIF"
     style="width: 70%; max-width: 600px; border: 1px solid #ccc; box-shadow: 0 0 8px rgba(0,0,0,0.1);">
</div>

<div style="margin-top: 10px;">
<span style="text-decoration: underline;">presented at:</span>
SNU Econometrics Workshop, SETA 2025, University of Sydney, KERIC 2025,
SNU Workshop on Recent Advances in Econometrics
</div>
</div>
</details>

<!-- SUM 버튼만 잠깐 숨김 -->
<!--
<details class="summary-section" style="margin-top: 10px;">
<summary><span class="abs-pill">SUM</span></summary>
<div class="summary-body">
...
</div>
</details>
-->
</div>

<div style="margin: 22px 0 30px 0;">
<span class="paper-title">On the Failure of the Bracketing Relationship in Staggered Treatment Designs</span><br>

<details style="margin-top: 10px;">
<summary><span class="abs-pill">ABS</span></summary>
<div style="font-size: 95%; margin-top: 10px; text-align: justify;">
<span>
Applied researchers often face a dilemma regarding whether to include lagged dependent variables.
When the outcome exhibits state dependence but lagged terms are omitted, standard estimates can be biased.
Following Angrist and Pischke (2009), many rely on a “bracketing relationship”, treating specifications
with and without lagged outcomes as bounds for the true causal effect. In this paper, we demonstrate that
this heuristic breaks down in staggered two-way fixed effects settings.
</span>
</div>
</details>
</div>

</div>

<div style="margin: 26px 0;"></div>

<h3>Work in progress</h3>

<!-- 여기서 counter를 다시 리셋 -->
<div style="counter-reset: paper-counter;">

<div style="margin: 22px 0 30px 0;">
<span class="paper-title">Deep Panel Quantile Regression</span><br>
joint with <a href="https://ccfang2.github.io/">Chencheng Fang</a> and
<a href="https://sites.google.com/view/gayeon-hong/">Gayeon Hong</a><br>
</div>

<div style="margin: 22px 0 30px 0;">
<span class="paper-title">Synthetic Difference-in-Differences with Missing Post-Treatment Outcomes</span><br>
joint with <a href="https://ccfang2.github.io/">Chencheng Fang</a><br>
</div>

</div>
