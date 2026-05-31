<script>
  document.addEventListener("DOMContentLoaded", function () {
    document.title = "Joonho (Phil) Hwang";

    const headerLink = document.querySelector("header h1 a");
    if (headerLink && headerLink.parentElement) {
      const text = headerLink.textContent;
      const h1 = headerLink.parentElement;
      h1.textContent = text;
    }

    const storageKey = "color-theme";
    const body = document.body;
    const btn = document.getElementById("theme-toggle");

    function applyTheme(theme) {
      body.classList.remove("theme-light", "theme-dark");

      if (theme === "dark") {
        body.classList.add("theme-dark");
      } else {
        body.classList.add("theme-light");
      }

      if (btn) {
        btn.textContent = theme === "dark" ? "☀️" : "🌙";
      }
    }

    const saved = localStorage.getItem(storageKey);

    if (saved === "light" || saved === "dark") {
      applyTheme(saved);
    } else {
      const prefersDark =
        window.matchMedia &&
        window.matchMedia("(prefers-color-scheme: dark)").matches;

      applyTheme(prefersDark ? "dark" : "light");
    }

    if (btn) {
      btn.addEventListener("click", function () {
        const isDark = body.classList.contains("theme-dark");
        const nextTheme = isDark ? "light" : "dark";

        applyTheme(nextTheme);
        localStorage.setItem(storageKey, nextTheme);
      });
    }

    document.querySelectorAll(".pill-details summary a").forEach(function (link) {
      link.addEventListener("click", function (event) {
        event.stopPropagation();
      });
    });
  });
</script>

<style>
  .paper-list {
    counter-reset: paper-counter;
  }

  .paper-title::before {
    counter-increment: paper-counter;
    content: "[" counter(paper-counter) "] ";
    font-weight: normal;
    margin-right: 0.25em;
  }
</style>

<button id="theme-toggle" type="button" aria-label="Toggle color mode">🌙</button>

<p>
  Hello. My name is Joonho (Phil) Hwang (황준호; 黃俊晧), and I am a fifth-year PhD student in economics at Seoul National University, where I am fortunate to be advised by Professor <a href="https://sites.google.com/site/misspecifiedjay/">Seojeong Lee</a>. My research interests are in econometrics, with a particular focus on
</p>

<ul>
  <li>panel data models</li>
  <li>causal inference</li>
</ul>

<h3>Working papers</h3>

<div class="paper-list">

  <div class="paper-item" style="margin: 22px 0 30px 0;">
    <span class="paper-title">Online Updating for Linear Panel Regressions</span><br>
    with <a href="https://sites.google.com/site/misspecifiedjay/">Seojeong Lee</a><br>

    <div class="paper-actions">
      <details class="pill-details">
        <summary>
          <span class="abs-pill abstract-pill">Abstract</span>
        </summary>

        <div class="abs-content">
          <p style="margin: 0 0 10px 0;">
            In this paper, we develop online updating methods for linear panel regression models. Online updating refers to procedures for sequentially updating parameter estimates as new data become available. In practice, the potential size of the dataset or data confidentiality constraints may preclude researchers from storing or accessing the entire dataset. We propose an online updating procedure for widely used linear regression models in panel data, where data expansion can occur through either (1) the arrival of new units or (2) the arrival of additional time periods for existing units. The proposed procedure yields closed-form expressions for updating both the point estimates and associated standard errors in each scenario.
          </p>

          <p style="margin: 0 0 6px 0;">
            <span style="font-weight: 500;">Award:</span>
            Best Third-Year Paper, Department of Economics, Seoul National University.
          </p>

          <p style="margin: 0;">
            <span style="font-weight: 500;">Presented at:</span>
            SNU Econometrics Workshop, SETA 2025 (University of Macau), University of Sydney, KERIC 2025, SNU Workshop on Recent Advances in Econometrics.
          </p>
        </div>
      </details>
    </div>
  </div>

  <div class="paper-item" style="margin: 22px 0 30px 0;">
    <span class="paper-title">On the Bracketing Relationship in Staggered Treatment Designs</span><br>
    <span class="paper-status">Submitted</span><br>

    <div class="paper-actions">
      <details class="pill-details">
        <summary>
          <span class="abs-pill abstract-pill">Abstract</span>

          <a
            href="https://drive.google.com/file/d/1OywpSJyjLC3es5_pC6MGTUEEu11rkCPJ/view?usp=sharing"
            target="_blank"
            rel="noopener noreferrer"
            class="abs-pill pdf-pill"
          >Pdf</a>

          <a
            href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6683845"
            target="_blank"
            rel="noopener noreferrer"
            class="abs-pill ssrn-pill"
          >SSRN</a>
        </summary>

        <div class="abs-content">
          <p style="margin: 0;">
            Researchers often use fixed-effects and lagged-dependent-variable (LDV) estimates as upper and lower bounds on a treatment effect. This paper shows that this bracketing relationship can fail in staggered treatment designs. In staggered two-way fixed effects settings, neither estimator necessarily bounds the true group-time average treatment effect. Monte Carlo simulations show that such failures are common. The results suggest caution in using fixed-effects and LDV estimates as informal bounds in staggered-adoption settings.
          </p>
        </div>
      </details>
    </div>
  </div>

</div>

<div style="margin: 26px 0;"></div>

<h3>Work in progress</h3>

<div class="paper-list">

  <div class="paper-item" style="margin: 10px 0 14px 0;">
    <span class="paper-title">Deep Panel Quantile Regression</span>
    with <a href="https://ccfang2.github.io/">Chencheng Fang</a> and
    <a href="https://sites.google.com/view/gayeon-hong/">Gayeon Hong</a>
  </div>

  <div class="paper-item" style="margin: 10px 0 14px 0;">
    <span class="paper-title">Synthetic Difference-in-Differences with Missing Post-Treatment Outcomes</span>
    with <a href="https://ccfang2.github.io/">Chencheng Fang</a>
  </div>

</div>
