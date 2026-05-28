<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Micole Kurt Gonda — Developer Profile</title>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=JetBrains+Mono:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg:        #080808;
      --bg-2:      #111111;
      --bg-3:      #1a1a1a;
      --border:    #1e1e1e;
      --border-2:  #2e2e2e;
      --text:      #f0ede8;
      --text-muted:#666;
      --text-dim:  #888;
      --amber:     #f59e0b;
      --amber-dim: #92610a;
      --amber-bright:#fbbf24;
      --green:     #22c55e;
      --red:       #ef4444;
      --blue:      #60a5fa;
      --purple:    #a78bfa;
    }

    body {
      font-family: 'Syne', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      -webkit-font-smoothing: antialiased;
    }

    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(rgba(245,158,11,0.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(245,158,11,0.025) 1px, transparent 1px);
      background-size: 56px 56px;
      pointer-events: none;
      z-index: 0;
    }

    .container {
      max-width: 940px;
      margin: 0 auto;
      padding: 0 2rem;
      position: relative;
      z-index: 1;
    }

    /* ── HERO ── */
    .hero {
      padding: 5.5rem 0 4rem;
      border-bottom: 1px solid var(--border);
    }

    .status-pill {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: rgba(245,158,11,0.07);
      border: 1px solid rgba(245,158,11,0.22);
      border-radius: 100px;
      padding: 7px 18px;
      font-family: 'JetBrains Mono', monospace;
      font-size: 10.5px;
      letter-spacing: 0.13em;
      text-transform: uppercase;
      color: var(--amber);
      margin-bottom: 2.25rem;
    }

    .status-dot {
      width: 6px;
      height: 6px;
      border-radius: 50%;
      background: var(--amber);
      animation: pulse 2.2s ease-in-out infinite;
      flex-shrink: 0;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.45; transform: scale(0.75); }
    }

    .hero h1 {
      font-family: 'Syne', sans-serif;
      font-size: clamp(3.2rem, 9vw, 6rem);
      font-weight: 800;
      letter-spacing: -0.035em;
      line-height: 0.92;
      color: var(--text);
      margin-bottom: 0;
    }

    .hero h1 .accent { color: var(--amber); }

    .hero-sub {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11.5px;
      color: var(--text-muted);
      letter-spacing: 0.09em;
      text-transform: uppercase;
      margin: 1.25rem 0 2.5rem;
    }

    .hero-meta {
      display: flex;
      gap: 2.5rem;
      margin-bottom: 2.5rem;
      flex-wrap: wrap;
    }

    .meta-item { display: flex; flex-direction: column; gap: 3px; }

    .meta-label {
      font-family: 'JetBrains Mono', monospace;
      font-size: 9.5px;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.11em;
    }

    .meta-value {
      font-size: 13.5px;
      font-weight: 600;
      color: var(--text);
    }

    .tags { display: flex; flex-wrap: wrap; gap: 7px; }

    .tag {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      padding: 5px 12px;
      border-radius: 4px;
      border: 1px solid var(--border-2);
      color: var(--text-dim);
      background: var(--bg-2);
      transition: border-color 0.18s, color 0.18s, background 0.18s;
      cursor: default;
    }

    .tag:hover {
      border-color: rgba(245,158,11,0.35);
      color: var(--amber);
      background: rgba(245,158,11,0.05);
    }

    .tag.hi {
      border-color: rgba(245,158,11,0.28);
      color: var(--amber);
      background: rgba(245,158,11,0.06);
    }

    /* ── SECTION SHELL ── */
    .section {
      padding: 3.5rem 0;
      border-bottom: 1px solid var(--border);
    }

    .section-header {
      display: flex;
      align-items: center;
      gap: 14px;
      margin-bottom: 2rem;
    }

    .section-num {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      color: var(--amber);
      letter-spacing: 0.04em;
    }

    .section-title {
      font-size: 10.5px;
      font-weight: 600;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--text-muted);
    }

    .section-line {
      flex: 1;
      height: 1px;
      background: var(--border);
    }

    /* ── GRID PANEL (reusable) ── */
    .grid-panel {
      display: grid;
      gap: 1px;
      background: var(--border);
      border: 1px solid var(--border);
      border-radius: 8px;
      overflow: hidden;
    }

    .grid-panel.cols-2 { grid-template-columns: 1fr 1fr; }
    .grid-panel.cols-3 { grid-template-columns: repeat(3, 1fr); }
    .grid-panel.cols-4 { grid-template-columns: repeat(4, 1fr); }

    .panel-cell {
      background: var(--bg);
      padding: 1.4rem 1.5rem;
      transition: background 0.18s;
    }

    .panel-cell:hover { background: var(--bg-2); }

    .cell-key {
      font-family: 'JetBrains Mono', monospace;
      font-size: 9.5px;
      color: var(--amber);
      text-transform: uppercase;
      letter-spacing: 0.11em;
      margin-bottom: 7px;
    }

    .cell-val {
      font-size: 13.5px;
      color: var(--text);
      font-weight: 500;
      line-height: 1.4;
    }

    .cell-title {
      font-family: 'JetBrains Mono', monospace;
      font-size: 9.5px;
      color: var(--amber);
      text-transform: uppercase;
      letter-spacing: 0.11em;
      margin-bottom: 1rem;
      padding-bottom: 0.7rem;
      border-bottom: 1px solid var(--border);
    }

    /* ── PROJECTS ── */
    .project-type {
      font-family: 'JetBrains Mono', monospace;
      font-size: 9px;
      text-transform: uppercase;
      letter-spacing: 0.13em;
      color: var(--amber);
    }

    .live-badge {
      display: inline-flex;
      align-items: center;
      gap: 5px;
      font-family: 'JetBrains Mono', monospace;
      font-size: 9px;
      color: var(--green);
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .live-dot {
      width: 5px;
      height: 5px;
      border-radius: 50%;
      background: var(--green);
      animation: pulse 2s infinite;
    }

    .project-name {
      font-size: 14.5px;
      font-weight: 700;
      color: var(--text);
      line-height: 1.25;
    }

    .project-location {
      font-size: 11.5px;
      color: var(--text-muted);
      font-family: 'JetBrains Mono', monospace;
    }

    .project-features {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 4px;
      flex: 1;
    }

    .project-features li {
      font-size: 12px;
      color: var(--text-dim);
      display: flex;
      align-items: flex-start;
      gap: 7px;
    }

    .project-features li::before {
      content: '—';
      color: var(--border-2);
      flex-shrink: 0;
    }

    .project-stack { display: flex; flex-wrap: wrap; gap: 4px; }

    .project-stack span {
      font-family: 'JetBrains Mono', monospace;
      font-size: 9px;
      padding: 3px 7px;
      border-radius: 3px;
      background: var(--bg-3);
      border: 1px solid var(--border-2);
      color: var(--text-dim);
    }

    .project-link {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10px;
      color: var(--amber);
      text-decoration: none;
      transition: color 0.15s;
    }

    .project-link:hover { color: var(--amber-bright); }

    /* ── PATTERNS TABLE ── */
    .pattern-wrap {
      border: 1px solid var(--border);
      border-radius: 8px;
      overflow: hidden;
    }

    .pattern-head {
      display: grid;
      grid-template-columns: 44px 1fr 130px 1fr;
      background: var(--bg-3);
      border-bottom: 1px solid var(--border);
    }

    .pattern-head > * {
      padding: 0.65rem 1.2rem;
      font-family: 'JetBrains Mono', monospace;
      font-size: 9px;
      text-transform: uppercase;
      letter-spacing: 0.11em;
      color: var(--text-muted);
      border-right: 1px solid var(--border);
    }

    .pattern-head > *:last-child { border-right: none; }

    .pattern-row {
      display: grid;
      grid-template-columns: 44px 1fr 130px 1fr;
      border-bottom: 1px solid var(--border);
      transition: background 0.18s;
    }

    .pattern-row:last-child { border-bottom: none; }
    .pattern-row:hover { background: var(--bg-2); }

    .pattern-row > * {
      padding: 1rem 1.2rem;
      border-right: 1px solid var(--border);
      display: flex;
      align-items: center;
    }

    .pattern-row > *:last-child { border-right: none; }

    .p-num {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      color: var(--text-muted);
      justify-content: center;
    }

    .p-name {
      font-size: 13px;
      font-weight: 600;
      color: var(--text);
    }

    .p-name a {
      color: inherit;
      text-decoration: none;
      transition: color 0.15s;
    }

    .p-name a:hover { color: var(--amber); }

    .p-cat {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10.5px;
    }

    .p-behavioral { color: var(--blue); }
    .p-structural  { color: var(--purple); }
    .p-creational  { color: var(--green); }
    .p-principles  { color: var(--amber); }

    .p-desc {
      font-size: 12px;
      color: var(--text-dim);
      line-height: 1.45;
    }

    /* ── CERTS ── */
    .cert-issuer {
      font-family: 'JetBrains Mono', monospace;
      font-size: 9.5px;
      text-transform: uppercase;
      letter-spacing: 0.11em;
      color: var(--amber);
      margin-bottom: 6px;
    }

    .cert-name {
      font-size: 13px;
      font-weight: 600;
      color: var(--text);
      line-height: 1.35;
      margin-bottom: 8px;
    }

    .cert-link {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10px;
      color: var(--text-muted);
      text-decoration: none;
      transition: color 0.15s;
    }

    .cert-link:hover { color: var(--amber); }

    /* ── PROFICIENCY ── */
    .prof-wrap {
      border: 1px solid var(--border);
      border-radius: 8px;
      overflow: hidden;
    }

    .prof-item {
      display: grid;
      grid-template-columns: 230px 1fr 40px;
      align-items: center;
      gap: 1.25rem;
      padding: 0.8rem 1.25rem;
      background: var(--bg);
      border-bottom: 1px solid var(--border);
      transition: background 0.18s;
    }

    .prof-item:last-child { border-bottom: none; }
    .prof-item:hover { background: var(--bg-2); }

    .prof-name {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11.5px;
      color: var(--text-dim);
    }

    .prof-track {
      height: 2px;
      background: var(--bg-3);
      border-radius: 2px;
      overflow: hidden;
    }

    .prof-fill {
      height: 100%;
      border-radius: 2px;
      background: var(--amber);
    }

    .prof-pct {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10.5px;
      color: var(--text-muted);
      text-align: right;
    }

    /* ── STATUS ── */
    .status-col-title {
      font-family: 'JetBrains Mono', monospace;
      font-size: 9.5px;
      text-transform: uppercase;
      letter-spacing: 0.11em;
      margin-bottom: 1rem;
      padding-bottom: 0.7rem;
      border-bottom: 1px solid var(--border);
    }

    .s-active  { color: var(--green); }
    .s-blocked { color: var(--red); }

    .status-item {
      display: flex;
      align-items: flex-start;
      gap: 9px;
      padding: 5px 0;
      font-size: 12.5px;
      color: var(--text-dim);
      line-height: 1.45;
    }

    .status-item .si-icon {
      font-family: 'JetBrains Mono', monospace;
      font-size: 12px;
      flex-shrink: 0;
      margin-top: 1px;
    }

    .si-icon.plus  { color: var(--green); }
    .si-icon.cross { color: var(--red); }

    /* ── FOOTER ── */
    .footer {
      padding: 3rem 0;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .footer-name {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      color: var(--text-muted);
    }

    .footer-link {
      font-family: 'JetBrains Mono', monospace;
      font-size: 12px;
      color: var(--amber);
      text-decoration: none;
      transition: color 0.15s;
    }

    .footer-link:hover { color: var(--amber-bright); }

    .footer-meta {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      color: var(--text-muted);
      text-align: right;
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 720px) {
      .grid-panel.cols-4 { grid-template-columns: 1fr 1fr; }
      .grid-panel.cols-3 { grid-template-columns: 1fr; }
      .grid-panel.cols-2 { grid-template-columns: 1fr; }
      .pattern-head,
      .pattern-row { grid-template-columns: 36px 1fr 100px; }
      .pattern-head > *:last-child,
      .pattern-row  > *:last-child { display: none; }
      .prof-item { grid-template-columns: 1fr 1fr 36px; }
      .hero h1 { font-size: 2.8rem; }
      .footer { flex-direction: column; gap: 1rem; text-align: center; }
    }
  </style>
</head>
<body>
<div class="container">

  <!-- ── HERO ── -->
  <section class="hero">
    <div class="status-pill">
      <span class="status-dot"></span>
      Software Engineering in Process · Still Learning
    </div>

    <h1>MICOLE<br><span class="accent">KURT</span><br>GONDA</h1>

    <p class="hero-sub">BS Computer Science &nbsp;·&nbsp; New Era University &nbsp;·&nbsp; 3rd Year &nbsp;·&nbsp; Quezon City, PH</p>

    <div class="hero-meta">
      <div class="meta-item">
        <span class="meta-label">Primary</span>
        <span class="meta-value">Java</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">Web</span>
        <span class="meta-value">React + Vite</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">Backend</span>
        <span class="meta-value">Supabase · Firebase</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">Paradigm</span>
        <span class="meta-value">OOP · SOLID · GoF</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">Target</span>
        <span class="meta-value">Full-Stack Dev</span>
      </div>
    </div>

    <div class="tags">
      <span class="tag hi">Java</span>
      <span class="tag hi">React</span>
      <span class="tag hi">Supabase</span>
      <span class="tag">Firebase</span>
      <span class="tag">Oracle Cloud</span>
      <span class="tag">PostgreSQL</span>
      <span class="tag">IBM DB2</span>
      <span class="tag">Netlify</span>
      <span class="tag">Vercel</span>
    </div>
  </section>

  <!-- ── 01 FOCUS ── -->
  <section class="section">
    <div class="section-header">
      <span class="section-num">01</span>
      <span class="section-title">Focus</span>
      <span class="section-line"></span>
    </div>
    <div class="grid-panel cols-2">
      <div class="panel-cell">
        <div class="cell-key">paradigm</div>
        <div class="cell-val">OOP · SOLID Principles · GoF Design Patterns</div>
      </div>
      <div class="panel-cell">
        <div class="cell-key">currently</div>
        <div class="cell-val">Design Patterns arc — Creational · Structural · Behavioral</div>
      </div>
      <div class="panel-cell">
        <div class="cell-key">building</div>
        <div class="cell-val">Client websites · Academic full-stack systems</div>
      </div>
      <div class="panel-cell">
        <div class="cell-key">targeting</div>
        <div class="cell-val">Full-Stack Developer — React · Node · PostgreSQL</div>
      </div>
    </div>
  </section>

  <!-- ── 02 STACK ── -->
  <section class="section">
    <div class="section-header">
      <span class="section-num">02</span>
      <span class="section-title">Stack</span>
      <span class="section-line"></span>
    </div>
    <div class="grid-panel cols-4">
      <div class="panel-cell">
        <div class="cell-title">Languages</div>
        <div class="tags" style="flex-direction:column;gap:6px">
          <span class="tag">Java</span>
          <span class="tag">JavaScript</span>
          <span class="tag">Python</span>
          <span class="tag">HTML5</span>
          <span class="tag">CSS3</span>
          <span class="tag">SQL</span>
          <span class="tag">PL/pgSQL</span>
        </div>
      </div>
      <div class="panel-cell">
        <div class="cell-title">Frameworks</div>
        <div class="tags" style="flex-direction:column;gap:6px">
          <span class="tag">React 18</span>
          <span class="tag">Tailwind CSS v3</span>
          <span class="tag">React Router v6</span>
          <span class="tag">Context API</span>
          <span class="tag">Vite</span>
          <span class="tag">Vitest</span>
          <span class="tag">ESLint</span>
        </div>
      </div>
      <div class="panel-cell">
        <div class="cell-title">Tooling</div>
        <div class="tags" style="flex-direction:column;gap:6px">
          <span class="tag">VS Code</span>
          <span class="tag">Eclipse IDE</span>
          <span class="tag">Git</span>
          <span class="tag">GitHub</span>
          <span class="tag">Lucidchart</span>
          <span class="tag">UML</span>
        </div>
      </div>
      <div class="panel-cell">
        <div class="cell-title">Cloud & Data</div>
        <div class="tags" style="flex-direction:column;gap:6px">
          <span class="tag">Supabase</span>
          <span class="tag">Firebase</span>
          <span class="tag">Google OAuth 2.0</span>
          <span class="tag">PostgreSQL</span>
          <span class="tag">IBM DB2</span>
          <span class="tag">Oracle Cloud</span>
          <span class="tag">Netlify / Vercel</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ── 03 LIVE PROJECTS ── -->
  <section class="section">
    <div class="section-header">
      <span class="section-num">03</span>
      <span class="section-title">Live Projects</span>
      <span class="section-line"></span>
    </div>
    <div class="grid-panel cols-3">

      <div class="panel-cell" style="display:flex;flex-direction:column;gap:0.8rem">
        <div style="display:flex;justify-content:space-between;align-items:center">
          <span class="project-type">Business Website</span>
          <span class="live-badge"><span class="live-dot"></span>Live</span>
        </div>
        <div class="project-name">QUEENee Glass &amp; Aluminum Works</div>
        <div class="project-location">General Santos City, PH</div>
        <ul class="project-features">
          <li>Product catalog</li>
          <li>Before/after install slider</li>
          <li>Direct contact</li>
        </ul>
        <div class="project-stack">
          <span>HTML5</span><span>CSS3</span><span>JavaScript</span><span>Netlify</span>
        </div>
        <a href="https://queenee-glass-aluminum-works.netlify.app/" class="project-link" target="_blank">
          queenee-glass-aluminum-works.netlify.app ↗
        </a>
      </div>

      <div class="panel-cell" style="display:flex;flex-direction:column;gap:0.8rem">
        <div style="display:flex;justify-content:space-between;align-items:center">
          <span class="project-type">Corporate Website</span>
          <span class="live-badge"><span class="live-dot"></span>Live</span>
        </div>
        <div class="project-name">OSMONT Water Technologies</div>
        <div class="project-location">Navotas City, PH</div>
        <ul class="project-features">
          <li>16 service categories</li>
          <li>Chemical &amp; engineering catalog</li>
          <li>Contact section</li>
        </ul>
        <div class="project-stack">
          <span>HTML5</span><span>CSS3</span><span>JavaScript</span><span>Netlify</span>
        </div>
        <a href="https://osmont-water-technologies.netlify.app/" class="project-link" target="_blank">
          osmont-water-technologies.netlify.app ↗
        </a>
      </div>

      <div class="panel-cell" style="display:flex;flex-direction:column;gap:0.8rem">
        <div style="display:flex;justify-content:space-between;align-items:center">
          <span class="project-type">Portfolio Website</span>
          <span class="live-badge"><span class="live-dot"></span>Live</span>
        </div>
        <div class="project-name">Jun Baluyot — Couture Fashion Designer</div>
        <div class="project-location">San Antonio, Pampanga, PH</div>
        <ul class="project-features">
          <li>Gown collections gallery</li>
          <li>Pageant accolades</li>
          <li>Atelier booking</li>
        </ul>
        <div class="project-stack">
          <span>HTML5</span><span>CSS3</span><span>JavaScript</span><span>Netlify</span>
        </div>
        <a href="https://junbaluyot-designer.netlify.app/" class="project-link" target="_blank">
          junbaluyot-designer.netlify.app ↗
        </a>
      </div>

    </div>
  </section>

  <!-- ── 04 DESIGN PATTERNS ── -->
  <section class="section">
    <div class="section-header">
      <span class="section-num">04</span>
      <span class="section-title">Design Patterns Arc</span>
      <span class="section-line"></span>
    </div>
    <div class="pattern-wrap">
      <div class="pattern-head">
        <div>#</div>
        <div>Repository</div>
        <div>Category</div>
        <div>What it demonstrates</div>
      </div>
      <div class="pattern-row">
        <div class="p-num">01</div>
        <div class="p-name"><a href="https://github.com/MicoleKurt/CommandPattern" target="_blank">CommandPattern ↗</a></div>
        <div class="p-cat p-behavioral">Behavioral</div>
        <div class="p-desc">Requests as objects — undoable operations, action queuing, decoupled invoker/receiver</div>
      </div>
      <div class="pattern-row">
        <div class="p-num">02</div>
        <div class="p-name"><a href="https://github.com/MicoleKurt/Adapter-Pattern" target="_blank">Adapter-Pattern ↗</a></div>
        <div class="p-cat p-structural">Structural</div>
        <div class="p-desc">Bridging incompatible interfaces — wrap legacy code without modifying it</div>
      </div>
      <div class="pattern-row">
        <div class="p-num">03</div>
        <div class="p-name"><a href="https://github.com/MicoleKurt/Facade-Patern" target="_blank">Facade-Pattern ↗</a></div>
        <div class="p-cat p-structural">Structural</div>
        <div class="p-desc">Unified high-level interface over a complex subsystem — reduce client coupling</div>
      </div>
      <div class="pattern-row">
        <div class="p-num">04</div>
        <div class="p-name"><a href="https://github.com/MicoleKurt/Prototype-Design-Pattern" target="_blank">Prototype-Design-Pattern ↗</a></div>
        <div class="p-cat p-creational">Creational</div>
        <div class="p-desc">Clone objects efficiently — decouple instantiation logic from implementation</div>
      </div>
      <div class="pattern-row">
        <div class="p-num">05</div>
        <div class="p-name"><a href="https://github.com/MicoleKurt/Solid-Design-Pattern" target="_blank">Solid-Design-Pattern ↗</a></div>
        <div class="p-cat p-principles">Principles</div>
        <div class="p-desc">SRP · OCP · LSP · ISP · DIP applied end-to-end across a real Java codebase</div>
      </div>
      <div class="pattern-row">
        <div class="p-num">06</div>
        <div class="p-name"><a href="https://github.com/MicoleKurt/Component-Design-Pattern-" target="_blank">Component-Design-Pattern ↗</a></div>
        <div class="p-cat p-structural">Structural</div>
        <div class="p-desc">Modular, composable component hierarchies for scalable, maintainable systems</div>
      </div>
    </div>
  </section>

  <!-- ── 05 CERTIFICATIONS ── -->
  <section class="section">
    <div class="section-header">
      <span class="section-num">05</span>
      <span class="section-title">Certifications</span>
      <span class="section-line"></span>
    </div>
    <div class="grid-panel cols-2">

      <div class="panel-cell">
        <div class="cert-issuer">IBM · Cognitive Class</div>
        <div class="cert-name">SQL and Relational Databases 101</div>
        <a href="https://courses.cognitiveclass.ai/certificates/4e4c7dc978fa4d9ca4a74211e034b51e" class="cert-link" target="_blank">Verify credential ↗</a>
      </div>

      <div class="panel-cell">
        <div class="cert-issuer">Oracle</div>
        <div class="cert-name">Oracle Cloud Infrastructure 2024 Foundations Associate</div>
        <a href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=22EB3D80EA6E24E346FA5AD51BE48E325F236FEE3CDE624C44BA07EB1D9D4A9F" class="cert-link" target="_blank">Verify credential ↗</a>
      </div>

      <div class="panel-cell">
        <div class="cert-issuer">Oracle</div>
        <div class="cert-name">Oracle Cloud Data Management Foundations Associate</div>
        <a href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=22EB3D80EA6E24E346FA5AD51BE48E327A58DD54BCBEA485E20C60BB91FD7D87" class="cert-link" target="_blank">Verify credential ↗</a>
      </div>

      <div class="panel-cell">
        <div class="cert-issuer">Oracle</div>
        <div class="cert-name">Oracle Cloud Infrastructure AI Foundations Associate 2024</div>
        <a href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=22EB3D80EA6E24E346FA5AD51BE48E325F236FEE3CDE624C44BA07EB1D9D4A9F" class="cert-link" target="_blank">Verify credential ↗</a>
      </div>

    </div>
  </section>

  <!-- ── 06 PROFICIENCY ── -->
  <section class="section">
    <div class="section-header">
      <span class="section-num">06</span>
      <span class="section-title">Proficiency</span>
      <span class="section-line"></span>
    </div>
    <div class="prof-wrap">
      <div class="prof-item"><span class="prof-name">Java</span><div class="prof-track"><div class="prof-fill" style="width:80%"></div></div><span class="prof-pct">80%</span></div>
      <div class="prof-item"><span class="prof-name">HTML / CSS</span><div class="prof-track"><div class="prof-fill" style="width:80%"></div></div><span class="prof-pct">80%</span></div>
      <div class="prof-item"><span class="prof-name">VS Code</span><div class="prof-track"><div class="prof-fill" style="width:80%"></div></div><span class="prof-pct">80%</span></div>
      <div class="prof-item"><span class="prof-name">Eclipse IDE</span><div class="prof-track"><div class="prof-fill" style="width:80%"></div></div><span class="prof-pct">80%</span></div>
      <div class="prof-item"><span class="prof-name">SOLID Principles</span><div class="prof-track"><div class="prof-fill" style="width:80%"></div></div><span class="prof-pct">80%</span></div>
      <div class="prof-item"><span class="prof-name">Design Patterns (GoF)</span><div class="prof-track"><div class="prof-fill" style="width:70%"></div></div><span class="prof-pct">70%</span></div>
      <div class="prof-item"><span class="prof-name">JavaScript</span><div class="prof-track"><div class="prof-fill" style="width:70%"></div></div><span class="prof-pct">70%</span></div>
      <div class="prof-item"><span class="prof-name">Lucidchart / UML</span><div class="prof-track"><div class="prof-fill" style="width:70%"></div></div><span class="prof-pct">70%</span></div>
      <div class="prof-item"><span class="prof-name">React + Vite</span><div class="prof-track"><div class="prof-fill" style="width:60%"></div></div><span class="prof-pct">60%</span></div>
      <div class="prof-item"><span class="prof-name">Tailwind CSS v3</span><div class="prof-track"><div class="prof-fill" style="width:60%"></div></div><span class="prof-pct">60%</span></div>
      <div class="prof-item"><span class="prof-name">Supabase / PostgreSQL</span><div class="prof-track"><div class="prof-fill" style="width:60%"></div></div><span class="prof-pct">60%</span></div>
      <div class="prof-item"><span class="prof-name">Firebase + Google Auth</span><div class="prof-track"><div class="prof-fill" style="width:60%"></div></div><span class="prof-pct">60%</span></div>
      <div class="prof-item"><span class="prof-name">IBM DB2 Cloud</span><div class="prof-track"><div class="prof-fill" style="width:60%"></div></div><span class="prof-pct">60%</span></div>
      <div class="prof-item"><span class="prof-name">Oracle Cloud</span><div class="prof-track"><div class="prof-fill" style="width:60%"></div></div><span class="prof-pct">60%</span></div>
      <div class="prof-item"><span class="prof-name">Netlify / Vercel</span><div class="prof-track"><div class="prof-fill" style="width:60%"></div></div><span class="prof-pct">60%</span></div>
    </div>
  </section>

  <!-- ── 07 STATUS ── -->
  <section class="section">
    <div class="section-header">
      <span class="section-num">07</span>
      <span class="section-title">Status</span>
      <span class="section-line"></span>
    </div>
    <div class="grid-panel cols-2">

      <div class="panel-cell">
        <div class="status-col-title s-active">Active</div>
        <div class="status-item"><span class="si-icon plus">+</span>Learning Design Patterns in Java — working through the full GoF catalog</div>
        <div class="status-item"><span class="si-icon plus">+</span>Practicing SOLID across every active repository</div>
        <div class="status-item"><span class="si-icon plus">+</span>Building client websites — HTML · CSS · JS · Netlify</div>
        <div class="status-item"><span class="si-icon plus">+</span>Studying Oracle Cloud Infrastructure and IBM DB2 data management</div>
        <div class="status-item"><span class="si-icon plus">+</span>Targeting Full-Stack Developer — React · Node · PostgreSQL</div>
      </div>

      <div class="panel-cell">
        <div class="status-col-title s-blocked">Blocked</div>
        <div class="status-item"><span class="si-icon cross">×</span>NullPointerException (ongoing, unresolved)</div>
        <div class="status-item"><span class="si-icon cross">×</span>Merge conflicts at 2am (recurring)</div>
        <div class="status-item"><span class="si-icon cross">×</span>Undocumented third-party APIs (permanent condition)</div>
      </div>

    </div>
  </section>

  <!-- ── FOOTER ── -->
  <footer class="footer">
    <span class="footer-name">Micole Kurt Gonda</span>
    <a href="https://github.com/MicoleKurt" class="footer-link" target="_blank">github.com/MicoleKurt ↗</a>
    <span class="footer-meta">Quezon City · Philippines · UTC +08:00</span>
  </footer>

</div>
</body>
</html>
