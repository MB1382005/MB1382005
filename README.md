<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mohammed Bahaa Attia — CS · AI/ML · Systems</title>
<meta name="description" content="Portfolio of Mohammed Bahaa Attia — CS student at MSA University specializing in AI/ML, software engineering, and systems.">
<meta property="og:title" content="Mohammed Bahaa Attia — CS · AI/ML · Systems">
<meta property="og:description" content="AI/ML engineer & CS student. Stacking ensembles, bilingual NLP, computer vision, systems.">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:      #0d0d0d;
    --bg2:     #141414;
    --bg3:     #1a1a1a;
    --border:  rgba(255,255,255,0.08);
    --border2: rgba(255,255,255,0.14);
    --text:    #e8e8e6;
    --muted:   #888884;
    --accent:  #7F77DD;
    --accent2: #1D9E75;
    --mono:    'JetBrains Mono', 'Fira Code', 'Courier New', monospace;
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

  /* NAV */
  nav {
    position: sticky; top: 0; z-index: 100;
    background: rgba(13,13,13,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 0.5px solid var(--border);
    padding: 1rem 0;
  }
  .nav-inner {
    display: flex; align-items: center; justify-content: space-between;
    max-width: 860px; margin: 0 auto; padding: 0 2rem;
  }
  .nav-logo { font-size: 12px; font-weight: 700; color: var(--accent); letter-spacing: 0.1em; }
  .nav-links { display: flex; gap: 1.5rem; }
  .nav-links a {
    font-size: 11px; color: var(--muted); letter-spacing: 0.06em;
    transition: color .15s;
  }
  .nav-links a:hover { color: var(--text); }
  .nav-cta {
    font-size: 11px; padding: 5px 14px;
    border: 0.5px solid var(--border2); border-radius: 6px;
    color: var(--text); transition: background .15s;
  }
  .nav-cta:hover { background: var(--bg3); }

  /* WRAP */
  .wrap { max-width: 860px; margin: 0 auto; padding: 0 2rem; }

  /* HERO */
  .hero { padding: 5rem 0 4rem; }

  .badge {
    display: inline-block;
    font-size: 10px; padding: 3px 12px;
    border: 0.5px solid var(--accent2);
    color: var(--accent2); border-radius: 999px;
    letter-spacing: 0.08em; margin-bottom: 1.5rem;
  }
  .badge::before { content: '● '; font-size: 8px; }

  h1 {
    font-size: clamp(28px, 5vw, 48px);
    font-weight: 700; letter-spacing: -0.02em;
    line-height: 1.05; margin-bottom: 1rem; color: #fff;
  }

  .hero-sub {
    font-size: 13px; color: var(--muted);
    max-width: 500px; line-height: 1.7; margin-bottom: 1.75rem;
  }

  .hero-links { display: flex; gap: .625rem; flex-wrap: wrap; margin-bottom: 3rem; }
  .hero-links a {
    display: flex; align-items: center; gap: 6px;
    font-size: 11px; color: var(--muted);
    padding: 5px 12px;
    border: 0.5px solid var(--border); border-radius: 6px;
    transition: all .15s;
  }
  .hero-links a:hover { color: var(--text); border-color: var(--border2); background: var(--bg3); }

  /* STATS */
  .stats {
    display: grid; grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 10px; margin-bottom: 0;
  }
  .stat {
    background: var(--bg2);
    border: 0.5px solid var(--border); border-radius: 8px;
    padding: .875rem 1rem;
  }
  .stat-num { font-size: 20px; font-weight: 700; color: var(--accent); }
  .stat-label { font-size: 10px; color: var(--muted); margin-top: 4px; line-height: 1.4; }

  /* DIVIDER */
  .divider { border: none; border-top: 0.5px solid var(--border); margin: 3.5rem 0; }

  /* SECTION HEADER */
  .sec-header { display: flex; align-items: baseline; gap: .75rem; margin-bottom: 1.5rem; }
  .sec-num { font-size: 10px; color: var(--muted); letter-spacing: 0.1em; }
  .sec-title { font-size: 12px; font-weight: 500; letter-spacing: 0.08em; color: var(--text); }

  /* PROJECTS GRID */
  .projects-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 12px;
  }

  .proj-card {
    background: var(--bg2);
    border: 0.5px solid var(--border); border-radius: 8px;
    padding: 1.25rem; position: relative;
    transition: border-color .2s, background .2s;
    cursor: pointer;
  }
  .proj-card:hover { border-color: var(--border2); background: var(--bg3); }

  .proj-idx { font-size: 10px; color: var(--muted); margin-bottom: .5rem; }
  .proj-tag {
    display: inline-block; font-size: 9px; padding: 2px 8px;
    border: 0.5px solid var(--accent); color: var(--accent);
    border-radius: 4px; letter-spacing: 0.06em; margin-bottom: .75rem;
  }
  .proj-title { font-size: 13px; font-weight: 500; color: #fff; margin-bottom: .5rem; }
  .proj-desc { font-size: 11px; color: var(--muted); line-height: 1.6; margin-bottom: 1rem; }

  .proj-chips { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 1rem; }
  .chip {
    font-size: 9px; padding: 2px 7px;
    background: var(--bg3); border: 0.5px solid var(--border);
    border-radius: 3px; color: var(--muted); letter-spacing: 0.03em;
  }
  .proj-link {
    font-size: 10px; color: var(--accent); letter-spacing: 0.05em;
    display: inline-flex; align-items: center; gap: 4px;
  }
  .proj-link:hover { text-decoration: underline; }

  /* STACK */
  .stack-groups { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 12px; }
  .stack-group {
    background: var(--bg2); border: 0.5px solid var(--border);
    border-radius: 8px; padding: 1rem;
  }
  .stack-group-title { font-size: 10px; color: var(--muted); letter-spacing: 0.1em; margin-bottom: .75rem; }
  .stack-items { display: flex; flex-wrap: wrap; gap: 6px; }
  .stack-item {
    font-size: 10px; padding: 3px 8px;
    border: 0.5px solid var(--border); border-radius: 3px;
    color: var(--muted); letter-spacing: 0.02em;
    transition: color .15s, border-color .15s;
  }
  .stack-item:hover { color: var(--text); border-color: var(--border2); }

  /* CREDENTIALS */
  .creds { display: flex; flex-direction: column; gap: 8px; }
  .cred {
    display: flex; align-items: center; gap: 1rem;
    background: var(--bg2); border: 0.5px solid var(--border);
    border-radius: 8px; padding: .875rem 1rem;
    transition: border-color .2s;
  }
  .cred:hover { border-color: var(--border2); }
  .cred-n { font-size: 10px; color: var(--muted); width: 24px; flex-shrink: 0; }
  .cred-body { flex: 1; }
  .cred-title { font-size: 12px; font-weight: 500; color: var(--text); }
  .cred-org { font-size: 10px; color: var(--muted); margin-top: 2px; }
  .cred-date { font-size: 10px; color: var(--muted); letter-spacing: 0.05em; flex-shrink: 0; }

  /* CONTACT */
  .contact-box {
    background: var(--bg2); border: 0.5px solid var(--border);
    border-radius: 8px; padding: 2rem;
  }
  .contact-headline { font-size: 18px; font-weight: 700; color: #fff; margin-bottom: 1.5rem; }
  .contact-headline span { color: var(--accent); }
  .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.25rem; margin-bottom: 1.5rem; }
  .contact-field label { font-size: 10px; color: var(--muted); display: block; margin-bottom: 4px; letter-spacing: 0.08em; }
  .contact-field span { font-size: 12px; color: var(--text); }
  .contact-field a { color: var(--accent); }
  .contact-field a:hover { text-decoration: underline; }
  .socials { display: flex; gap: 8px; flex-wrap: wrap; }
  .social-btn {
    font-size: 10px; padding: 6px 14px;
    border: 0.5px solid var(--border2); border-radius: 6px;
    color: var(--muted); letter-spacing: 0.06em;
    transition: all .15s;
  }
  .social-btn:hover { color: var(--text); background: var(--bg3); }

  /* FOOTER */
  footer {
    text-align: center; padding: 2rem;
    font-size: 10px; color: var(--muted);
    border-top: 0.5px solid var(--border); margin-top: 3.5rem;
    letter-spacing: 0.06em;
  }

  /* AVATAR */
  .avatar-wrap { display: flex; align-items: center; gap: 1rem; margin-bottom: 1.5rem; }
  .avatar {
    width: 52px; height: 52px; border-radius: 50%;
    border: 1.5px solid var(--border2); object-fit: cover;
  }
  .avatar-name { font-size: 13px; font-weight: 500; color: #fff; }
  .avatar-handle { font-size: 11px; color: var(--muted); }

  @media (max-width: 640px) {
    .stats { grid-template-columns: repeat(2, 1fr); }
    .contact-grid { grid-template-columns: 1fr; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-inner">
    <span class="nav-logo">M.attia.system</span>
    <div class="nav-links">
      <a href="#projects">Projects</a>
      <a href="#stack">Stack</a>
      <a href="#credentials">Credentials</a>
      <a href="#contact">Contact</a>
    </div>
    <a href="mailto:mohamed.bahaa5@msa.edu.eg" class="nav-cta">Hire ↗</a>
  </div>
</nav>

<main class="wrap">

  <!-- HERO -->
  <section class="hero" id="top">
    <div class="avatar-wrap">
      <img class="avatar" src="https://avatars.githubusercontent.com/u/147273516?v=4" alt="Mohammed Bahaa Attia">
      <div>
        <div class="avatar-name">Mohammed Bahaa Attia</div>
        <div class="avatar-handle">@MB1382005</div>
      </div>
    </div>

    <div class="badge">Available for Internships &amp; Research</div>

    <h1>MOHAMMED<br>BAHAA ATTIA</h1>

    <p class="hero-sub">
      CS student specializing in AI/ML, software engineering &amp; systems.
      Bridging mathematical theory and high-performance software — at MSA University, Giza.
    </p>

    <div class="hero-links">
      <a href="https://github.com/MB1382005" target="_blank">
        <svg width="12" height="12" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.167 6.839 9.49.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.604-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.464-1.11-1.464-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0112 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.202 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.578.688.48C19.138 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"/></svg>
        GitHub
      </a>
      <a href="https://linkedin.com/in/MB1382005" target="_blank">
        <svg width="12" height="12" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"/><circle cx="4" cy="4" r="2"/></svg>
        LinkedIn
      </a>
      <a href="https://kaggle.com/MB1382005" target="_blank">
        <svg width="12" height="12" viewBox="0 0 24 24" fill="currentColor"><path d="M18.825 23.859c-.022.092-.117.141-.281.141h-3.139c-.187 0-.351-.082-.492-.248l-5.178-6.589-1.448 1.374v5.111c0 .235-.117.352-.351.352H5.505c-.236 0-.354-.117-.354-.352V.353c0-.233.118-.353.354-.353h2.431c.234 0 .351.12.351.353v14.343l6.203-6.272c.165-.165.33-.246.495-.246h3.239c.144 0 .236.06.285.18.046.149.034.255-.036.315l-6.555 6.344 6.836 8.507c.095.104.117.208.07.334z"/></svg>
        Kaggle
      </a>
      <a href="mailto:mohamed.bahaa5@msa.edu.eg">
        <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Email
      </a>
    </div>

    <div class="stats">
      <div class="stat">
        <div class="stat-num">3.69</div>
        <div class="stat-label">GPA / 4.0<br>MSA University</div>
      </div>
      <div class="stat">
        <div class="stat-num">~90%</div>
        <div class="stat-label">Courses graded<br>A / A−</div>
      </div>
      <div class="stat">
        <div class="stat-num">2× 🥈</div>
        <div class="stat-label">Deep Minds AI<br>winner</div>
      </div>
      <div class="stat">
        <div class="stat-num">83.5%</div>
        <div class="stat-label">Best model AUC<br>301K records</div>
      </div>
    </div>
  </section>

  <hr class="divider">

  <!-- PROJECTS — INTELLIGENCE -->
  <section id="projects">
    <div class="sec-header">
      <span class="sec-num">01 /</span>
      <span class="sec-title">INTELLIGENCE &amp; LOGIC</span>
    </div>
    <div class="projects-grid">

      <a href="https://github.com/MB1382005/heart-disease-prediction" target="_blank" class="proj-card">
        <div class="proj-idx">[01]</div>
        <div class="proj-tag">AI / ML</div>
        <div class="proj-title">Heart Disease Prediction</div>
        <div class="proj-desc">5-model stacking ensemble (XGBoost · LightGBM · Scikit-learn) on 301,717 CDC samples. Engineered 15 features and applied SMOTE on a 91/9 class imbalance — achieving 53.8% recall on a 60K held-out set.</div>
        <div class="proj-chips">
          <span class="chip">XGBoost</span><span class="chip">LightGBM</span><span class="chip">SMOTE</span><span class="chip">Scikit-learn</span>
        </div>
        <span class="proj-link">View source →</span>
      </a>

      <a href="https://github.com/MB1382005/laptop-recommender-system" target="_blank" class="proj-card">
        <div class="proj-idx">[02]</div>
        <div class="proj-tag">NLP · IR</div>
        <div class="proj-title">AI Laptop Recommender + IR System</div>
        <div class="proj-desc">Bilingual Arabic/English engine — TensorFlow embeddings, cosine similarity, BM25 IR fallback, Flask web app with interactive EDA dashboard.</div>
        <div class="proj-chips">
          <span class="chip">TensorFlow</span><span class="chip">BM25</span><span class="chip">Flask</span><span class="chip">Arabic NLP</span>
        </div>
        <span class="proj-link">View source →</span>
      </a>

      <a href="https://github.com/MB1382005/brain-tumor-classification" target="_blank" class="proj-card">
        <div class="proj-idx">[03]</div>
        <div class="proj-tag">CNN · Computer Vision</div>
        <div class="proj-title">Brain Tumor MRI Classifier</div>
        <div class="proj-desc">Multi-class tumor classification from MRI scans with a full image preprocessing pipeline — normalization, augmentation, and feature extraction.</div>
        <div class="proj-chips">
          <span class="chip">CNN</span><span class="chip">OpenCV</span><span class="chip">Keras</span>
        </div>
        <span class="proj-link">View source →</span>
      </a>

      <a href="https://github.com/MB1382005/maze-search-algorithms" target="_blank" class="proj-card">
        <div class="proj-idx">[04]</div>
        <div class="proj-tag">BFS · DFS · A* · Classical AI</div>
        <div class="proj-title">Maze Solver — Search Algorithms</div>
        <div class="proj-desc">BFS, DFS and A* implemented with a step-by-step Tkinter visualization for live pathfinding comparison.</div>
        <div class="proj-chips">
          <span class="chip">A*</span><span class="chip">BFS</span><span class="chip">DFS</span><span class="chip">Tkinter</span>
        </div>
        <span class="proj-link">View source →</span>
      </a>

    </div>
  </section>

  <hr class="divider">

  <!-- PROJECTS — SYSTEMS -->
  <section>
    <div class="sec-header">
      <span class="sec-num">02 /</span>
      <span class="sec-title">SOFTWARE ENGINEERING</span>
    </div>
    <div class="projects-grid">

      <div class="proj-card">
        <div class="proj-idx">[05]</div>
        <div class="proj-tag">Full-stack ERP</div>
        <div class="proj-title">Pharmacy Management System</div>
        <div class="proj-desc">PHP/MySQL platform with authentication, inventory &amp; reviews modules, an AI chatbot for medication alternatives, and a clean OOP architecture.</div>
        <div class="proj-chips">
          <span class="chip">PHP</span><span class="chip">MySQL</span><span class="chip">OOP</span><span class="chip">AI Chatbot</span>
        </div>
      </div>

      <div class="proj-card">
        <div class="proj-idx">[06]</div>
        <div class="proj-tag">Business Systems</div>
        <div class="proj-title">Odoo ERP Customization</div>
        <div class="proj-desc">Business-process configuration and custom module development on Odoo.</div>
        <div class="proj-chips">
          <span class="chip">Odoo</span><span class="chip">Python</span><span class="chip">ERP</span>
        </div>
      </div>

      <a href="https://github.com/MB1382005/cpp-hotel-booking-system" target="_blank" class="proj-card">
        <div class="proj-idx">[07]</div>
        <div class="proj-tag">Systems Programming</div>
        <div class="proj-title">Hotel Booking System</div>
        <div class="proj-desc">OOP design, file I/O and application architecture implemented in C++.</div>
        <div class="proj-chips">
          <span class="chip">C++</span><span class="chip">OOP</span><span class="chip">File I/O</span>
        </div>
        <span class="proj-link">View source →</span>
      </a>

      <a href="https://github.com/MB1382005/csharp-platformer-game" target="_blank" class="proj-card">
        <div class="proj-idx">[08]</div>
        <div class="proj-tag">Game Programming</div>
        <div class="proj-title">C# Platformer Game</div>
        <div class="proj-desc">2D platformer in C# — game loop, collision detection, and OOP design patterns.</div>
        <div class="proj-chips">
          <span class="chip">C#</span><span class="chip">Game Loop</span><span class="chip">OOP</span>
        </div>
        <span class="proj-link">View source →</span>
      </a>

    </div>
  </section>

  <hr class="divider">

  <!-- STACK -->
  <section id="stack">
    <div class="sec-header">
      <span class="sec-num">04 /</span>
      <span class="sec-title">TECHNICAL INVENTORY — n = 36 components</span>
    </div>
    <div class="stack-groups">
      <div class="stack-group">
        <div class="stack-group-title">ML / AI</div>
        <div class="stack-items">
          <span class="stack-item">TensorFlow</span>
          <span class="stack-item">Keras</span>
          <span class="stack-item">PyTorch</span>
          <span class="stack-item">Scikit-learn</span>
          <span class="stack-item">XGBoost</span>
          <span class="stack-item">LightGBM</span>
          <span class="stack-item">OpenCV</span>
          <span class="stack-item">NLP</span>
          <span class="stack-item">SMOTE</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Languages</div>
        <div class="stack-items">
          <span class="stack-item">Python</span>
          <span class="stack-item">C++</span>
          <span class="stack-item">C#</span>
          <span class="stack-item">PHP</span>
          <span class="stack-item">JavaScript</span>
          <span class="stack-item">SQL</span>
          <span class="stack-item">Embedded C</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Data</div>
        <div class="stack-items">
          <span class="stack-item">Pandas</span>
          <span class="stack-item">NumPy</span>
          <span class="stack-item">Power BI</span>
          <span class="stack-item">Feature Eng.</span>
          <span class="stack-item">EDA</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Systems</div>
        <div class="stack-items">
          <span class="stack-item">Linux</span>
          <span class="stack-item">Docker</span>
          <span class="stack-item">AWS</span>
          <span class="stack-item">MLflow</span>
          <span class="stack-item">Git</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Web</div>
        <div class="stack-items">
          <span class="stack-item">Flask</span>
          <span class="stack-item">PHP</span>
          <span class="stack-item">HTML</span>
          <span class="stack-item">CSS</span>
          <span class="stack-item">JavaScript</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Databases / ERP</div>
        <div class="stack-items">
          <span class="stack-item">PostgreSQL</span>
          <span class="stack-item">MySQL</span>
          <span class="stack-item">Odoo</span>
        </div>
      </div>
    </div>
  </section>

  <hr class="divider">

  <!-- CREDENTIALS -->
  <section id="credentials">
    <div class="sec-header">
      <span class="sec-num">05 /</span>
      <span class="sec-title">VERIFIED CREDENTIALS</span>
    </div>
    <div class="creds">
      <div class="cred">
        <span class="cred-n">01</span>
        <div class="cred-body">
          <div class="cred-title">Deep Minds AI Competition — 2nd Place ×2</div>
          <div class="cred-org">MSA University</div>
        </div>
        <span class="cred-date">MSA UNIV</span>
      </div>
      <div class="cred">
        <span class="cred-n">02</span>
        <div class="cred-body">
          <div class="cred-title">Huawei HCIA-AI V4.0 Certification</div>
        </div>
        <span class="cred-date">SEP 2025</span>
      </div>
      <div class="cred">
        <span class="cred-n">03</span>
        <div class="cred-body">
          <div class="cred-title">AWS Educate — Cloud Foundations</div>
        </div>
        <span class="cred-date">APR 2024</span>
      </div>
      <div class="cred">
        <span class="cred-n">04</span>
        <div class="cred-body">
          <div class="cred-title">Data Science &amp; AI Masters — AWS</div>
        </div>
        <span class="cred-date">2024 — NOW</span>
      </div>
      <div class="cred">
        <span class="cred-n">05</span>
        <div class="cred-body">
          <div class="cred-title">Master Data Science &amp; AI — Instant Academy / Udemy</div>
        </div>
        <span class="cred-date">2025 — NOW</span>
      </div>
      <div class="cred">
        <span class="cred-n">06</span>
        <div class="cred-body">
          <div class="cred-title">IEEE Student Member — MSA Student Branch</div>
        </div>
        <span class="cred-date">ACTIVE</span>
      </div>
    </div>
  </section>

  <hr class="divider">

  <!-- CONTACT -->
  <section id="contact">
    <div class="sec-header">
      <span class="sec-num">06 /</span>
      <span class="sec-title">ESTABLISH CONNECTION</span>
    </div>
    <div class="contact-box">
      <div class="contact-headline">Let's build <span>something rigorous.</span></div>
      <div class="contact-grid">
        <div class="contact-field">
          <label>Email</label>
          <span><a href="mailto:mohamed.bahaa5@msa.edu.eg">mohamed.bahaa5@msa.edu.eg</a></span>
        </div>
        <div class="contact-field">
          <label>Location</label>
          <span>MSA University · Giza, Egypt</span>
        </div>
        <div class="contact-field">
          <label>Languages</label>
          <span>Arabic (native) · English (professional)</span>
        </div>
        <div class="contact-field">
          <label>Status</label>
          <span style="color: var(--accent2);">● Available for hire</span>
        </div>
      </div>
      <div class="socials">
        <a href="https://linkedin.com/in/MB1382005" target="_blank" class="social-btn">IN ↗</a>
        <a href="https://kaggle.com/MB1382005" target="_blank" class="social-btn">KG ↗</a>
        <a href="https://github.com/MB1382005" target="_blank" class="social-btn">GH ↗</a>
        <a href="mailto:mohamed.bahaa5@msa.edu.eg" class="social-btn">Email ↗</a>
      </div>
    </div>
  </section>

</main>

<footer>
  © 2026 Mohammed Bahaa Attia · System.stable · Built with precision · v1.0
</footer>

</body>
</html>
