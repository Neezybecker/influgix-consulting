[index.html](https://github.com/user-attachments/files/28957341/index.html)
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>INFLUX DIGIT – Accélérez votre croissance digitale</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg:       #0b0b1a;
      --bg2:      #12122a;
      --card:     #141428;
      --card2:    #1a1a35;
      --violet:   #7c3aed;
      --violet2:  #9f67ff;
      --violet3:  #c4a0ff;
      --white:    #ffffff;
      --muted:    #9899b8;
      --border:   rgba(124,58,237,.25);
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--white);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* ── NAVBAR ── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: 0 5%;
      height: 70px;
      background: rgba(11,11,26,.85);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid var(--border);
    }

    .nav-logo {
      display: flex; align-items: center; gap: 10px;
      text-decoration: none;
    }

    .nav-logo-icon {
      width: 38px; height: 38px;
      background: linear-gradient(135deg, var(--violet), var(--violet2));
      border-radius: 8px;
      display: flex; align-items: center; justify-content: center;
      font-weight: 900; font-size: 16px; color: #fff;
      letter-spacing: -1px;
      box-shadow: 0 0 18px rgba(124,58,237,.55);
    }

    .nav-logo-text { display: flex; flex-direction: column; }
    .nav-logo-name { font-weight: 800; font-size: .95rem; color: var(--white); line-height: 1; }
    .nav-logo-sub  { font-size: .62rem; color: var(--muted); letter-spacing: .04em; }

    .nav-links {
      display: flex; gap: 32px; list-style: none;
    }

    .nav-links a {
      text-decoration: none; color: var(--muted); font-size: .88rem; font-weight: 500;
      transition: color .2s;
      position: relative;
    }

    .nav-links a:hover,
    .nav-links a.active { color: var(--white); }

    .nav-links a.active::after {
      content: '';
      position: absolute; bottom: -4px; left: 0; right: 0;
      height: 2px;
      background: var(--violet2);
      border-radius: 2px;
    }

    .nav-cta {
      background: linear-gradient(135deg, var(--violet), var(--violet2));
      color: #fff !important;
      padding: 10px 22px;
      border-radius: 8px;
      font-weight: 600;
      font-size: .88rem;
      text-decoration: none;
      display: flex; align-items: center; gap: 8px;
      transition: opacity .2s, box-shadow .2s;
      box-shadow: 0 0 20px rgba(124,58,237,.4);
    }
    .nav-cta:hover { opacity: .9; box-shadow: 0 0 30px rgba(124,58,237,.65); }

    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      padding: 120px 7% 80px;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute; top: -200px; right: -200px;
      width: 700px; height: 700px;
      background: radial-gradient(circle, rgba(124,58,237,.18) 0%, transparent 70%);
      pointer-events: none;
    }
    .hero::after {
      content: '';
      position: absolute; bottom: -100px; left: -100px;
      width: 400px; height: 400px;
      background: radial-gradient(circle, rgba(124,58,237,.1) 0%, transparent 70%);
      pointer-events: none;
    }

    .hero-left { z-index: 2; }

    .hero-eyebrow {
      font-size: .78rem; font-weight: 700;
      color: var(--violet2); letter-spacing: .14em; text-transform: uppercase;
      margin-bottom: 22px;
    }

    .hero-title {
      font-size: clamp(2.4rem, 4.5vw, 4rem);
      font-weight: 800;
      line-height: 1.1;
      margin-bottom: 22px;
    }

    .hero-title .highlight {
      background: linear-gradient(90deg, var(--violet2), var(--violet3));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .hero-desc {
      color: var(--muted);
      font-size: 1rem;
      max-width: 440px;
      margin-bottom: 40px;
      line-height: 1.7;
    }

    .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }

    .btn-primary {
      background: linear-gradient(135deg, var(--violet), var(--violet2));
      color: #fff;
      padding: 14px 28px;
      border-radius: 10px;
      font-weight: 700;
      font-size: .92rem;
      text-decoration: none;
      display: inline-flex; align-items: center; gap: 8px;
      box-shadow: 0 0 24px rgba(124,58,237,.45);
      transition: transform .2s, box-shadow .2s;
    }
    .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 0 36px rgba(124,58,237,.7); }

    .btn-outline {
      border: 1.5px solid rgba(255,255,255,.25);
      color: #fff;
      padding: 14px 28px;
      border-radius: 10px;
      font-weight: 600;
      font-size: .92rem;
      text-decoration: none;
      transition: border-color .2s, background .2s;
    }
    .btn-outline:hover { border-color: var(--violet2); background: rgba(124,58,237,.12); }

    /* 3D Logo hero */
    .hero-right {
      display: flex; justify-content: center; align-items: center;
      z-index: 2;
      position: relative;
    }

    .hero-logo-3d {
      width: 360px; height: 360px;
      position: relative;
      animation: float 5s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50%       { transform: translateY(-18px); }
    }

    .hero-logo-3d svg { width: 100%; height: 100%; }

    .glow-ring {
      position: absolute;
      bottom: -20px; left: 50%;
      transform: translateX(-50%);
      width: 200px; height: 30px;
      background: radial-gradient(ellipse, rgba(124,58,237,.5) 0%, transparent 70%);
      filter: blur(8px);
      animation: glow-pulse 5s ease-in-out infinite;
    }
    @keyframes glow-pulse {
      0%, 100% { opacity: .6; }
      50%       { opacity: 1; }
    }

    /* Floating orbs */
    .orb {
      position: absolute;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--violet), var(--violet2));
      opacity: .55;
    }
    .orb-1 { width: 16px; height: 16px; top: 18%; left: 55%; animation: orb1 7s ease-in-out infinite; }
    .orb-2 { width: 10px; height: 10px; top: 30%; left: 80%; animation: orb2 9s ease-in-out infinite; }
    .orb-3 { width: 20px; height: 20px; bottom: 25%; right: 10%; animation: orb3 6s ease-in-out infinite; }

    @keyframes orb1 { 0%,100%{transform:translate(0,0)}50%{transform:translate(8px,-12px)} }
    @keyframes orb2 { 0%,100%{transform:translate(0,0)}50%{transform:translate(-6px,10px)} }
    @keyframes orb3 { 0%,100%{transform:translate(0,0)}50%{transform:translate(10px,-8px)} }

    /* ── EXPERTISES ── */
    .section {
      padding: 100px 7%;
    }

    .section-label {
      text-align: center;
      font-size: .78rem; font-weight: 700; color: var(--violet2);
      letter-spacing: .14em; text-transform: uppercase;
      margin-bottom: 18px;
    }

    .section-title {
      text-align: center;
      font-size: clamp(1.7rem, 3vw, 2.4rem);
      font-weight: 800;
      line-height: 1.25;
      max-width: 640px;
      margin: 0 auto 60px;
    }

    .section-title .highlight {
      background: linear-gradient(90deg, var(--violet2), var(--violet3));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .expertises-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    @media (max-width: 900px) { .expertises-grid { grid-template-columns: repeat(2,1fr); } }
    @media (max-width: 560px) { .expertises-grid { grid-template-columns: 1fr; } }

    .expertise-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 36px 28px;
      text-align: center;
      transition: border-color .3s, transform .3s, box-shadow .3s;
    }

    .expertise-card:hover {
      border-color: var(--violet2);
      transform: translateY(-5px);
      box-shadow: 0 12px 40px rgba(124,58,237,.25);
    }

    .expertise-icon {
      width: 56px; height: 56px;
      background: rgba(124,58,237,.15);
      border-radius: 12px;
      display: flex; align-items: center; justify-content: center;
      margin: 0 auto 20px;
      font-size: 1.6rem;
    }

    .expertise-card h3 {
      font-size: 1rem; font-weight: 700; margin-bottom: 12px;
    }

    .expertise-card p {
      color: var(--muted); font-size: .86rem; line-height: 1.65;
    }

    /* ── STATS + REALISATIONS ── */
    .split-section {
      padding: 80px 7%;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }

    @media (max-width: 800px) { .split-section { grid-template-columns: 1fr; } }

    .stats-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 24px;
    }

    .stat-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 30px 24px;
    }

    .stat-icon { font-size: 1.8rem; margin-bottom: 12px; }

    .stat-number {
      font-size: 2.4rem; font-weight: 900;
      background: linear-gradient(90deg, var(--violet2), var(--violet3));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
      line-height: 1;
      margin-bottom: 6px;
    }

    .stat-label { font-size: .82rem; color: var(--muted); }

    .real-label {
      font-size: .78rem; font-weight: 700; color: var(--violet2);
      letter-spacing: .14em; text-transform: uppercase;
      margin-bottom: 16px;
    }

    .real-title {
      font-size: clamp(1.5rem, 2.5vw, 2rem); font-weight: 800;
      line-height: 1.25; margin-bottom: 28px;
    }

    .real-link {
      color: var(--violet2);
      text-decoration: none;
      font-weight: 600; font-size: .9rem;
      display: inline-flex; align-items: center; gap: 6px;
      transition: gap .2s;
    }
    .real-link:hover { gap: 12px; }

    .real-mockups {
      display: flex; gap: 12px; margin-top: 28px;
    }

    .mockup {
      flex: 1;
      border-radius: 10px;
      overflow: hidden;
      border: 1px solid var(--border);
      background: var(--card2);
      aspect-ratio: 4/3;
      display: flex; align-items: center; justify-content: center;
      position: relative;
    }

    .mockup-label {
      position: absolute; bottom: 8px; left: 10px;
      font-size: .65rem; color: var(--muted); font-weight: 600;
    }

    /* Mockup inner design */
    .mockup-inner {
      width: 90%; height: 80%;
      border-radius: 6px;
      background: linear-gradient(135deg, var(--card), var(--card2));
      position: relative;
      overflow: hidden;
    }
    .mockup-bar {
      height: 18%;
      background: var(--violet);
      opacity: .7;
      border-radius: 4px 4px 0 0;
    }
    .mockup-line {
      height: 6px; border-radius: 3px;
      background: rgba(255,255,255,.08);
      margin: 6px 8px;
    }
    .mockup-line.short { width: 60%; }

    /* ── CTA BAND ── */
    .cta-band {
      margin: 0 7% 80px;
      background: linear-gradient(135deg, rgba(124,58,237,.25), rgba(159,103,255,.15));
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 70px 10%;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    .cta-band::before {
      content: '';
      position: absolute; inset: 0;
      background: radial-gradient(ellipse at center, rgba(124,58,237,.2) 0%, transparent 70%);
    }
    .cta-band h2 {
      font-size: clamp(1.6rem, 3vw, 2.2rem); font-weight: 800; margin-bottom: 16px;
      position: relative;
    }
    .cta-band p {
      color: var(--muted); margin-bottom: 36px; position: relative; max-width: 500px; margin-left: auto; margin-right: auto;
    }
    .cta-band .btn-primary { display: inline-flex; position: relative; }

    /* ── FOOTER ── */
    footer {
      border-top: 1px solid var(--border);
      padding: 50px 7% 30px;
    }

    .footer-top {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1fr;
      gap: 40px;
      margin-bottom: 48px;
    }

    @media (max-width: 900px) { .footer-top { grid-template-columns: 1fr 1fr; } }
    @media (max-width: 560px) { .footer-top { grid-template-columns: 1fr; } }

    .footer-brand p { color: var(--muted); font-size: .85rem; margin-top: 14px; max-width: 260px; line-height: 1.7; }

    .footer-col h4 { font-size: .82rem; font-weight: 700; margin-bottom: 16px; color: var(--white); letter-spacing: .04em; }

    .footer-col ul { list-style: none; }
    .footer-col li { margin-bottom: 10px; }
    .footer-col a { color: var(--muted); text-decoration: none; font-size: .84rem; transition: color .2s; }
    .footer-col a:hover { color: var(--violet2); }

    .footer-bottom {
      border-top: 1px solid var(--border);
      padding-top: 24px;
      display: flex; justify-content: space-between; align-items: center;
      flex-wrap: wrap; gap: 12px;
    }

    .footer-bottom p { color: var(--muted); font-size: .78rem; }

    /* ── RESPONSIVE HERO ── */
    @media (max-width: 900px) {
      .hero {
        grid-template-columns: 1fr;
        text-align: center;
        padding-top: 110px;
      }
      .hero-right { display: none; }
      .hero-desc { margin: 0 auto 36px; }
      .hero-btns { justify-content: center; }
    }

    @media (max-width: 700px) {
      nav .nav-links { display: none; }
    }
  </style>
</head>
<body>

<!-- ─── NAVBAR ─── -->
<nav>
  <a href="#" class="nav-logo">
    <div class="nav-logo-icon">ID</div>
    <div class="nav-logo-text">
      <span class="nav-logo-name">INFLUX DIGIT</span>
      <span class="nav-logo-sub">Accélérez votre croissance digitale</span>
    </div>
  </a>

  <ul class="nav-links">
    <li><a href="#" class="active">Accueil</a></li>
    <li><a href="#about">À propos</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#realisations">Réalisations</a></li>
    <li><a href="#processus">Processus</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>

  <a href="#contact" class="nav-cta">Parlons de votre projet →</a>
</nav>


<!-- ─── HERO ─── -->
<section class="hero">
  <div class="hero-left">
    <p class="hero-eyebrow">Agence Digitale</p>
    <h1 class="hero-title">
      Nous transformons<br>
      vos idées en<br>
      <span class="highlight">croissance digitale.</span>
    </h1>
    <p class="hero-desc">
      Stratégie, création et performance : nous concevons des solutions
      digitales sur-mesure pour propulser votre marque.
    </p>
    <div class="hero-btns">
      <a href="#services" class="btn-primary">Découvrir nos services →</a>
      <a href="#realisations" class="btn-outline">Voir nos réalisations</a>
    </div>
  </div>

  <div class="hero-right">
    <!-- Floating orbs -->
    <div class="orb orb-1"></div>
    <div class="orb orb-2"></div>
    <div class="orb orb-3"></div>

    <div class="hero-logo-3d">
      <!-- SVG 3D-style ID logo -->
      <svg viewBox="0 0 360 360" fill="none" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <linearGradient id="vg1" x1="0" y1="0" x2="1" y2="1">
            <stop offset="0%" stop-color="#9f67ff"/>
            <stop offset="100%" stop-color="#6b21d8"/>
          </linearGradient>
          <linearGradient id="vg2" x1="0" y1="0" x2="1" y2="1">
            <stop offset="0%" stop-color="#c4a0ff"/>
            <stop offset="100%" stop-color="#7c3aed"/>
          </linearGradient>
          <filter id="glow">
            <feGaussianBlur stdDeviation="8" result="blur"/>
            <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
          </filter>
          <filter id="shadow">
            <feDropShadow dx="4" dy="8" stdDeviation="10" flood-color="#7c3aed" flood-opacity=".6"/>
          </filter>
        </defs>

        <!-- Base platform -->
        <ellipse cx="180" cy="310" rx="120" ry="22"
          fill="url(#vg1)" opacity=".35"/>
        <ellipse cx="180" cy="304" rx="106" ry="16"
          fill="url(#vg1)" opacity=".5"/>

        <!-- Letter I -->
        <g filter="url(#shadow)">
          <!-- I face -->
          <rect x="88" y="85" width="48" height="200" rx="6" fill="url(#vg2)"/>
          <!-- I right side (3D depth) -->
          <path d="M136 85 L152 101 L152 301 L136 285 Z" fill="#5a1db0"/>
          <!-- I top face -->
          <path d="M88 85 L104 69 L152 69 L136 85 Z" fill="#b48fff"/>
          <!-- I bottom face -->
          <path d="M88 285 L104 301 L152 301 L136 285 Z" fill="#3d0f8a"/>
        </g>

        <!-- Letter D -->
        <g filter="url(#shadow)">
          <!-- D face -->
          <path d="M160 85 L200 85 Q270 85 270 185 Q270 285 200 285 L160 285 Z"
            fill="url(#vg1)"/>
          <!-- D inner hole -->
          <path d="M186 120 L200 120 Q234 120 234 185 Q234 250 200 250 L186 250 Z"
            fill="#0b0b1a"/>
          <!-- D right edge glow -->
          <path d="M270 185 Q270 285 200 285 L210 295 Q285 295 285 185 Q285 85 210 75 L200 85 Q270 85 270 185 Z"
            fill="#5a1db0" opacity=".8"/>
          <!-- D top face -->
          <path d="M160 85 L170 69 L210 69 Q290 70 290 185 L285 185 Q285 85 210 85 Z"
            fill="#b48fff"/>
        </g>

        <!-- Highlight gleam -->
        <ellipse cx="145" cy="100" rx="10" ry="4" fill="white" opacity=".25" transform="rotate(-30 145 100)"/>
        <ellipse cx="200" cy="105" rx="18" ry="5" fill="white" opacity=".2" transform="rotate(-15 200 105)"/>
      </svg>

      <div class="glow-ring"></div>
    </div>
  </div>
</section>


<!-- ─── EXPERTISES ─── -->
<section class="section" id="services">
  <p class="section-label">Nos Expertises</p>
  <h2 class="section-title">
    Des solutions digitales complètes<br>
    pour des <span class="highlight">résultats mesurables.</span>
  </h2>

  <div class="expertises-grid">

    <div class="expertise-card">
      <div class="expertise-icon">🎯</div>
      <h3>Stratégie Digitale</h3>
      <p>Nous définissons des stratégies sur-mesure alignées à vos objectifs business pour maximiser votre impact en ligne.</p>
    </div>

    <div class="expertise-card">
      <div class="expertise-icon">✏️</div>
      <h3>Branding & Design</h3>
      <p>Nous créons des identités visuelles fortes et cohérentes qui marquent les esprits et renforcent votre crédibilité.</p>
    </div>

    <div class="expertise-card">
      <div class="expertise-icon">💻</div>
      <h3>Développement Web</h3>
      <p>Des sites web performants, modernes et optimisés pour convertir vos visiteurs en clients fidèles.</p>
    </div>

    <div class="expertise-card">
      <div class="expertise-icon">📈</div>
      <h3>Marketing Digital</h3>
      <p>Nous attirons, engageons et convertissons votre audience en clients grâce à des campagnes ciblées et efficaces.</p>
    </div>

    <div class="expertise-card">
      <div class="expertise-icon">📣</div>
      <h3>Réseaux Sociaux</h3>
      <p>Nous développons votre notoriété et créons une communauté engagée autour de votre marque sur toutes les plateformes.</p>
    </div>

    <div class="expertise-card">
      <div class="expertise-icon">📊</div>
      <h3>Analyse & Performance</h3>
      <p>Nous analysons, optimisons et pilotons vos actions digitales pour un ROI maximal et une croissance durable.</p>
    </div>

  </div>
</section>


<!-- ─── STATS + RÉALISATIONS ─── -->
<div class="split-section" id="realisations">

  <!-- Stats -->
  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-icon">👥</div>
      <div class="stat-number">50+</div>
      <div class="stat-label">Clients satisfaits et accompagnés</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">🚀</div>
      <div class="stat-number">120+</div>
      <div class="stat-label">Projets réalisés avec succès</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">📉</div>
      <div class="stat-number">300%</div>
      <div class="stat-label">Croissance moyenne de nos clients</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">🏆</div>
      <div class="stat-number">5+</div>
      <div class="stat-label">Années d'expérience à votre service</div>
    </div>
  </div>

  <!-- Réalisations -->
  <div>
    <p class="real-label">Nos Réalisations</p>
    <h2 class="real-title">Des projets qui parlent<br>mieux que les mots.</h2>
    <a href="#" class="real-link">Voir nos réalisations →</a>

    <div class="real-mockups">
      <div class="mockup">
        <div class="mockup-inner">
          <div class="mockup-bar" style="background:linear-gradient(90deg,#7c3aed,#9f67ff)"></div>
          <div class="mockup-line"></div>
          <div class="mockup-line short"></div>
          <div class="mockup-line"></div>
        </div>
        <span class="mockup-label">ELEVATA</span>
      </div>
      <div class="mockup">
        <div class="mockup-inner">
          <div class="mockup-bar" style="background:linear-gradient(90deg,#1a6b3a,#3aaa6b)"></div>
          <div class="mockup-line"></div>
          <div class="mockup-line short"></div>
          <div class="mockup-line"></div>
        </div>
        <span class="mockup-label">Pure by nature</span>
      </div>
      <div class="mockup">
        <div class="mockup-inner">
          <div class="mockup-bar" style="background:linear-gradient(90deg,#1a3a6b,#3a6baa)"></div>
          <div class="mockup-line"></div>
          <div class="mockup-line short"></div>
          <div class="mockup-line"></div>
        </div>
        <span class="mockup-label">Voyagez autrement</span>
      </div>
    </div>
  </div>

</div>


<!-- ─── CTA BAND ─── -->
<section>
  <div class="cta-band" id="contact">
    <h2>Prêt à propulser votre marque ?</h2>
    <p>Discutons de votre projet et construisons ensemble votre stratégie digitale sur-mesure.</p>
    <a href="mailto:contact@influxdigit.com" class="btn-primary">Parlons de votre projet →</a>
  </div>
</section>


<!-- ─── FOOTER ─── -->
<footer>
  <div class="footer-top">

    <div class="footer-brand">
      <a href="#" class="nav-logo" style="display:inline-flex">
        <div class="nav-logo-icon">ID</div>
        <div class="nav-logo-text">
          <span class="nav-logo-name">INFLUX DIGIT</span>
          <span class="nav-logo-sub">Accélérez votre croissance digitale</span>
        </div>
      </a>
      <p>Votre partenaire digital de confiance en Afrique de l'Ouest. Nous transformons vos ambitions en résultats concrets.</p>
    </div>

    <div class="footer-col" id="about">
      <h4>Services</h4>
      <ul>
        <li><a href="#">Stratégie Digitale</a></li>
        <li><a href="#">Branding & Design</a></li>
        <li><a href="#">Développement Web</a></li>
        <li><a href="#">Marketing Digital</a></li>
        <li><a href="#">Réseaux Sociaux</a></li>
      </ul>
    </div>

    <div class="footer-col" id="processus">
      <h4>Entreprise</h4>
      <ul>
        <li><a href="#">À propos</a></li>
        <li><a href="#">Notre équipe</a></li>
        <li><a href="#">Réalisations</a></li>
        <li><a href="#">Processus</a></li>
        <li><a href="#">Blog</a></li>
      </ul>
    </div>

    <div class="footer-col">
      <h4>Contact</h4>
      <ul>
        <li><a href="mailto:contact@influxdigit.com">contact@influxdigit.com</a></li>
        <li><a href="tel:+226 70 89 78 68">+226 70 89 78 68</a></li>
        <li><a href="#">Ouagadougou, Burkina Faso</a></li>
      </ul>
    </div>

  </div>

  <div class="footer-bottom">
    <p>© 2026 INFLUX DIGIT. Tous droits réservés.</p>
    <p>Conçu avec ♥ à Ouagadougou</p>
  </div>
</footer>

</body>
</html>
