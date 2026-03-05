<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Fahad Bin Khalid — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=JetBrains+Mono:wght@300;400;500;700&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg:       #030712;
    --surface:  #0a0f1e;
    --card:     #0d1424;
    --border:   #1a2540;
    --glow:     #00d4ff;
    --accent:   #0ea5e9;
    --violet:   #8b5cf6;
    --pink:     #ec4899;
    --green:    #10b981;
    --orange:   #f97316;
    --text:     #e2e8f0;
    --muted:    #64748b;
    --dim:      #1e293b;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── ANIMATED GRID BG ── */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image:
      linear-gradient(var(--border) 1px, transparent 1px),
      linear-gradient(90deg, var(--border) 1px, transparent 1px);
    background-size: 60px 60px;
    opacity: 0.35;
    z-index: 0;
    animation: gridMove 20s linear infinite;
  }

  @keyframes gridMove {
    0%   { background-position: 0 0; }
    100% { background-position: 60px 60px; }
  }

  body::after {
    content: '';
    position: fixed; inset: 0;
    background: radial-gradient(ellipse 80% 50% at 50% -10%, rgba(0,212,255,0.08) 0%, transparent 60%),
                radial-gradient(ellipse 60% 40% at 90% 80%, rgba(139,92,246,0.06) 0%, transparent 50%);
    z-index: 0;
    pointer-events: none;
  }

  .container {
    max-width: 960px;
    margin: 0 auto;
    padding: 40px 24px 80px;
    position: relative;
    z-index: 1;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 80px 0 60px;
    position: relative;
  }

  .hero-label {
    display: inline-block;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.3em;
    color: var(--glow);
    text-transform: uppercase;
    border: 1px solid rgba(0,212,255,0.3);
    padding: 6px 18px;
    border-radius: 2px;
    margin-bottom: 28px;
    background: rgba(0,212,255,0.05);
    animation: fadeDown 0.8s ease both;
  }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(48px, 8vw, 84px);
    font-weight: 800;
    line-height: 0.95;
    letter-spacing: -0.03em;
    background: linear-gradient(135deg, #ffffff 0%, #94a3b8 50%, #00d4ff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: fadeDown 0.8s 0.1s ease both;
    margin-bottom: 16px;
  }

  .hero-role {
    font-size: 13px;
    color: var(--muted);
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 36px;
    animation: fadeDown 0.8s 0.2s ease both;
  }

  .hero-role span { color: var(--glow); }

  .hero-tags {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 44px;
    animation: fadeDown 0.8s 0.3s ease both;
  }

  .tag {
    font-size: 11px;
    padding: 5px 14px;
    border-radius: 2px;
    letter-spacing: 0.05em;
    font-weight: 500;
  }

  .tag-blue  { background: rgba(14,165,233,0.1); color: #38bdf8; border: 1px solid rgba(14,165,233,0.25); }
  .tag-violet{ background: rgba(139,92,246,0.1); color: #a78bfa; border: 1px solid rgba(139,92,246,0.25); }
  .tag-green { background: rgba(16,185,129,0.1); color: #34d399; border: 1px solid rgba(16,185,129,0.25); }
  .tag-orange{ background: rgba(249,115,22,0.1); color: #fb923c; border: 1px solid rgba(249,115,22,0.25); }
  .tag-pink  { background: rgba(236,72,153,0.1); color: #f472b6; border: 1px solid rgba(236,72,153,0.25); }

  .hero-links {
    display: flex;
    gap: 12px;
    justify-content: center;
    animation: fadeDown 0.8s 0.4s ease both;
  }

  .btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-size: 12px;
    font-family: 'JetBrains Mono', monospace;
    font-weight: 500;
    padding: 10px 22px;
    border-radius: 2px;
    text-decoration: none;
    letter-spacing: 0.05em;
    transition: all 0.2s ease;
    cursor: pointer;
    border: none;
  }

  .btn-primary {
    background: var(--glow);
    color: #000;
  }
  .btn-primary:hover { background: #38e0ff; transform: translateY(-2px); box-shadow: 0 8px 24px rgba(0,212,255,0.3); }

  .btn-outline {
    background: transparent;
    color: var(--text);
    border: 1px solid var(--border);
  }
  .btn-outline:hover { border-color: var(--glow); color: var(--glow); transform: translateY(-2px); }

  /* ── DIVIDER ── */
  .divider {
    display: flex;
    align-items: center;
    gap: 16px;
    margin: 48px 0 40px;
  }

  .divider-line { flex: 1; height: 1px; background: var(--border); }

  .divider-label {
    font-size: 10px;
    letter-spacing: 0.4em;
    color: var(--muted);
    text-transform: uppercase;
    white-space: nowrap;
  }

  /* ── SECTION TITLE ── */
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.4em;
    text-transform: uppercase;
    color: var(--glow);
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ── ABOUT GRID ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 16px;
  }

  .card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 28px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s, transform 0.3s;
  }

  .card:hover {
    border-color: rgba(0,212,255,0.3);
    transform: translateY(-2px);
  }

  .card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--glow), transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }

  .card:hover::before { opacity: 1; }

  .card-num {
    position: absolute;
    top: 20px; right: 24px;
    font-size: 10px;
    color: var(--dim);
    letter-spacing: 0.2em;
  }

  .code-block {
    background: rgba(0,0,0,0.4);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 20px;
    font-size: 12px;
    line-height: 2;
    position: relative;
  }

  .code-block::before {
    content: '● ● ●';
    position: absolute;
    top: 10px; left: 16px;
    font-size: 9px;
    color: var(--muted);
    letter-spacing: 4px;
  }

  .code-block pre { margin-top: 16px; }

  .c-key    { color: #8b5cf6; }
  .c-str    { color: #34d399; }
  .c-arr    { color: #f97316; }
  .c-punct  { color: #64748b; }
  .c-val    { color: #38bdf8; }
  .c-comment{ color: #334155; }

  /* status items */
  .status-list { list-style: none; }

  .status-list li {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 10px 0;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    font-size: 12px;
    color: #94a3b8;
  }

  .status-list li:last-child { border-bottom: none; }

  .status-icon {
    width: 28px;
    height: 28px;
    border-radius: 2px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 13px;
    flex-shrink: 0;
  }

  .status-key { color: var(--muted); min-width: 80px; font-size: 10px; letter-spacing: 0.05em; }
  .status-val { color: var(--text); }

  /* ── TECH GRID ── */
  .tech-categories {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
  }

  .tech-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 20px 16px;
    transition: all 0.3s;
  }

  .tech-card:hover {
    border-color: rgba(0,212,255,0.25);
    transform: translateY(-3px);
    box-shadow: 0 12px 32px rgba(0,0,0,0.4);
  }

  .tech-cat-title {
    font-size: 9px;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 14px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border);
  }

  .tech-item {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 6px 0;
    font-size: 11px;
    color: #94a3b8;
    transition: color 0.2s;
  }

  .tech-item:hover { color: var(--text); }

  .tech-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  /* ── SKILL BARS ── */
  .skill-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
  }

  .skill-row {
    display: flex;
    flex-direction: column;
    gap: 6px;
    padding: 14px 18px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    transition: border-color 0.3s;
  }

  .skill-row:hover { border-color: rgba(0,212,255,0.2); }

  .skill-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 11px;
  }

  .skill-name { color: var(--text); }
  .skill-pct  { color: var(--glow); font-weight: 700; }

  .skill-bar {
    height: 2px;
    background: var(--dim);
    border-radius: 2px;
    overflow: hidden;
  }

  .skill-fill {
    height: 100%;
    border-radius: 2px;
    animation: fillBar 1.5s cubic-bezier(.4,0,.2,1) both;
    animation-delay: var(--delay, 0s);
  }

  @keyframes fillBar {
    from { width: 0; }
    to   { width: var(--w); }
  }

  /* ── STATS GRID ── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
    margin-bottom: 12px;
  }

  .stat-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 24px;
    text-align: center;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
  }

  .stat-card:hover { border-color: rgba(0,212,255,0.3); transform: translateY(-3px); }

  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 42px;
    font-weight: 800;
    line-height: 1;
    margin-bottom: 6px;
  }

  .stat-label {
    font-size: 9px;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--muted);
  }

  /* ── GITHUB IMG CARDS ── */
  .gh-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 12px;
  }

  .gh-img-wrap {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
    transition: all 0.3s;
  }

  .gh-img-wrap:hover { border-color: rgba(0,212,255,0.3); transform: translateY(-2px); }

  .gh-img-wrap img { width: 100%; display: block; }

  .gh-full {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
    margin-bottom: 12px;
    transition: all 0.3s;
  }

  .gh-full:hover { border-color: rgba(0,212,255,0.3); }
  .gh-full img { width: 100%; display: block; }

  /* ── FOOTER ── */
  .footer {
    margin-top: 80px;
    padding-top: 40px;
    border-top: 1px solid var(--border);
    text-align: center;
  }

  .footer-title {
    font-family: 'Syne', sans-serif;
    font-size: 28px;
    font-weight: 800;
    letter-spacing: -0.02em;
    margin-bottom: 8px;
    background: linear-gradient(90deg, #ffffff, #00d4ff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .footer-sub {
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.1em;
    margin-bottom: 32px;
  }

  .footer-links {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 48px;
  }

  .footer-quote {
    font-size: 12px;
    color: var(--muted);
    max-width: 480px;
    margin: 0 auto;
    line-height: 2;
    border-left: 2px solid var(--glow);
    padding-left: 20px;
    text-align: left;
  }

  .footer-quote em { color: #94a3b8; }

  .footer-sig {
    margin-top: 48px;
    font-size: 10px;
    color: var(--dim);
    letter-spacing: 0.3em;
    text-transform: uppercase;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .fade-up {
    opacity: 0;
    transform: translateY(24px);
    animation: fadeUp 0.7s ease forwards;
    animation-delay: var(--d, 0s);
  }

  @keyframes fadeUp {
    to { opacity: 1; transform: translateY(0); }
  }

  /* ── PULSE DOT ── */
  .pulse {
    display: inline-block;
    width: 7px; height: 7px;
    border-radius: 50%;
    background: var(--green);
    box-shadow: 0 0 0 0 rgba(16,185,129,0.6);
    animation: pulse 2s infinite;
    margin-right: 6px;
    vertical-align: middle;
  }

  @keyframes pulse {
    0%   { box-shadow: 0 0 0 0 rgba(16,185,129,0.6); }
    70%  { box-shadow: 0 0 0 8px rgba(16,185,129,0); }
    100% { box-shadow: 0 0 0 0 rgba(16,185,129,0); }
  }

  /* ── SCANLINE EFFECT ── */
  .hero::after {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,0,0,0.03) 2px,
      rgba(0,0,0,0.03) 4px
    );
    pointer-events: none;
  }

  /* responsive */
  @media (max-width: 700px) {
    .about-grid, .tech-categories, .stats-grid, .gh-grid, .skill-grid {
      grid-template-columns: 1fr;
    }
    .tech-categories { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- ═══ HERO ═══ -->
  <section class="hero">
    <div class="hero-label">⬡ &nbsp;Available for Remote &amp; Freelance&nbsp; ⬡</div>
    <h1 class="hero-name">Fahad<br/>Bin Khalid</h1>
    <p class="hero-role">
      <span>Senior</span> Full-Stack Engineer &nbsp;/&nbsp; SaaS Architect
    </p>
    <div class="hero-tags">
      <span class="tag tag-blue">Laravel</span>
      <span class="tag tag-violet">PHP</span>
      <span class="tag tag-green">Next.js</span>
      <span class="tag tag-orange">AWS</span>
      <span class="tag tag-pink">System Design</span>
      <span class="tag tag-blue">REST APIs</span>
      <span class="tag tag-violet">Docker</span>
      <span class="tag tag-green">MySQL</span>
    </div>
    <div class="hero-links">
      <a class="btn btn-primary" href="https://fahadrajpoot537.github.io/Portfolio/">⬡ Portfolio</a>
      <a class="btn btn-outline" href="https://linkedin.com/in/fahad-bin-khalid-experienced-full-stack-laravel-developer-1b2136222/">LinkedIn</a>
      <a class="btn btn-outline" href="mailto:fahadrajpoot537@gmail.com">fahadrajpoot537@gmail.com</a>
    </div>
  </section>

  <!-- ═══ ABOUT ═══ -->
  <div class="divider"><div class="divider-line"></div><span class="divider-label">01 — Identity</span><div class="divider-line"></div></div>

  <div class="section-title">$ whoami &amp;&amp; status</div>

  <div class="about-grid fade-up" style="--d:0.1s">
    <div class="code-block">
      <pre><span class="c-key">const</span> <span class="c-val">fahad</span> <span class="c-punct">=</span> <span class="c-punct">{</span>
  <span class="c-key">name</span><span class="c-punct">:</span>     <span class="c-str">"Fahad Bin Khalid"</span><span class="c-punct">,</span>
  <span class="c-key">role</span><span class="c-punct">:</span>     <span class="c-str">"Sr. Full-Stack Engineer"</span><span class="c-punct">,</span>
  <span class="c-key">location</span><span class="c-punct">:</span> <span class="c-str">"Pakistan 🇵🇰"</span><span class="c-punct">,</span>
  <span class="c-key">exp</span><span class="c-punct">:</span>      <span class="c-str">"5+ Years"</span><span class="c-punct">,</span>

  <span class="c-key">stack</span><span class="c-punct">:</span> <span class="c-arr">[</span>
    <span class="c-str">"Laravel"</span><span class="c-punct">,</span> <span class="c-str">"PHP"</span><span class="c-punct">,</span>
    <span class="c-str">"Next.js"</span><span class="c-punct">,</span> <span class="c-str">"AWS"</span><span class="c-punct">,</span>
  <span class="c-arr">]</span><span class="c-punct">,</span>

  <span class="c-key">arch</span><span class="c-punct">:</span>     <span class="c-str">"Microservices | Event-Driven"</span><span class="c-punct">,</span>
  <span class="c-key">motto</span><span class="c-punct">:</span>    <span class="c-str">"Ship fast. Scale smart."</span><span class="c-punct">,</span>
  <span class="c-key">learning</span><span class="c-punct">:</span> <span class="c-arr">[</span><span class="c-str">"Django"</span><span class="c-punct">,</span> <span class="c-str">"Python"</span><span class="c-arr">]</span><span class="c-punct">,</span>
<span class="c-punct">}</span><span class="c-punct">;</span></pre>
    </div>

    <div class="card">
      <div class="card-num">01</div>
      <div class="section-title" style="margin-bottom:18px;font-size:9px"><span class="pulse"></span>LIVE STATUS</div>
      <ul class="status-list">
        <li>
          <div class="status-icon" style="background:rgba(14,165,233,0.1)">🔭</div>
          <div><div class="status-key">Building</div><div class="status-val">SaaS Platform (Laravel)</div></div>
        </li>
        <li>
          <div class="status-icon" style="background:rgba(16,185,129,0.1)">🌍</div>
          <div><div class="status-key">Domain</div><div class="status-val">Property Listing Systems</div></div>
        </li>
        <li>
          <div class="status-icon" style="background:rgba(139,92,246,0.1)">🧠</div>
          <div><div class="status-key">Learning</div><div class="status-val">Django &amp; Python</div></div>
        </li>
        <li>
          <div class="status-icon" style="background:rgba(249,115,22,0.1)">⚡</div>
          <div><div class="status-key">Goal</div><div class="status-val">World-class Architecture</div></div>
        </li>
        <li>
          <div class="status-icon" style="background:rgba(236,72,153,0.1)">📬</div>
          <div><div class="status-key">Contact</div><div class="status-val">fahadrajpoot537@gmail.com</div></div>
        </li>
      </ul>
    </div>
  </div>

  <!-- ═══ TECH ═══ -->
  <div class="divider"><div class="divider-line"></div><span class="divider-label">02 — Arsenal</span><div class="divider-line"></div></div>
  <div class="section-title">$ cat tech-stack.json</div>

  <div class="tech-categories fade-up" style="--d:0.15s">
    <div class="tech-card">
      <div class="tech-cat-title">⚙ Backend</div>
      <div class="tech-item"><div class="tech-dot" style="background:#ff2d20"></div>Laravel</div>
      <div class="tech-item"><div class="tech-dot" style="background:#8892bf"></div>PHP</div>
      <div class="tech-item"><div class="tech-dot" style="background:#339933"></div>Node.js</div>
      <div class="tech-item"><div class="tech-dot" style="background:#092e20"></div>Django</div>
      <div class="tech-item"><div class="tech-dot" style="background:#00d4ff"></div>REST APIs</div>
    </div>
    <div class="tech-card">
      <div class="tech-cat-title">🎨 Frontend</div>
      <div class="tech-item"><div class="tech-dot" style="background:#61dafb"></div>React</div>
      <div class="tech-item"><div class="tech-dot" style="background:#ffffff"></div>Next.js</div>
      <div class="tech-item"><div class="tech-dot" style="background:#4fc08d"></div>Vue.js</div>
      <div class="tech-item"><div class="tech-dot" style="background:#f7df1e"></div>JavaScript</div>
      <div class="tech-item"><div class="tech-dot" style="background:#38b2ac"></div>Tailwind CSS</div>
    </div>
    <div class="tech-card">
      <div class="tech-cat-title">🗄 Databases</div>
      <div class="tech-item"><div class="tech-dot" style="background:#4479a1"></div>MySQL</div>
      <div class="tech-item"><div class="tech-dot" style="background:#47a248"></div>MongoDB</div>
      <div class="tech-item"><div class="tech-dot" style="background:#003545"></div>MariaDB</div>
      <div class="tech-item"><div class="tech-dot" style="background:#dc382d"></div>Redis</div>
    </div>
    <div class="tech-card">
      <div class="tech-cat-title">☁ DevOps</div>
      <div class="tech-item"><div class="tech-dot" style="background:#ff9900"></div>AWS</div>
      <div class="tech-item"><div class="tech-dot" style="background:#2496ed"></div>Docker</div>
      <div class="tech-item"><div class="tech-dot" style="background:#009639"></div>Nginx</div>
      <div class="tech-item"><div class="tech-dot" style="background:#fcc624"></div>Linux</div>
      <div class="tech-item"><div class="tech-dot" style="background:#f05032"></div>Git</div>
    </div>
  </div>

  <!-- ═══ SKILLS ═══ -->
  <div class="divider"><div class="divider-line"></div><span class="divider-label">03 — Proficiency</span><div class="divider-line"></div></div>
  <div class="section-title">$ skill --benchmark</div>

  <div class="skill-grid fade-up" style="--d:0.2s">
    <div class="skill-row">
      <div class="skill-header"><span class="skill-name">Laravel / PHP</span><span class="skill-pct">95%</span></div>
      <div class="skill-bar"><div class="skill-fill" style="--w:95%;background:linear-gradient(90deg,#ff2d20,#ff6b6b);--delay:0.3s"></div></div>
    </div>
    <div class="skill-row">
      <div class="skill-header"><span class="skill-name">REST API Design</span><span class="skill-pct">92%</span></div>
      <div class="skill-bar"><div class="skill-fill" style="--w:92%;background:linear-gradient(90deg,#0ea5e9,#38bdf8);--delay:0.4s"></div></div>
    </div>
    <div class="skill-row">
      <div class="skill-header"><span class="skill-name">Next.js / React</span><span class="skill-pct">88%</span></div>
      <div class="skill-bar"><div class="skill-fill" style="--w:88%;background:linear-gradient(90deg,#61dafb,#a5f3fc);--delay:0.5s"></div></div>
    </div>
    <div class="skill-row">
      <div class="skill-header"><span class="skill-name">System Architecture</span><span class="skill-pct">85%</span></div>
      <div class="skill-bar"><div class="skill-fill" style="--w:85%;background:linear-gradient(90deg,#8b5cf6,#a78bfa);--delay:0.6s"></div></div>
    </div>
    <div class="skill-row">
      <div class="skill-header"><span class="skill-name">AWS / DevOps</span><span class="skill-pct">80%</span></div>
      <div class="skill-bar"><div class="skill-fill" style="--w:80%;background:linear-gradient(90deg,#ff9900,#fbbf24);--delay:0.7s"></div></div>
    </div>
    <div class="skill-row">
      <div class="skill-header"><span class="skill-name">Vue.js</span><span class="skill-pct">75%</span></div>
      <div class="skill-bar"><div class="skill-fill" style="--w:75%;background:linear-gradient(90deg,#4fc08d,#6ee7b7);--delay:0.8s"></div></div>
    </div>
    <div class="skill-row">
      <div class="skill-header"><span class="skill-name">MongoDB</span><span class="skill-pct">70%</span></div>
      <div class="skill-bar"><div class="skill-fill" style="--w:70%;background:linear-gradient(90deg,#47a248,#86efac);--delay:0.9s"></div></div>
    </div>
    <div class="skill-row">
      <div class="skill-header"><span class="skill-name">Django / Python</span><span class="skill-pct" style="color:#f97316">40% ↗</span></div>
      <div class="skill-bar"><div class="skill-fill" style="--w:40%;background:linear-gradient(90deg,#f97316,#fb923c);--delay:1s"></div></div>
    </div>
  </div>

  <!-- ═══ STATS ═══ -->
  <div class="divider"><div class="divider-line"></div><span class="divider-label">04 — GitHub Analytics</span><div class="divider-line"></div></div>
  <div class="section-title">$ git log --stat --global</div>

  <div class="stats-grid fade-up" style="--d:0.25s">
    <div class="stat-card">
      <div class="stat-num" style="background:linear-gradient(135deg,#00d4ff,#0ea5e9);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text">5+</div>
      <div class="stat-label">Years Experience</div>
    </div>
    <div class="stat-card">
      <div class="stat-num" style="background:linear-gradient(135deg,#8b5cf6,#ec4899);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text">50+</div>
      <div class="stat-label">Projects Shipped</div>
    </div>
    <div class="stat-card">
      <div class="stat-num" style="background:linear-gradient(135deg,#10b981,#34d399);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text">12+</div>
      <div class="stat-label">Tech Stack Items</div>
    </div>
  </div>

  <div class="gh-grid fade-up" style="--d:0.3s">
    <div class="gh-img-wrap">
      <img src="https://github-readme-stats.vercel.app/api?username=fahadrajpoot537&show_icons=true&hide_border=true&bg_color=0d1424&title_color=00d4ff&icon_color=0ea5e9&text_color=94a3b8&ring_color=8b5cf6&border_radius=4&include_all_commits=true&count_private=true" alt="GitHub Stats"/>
    </div>
    <div class="gh-img-wrap">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=fahadrajpoot537&layout=donut&hide_border=true&bg_color=0d1424&title_color=00d4ff&text_color=94a3b8&border_radius=4&langs_count=8" alt="Top Languages"/>
    </div>
  </div>

  <div class="gh-full fade-up" style="--d:0.35s">
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=fahadrajpoot537&hide_border=true&background=0d1424&stroke=1a2540&ring=00d4ff&fire=ec4899&currStreakLabel=00d4ff&sideLabels=64748b&dates=334155&border_radius=4" alt="Streak Stats" style="width:100%"/>
  </div>

  <div class="gh-full fade-up" style="--d:0.4s">
    <img src="https://github-readme-activity-graph.vercel.app/graph?username=fahadrajpoot537&theme=tokyo-night&bg_color=0d1424&color=00d4ff&line=0ea5e9&point=ffffff&area_color=8b5cf6&area=true&hide_border=true&radius=4" alt="Activity Graph" style="width:100%"/>
  </div>

  <!-- ═══ TROPHIES ═══ -->
  <div class="divider"><div class="divider-line"></div><span class="divider-label">05 — Achievements</span><div class="divider-line"></div></div>
  <div class="section-title">$ github achievements --all</div>

  <div class="gh-full fade-up" style="--d:0.45s">
    <img src="https://github-profile-trophy.vercel.app/?username=fahadrajpoot537&theme=discord&no-frame=true&no-bg=true&margin-w=6&column=7" alt="Trophies" style="width:100%;padding:12px 0"/>
  </div>

  <!-- ═══ FOOTER ═══ -->
  <footer class="footer fade-up" style="--d:0.5s">
    <div class="footer-title">Let's Build Together</div>
    <div class="footer-sub">Open to remote roles, freelance &amp; SaaS collaborations</div>
    <div class="footer-links">
      <a class="btn btn-primary" href="https://fahadrajpoot537.github.io/Portfolio/">⬡ Portfolio</a>
      <a class="btn btn-outline" href="https://linkedin.com/in/fahad-bin-khalid-experienced-full-stack-laravel-developer-1b2136222/">💼 LinkedIn</a>
      <a class="btn btn-outline" href="mailto:fahadrajpoot537@gmail.com">📩 Email</a>
    </div>
    <div class="footer-quote">
      <em>"Designing scalable architectures and transforming<br/>complex ideas into powerful SaaS applications."</em><br/><br/>
      — <strong>Fahad Bin Khalid</strong>
    </div>
    <div class="footer-sig" style="margin-top:48px">⬡ crafted with precision &nbsp;·&nbsp; Fahad Bin Khalid &nbsp;·&nbsp; Pakistan 🇵🇰</div>
  </footer>

</div>
</body>
</html>
