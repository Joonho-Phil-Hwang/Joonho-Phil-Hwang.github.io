<title>Joonho (Phil) Hwang</title>

<style>
.paper-title::before {
  counter-increment: paper-counter;
  content: "[" counter(paper-counter) "] ";
  font-weight: normal;
  margin-right: 0.25em;
}
</style>

<!-- 다크/라이트 모드 토글 버튼 -->
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

  // 초기 테마: 저장된 값 있으면 사용, 없으면 시스템 설정에 맞춤
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

### Welcome!

My name is Joonho (Phil) Hwang (황준호; 黃俊晧), and I am a fourth-year PhD student in economics at Seoul National University, where I am fortunate to be advised by Professor [Seojeong Lee](https://sites.google.com/site/misspecifiedjay/). <!--  My research interests are in econometrics, with a particular focus on panel data and causal inference. Click [here](https://drive.google.com/file/d/1XJup-ITYEBFdmSa03X9ZxbdulQQxOb-A/view?usp=sharing) for a copy of my CV. My email is <a href="mailto:jhhwang24@snu.ac.kr">jhhwang24@snu.ac.kr</a>. -->

### Research interests

Econometrics, with an emphasis on  
<ul class="research-list">
  <li>static and dynamic panel data models</li>
  <li>causal inference and difference-in-differences</li>
  <li>machine learning methods for panel regressions</li>
</ul>


### Working papers
<div style="counter-reset: paper-counter;">
  <span class="paper-title">Online Updating for Linear Panel Regressions</span><br>  
  joint with <a href="https://sites.google.com/site/misspecifiedjay/">Seojeong Lee</a><br>
  <details>
    <summary>[Abstract]</summary>
    <div style="font-size: 95%; margin-top: 10px; text-align: justify;">
      <span>
        In this paper, we develop online updating methods for linear panel regression models. Online updating refers to procedures for sequentially updating parameter estimates as new data become available. In practice, the potential size of the dataset or data confidentiality constraints may preclude researchers from storing or accessing the entire dataset. We propose an online updating procedure for widely used linear regression models in panel data, where data expansion can occur through either (1) the arrival of new units or (2) the arrival of additional time periods for existing units. The proposed procedure yields closed-form expressions for updating both the point estimates and associated standard errors in each scenario.
        <br><br>
        <em>What is online updating?</em>  See the example below:
      </span>
      <div style="text-align: center; margin-top: 10px;">
        <img src="https://github.com/Joonho-Phil-Hwang/Online_updating/blob/main/beta_path.gif?raw=true"
             alt="Online Updating Beta Path GIF"
             style="width: 70%; max-width: 600px; border: 1px solid #ccc; box-shadow: 0 0 8px rgba(0,0,0,0.1);">
      </div>
      <div style="margin-top: 10px;">
        <span style="text-decoration: underline;">presented at:</span> 
        SNU Econometrics Workshop, SETA 2025, University of Sydney, KERIC 2025, SNU Workshop on Recent Advances in Econometrics
      </div>
    </div>
  </details>
  
</div>

<div style="margin: 20px 0;"></div> <!-- 제목 사이 간격 -->

### Work in progress
<div style="counter-reset: paper-counter;">
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
</div>

<div style="margin: 10px 0;"></div> <!-- 간격 조정 -->
<div>
  <span class="paper-title">Dynamic Misspecification in Extended Two-Way Fixed Effects Regression</span><br>
  <!--
  <details>
    <summary>
      <span style="font-weight: bold; color: gray;">abstract</span>
    </summary>
    <span style="font-size: 95%; margin-top: 10px; display: block; text-align: justify;">
      tbd
    </span>
  </details>
  -->
</div>

<div style="text-align: center; font-size: 90%; color: gray; margin-top: 40px;">
</div>
