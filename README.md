<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Micole Kurt Gonda</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Share+Tech+Mono&family=Rajdhani:wght@400;600;700&display=swap" rel="stylesheet"/>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Rajdhani',sans-serif;background:#000;color:#fff;position:relative;overflow-x:hidden;min-height:900px}
.bg-gif{position:fixed;inset:0;width:100%;height:100%;object-fit:cover;object-position:center top;z-index:0;opacity:0.55}
.overlay{position:fixed;inset:0;background:linear-gradient(to bottom,rgba(0,0,0,0.35) 0%,rgba(0,0,0,0.7) 40%,rgba(0,0,0,0.97) 75%,#000 100%);z-index:1}
.web-svg{position:fixed;inset:0;width:100%;height:100%;z-index:2;pointer-events:none}
.content{position:relative;z-index:3;padding:0 0 48px;max-width:680px;margin:0 auto}
.hero{padding:200px 36px 0;text-align:center}
.hero-eyebrow{font-family:'Share Tech Mono',monospace;font-size:11px;letter-spacing:4px;color:#CC0000;margin-bottom:10px;text-transform:uppercase}
.hero-name{font-family:'Bebas Neue',sans-serif;font-size:68px;line-height:1;letter-spacing:4px;color:#fff;text-shadow:0 0 60px rgba(204,0,0,0.6)}
.hero-name span{color:#CC0000}
.hero-sub{font-size:13px;letter-spacing:3px;color:#aaa;text-transform:uppercase;margin-top:8px;font-weight:600}
.hero-quote{font-family:'Share Tech Mono',monospace;font-size:13px;color:#CC0000;margin:18px auto 0;max-width:520px;line-height:1.7;border-top:1px solid #CC000040;border-bottom:1px solid #CC000040;padding:12px 0}
.div-line{height:1px;background:linear-gradient(90deg,transparent,#CC000060,transparent);margin:32px 0}
.sec{padding:0 32px;margin-top:28px}
.sec-label{font-family:'Share Tech Mono',monospace;font-size:10px;letter-spacing:4px;color:#CC0000;text-transform:uppercase;margin-bottom:14px;display:flex;align-items:center;gap:10px}
.sec-label::after{content:'';flex:1;height:1px;background:#CC000030}
.skill-row{display:flex;align-items:center;gap:12px;margin-bottom:12px}
.sk-name{font-family:'Share Tech Mono',monospace;font-size:11px;color:#aaa;width:110px;flex-shrink:0}
.sk-track{flex:1;height:4px;background:#1a0000;border-radius:2px;overflow:hidden}
.sk-fill{height:100%;background:#CC0000;border-radius:2px;animation:grow 1.4s ease forwards;transform:scaleX(0);transform-origin:left}
@keyframes grow{to{transform:scaleX(1)}}
.sk-pct{font-family:'Share Tech Mono',monospace;font-size:11px;color:#CC0000;width:32px;text-align:right;flex-shrink:0}
.cert-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.cert-card{background:rgba(10,0,0,0.8);border:1px solid #CC000035;border-radius:4px;padding:14px 16px;display:flex;flex-direction:column;gap:6px;text-decoration:none;transition:border-color 0.2s,background 0.2s}
.cert-card:hover{border-color:#CC0000;background:rgba(204,0,0,0.08)}
.cert-icon{font-size:14px}
.cert-name{font-size:12px;font-weight:700;color:#fff;line-height:1.4}
.cert-issuer{font-family:'Share Tech Mono',monospace;font-size:10px;color:#CC0000;letter-spacing:1px}
.cert-verify{font-family:'Share Tech Mono',monospace;font-size:10px;color:#555;margin-top:2px}
.cert-card:hover .cert-verify{color:#CC0000}
.repo-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.repo-card{background:rgba(10,0,0,0.8);border:1px solid #CC000030;border-radius:4px;padding:14px 16px;transition:border-color 0.2s}
.repo-card:hover{border-color:#CC0000}
.repo-name{font-family:'Share Tech Mono',monospace;font-size:11px;color:#CC0000;margin-bottom:5px}
.repo-tag{display:inline-block;font-family:'Share Tech Mono',monospace;font-size:9px;color:#880000;background:#1a0000;border:1px solid #440000;border-radius:2px;padding:2px 6px;margin-bottom:6px}
.repo-desc{font-size:11px;color:#888;line-height:1.4}
.terminal{background:rgba(5,0,0,0.9);border:1px solid #CC000040;border-radius:4px;padding:18px 22px;font-family:'Share Tech Mono',monospace;font-size:12px;line-height:2}
.t-line{display:flex;gap:14px}
.t-plus{color:#2da44e}.t-minus{color:#CC0000}.t-key{color:#777;min-width:70px}.t-val{color:#ddd}
.stats-row{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.stat-card{background:rgba(10,0,0,0.8);border:1px solid #CC000030;border-radius:4px;padding:16px;text-align:center}
.stat-num{font-family:'Bebas Neue',sans-serif;font-size:36px;color:#CC0000;line-height:1}
.stat-lbl{font-family:'Share Tech Mono',monospace;font-size:10px;color:#555;letter-spacing:2px;margin-top:4px}
.footer{margin-top:36px;padding:20px 32px;border-top:1px solid #CC000025;display:flex;align-items:center;justify-content:space-between}
.footer-left{font-family:'Share Tech Mono',monospace;font-size:10px;color:#444;letter-spacing:2px}
.footer-right{font-family:'Share Tech Mono',monospace;font-size:10px;color:#CC0000;letter-spacing:1px}
.connect-row{display:flex;gap:10px;flex-wrap:wrap}
.connect-pill{background:rgba(10,0,0,0.8);border:1px solid #CC000040;border-radius:3px;padding:9px 18px;font-family:'Share Tech Mono',monospace;font-size:12px;color:#CC0000;display:flex;align-items:center;gap:8px;text-decoration:none;transition:background 0.15s,border-color 0.15s}
.connect-pill:hover{background:rgba(204,0,0,0.12);border-color:#CC0000}
</style>
</head>
<body>

<img class="bg-gif" src="https://wallpapers-clan.com/wp-content/uploads/2024/08/marvel-spider-man-eyes-gif-desktop-wallpaper-preview.gif" alt=""/>
<div class="overlay"></div>

<svg class="web-svg" viewBox="0 0 680 900" preserveAspectRatio="xMidYMid slice">
  <g opacity="0.25" stroke="#CC0000" fill="none" stroke-width="0.8">
    <line x1="340" y1="0" x2="20" y2="260"/>
    <line x1="340" y1="0" x2="660" y2="260"/>
    <line x1="340" y1="0" x2="180" y2="200"/>
    <line x1="340" y1="0" x2="500" y2="200"/>
    <line x1="340" y1="0" x2="340" y2="220"/>
    <line x1="340" y1="0" x2="80" y2="160"/>
    <line x1="340" y1="0" x2="600" y2="160"/>
    <ellipse cx="340" cy="0" rx="80" ry="65"/>
    <ellipse cx="340" cy="0" rx="165" ry="130"/>
    <ellipse cx="340" cy="0" rx="255" ry="195"/>
    <ellipse cx="340" cy="0" rx="360" ry="280"/>
  </g>
</svg>

<div class="content">
  <div class="hero">
    <div class="hero-eyebrow">// github.com/MicoleKurt</div>
    <div class="hero-name">Micole <span>Kurt</span> Gonda</div>
    <div class="hero-sub">BS Computer Science &nbsp;·&nbsp; New Era University &nbsp;·&nbsp; 3rd Year</div>
    <div class="hero-quote">"With great power comes great responsibility — and an equal measure of unresolved merge conflicts."</div>
  </div>

  <div class="div-line" style="margin:32px 32px 0"></div>

  <div class="sec">
    <div class="sec-label">Skill Suite</div>
    <div class="skill-row"><span class="sk-name">Java</span><div class="sk-track"><div class="sk-fill" style="width:80%"></div></div><span class="sk-pct">80%</span></div>
    <div class="skill-row"><span class="sk-name">Eclipse IDE</span><div class="sk-track"><div class="sk-fill" style="width:80%;animation-delay:0.1s"></div></div><span class="sk-pct">80%</span></div>
    <div class="skill-row"><span class="sk-name">Lucidchart</span><div class="sk-track"><div class="sk-fill" style="width:70%;animation-delay:0.2s"></div></div><span class="sk-pct">70%</span></div>
    <div class="skill-row"><span class="sk-name">IBM DB2 Cloud</span><div class="sk-track"><div class="sk-fill" style="width:60%;animation-delay:0.3s"></div></div><span class="sk-pct">60%</span></div>
  </div>

  <div class="div-line" style="margin:28px 32px 0"></div>

  <div class="sec">
    <div class="sec-label">Certifications</div>
    <div class="cert-grid">
      <a class="cert-card" href="https://courses.cognitiveclass.ai/certificates/4e4c7dc978fa4d9ca4a74211e034b51e" target="_blank">
        <div class="cert-icon">🔴</div>
        <div class="cert-name">SQL and Relational Databases 101</div>
        <div class="cert-issuer">IBM · Cognitive Class</div>
        <div class="cert-verify">→ Verify credential</div>
      </a>
      <a class="cert-card" href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=22EB3D80EA6E24E346FA5AD51BE48E325F236FEE3CDE624C44BA07EB1D9D4A9F" target="_blank">
        <div class="cert-icon">☁️</div>
        <div class="cert-name">OCI 2024 Certified Foundations Associate</div>
        <div class="cert-issuer">Oracle Cloud</div>
        <div class="cert-verify">→ Verify credential</div>
      </a>
      <a class="cert-card" href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=22EB3D80EA6E24E346FA5AD51BE48E327A58DD54BCBEA485E20C60BB91FD7D87" target="_blank">
        <div class="cert-icon">🗄️</div>
        <div class="cert-name">OCI Data Management Foundations Associate</div>
        <div class="cert-issuer">Oracle Cloud</div>
        <div class="cert-verify">→ Verify credential</div>
      </a>
      <a class="cert-card" href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=22EB3D80EA6E24E346FA5AD51BE48E325F236FEE3CDE624C44BA07EB1D9D4A9F" target="_blank">
        <div class="cert-icon">🤖</div>
        <div class="cert-name">OCI AI Foundations Associate (2024)</div>
        <div class="cert-issuer">Oracle Cloud</div>
        <div class="cert-verify">→ Verify credential</div>
      </a>
    </div>
  </div>

  <div class="div-line" style="margin:28px 32px 0"></div>

  <div class="sec">
    <div class="sec-label">Design Patterns Arc</div>
    <div class="repo-grid">
      <div class="repo-card"><div class="repo-name">CommandPattern</div><div class="repo-tag">BEHAVIORAL</div><div class="repo-desc">Encapsulating requests as standalone objects for decoupled execution</div></div>
      <div class="repo-card"><div class="repo-name">Adapter-Pattern</div><div class="repo-tag">STRUCTURAL</div><div class="repo-desc">Bridging incompatible interfaces through structural abstraction</div></div>
      <div class="repo-card"><div class="repo-name">Facade-Pattern</div><div class="repo-tag">STRUCTURAL</div><div class="repo-desc">Simplifying complex subsystems behind a unified interface</div></div>
      <div class="repo-card"><div class="repo-name">Prototype-Design-Pattern</div><div class="repo-tag">CREATIONAL</div><div class="repo-desc">Object cloning strategies for efficient instantiation</div></div>
      <div class="repo-card"><div class="repo-name">Solid-Design-Pattern</div><div class="repo-tag">PRINCIPLES</div><div class="repo-desc">SOLID applied within a pattern-driven architecture</div></div>
      <div class="repo-card"><div class="repo-name">Component-Design-Pattern</div><div class="repo-tag">STRUCTURAL</div><div class="repo-desc">Reusable component hierarchies and composition</div></div>
    </div>
  </div>

  <div class="div-line" style="margin:28px 32px 0"></div>

  <div class="sec">
    <div class="sec-label">Stats</div>
    <div class="stats-row">
      <div class="stat-card"><div class="stat-num">138</div><div class="stat-lbl">Contributions</div></div>
      <div class="stat-card"><div class="stat-num">6</div><div class="stat-lbl">Repositories</div></div>
      <div class="stat-card"><div class="stat-num">4</div><div class="stat-lbl">Certifications</div></div>
    </div>
  </div>

  <div class="div-line" style="margin:28px 32px 0"></div>

  <div class="sec">
    <div class="sec-label">Live Status</div>
    <div class="terminal">
      <div class="t-line"><span class="t-plus">+</span><span class="t-key">learning</span><span class="t-val">Design Patterns in Java — Creational · Structural · Behavioral</span></div>
      <div class="t-line"><span class="t-plus">+</span><span class="t-key">building</span><span class="t-val">Academic projects at New Era University</span></div>
      <div class="t-line"><span class="t-plus">+</span><span class="t-key">goal</span><span class="t-val">Full-Stack Developer</span></div>
      <div class="t-line"><span class="t-minus">-</span><span class="t-key">nemeses</span><span class="t-val">NullPointerException · merge conflicts · undocumented APIs</span></div>
    </div>
  </div>

  <div class="div-line" style="margin:28px 32px 0"></div>

  <div class="sec">
    <div class="sec-label">Connect</div>
    <div class="connect-row">
      <a class="connect-pill" href="https://github.com/MicoleKurt" target="_blank">
        <svg width="14" height="14" viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
        github.com/MicoleKurt
      </a>
    </div>
  </div>

  <div class="footer">
    <div class="footer-left">MICOLE KURT GONDA · NEU · 2023–PRESENT</div>
    <div class="footer-right">THREADS OF LOGIC. WEBS OF STRUCTURE. 🕷</div>
  </div>
</div>

</body>
</html>
