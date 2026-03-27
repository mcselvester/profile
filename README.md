<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cody Selvester — Director of Program Management | VP Enterprise Delivery</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400&family=DM+Mono:wght@300;400;500&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0a0a0f;
    --paper: #f5f2eb;
    --gold: #b8972a;
    --gold-light: #e2c97a;
    --slate: #3a3a4a;
    --muted: #7a7a8a;
    --navy: #1a2744;
    --line: rgba(184,151,42,0.2);
    --white: #fff;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }

  body {
    font-family: 'Instrument Sans', sans-serif;
    background: var(--paper);
    color: var(--ink);
    overflow-x: hidden;
  }

  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.035'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 200;
    display: flex; justify-content: space-between; align-items: center;
    padding: 1.1rem 4rem;
    background: rgba(245,242,235,0.9);
    backdrop-filter: blur(16px);
    border-bottom: 1px solid var(--line);
    transition: box-shadow 0.3s;
  }

  nav.scrolled { box-shadow: 0 2px 20px rgba(10,10,15,0.08); }

  .nav-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.05rem; font-weight: 600;
    letter-spacing: 0.06em; color: var(--navy);
    display: flex; flex-direction: column; line-height: 1.1;
  }
  .nav-name span {
    font-family: 'DM Mono', monospace;
    font-size: 0.55rem; letter-spacing: 0.2em;
    text-transform: uppercase; color: var(--gold);
    font-weight: 400; margin-top: 2px;
  }

  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-family: 'DM Mono', monospace; font-size: 0.65rem;
    letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--muted); text-decoration: none; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* HERO */
  #hero {
    min-height: 100vh;
    display: flex; align-items: center;
    padding: 7rem 4rem 5rem;
    position: relative; overflow: hidden;
  }

  .hero-watermark {
    position: absolute; right: -3vw; bottom: -5vh;
    font-family: 'Cormorant Garamond', serif;
    font-size: 28vw; font-weight: 700; line-height: 0.85;
    color: transparent;
    -webkit-text-stroke: 1px rgba(26,39,68,0.07);
    pointer-events: none; user-select: none;
    letter-spacing: -0.05em;
  }

  .hero-inner {
    max-width: 1200px; margin: 0 auto; width: 100%;
    display: grid; grid-template-columns: 3fr 2fr; gap: 5rem; align-items: center;
  }

  .hero-left { animation: fadeUp 0.9s ease both; }

  .hero-badge {
    display: inline-flex; align-items: center; gap: 0.75rem;
    background: rgba(26,39,68,0.06); border: 1px solid rgba(26,39,68,0.12);
    padding: 0.5rem 1rem; margin-bottom: 2rem;
    font-family: 'DM Mono', monospace; font-size: 0.62rem;
    letter-spacing: 0.15em; text-transform: uppercase; color: var(--navy);
  }

  .badge-dot {
    width: 6px; height: 6px; background: var(--gold); border-radius: 50%;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.7); }
  }

  h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3.2rem, 5.5vw, 5rem);
    font-weight: 600; line-height: 1.0;
    color: var(--navy); margin-bottom: 0.2rem;
  }

  h1 em {
    font-style: italic; font-weight: 300; color: var(--gold); display: block;
  }

  .hero-titles {
    margin: 1.5rem 0;
    display: flex; flex-direction: column; gap: 0.3rem;
  }

  .hero-title-item {
    font-family: 'DM Mono', monospace; font-size: 0.7rem;
    letter-spacing: 0.14em; text-transform: uppercase;
    color: var(--muted); display: flex; align-items: center; gap: 0.75rem;
  }

  .hero-title-item::before {
    content: ''; display: block; width: 1.5rem; height: 1px; background: var(--gold);
  }

  .hero-summary {
    font-size: 1.0rem; line-height: 1.8; color: var(--slate);
    max-width: 520px; margin: 1.75rem 0 2.5rem;
    border-left: 2px solid var(--gold); padding-left: 1.25rem;
  }

  .hero-ctas { display: flex; gap: 1rem; flex-wrap: wrap; }

  .btn-primary {
    background: var(--navy); color: var(--paper);
    padding: 0.9rem 2.25rem;
    font-family: 'DM Mono', monospace; font-size: 0.65rem;
    letter-spacing: 0.18em; text-transform: uppercase;
    text-decoration: none; border: 1px solid var(--navy);
    transition: all 0.25s; display: inline-block;
  }
  .btn-primary:hover { background: var(--gold); border-color: var(--gold); transform: translateY(-2px); }

  .btn-ghost {
    background: transparent; color: var(--navy);
    padding: 0.9rem 2.25rem;
    font-family: 'DM Mono', monospace; font-size: 0.65rem;
    letter-spacing: 0.18em; text-transform: uppercase;
    text-decoration: none; border: 1px solid var(--navy);
    transition: all 0.25s; display: inline-block;
  }
  .btn-ghost:hover { background: var(--navy); color: var(--paper); transform: translateY(-2px); }

  /* Hero stats */
  .hero-right { animation: fadeUp 0.9s 0.15s ease both; }

  .stat-stack { display: flex; flex-direction: column; gap: 1rem; }

  .stat-box {
    background: var(--navy);
    padding: 1.5rem 1.75rem;
    position: relative; overflow: hidden;
    transition: transform 0.2s;
  }
  .stat-box:hover { transform: translateX(4px); }

  .stat-box::before {
    content: '';
    position: absolute; left: 0; top: 0; bottom: 0; width: 3px;
    background: var(--gold);
  }

  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.8rem; font-weight: 700; line-height: 1;
    color: var(--white); margin-bottom: 0.25rem;
  }

  .stat-desc {
    font-family: 'DM Mono', monospace; font-size: 0.62rem;
    letter-spacing: 0.12em; text-transform: uppercase; color: var(--gold-light);
  }

  .stat-sub {
    font-size: 0.8rem; color: rgba(255,255,255,0.5);
    margin-top: 0.25rem; line-height: 1.4;
  }

  /* SECTION BASE */
  .section-wrap {
    max-width: 1200px; margin: 0 auto;
    padding: 6rem 4rem;
  }

  .section-label {
    font-family: 'DM Mono', monospace; font-size: 0.62rem;
    letter-spacing: 0.25em; text-transform: uppercase; color: var(--gold);
    margin-bottom: 0.6rem; display: flex; align-items: center; gap: 0.75rem;
  }
  .section-label::after { content: ''; display: block; width: 2.5rem; height: 1px; background: var(--gold); }

  h2 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.8rem, 3.5vw, 2.75rem);
    font-weight: 600; color: var(--navy); line-height: 1.1;
    margin-bottom: 2.5rem;
  }

  /* TARGETING STRIP */
  #targeting {
    background: var(--navy);
    padding: 3rem 4rem;
  }
  #targeting .inner {
    max-width: 1200px; margin: 0 auto;
    display: grid; grid-template-columns: repeat(4, 1fr); gap: 1px;
    background: rgba(184,151,42,0.2);
  }
  .target-role {
    background: var(--navy); padding: 1.5rem;
    text-align: center; transition: background 0.2s;
  }
  .target-role:hover { background: rgba(255,255,255,0.05); }
  .target-role .role-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.05rem; font-weight: 600; color: var(--white);
    margin-bottom: 0.35rem;
  }
  .target-role .role-sub {
    font-family: 'DM Mono', monospace; font-size: 0.6rem;
    letter-spacing: 0.1em; text-transform: uppercase; color: var(--gold);
  }

  /* EXPERTISE */
  #expertise { background: var(--paper); }

  .expertise-grid {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem;
  }

  .expertise-card {
    background: var(--white); padding: 2rem;
    border-top: 2px solid var(--gold);
    box-shadow: 0 2px 20px rgba(10,10,15,0.04);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .expertise-card:hover { transform: translateY(-4px); box-shadow: 0 8px 32px rgba(10,10,15,0.08); }

  .expertise-card h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.2rem; font-weight: 600; color: var(--navy); margin-bottom: 0.6rem;
  }
  .expertise-card p { font-size: 0.85rem; line-height: 1.7; color: var(--muted); }

  /* EXPERIENCE */
  #experience { background: #f0ede4; }

  .job-entry {
    padding: 2.5rem 0;
    border-bottom: 1px solid rgba(184,151,42,0.15);
  }
  .job-entry:last-child { border-bottom: none; }

  .job-top {
    display: grid; grid-template-columns: 1fr auto; align-items: start;
    gap: 1rem; margin-bottom: 0.4rem;
  }

  .job-company {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.55rem; font-weight: 600; color: var(--navy);
  }

  .job-date {
    font-family: 'DM Mono', monospace; font-size: 0.62rem;
    letter-spacing: 0.1em; color: var(--gold);
    text-transform: uppercase; white-space: nowrap;
    margin-top: 0.4rem;
  }

  .job-role {
    font-family: 'DM Mono', monospace; font-size: 0.68rem;
    letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--muted); margin-bottom: 1.25rem;
  }

  .job-bullets { list-style: none; display: flex; flex-direction: column; gap: 0.5rem; }
  .job-bullets li {
    font-size: 0.9rem; line-height: 1.7; color: var(--slate);
    padding-left: 1.25rem; position: relative;
  }
  .job-bullets li::before {
    content: '▪'; position: absolute; left: 0; color: var(--gold); font-size: 0.65rem; top: 0.3rem;
  }
  .job-bullets strong { color: var(--navy); font-weight: 600; }

  /* AWARDS */
  #awards { background: var(--white); }
  .awards-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 2rem; }
  .award-card {
    border-left: 3px solid var(--gold); padding: 1.5rem 1.75rem;
    background: var(--paper);
  }
  .award-card .award-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem; font-weight: 600; color: var(--navy); margin-bottom: 0.3rem;
  }
  .award-card .award-org {
    font-family: 'DM Mono', monospace; font-size: 0.6rem;
    letter-spacing: 0.12em; text-transform: uppercase; color: var(--gold);
    margin-bottom: 0.6rem;
  }
  .award-card p { font-size: 0.82rem; color: var(--muted); line-height: 1.6; }

  /* CREDENTIALS */
  #credentials { background: var(--paper); }
  .cred-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; }
  .edu-block h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.2rem; font-weight: 600; color: var(--navy);
  }
  .edu-block .degree { font-size: 0.9rem; color: var(--slate); margin: 0.25rem 0; }
  .edu-block .meta {
    font-family: 'DM Mono', monospace; font-size: 0.62rem;
    letter-spacing: 0.08em; color: var(--gold);
    margin-bottom: 1.25rem;
  }

  .cert-chips {
    display: flex; flex-wrap: wrap; gap: 0.5rem;
    margin-top: 0.75rem;
  }
  .cert-chip {
    background: var(--navy); color: var(--gold-light);
    padding: 0.35rem 0.85rem;
    font-family: 'DM Mono', monospace; font-size: 0.6rem;
    letter-spacing: 0.1em; text-transform: uppercase;
  }

  /* CONTACT */
  #contact {
    background: var(--navy); padding: 6rem 4rem;
    text-align: center;
  }
  #contact .section-label { justify-content: center; color: var(--gold); }
  #contact .section-label::after { display: none; }
  #contact h2 { color: var(--white); }
  #contact .sub { font-size: 1rem; color: rgba(255,255,255,0.55); margin-bottom: 3rem; max-width: 560px; margin-left: auto; margin-right: auto; line-height: 1.75; }

  .contact-row { display: flex; justify-content: center; gap: 3rem; flex-wrap: wrap; }
  .contact-item {
    display: flex; flex-direction: column; align-items: center; gap: 0.4rem;
    text-decoration: none; transition: transform 0.2s;
  }
  .contact-item:hover { transform: translateY(-3px); }
  .contact-item .c-label {
    font-family: 'DM Mono', monospace; font-size: 0.55rem;
    letter-spacing: 0.2em; text-transform: uppercase; color: var(--gold);
  }
  .contact-item .c-val {
    font-size: 0.92rem; color: var(--white); font-weight: 500;
  }

  footer {
    background: var(--ink); padding: 1.25rem;
    text-align: center;
    font-family: 'DM Mono', monospace; font-size: 0.58rem;
    letter-spacing: 0.1em; color: rgba(255,255,255,0.18);
  }

  /* DIVIDER */
  .divider { height: 1px; background: linear-gradient(to right, transparent, var(--gold), transparent); opacity: 0.35; }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(28px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .reveal {
    opacity: 0; transform: translateY(22px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.on { opacity: 1; transform: none; }

  /* MOBILE */
  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    #hero { padding: 6rem 1.5rem 3rem; }
    .hero-inner { grid-template-columns: 1fr; gap: 2.5rem; }
    .hero-watermark { display: none; }
    .section-wrap { padding: 4rem 1.5rem; }
    #targeting { padding: 2rem 1.5rem; }
    #targeting .inner { grid-template-columns: 1fr 1fr; }
    .expertise-grid { grid-template-columns: 1fr; }
    .awards-grid, .cred-grid { grid-template-columns: 1fr; }
    #contact { padding: 4rem 1.5rem; }
  }
</style>
</head>
<body>

<nav id="nav">
  <div class="nav-name">
    Cody Selvester
    <span>Enterprise Program Executive</span>
  </div>
  <ul class="nav-links">
    <li><a href="#targeting">Target Roles</a></li>
    <li><a href="#expertise">Expertise</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#credentials">Credentials</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-watermark">CS</div>
  <div class="hero-inner">
    <div class="hero-left">
      <div class="hero-badge">
        <div class="badge-dot"></div>
        Open to Executive & Director Opportunities
      </div>
      <h1>
        Matthew "Cody" Selvester
        <em>MBA · PMP · Lean Six Sigma</em>
      </h1>
      <div class="hero-titles">
        <div class="hero-title-item">Director of Program Management</div>
        <div class="hero-title-item">VP, Enterprise Delivery & EPMO</div>
        <div class="hero-title-item">Head of PMO / Chief of Staff</div>
      </div>
      <p class="hero-summary">
        20 years turning high-risk, high-visibility programs around — and building the governance infrastructure that prevents those crises from recurring. Brought in when failure isn't an option.
      </p>
      <div class="hero-ctas">
        <a href="#experience" class="btn-primary">View My Record</a>
        <a href="#contact" class="btn-ghost">Let's Talk</a>
      </div>
    </div>
    <div class="hero-right">
      <div class="stat-stack">
        <div class="stat-box">
          <div class="stat-num">$40M+</div>
          <div class="stat-desc">Fraud losses prevented</div>
          <div class="stat-sub">AI detection platform · 2025 Banking Tech Award</div>
        </div>
        <div class="stat-box">
          <div class="stat-num">$10M+</div>
          <div class="stat-desc">Recurring revenue generated</div>
          <div class="stat-sub">Enterprise Simplification Program, First Tech FCU</div>
        </div>
        <div class="stat-box">
          <div class="stat-num">20 yrs</div>
          <div class="stat-desc">Executive-level delivery</div>
          <div class="stat-sub">FinTech · Banking · SaaS · Healthcare · Fortune 500</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TARGETING STRIP -->
<div id="targeting">
  <div class="inner">
    <div class="target-role">
      <div class="role-title">Director, Program Management</div>
      <div class="role-sub">Enterprise · EPMO · Delivery</div>
    </div>
    <div class="target-role">
      <div class="role-title">VP, Enterprise Delivery</div>
      <div class="role-sub">Transformation · Governance</div>
    </div>
    <div class="target-role">
      <div class="role-title">Head of PMO</div>
      <div class="role-sub">Build-Out · Scale · Maturity</div>
    </div>
    <div class="target-role">
      <div class="role-title">Chief of Staff</div>
      <div class="role-sub">Executive Operations · Strategy</div>
    </div>
  </div>
</div>

<!-- EXPERTISE -->
<section id="expertise">
  <div class="section-wrap">
    <div class="section-label">Where I Excel</div>
    <h2>Executive-Level Capabilities</h2>
    <div class="expertise-grid">
      <div class="expertise-card reveal">
        <h3>EPMO Design & Governance</h3>
        <p>Built Enterprise PMOs from scratch — formalizing governance, standing up executive reporting, and creating the operating cadence that sustains delivery at scale.</p>
      </div>
      <div class="expertise-card reveal">
        <h3>Program Recovery & Turnaround</h3>
        <p>Repeatedly brought in to stabilize complex, failing programs under executive and regulatory scrutiny. Restores delivery confidence within weeks, not quarters.</p>
      </div>
      <div class="expertise-card reveal">
        <h3>AI & Fraud Platform Delivery</h3>
        <p>End-to-end deployment of enterprise AI initiatives with measurable outcomes — including an award-winning fraud detection platform that prevented $40M+ in losses.</p>
      </div>
      <div class="expertise-card reveal">
        <h3>Regulatory & Compliance Programs</h3>
        <p>Deep experience with FDIC-mandated KYC, KYB, and AML programs. Protects audit outcomes and reduces organizational regulatory exposure.</p>
      </div>
      <div class="expertise-card reveal">
        <h3>Revenue & Cost Impact</h3>
        <p>Architected programs that generate top-line revenue and protect margin — including a $10M+ ARR initiative and enterprise-wide efficiency gains of 40%.</p>
      </div>
      <div class="expertise-card reveal">
        <h3>Organizational Transformation</h3>
        <p>Builds the people, processes, and governance needed for lasting change — PM Communities of Practice, delivery maturity models, and cross-functional alignment.</p>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-wrap">
    <div class="section-label">Career History</div>
    <h2>20 Years of<br>High-Stakes Delivery</h2>

    <div class="job-entry reveal">
      <div class="job-top">
        <div class="job-company">Relanto AI</div>
        <div class="job-date">Nov 2025 – Present</div>
      </div>
      <div class="job-role">Lead Technical Program Manager · Fremont, CA</div>
      <ul class="job-bullets">
        <li>Leading a global portfolio of <strong>11 concurrent AI, analytics & enterprise platform initiatives</strong> for a Fortune 500 technology organization</li>
        <li>Directing cross-functional delivery across <strong>90+ engineers, architects & analysts</strong> spanning onsite and offshore teams</li>
        <li>Establishing executive governance infrastructure: portfolio reporting, risk management, dependency tracking, and stakeholder alignment</li>
        <li>Driving AI-enabled automation and analytics platforms supporting finance operations, enterprise reporting, and data governance</li>
      </ul>
    </div>

    <div class="job-entry reveal">
      <div class="job-top">
        <div class="job-company">Independent Consultant</div>
        <div class="job-date">Jan 2025 – Nov 2025</div>
      </div>
      <div class="job-role">Fractional Executive / Management Consultant · Concord, CA</div>
      <ul class="job-bullets">
        <li>Led M&A technical readiness for a B2B SaaS platform, consolidating cloud tooling and reducing post-acquisition operational risk</li>
        <li>Restored delivery cadence <strong>within 90 days</strong> by restructuring vendor contracts and stabilizing a global cloud security and fraud platform</li>
        <li>Architected and deployed ERP and go-to-market platforms with embedded audit, compliance, and fraud controls</li>
      </ul>
    </div>

    <div class="job-entry reveal">
      <div class="job-top">
        <div class="job-company">First Tech Federal Credit Union</div>
        <div class="job-date">Mar 2022 – Sep 2024</div>
      </div>
      <div class="job-role">Senior Principal Program Manager / Interim Director, EPMO · San Jose, CA</div>
      <ul class="job-bullets">
        <li>Deployed AI-driven fraud detection platform, <strong>preventing $40M+ in losses</strong> — honored with the 2025 Banking Tech Award for Best Use of Technology in Combatting Fraud</li>
        <li>Architected and delivered enterprise Simplification Program generating <strong>$10M+ in recurring annual revenue</strong></li>
        <li>Delivered six-week Online & Mobile Banking release across cybersecurity, fraud, legal, marketing, and UAT teams</li>
        <li>Built and scaled the Enterprise PMO from the ground up — governance, PM mentorship, and executive dashboards</li>
        <li>Improved enterprise delivery efficiency <strong>40%</strong> through systematic workflow redesign and tooling modernization</li>
        <li>Established PM Community of Practice, elevating execution discipline and delivery maturity organization-wide</li>
      </ul>
    </div>

    <div class="job-entry reveal">
      <div class="job-top">
        <div class="job-company">Bank of the West (BNP Paribas)</div>
        <div class="job-date">May 2015 – Mar 2022</div>
      </div>
      <div class="job-role">Senior Program Manager – Strategic Programs · San Ramon, CA</div>
      <ul class="job-bullets">
        <li>Delivered <strong>FDIC-mandated KYC, KYB & AML</strong> compliance programs, protecting audit outcomes and reducing enterprise regulatory exposure</li>
        <li>Governed a portfolio of <strong>15+ enterprise programs</strong>, increasing success rates 45% through governance redesign</li>
        <li>Translated NPS and CX analytics into enterprise-wide initiatives adopted across multiple lines of business</li>
      </ul>
    </div>

    <div class="job-entry reveal">
      <div class="job-top">
        <div class="job-company">AssetMark</div>
        <div class="job-date">Sep 2013 – May 2015</div>
      </div>
      <div class="job-role">Program Manager – Strategic Growth & Acceleration · Concord, CA</div>
      <ul class="job-bullets">
        <li>Built growth programs increasing advisor sign-ups <strong>33%</strong> and raising average production from $900K to $1.3M</li>
        <li>Expanded national distribution, adding <strong>450+ advisors</strong> and generating $800M+ in new production</li>
        <li>Designed onboarding frameworks reducing advisor time-to-productivity by <strong>58%</strong></li>
      </ul>
    </div>

    <div class="job-entry reveal">
      <div class="job-top">
        <div class="job-company">Kaiser Permanente · Wells Fargo · Amplify Tech</div>
        <div class="job-date">2005 – 2013</div>
      </div>
      <div class="job-role">Project Manager / Consultant · Finance · Healthcare · FinTech</div>
      <ul class="job-bullets">
        <li>Delivered compliance, IT, and enterprise transformation programs across regulated industries</li>
        <li>Built foundational expertise in delivery discipline, regulatory compliance, and stakeholder alignment</li>
      </ul>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- AWARDS -->
<section id="awards">
  <div class="section-wrap">
    <div class="section-label">Recognition</div>
    <h2>Awards & Honors</h2>
    <div class="awards-grid">
      <div class="award-card reveal">
        <div class="award-name">2025 Banking Tech Award</div>
        <div class="award-org">Best Use of Technology in Combatting Fraud</div>
        <p>Recognized for leading the AI-driven fraud detection platform deployment at First Tech FCU that prevented $40M+ in losses.</p>
      </div>
      <div class="award-card reveal">
        <div class="award-name">2023 Being Dynamic Award</div>
        <div class="award-org">First Tech Federal Credit Union</div>
        <p>Honored for advancing innovation, cultivating continuous improvement culture, and delivering measurable business outcomes.</p>
      </div>
      <div class="award-card reveal">
        <div class="award-name">2020 Leadership Award</div>
        <div class="award-org">Bank of the West</div>
        <p>Recognized for fostering cross-functional collaboration and building a high-performing culture across professional services teams.</p>
      </div>
      <div class="award-card reveal">
        <div class="award-name">Beta Gamma Sigma</div>
        <div class="award-org">UMass Dartmouth · MBA with 4.0 GPA</div>
        <p>Inducted into the international honor society for collegiate schools of business — top academic distinction.</p>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- CREDENTIALS -->
<section id="credentials">
  <div class="section-wrap">
    <div class="section-label">Education & Certifications</div>
    <h2>Credentials</h2>
    <div class="cred-grid">
      <div class="reveal">
        <div class="edu-block" style="margin-bottom:1.5rem;">
          <h3>University of Massachusetts Dartmouth</h3>
          <div class="degree">Master of Business Administration (MBA)</div>
          <div class="meta">Organizational Leadership · GPA 4.0 · Beta Gamma Sigma Honor Society</div>
        </div>
        <div class="edu-block">
          <h3>California State University, Chico</h3>
          <div class="degree">Bachelor of Science, Business Management</div>
          <div class="meta">Cum Laude · First Place, GLO-BUS Business Simulation</div>
        </div>
      </div>
      <div class="reveal">
        <div class="section-label" style="margin-bottom:1rem;">Active Certifications</div>
        <div class="cert-chips">
          <div class="cert-chip">PMP</div>
          <div class="cert-chip">PMI-ACP</div>
          <div class="cert-chip">CSM</div>
          <div class="cert-chip">ITIL</div>
          <div class="cert-chip">Lean Six Sigma Black Belt</div>
          <div class="cert-chip">MIT Strategic Tech Roadmapping</div>
          <div class="cert-chip">AI Foundations · IBM · NVIDIA · Google</div>
          <div class="cert-chip">Vertex AI Prompt Design</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label">Let's Connect</div>
  <h2 style="margin-bottom:1rem;">Ready to Lead<br>Your Next Initiative</h2>
  <p class="sub">Whether you're building an EPMO, stabilizing a critical program, or launching enterprise transformation — let's have a conversation.</p>
  <div class="contact-row">
    <a href="tel:5305015654" class="contact-item">
      <span class="c-label">Phone</span>
      <span class="c-val">530-501-5654</span>
    </a>
    <a href="mailto:mcselvester@gmail.com" class="contact-item">
      <span class="c-label">Email</span>
      <span class="c-val">mcselvester@gmail.com</span>
    </a>
    <a href="https://linkedin.com/in/mcselvester" target="_blank" class="contact-item">
      <span class="c-label">LinkedIn</span>
      <span class="c-val">linkedin.com/in/mcselvester</span>
    </a>
    <a href="#" class="contact-item">
      <span class="c-label">Location</span>
      <span class="c-val">Concord, CA · Bay Area</span>
    </a>
  </div>
</section>

<footer>© 2026 Matthew "Cody" Selvester · Concord, CA · Open to Director & VP Opportunities</footer>

<script>
  // Nav scroll effect
  window.addEventListener('scroll', () => {
    document.getElementById('nav').classList.toggle('scrolled', window.scrollY > 40);
  });

  // Scroll reveal
  const items = document.querySelectorAll('.reveal');
  const obs = new IntersectionObserver((entries) => {
    entries.forEach((e, i) => {
      if (e.isIntersecting) {
        setTimeout(() => e.target.classList.add('on'), i * 90);
        obs.unobserve(e.target);
      }
    });
  }, { threshold: 0.08 });
  items.forEach(el => obs.observe(el));
</script>
</body>
</html>
