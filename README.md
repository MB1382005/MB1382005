<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mohammed Bahaa Attia — CS · AI/ML · Systems</title>
<meta name="description" content="Portfolio of Mohammed Bahaa Attia — CS student at MSA University specializing in AI/ML, software engineering, and systems.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d0d0d;
    --bg2: #141414;
    --bg3: #1a1a1a;
    --border: rgba(255,255,255,0.08);
    --border2: rgba(255,255,255,0.14);
    --text: #e8e8e6;
    --muted: #888884;
    --accent: #7F77DD;
    --accent2: #1D9E75;
    --mono: 'JetBrains Mono', monospace;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--mono);
    font-size: 14px;
    line-height: 1.6;
    min-height: 100vh;
  }

  a { color: inherit; text-decoration: none; }

  /* LAYOUT */
  .wrap { max-width: 860px; margin: 0 auto; padding: 0 2rem; }

  /* NAV */
  nav {
    position: sticky; top: 0; z-index: 100;
    background: rgba(13,13,13,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 0.5px solid var(--border);
    padding: 1rem 0;
  }
  .nav-inner {
    display: flex; align-items: center;
    justify-content: space-between;
    max-width: 860px; margin: 0 auto; padding: 0 2rem;
  }
  .nav-logo { font-size: 12px; font-weight: 700; letter-spacing: 0.1em; color: var(--accent); }
  .nav-links { display: flex; gap: 1.5rem; }
  .nav-links a { font-size: 11px; color: var(--muted); letter-spacing: 0.06em; transition: color .15s; }
  .nav-links a:hover { color: var(--text); }
  .nav-cta a {
    font-size: 11px; padding: 5px 14px;
    border: 0.5px solid var(--border2);
    border-radius: 6px; color: var(--text);
    transition: background .15s;
  }
  .nav-cta a:hover { background: var(--bg3); }

  /* HERO */
  .hero { padding: 5rem 0 4rem; }
  .badge {
    display: inline-block; font-size: 10px;
    padding: 3px 12px; border: 0.5px solid var(--accent2);
    color: var(--accent2); border-radius: 999px;
    letter-spacing: 0.08em; margin-bottom: 1.5rem;
  }
  .badge::before { content: '● '; font-size: 8px; }
  h1 {
    font-size: clamp(28px, 5vw, 48px);
    font-weight: 700; letter-spacing: -0.02em;
    line-height: 1.05; margin-bottom: 1rem;
    color: #fff;
  }
  .hero-sub {
    font-size: 13px; color: var(--muted);
    max-width: 500px; line-height: 1.7; margin-bottom: 1.75rem;
  }
  .hero-links { display: flex; gap: .625rem; flex-wrap: wrap; margin-bottom: 3rem; }
  .hero-links a {
    display: flex; align-items: center; gap: 6px;
    font-size: 11px; color: var(--muted);
    padding: 5px 12px; border: 0.5px solid var(--border);
    border-radius: 6px; transition: all .15s;
  }
  .hero-links a:hover { color: var(--text); border-color: var(--border2); background: var(--bg3); }

  /* STATS */
  .stats {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 10px; margin-bottom: 0;
  }
  .stat {
    background: var(--bg2);
    border: 0.5px solid var(--border);
    border-radius: 8px; padding: .875rem 1rem;
  }
  .stat-num { font-size: 20px; font-weight: 700; color: var(--accent); }
  .stat-label { font-size: 10px; color: var(--muted); margin-top: 4px; line-height: 1.4; }

  /* DIVIDER */
  .divider { border: none; border-top: 0.5px solid var(--border); margin: 3.5rem 0; }

  /* SECTION */
  .sec-header {
    display: flex; align-items: baseline; gap: .75rem;
    margin-bottom: 1.5rem;
  }
  .sec-num { font-size: 10px; color: var(--muted); letter-spacing: 0.1em; }
  .sec-title { font-size: 12px; font-weight: 500; letter-spacing: 0.08em; color: var(--text); }
  section { margin-bottom: 3rem; }

  /* PROJECT CARDS */
  .proj-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 10px;
  }
  .proj {
    background: var(--bg2);
    border: 0.5px solid var(--border);
    border-radius: 10px; padding: 1.125rem 1.25rem;
    display: block; position: relative;
    transition: border-color .2s, background .2s;
    cursor: pointer;
  }
  .proj:hover { border-color: var(--border2); background: var(--bg3); }
  .proj-header { display: flex; align-items: flex-start; justify-content: space-between; margin-bottom: .625rem; }
  .proj-tag { font-size: 9px; color: var(--muted); letter-spacing: 0.08em; }
  .proj-badge {
    font-size: 9px; padding: 2px 8px;
    border-radius: 999px; background: rgba(127,119,221,0.12);
    border: 0.5px solid rgba(127,119,221,0.3);
    color: var(--accent);
  }
  .proj-name { font-size: 13px; font-weight: 500; color: #fff; margin-bottom: .4rem; }
  .proj-desc { font-size: 11px; color: var(--muted); line-height: 1.65; margin-bottom: .875rem; }
  .chips { display: flex; flex-wrap: wrap; gap: 5px; }
  .chip {
    font-size: 9px; padding: 2px 8px;
    border-radius: 5px;
    background: rgba(255,255,255,0.04);
    border: 0.5px solid var(--border);
    color: var(--muted);
  }
  .chip.a {
    background: rgba(127,119,221,0.1);
    border-color: rgba(127,119,221,0.25);
    color: #AFA9EC;
  }
  .proj-link {
    position: absolute; top: 1rem; right: 1.25rem;
    font-size: 11px; color: var(--muted);
    opacity: 0; transition: opacity .15s;
  }
  .proj:hover .proj-link { opacity: 1; }

  /* STACK */
  .stack-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
    gap: 10px;
  }
  .stack-group {
    background: var(--bg2);
    border: 0.5px solid var(--border);
    border-radius: 8px; padding: .875rem 1rem;
  }
  .stack-cat { font-size: 9px; color: var(--muted); letter-spacing: 0.1em; margin-bottom: .625rem; }
  .stack-items { display: flex; flex-wrap: wrap; gap: 4px; }
  .stack-item {
    font-size: 10px; padding: 2px 7px;
    border-radius: 5px;
    background: rgba(255,255,255,0.04);
    border: 0.5px solid var(--border);
    color: var(--text);
  }

  /* CREDENTIALS */
  .cred-list { display: flex; flex-direction: column; gap: 8px; }
  .cred {
    display: flex; align-items: center; gap: .875rem;
    padding: .875rem 1.125rem;
    border: 0.5px solid var(--border);
    border-radius: 8px; background: var(--bg2);
  }
  .cred-icon { font-size: 15px; flex-shrink: 0; }
  .cred-text { font-size: 12px; flex: 1; color: var(--text); }
  .cred-date { font-size: 10px; color: var(--muted); flex-shrink: 0; letter-spacing: 0.06em; }

  /* CONTACT */
  .contact-card {
    background: var(--bg2);
    border: 0.5px solid var(--border);
    border-radius: 12px; padding: 2rem;
    display: flex; align-items: center;
    justify-content: space-between; flex-wrap: wrap; gap: 1.5rem;
  }
  .contact-title { font-size: 16px; font-weight: 500; color: #fff; margin-bottom: .5rem; }
  .contact-sub { font-size: 12px; color: var(--muted); line-height: 1.7; }
  .contact-actions { display: flex; gap: .5rem; flex-wrap: wrap; align-items: center; }
  .contact-actions a {
    font-size: 11px; padding: 7px 16px;
    border: 0.5px solid var(--border2);
    border-radius: 6px; transition: all .15s;
  }
  .contact-actions a:hover { background: var(--bg3); }
  .contact-actions a.primary {
    background: var(--accent);
    border-color: var(--accent);
    color: #fff;
  }
  .contact-actions a.primary:hover { opacity: .88; }

  /* FOOTER */
  footer {
    text-align: center; font-size: 10px;
    color: var(--muted); letter-spacing: 0.06em;
    padding: 2rem 0 3rem;
    border-top: 0.5px solid var(--border);
    margin-top: 1rem;
  }

  /* MOBILE */
  @media (max-width: 600px) {
    .stats { grid-template-columns: repeat(2, 1fr); }
    .nav-links { display: none; }
    h1 { font-size: 28px; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-inner">
    <div class="nav-logo">M.attia.system</div>
    <div class="nav-links">
      <a href="#projects">projects</a>
      <a href="#stack">stack</a>
      <a href="#credentials">credentials</a>
      <a href="#contact">contact</a>
    </div>
    <div class="nav-cta"><a href="mailto:mohamed.bahaa5@msa.edu.eg">hire ↗</a></div>
  </div>
</nav>

<div class="wrap">

  <!-- HERO -->
  <section class="hero">
    <div class="badge">available for internships &amp; research</div>
    <h1>MOHAMMED<br>BAHAA ATTIA</h1>
    <p class="hero-sub">CS student specializing in AI/ML, software engineering &amp; systems. Bridging mathematical theory and high-performance software — at MSA University, Giza.</p>
    <div class="hero-links">
      <a href="https://linkedin.com/in/MB1382005" target="_blank" rel="noopener">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
        LinkedIn
      </a>
      <a href="https://kaggle.com/MB1382005" target="_blank" rel="noopener">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor"><path d="M18.825 23.859c-.022.092-.117.141-.281.141h-3.139c-.187 0-.351-.082-.492-.248l-5.178-6.589-1.448 1.374v5.111c0 .235-.117.352-.351.352H5.505c-.236 0-.354-.117-.354-.352V.353c0-.233.118-.353.354-.353h2.431c.234 0 .351.12.351.353v14.343l6.203-6.272c.165-.165.33-.246.495-.246h3.239c.144 0 .236.06.285.18.046.149.034.255-.036.315l-6.555 6.344 6.836 8.507c.095.104.117.208.07.334z"/></svg>
        Kaggle
      </a>
      <a href="https://github.com/MB1382005" target="_blank" rel="noopener">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
        GitHub
      </a>
      <a href="mailto:mohamed.bahaa5@msa.edu.eg">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Email
      </a>
    </div>

    <div class="stats">
      <div class="stat"><div class="stat-num">3.69</div><div class="stat-label">GPA / 4.0<br>MSA University</div></div>
      <div class="stat"><div class="stat-num">~90%</div><div class="stat-label">courses graded<br>A or A−</div></div>
      <div class="stat"><div class="stat-num">×2 🥈</div><div class="stat-label">Deep Minds AI<br>2nd place</div></div>
      <div class="stat"><div class="stat-num">83.5%</div><div class="stat-label">AUC on 301K<br>clinical records</div></div>
    </div>
  </section>

  <hr class="divider">

  <!-- PROJECTS -->
  <section id="projects">
    <div class="sec-header"><span class="sec-num">01 /</span><span class="sec-title">AI / ML</span></div>
    <div class="proj-grid">
      <a class="proj" href="https://github.com/MB1382005/heart-disease-prediction" target="_blank" rel="noopener">
        <div class="proj-header"><span class="proj-tag">[01] AI / ML</span><span class="proj-badge">AUC 83.51%</span></div>
        <div class="proj-name">Heart Disease Prediction</div>
        <div class="proj-desc">5-model stacking ensemble on 301,717 CDC samples. Engineered 15 features, SMOTE on 91/9 imbalance — 53.8% recall on 60K held-out set.</div>
        <div class="chips"><span class="chip a">XGBoost</span><span class="chip a">LightGBM</span><span class="chip">SMOTE</span><span class="chip">Scikit-learn</span></div>
        <span class="proj-link">↗</span>
      </a>
      <a class="proj" href="https://github.com/MB1382005/laptop-recommender-system" target="_blank" rel="noopener">
        <div class="proj-header"><span class="proj-tag">[02] NLP · IR</span><span class="proj-badge">8+ intents</span></div>
        <div class="proj-name">AI Laptop Recommender + IR System</div>
        <div class="proj-desc">Bilingual Arabic/English engine — TensorFlow embeddings, cosine similarity, BM25 fallback, Flask app with EDA dashboard.</div>
        <div class="chips"><span class="chip a">TensorFlow</span><span class="chip">BM25</span><span class="chip">Flask</span><span class="chip">Arabic NLP</span></div>
        <span class="proj-link">↗</span>
      </a>
      <a class="proj" href="https://github.com/MB1382005/brain-tumor-classification" target="_blank" rel="noopener">
        <div class="proj-header"><span class="proj-tag">[03] Computer Vision</span><span class="proj-badge">CNN</span></div>
        <div class="proj-name">Brain Tumor MRI Classifier</div>
        <div class="proj-desc">Multi-class tumor classification from MRI scans — full preprocessing pipeline, normalization, augmentation, feature extraction.</div>
        <div class="chips"><span class="chip a">CNN</span><span class="chip">OpenCV</span><span class="chip">Keras</span></div>
        <span class="proj-link">↗</span>
      </a>
      <a class="proj" href="https://github.com/MB1382005/maze-search-algorithms" target="_blank" rel="noopener">
        <div class="proj-header"><span class="proj-tag">[04] Classical AI</span><span class="proj-badge">BFS · DFS · A*</span></div>
        <div class="proj-name">Maze Solver — Search Algorithms</div>
        <div class="proj-desc">BFS, DFS and A* with step-by-step Tkinter visualization for live pathfinding comparison.</div>
        <div class="chips"><span class="chip a">A*</span><span class="chip">BFS</span><span class="chip">DFS</span><span class="chip">Tkinter</span></div>
        <span class="proj-link">↗</span>
      </a>
    </div>
  </section>

  <section>
    <div class="sec-header"><span class="sec-num">02 /</span><span class="sec-title">Software Engineering</span></div>
    <div class="proj-grid">
      <div class="proj">
        <div class="proj-header"><span class="proj-tag">[05] Full-stack ERP</span></div>
        <div class="proj-name">Pharmacy Management System</div>
        <div class="proj-desc">PHP/MySQL platform with auth, inventory &amp; reviews modules, AI chatbot for medication alternatives, OOP architecture.</div>
        <div class="chips"><span class="chip">PHP</span><span class="chip">MySQL</span><span class="chip">OOP</span><span class="chip">AI Chatbot</span></div>
      </div>
      <div class="proj">
        <div class="proj-header"><span class="proj-tag">[06] Business Systems</span></div>
        <div class="proj-name">Odoo ERP Customization</div>
        <div class="proj-desc">Business-process configuration and custom module development on Odoo.</div>
        <div class="chips"><span class="chip">Odoo</span><span class="chip">Python</span><span class="chip">ERP</span></div>
      </div>
      <a class="proj" href="https://github.com/MB1382005/cpp-hotel-booking-system" target="_blank" rel="noopener">
        <div class="proj-header"><span class="proj-tag">[07] Systems</span></div>
        <div class="proj-name">Hotel Booking System</div>
        <div class="proj-desc">OOP design, file I/O and application architecture implemented in C++.</div>
        <div class="chips"><span class="chip">C++</span><span class="chip">OOP</span><span class="chip">File I/O</span></div>
        <span class="proj-link">↗</span>
      </a>
      <a class="proj" href="https://github.com/MB1382005/csharp-platformer-game" target="_blank" rel="noopener">
        <div class="proj-header"><span class="proj-tag">[08] Game Dev</span></div>
        <div class="proj-name">C# Platformer Game</div>
        <div class="proj-desc">2D platformer in C# — game loop, collision detection, OOP design patterns.</div>
        <div class="chips"><span class="chip">C#</span><span class="chip">Game Loop</span><span class="chip">OOP</span></div>
        <span class="proj-link">↗</span>
      </a>
    </div>
  </section>

  <section>
    <div class="sec-header"><span class="sec-num">03 /</span><span class="sec-title">CS Fundamentals</span></div>
    <div class="proj-grid">
      <div class="proj">
        <div class="proj-header"><span class="proj-tag">[09] Language Implementation</span></div>
        <div class="proj-name">Compiler Design</div>
        <div class="proj-desc">Lexer and parser in C++ — tokenization, grammar rules, and syntax analysis.</div>
        <div class="chips"><span class="chip">C++</span><span class="chip">Lexer</span><span class="chip">Parser</span></div>
      </div>
      <div class="proj">
        <div class="proj-header"><span class="proj-tag">[10] Algorithms</span></div>
        <div class="proj-name">Problem Solving</div>
        <div class="proj-desc">Competitive-style problem solving across data structures, algorithms and system design.</div>
        <div class="chips"><span class="chip">Algorithms</span><span class="chip">C++</span><span class="chip">C#</span><span class="chip">DS</span></div>
      </div>
    </div>
  </section>

  <hr class="divider">

  <!-- STACK -->
  <section id="stack">
    <div class="sec-header"><span class="sec-num">04 /</span><span class="sec-title">Technical Inventory</span></div>
    <div class="stack-grid">
      <div class="stack-group">
        <div class="stack-cat">ML / AI</div>
        <div class="stack-items">
          <span class="stack-item">TensorFlow</span><span class="stack-item">Keras</span><span class="stack-item">PyTorch</span><span class="stack-item">Scikit-learn</span><span class="stack-item">XGBoost</span><span class="stack-item">LightGBM</span><span class="stack-item">OpenCV</span><span class="stack-item">NLP</span><span class="stack-item">SMOTE</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-cat">Languages</div>
        <div class="stack-items">
          <span class="stack-item">Python</span><span class="stack-item">C++</span><span class="stack-item">C#</span><span class="stack-item">PHP</span><span class="stack-item">JavaScript</span><span class="stack-item">SQL</span><span class="stack-item">Embedded C</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-cat">Data</div>
        <div class="stack-items">
          <span class="stack-item">Pandas</span><span class="stack-item">NumPy</span><span class="stack-item">Power BI</span><span class="stack-item">Feature Eng.</span><span class="stack-item">EDA</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-cat">Systems</div>
        <div class="stack-items">
          <span class="stack-item">Linux</span><span class="stack-item">Docker</span><span class="stack-item">AWS</span><span class="stack-item">MLflow</span><span class="stack-item">Git</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-cat">Web</div>
        <div class="stack-items">
          <span class="stack-item">Flask</span><span class="stack-item">PHP</span><span class="stack-item">HTML</span><span class="stack-item">CSS</span><span class="stack-item">JavaScript</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-cat">Databases / ERP</div>
        <div class="stack-items">
          <span class="stack-item">PostgreSQL</span><span class="stack-item">MySQL</span><span class="stack-item">Odoo</span>
        </div>
      </div>
    </div>
  </section>

  <hr class="divider">

  <!-- CREDENTIALS -->
  <section id="credentials">
    <div class="sec-header"><span class="sec-num">05 /</span><span class="sec-title">Verified Credentials</span></div>
    <div class="cred-list">
      <div class="cred"><span class="cred-icon">🥈</span><span class="cred-text">Deep Minds AI Competition — 2nd Place ×2 · MSA University</span><span class="cred-date">MSA UNIV</span></div>
      <div class="cred"><span class="cred-icon">📜</span><span class="cred-text">Huawei HCIA-AI V4.0 Certification</span><span class="cred-date">SEP 2025</span></div>
      <div class="cred"><span class="cred-icon">☁️</span><span class="cred-text">AWS Educate — Cloud Foundations</span><span class="cred-date">APR 2024</span></div>
      <div class="cred"><span class="cred-icon">📚</span><span class="cred-text">Data Science &amp; AI Masters — Amazon Web Services</span><span class="cred-date">2024 — NOW</span></div>
      <div class="cred"><span class="cred-icon">📚</span><span class="cred-text">Master Data Science &amp; AI — Instant Academy / Udemy</span><span class="cred-date">2025 — NOW</span></div>
      <div class="cred"><span class="cred-icon">⚡</span><span class="cred-text">IEEE Student Member — MSA Student Branch</span><span class="cred-date">ACTIVE</span></div>
    </div>
  </section>

  <hr class="divider">

  <!-- CONTACT -->
  <section id="contact">
    <div class="sec-header"><span class="sec-num">06 /</span><span class="sec-title">Establish Connection</span></div>
    <div class="contact-card">
      <div>
        <div class="contact-title">Let's build something rigorous.</div>
        <div class="contact-sub">MSA University · Giza, Egypt<br>Arabic (native) · English (professional)</div>
      </div>
      <div class="contact-actions">
        <a class="primary" href="mailto:mohamed.bahaa5@msa.edu.eg">Hire ↗</a>
        <a href="https://linkedin.com/in/MB1382005" target="_blank" rel="noopener">LinkedIn</a>
        <a href="https://kaggle.com/MB1382005" target="_blank" rel="noopener">Kaggle</a>
        <a href="https://github.com/MB1382005" target="_blank" rel="noopener">GitHub</a>
      </div>
    </div>
  </section>

  <footer>© 2026 Mohammed Bahaa Attia · system.stable · built with precision · v1.0</footer>

</div>
</body>
</html>
