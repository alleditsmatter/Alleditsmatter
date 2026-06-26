<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>All Edits Matter — Medical Marketing Agency</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;700;900&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --navy: #0A1628;
    --navy-mid: #1E3A5F;
    --blue-accent: #4A9EFF;
    --blue-soft: #EBF3FF;
    --white: #FFFFFF;
    --off-white: #F7F9FC;
    --text-muted: #6B7A8D;
    --rule: rgba(10,22,40,0.12);
    --gold: #C9A84C;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--white);
    color: var(--navy);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5vw;
    height: 72px;
    background: rgba(255,255,255,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--rule);
  }

  .nav-logo {
    display: flex; align-items: center; gap: 10px;
    text-decoration: none;
  }

  .logo-mark {
    width: 36px; height: 36px;
    background: var(--navy);
    border-radius: 6px;
    display: flex; align-items: center; justify-content: center;
    position: relative;
    flex-shrink: 0;
  }

  .logo-mark::before {
    content: 'AEM';
    color: var(--white);
    font-family: 'Inter', sans-serif;
    font-weight: 600;
    font-size: 9px;
    letter-spacing: 0.5px;
  }

  .logo-text {
    font-family: 'Playfair Display', serif;
    font-weight: 700;
    font-size: 17px;
    color: var(--navy);
    letter-spacing: -0.3px;
    line-height: 1.1;
  }

  .logo-sub {
    font-family: 'Inter', sans-serif;
    font-size: 9px;
    font-weight: 500;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--text-muted);
    display: block;
  }

  .nav-links {
    display: flex; align-items: center; gap: 36px;
    list-style: none;
  }

  .nav-links a {
    font-size: 13px; font-weight: 500;
    color: var(--navy); text-decoration: none;
    letter-spacing: 0.2px;
    opacity: 0.75;
    transition: opacity 0.2s;
  }

  .nav-links a:hover { opacity: 1; }

  .btn-nav {
    background: var(--navy);
    color: var(--white) !important;
    opacity: 1 !important;
    padding: 9px 22px;
    border-radius: 4px;
    font-size: 13px !important;
    font-weight: 500 !important;
    transition: background 0.2s !important;
  }

  .btn-nav:hover { background: var(--navy-mid) !important; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding-top: 72px;
  }

  .hero-left {
    background: var(--navy);
    display: flex; flex-direction: column; justify-content: center;
    padding: 80px 6vw 80px 5vw;
  }

  .hero-eyebrow {
    font-size: 11px; font-weight: 500; letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--blue-accent);
    margin-bottom: 28px;
  }

  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(38px, 4.5vw, 62px);
    font-weight: 700;
    color: var(--white);
    line-height: 1.1;
    letter-spacing: -1px;
    margin-bottom: 28px;
  }

  .hero-title em {
    font-style: italic;
    color: var(--blue-accent);
  }

  .hero-body {
    font-size: 15px; line-height: 1.75;
    color: rgba(255,255,255,0.65);
    max-width: 440px;
    margin-bottom: 48px;
  }

  .hero-cta-group {
    display: flex; align-items: center; gap: 20px;
    flex-wrap: wrap;
  }

  .btn-primary {
    background: var(--blue-accent);
    color: var(--white);
    padding: 14px 30px;
    border-radius: 4px;
    font-size: 14px; font-weight: 600;
    text-decoration: none;
    letter-spacing: 0.2px;
    transition: background 0.2s, transform 0.15s;
    display: inline-block;
  }

  .btn-primary:hover { background: #3a8eef; transform: translateY(-1px); }

  .btn-ghost {
    color: rgba(255,255,255,0.75);
    font-size: 14px; font-weight: 500;
    text-decoration: none;
    display: flex; align-items: center; gap: 8px;
    transition: color 0.2s;
  }

  .btn-ghost:hover { color: var(--white); }
  .btn-ghost::after { content: '→'; }

  .hero-right {
    background: var(--off-white);
    display: flex; flex-direction: column; justify-content: center;
    padding: 80px 5vw 80px 6vw;
    gap: 0;
  }

  .hero-stats-title {
    font-size: 11px; font-weight: 500; letter-spacing: 3px;
    text-transform: uppercase; color: var(--text-muted);
    margin-bottom: 48px;
  }

  .stat-block {
    padding: 32px 0;
    border-bottom: 1px solid var(--rule);
  }

  .stat-block:first-of-type { border-top: 1px solid var(--rule); }

  .stat-number {
    font-family: 'Playfair Display', serif;
    font-size: 52px;
    font-weight: 700;
    color: var(--navy);
    line-height: 1;
    letter-spacing: -2px;
  }

  .stat-number span {
    font-size: 26px;
    color: var(--blue-accent);
    letter-spacing: 0;
  }

  .stat-label {
    font-size: 13px; font-weight: 400;
    color: var(--text-muted);
    margin-top: 8px;
    line-height: 1.5;
  }

  /* ── SECTION BASE ── */
  section { padding: 100px 5vw; }

  .section-eyebrow {
    font-size: 11px; font-weight: 500; letter-spacing: 3px;
    text-transform: uppercase; color: var(--blue-accent);
    margin-bottom: 20px;
    display: block;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(30px, 3.5vw, 48px);
    font-weight: 700;
    line-height: 1.15;
    letter-spacing: -0.5px;
    color: var(--navy);
    margin-bottom: 20px;
  }

  .section-body {
    font-size: 15px; line-height: 1.8;
    color: var(--text-muted);
    max-width: 520px;
  }

  /* ── TRUST BAR ── */
  .trust-bar {
    background: var(--navy);
    padding: 24px 5vw;
    display: flex; align-items: center; justify-content: center;
    gap: 60px;
    flex-wrap: wrap;
  }

  .trust-item {
    font-size: 12px; font-weight: 500; letter-spacing: 2px;
    text-transform: uppercase;
    color: rgba(255,255,255,0.5);
  }

  .trust-separator {
    width: 1px; height: 16px;
    background: rgba(255,255,255,0.15);
  }

  /* ── WHY US ── */
  .why-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0;
    margin-top: 80px;
    border: 1px solid var(--rule);
  }

  .why-card {
    padding: 48px 44px;
    border-right: 1px solid var(--rule);
    border-bottom: 1px solid var(--rule);
    position: relative;
    transition: background 0.2s;
  }

  .why-card:hover { background: var(--blue-soft); }
  .why-card:nth-child(2n) { border-right: none; }

  .why-icon {
    width: 44px; height: 44px;
    background: var(--navy);
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 24px;
    font-size: 20px;
  }

  .why-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 20px; font-weight: 600;
    color: var(--navy);
    margin-bottom: 14px;
    line-height: 1.3;
  }

  .why-card p {
    font-size: 14px; line-height: 1.8;
    color: var(--text-muted);
  }

  /* ── SERVICES ── */
  .services { background: var(--navy); }
  .services .section-title { color: var(--white); }
  .services .section-body { color: rgba(255,255,255,0.55); }

  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: rgba(255,255,255,0.08);
    margin-top: 64px;
    border: 1px solid rgba(255,255,255,0.08);
  }

  .service-card {
    background: var(--navy);
    padding: 44px 36px;
    transition: background 0.25s;
    position: relative;
    overflow: hidden;
  }

  .service-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: var(--blue-accent);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }

  .service-card:hover { background: var(--navy-mid); }
  .service-card:hover::before { transform: scaleX(1); }

  .service-num {
    font-size: 11px; font-weight: 500; letter-spacing: 3px;
    color: var(--blue-accent);
    margin-bottom: 24px;
    display: block;
  }

  .service-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 20px; font-weight: 600;
    color: var(--white);
    margin-bottom: 16px;
    line-height: 1.3;
  }

  .service-card p {
    font-size: 13.5px; line-height: 1.75;
    color: rgba(255,255,255,0.5);
  }

  /* ── PROCESS ── */
  .process { background: var(--off-white); }

  .process-steps {
    display: flex; flex-direction: column;
    margin-top: 64px;
    border-top: 1px solid var(--rule);
  }

  .process-step {
    display: grid;
    grid-template-columns: 80px 1fr 1fr;
    align-items: start;
    padding: 40px 0;
    border-bottom: 1px solid var(--rule);
    gap: 40px;
  }

  .step-num {
    font-family: 'Playfair Display', serif;
    font-size: 40px; font-weight: 700;
    color: var(--blue-accent);
    opacity: 0.35;
    line-height: 1;
  }

  .step-title {
    font-family: 'Playfair Display', serif;
    font-size: 22px; font-weight: 600;
    color: var(--navy);
    margin-bottom: 10px;
  }

  .step-desc {
    font-size: 14px; line-height: 1.8;
    color: var(--text-muted);
  }

  .step-detail {
    font-size: 13px; line-height: 1.75;
    color: var(--text-muted);
    padding-left: 20px;
    border-left: 2px solid var(--rule);
  }

  /* ── SOCIAL PROOF ── */
  .proof-header {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: end;
    margin-bottom: 64px;
  }

  .testimonials {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
    margin-top: 0;
  }

  .testimonial {
    background: var(--off-white);
    padding: 36px 32px;
    border-radius: 2px;
    position: relative;
  }

  .testimonial::before {
    content: '"';
    font-family: 'Playfair Display', serif;
    font-size: 72px;
    color: var(--blue-accent);
    opacity: 0.2;
    position: absolute;
    top: 10px; left: 24px;
    line-height: 1;
  }

  .testimonial p {
    font-size: 14px; line-height: 1.8;
    color: var(--navy);
    margin-bottom: 24px;
    padding-top: 20px;
    font-style: italic;
  }

  .testimonial-author {
    display: flex; align-items: center; gap: 12px;
  }

  .author-avatar {
    width: 40px; height: 40px;
    background: var(--navy);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 14px; font-weight: 600;
    color: var(--white);
    flex-shrink: 0;
  }

  .author-name {
    font-size: 13px; font-weight: 600;
    color: var(--navy);
  }

  .author-role {
    font-size: 12px; color: var(--text-muted);
  }

  /* ── CTA ── */
  .cta-section {
    background: var(--navy);
    text-align: center;
    padding: 120px 5vw;
    position: relative;
    overflow: hidden;
  }

  .cta-section::before {
    content: '';
    position: absolute;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(74,158,255,0.12) 0%, transparent 70%);
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    pointer-events: none;
  }

  .cta-section .section-title {
    color: var(--white);
    max-width: 600px;
    margin: 0 auto 20px;
  }

  .cta-section .section-body {
    max-width: 480px;
    margin: 0 auto 48px;
    color: rgba(255,255,255,0.55);
  }

  .cta-form {
    display: flex; gap: 12px; justify-content: center;
    flex-wrap: wrap;
    max-width: 480px;
    margin: 0 auto;
  }

  .cta-form input {
    flex: 1; min-width: 200px;
    padding: 14px 18px;
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 4px;
    color: var(--white);
    font-size: 14px; font-family: 'Inter', sans-serif;
    outline: none;
    transition: border-color 0.2s;
  }

  .cta-form input::placeholder { color: rgba(255,255,255,0.35); }
  .cta-form input:focus { border-color: var(--blue-accent); }

  .cta-form button {
    background: var(--blue-accent);
    color: var(--white);
    border: none; cursor: pointer;
    padding: 14px 28px;
    border-radius: 4px;
    font-size: 14px; font-weight: 600;
    font-family: 'Inter', sans-serif;
    transition: background 0.2s;
    white-space: nowrap;
  }

  .cta-form button:hover { background: #3a8eef; }

  .cta-note {
    font-size: 12px; color: rgba(255,255,255,0.35);
    margin-top: 16px;
  }

  /* ── FOOTER ── */
  footer {
    background: #060E1A;
    padding: 60px 5vw 32px;
    color: rgba(255,255,255,0.4);
  }

  .footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 1fr;
    gap: 48px;
    padding-bottom: 48px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
    margin-bottom: 32px;
  }

  .footer-brand-name {
    font-family: 'Playfair Display', serif;
    font-size: 18px; font-weight: 700;
    color: var(--white);
    margin-bottom: 14px;
  }

  .footer-brand-desc {
    font-size: 13px; line-height: 1.75;
    margin-bottom: 24px;
    max-width: 280px;
  }

  .footer-col h4 {
    font-size: 11px; font-weight: 600; letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--white);
    margin-bottom: 20px;
  }

  .footer-col ul { list-style: none; }

  .footer-col ul li {
    margin-bottom: 10px;
  }

  .footer-col ul li a {
    font-size: 13px;
    color: rgba(255,255,255,0.4);
    text-decoration: none;
    transition: color 0.2s;
  }

  .footer-col ul li a:hover { color: rgba(255,255,255,0.8); }

  .footer-bottom {
    display: flex; justify-content: space-between; align-items: center;
    font-size: 12px;
    flex-wrap: wrap; gap: 12px;
  }

  .footer-bottom a {
    color: rgba(255,255,255,0.4);
    text-decoration: none;
  }

  /* ── BADGE ── */
  .badge {
    display: inline-block;
    background: rgba(74,158,255,0.12);
    color: var(--blue-accent);
    font-size: 11px; font-weight: 500; letter-spacing: 1px;
    padding: 4px 10px; border-radius: 2px;
    text-transform: uppercase;
    margin-bottom: 16px;
  }

  /* ── MOBILE ── */
  @media (max-width: 900px) {
    .hero { grid-template-columns: 1fr; }
    .hero-left { padding: 60px 6vw; }
    .hero-right { padding: 60px 6vw; display: none; }
    .why-grid { grid-template-columns: 1fr; }
    .why-card { border-right: none; }
    .services-grid { grid-template-columns: 1fr; }
    .process-step { grid-template-columns: 60px 1fr; }
    .step-detail { display: none; }
    .testimonials { grid-template-columns: 1fr; }
    .proof-header { grid-template-columns: 1fr; gap: 24px; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    .nav-links { display: none; }
  }

  /* scroll animations */
  .fade-up {
    opacity: 0;
    transform: translateY(28px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .fade-up.visible {
    opacity: 1;
    transform: translateY(0);
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">
    <div class="logo-mark"></div>
    <div>
      <span class="logo-text">All Edits Matter</span>
      <span class="logo-sub">Medical Marketing Agency</span>
    </div>
  </a>
  <ul class="nav-links">
    <li><a href="#why">Why Us</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#process">Process</a></li>
    <li><a href="#results">Results</a></li>
    <li><a href="#contact" class="btn-nav">Get a Free Audit</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <p class="hero-eyebrow">Exclusive to Healthcare & Medical Practices</p>
    <h1 class="hero-title">
      Marketing that<br/>
      fills your<br/>
      <em>appointment book.</em>
    </h1>
    <p class="hero-body">
      We help dental clinics, medical practices, and hospitals across the US attract more patients, dominate local search, and build a reputation that makes choosing you an easy decision.
    </p>
    <div class="hero-cta-group">
      <a href="#contact" class="btn-primary">Get Your Free Clinic Audit</a>
      <a href="#services" class="btn-ghost">See our services</a>
    </div>
  </div>
  <div class="hero-right">
    <p class="hero-stats-title">Proven results across US clinics</p>
    <div class="stat-block fade-up">
      <div class="stat-number">3.8<span>×</span></div>
      <div class="stat-label">Average increase in new patient inquiries within 90 days</div>
    </div>
    <div class="stat-block fade-up">
      <div class="stat-number">200<span>+</span></div>
      <div class="stat-label">Healthcare practices grown across the United States</div>
    </div>
    <div class="stat-block fade-up">
      <div class="stat-number">#1</div>
      <div class="stat-label">Google rankings achieved for local medical searches</div>
    </div>
  </div>
</section>

<!-- TRUST BAR -->
<div class="trust-bar">
  <span class="trust-item">Dental Clinics</span>
  <div class="trust-separator"></div>
  <span class="trust-item">Medical Practices</span>
  <div class="trust-separator"></div>
  <span class="trust-item">Hospitals</span>
  <div class="trust-separator"></div>
  <span class="trust-item">Urgent Care Centers</span>
  <div class="trust-separator"></div>
  <span class="trust-item">Specialty Clinics</span>
  <div class="trust-separator"></div>
  <span class="trust-item">Cosmetic Practices</span>
</div>

<!-- WHY US -->
<section id="why">
  <div class="fade-up">
    <span class="section-eyebrow">Why All Edits Matter</span>
    <h2 class="section-title">We only work with<br/>healthcare. That's our edge.</h2>
    <p class="section-body">Generic marketing agencies treat your clinic like a restaurant. We understand patient psychology, HIPAA sensitivities, and what it takes to earn trust in medical marketing.</p>
  </div>

  <div class="why-grid">
    <div class="why-card fade-up">
      <div class="why-icon">🏥</div>
      <h3>Healthcare-Only Focus</h3>
      <p>We don't take on ecommerce brands or restaurants. Every strategy we build is crafted for the unique dynamics of medical and dental patient acquisition.</p>
    </div>
    <div class="why-card fade-up">
      <div class="why-icon">📈</div>
      <h3>ROI-First Thinking</h3>
      <p>We measure success in booked appointments, not vanity metrics. Every campaign is tracked against real revenue outcomes for your practice.</p>
    </div>
    <div class="why-card fade-up">
      <div class="why-icon">🔒</div>
      <h3>HIPAA-Aware Marketing</h3>
      <p>We understand the compliance landscape. Your campaigns are built with patient privacy baked in — no workarounds, no risk to your license.</p>
    </div>
    <div class="why-card fade-up">
      <div class="why-icon">🌐</div>
      <h3>US Market Specialists</h3>
      <p>We live and breathe the US healthcare market — local SEO, Google Health ads, insurance-based targeting, and competitive clinic markets.</p>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
  <span class="section-eyebrow">What we do</span>
  <h2 class="section-title">Six services.<br/>One goal — more patients.</h2>
  <p class="section-body">Every service is designed specifically for clinics and medical practices looking to grow their patient base sustainably.</p>

  <div class="services-grid">
    <div class="service-card fade-up">
      <span class="service-num">01</span>
      <h3>SEO & Google Rankings</h3>
      <p>Dominate "dentist near me" and specialty searches in your city. We build long-term organic visibility that brings patients in while you sleep.</p>
    </div>
    <div class="service-card fade-up">
      <span class="service-num">02</span>
      <h3>Social Media Marketing</h3>
      <p>Build a trusted presence on Instagram and Facebook that attracts patients, showcases your expertise, and keeps your community engaged.</p>
    </div>
    <div class="service-card fade-up">
      <span class="service-num">03</span>
      <h3>Paid Ads (Meta & Google)</h3>
      <p>Precision-targeted campaigns that put your practice in front of patients actively searching for your services — with ad spend that converts.</p>
    </div>
    <div class="service-card fade-up">
      <span class="service-num">04</span>
      <h3>Clinic Website Design</h3>
      <p>Fast, mobile-first, conversion-optimized websites that make it effortless for patients to find you, trust you, and book an appointment.</p>
    </div>
    <div class="service-card fade-up">
      <span class="service-num">05</span>
      <h3>Reputation Management</h3>
      <p>Systematically grow your Google reviews, respond to feedback professionally, and build the 5-star profile patients are looking for.</p>
    </div>
    <div class="service-card fade-up">
      <span class="service-num">06</span>
      <h3>Lead Generation</h3>
      <p>End-to-end funnels designed to capture, nurture, and convert patient leads — from first click to confirmed appointment on your calendar.</p>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="process" id="process">
  <div class="fade-up">
    <span class="section-eyebrow">How it works</span>
    <h2 class="section-title">From first call to<br/>full waiting room.</h2>
    <p class="section-body">A clear, four-step engagement built around your practice's specific goals — no bloated retainers or mystery deliverables.</p>
  </div>

  <div class="process-steps">
    <div class="process-step fade-up">
      <div class="step-num">01</div>
      <div>
        <div class="step-title">Free Clinic Audit</div>
        <p class="step-desc">We review your current online presence — SEO, reviews, ads, website — and identify exactly where growth is being lost.</p>
      </div>
      <div class="step-detail">We deliver a comprehensive 20-point audit report covering your Google Business Profile, local search rankings, competitor gap analysis, and conversion bottlenecks. No sales pitch — just clarity.</div>
    </div>
    <div class="process-step fade-up">
      <div class="step-num">02</div>
      <div>
        <div class="step-title">Custom Strategy Build</div>
        <p class="step-desc">We design a 90-day growth plan tailored to your specialty, location, budget, and competitive landscape.</p>
      </div>
      <div class="step-detail">Your strategy includes channel prioritization, monthly content calendars, ad budget allocation, and milestone-based KPIs so you always know what we're working towards and why.</div>
    </div>
    <div class="process-step fade-up">
      <div class="step-num">03</div>
      <div>
        <div class="step-title">Launch & Execute</div>
        <p class="step-desc">Our team handles everything — campaigns, content, website updates, review outreach — so you focus on your patients.</p>
      </div>
      <div class="step-detail">You get a dedicated account manager, weekly execution updates, and access to a real-time dashboard showing leads, rankings, and ad performance at any time.</div>
    </div>
    <div class="process-step fade-up">
      <div class="step-num">04</div>
      <div>
        <div class="step-title">Report & Scale</div>
        <p class="step-desc">Monthly reporting ties every dollar back to real patient acquisition — and we scale what's working.</p>
      </div>
      <div class="step-detail">No vanity metrics. Your monthly report includes cost-per-lead, appointment conversion rate, revenue attributed to campaigns, and strategic recommendations for the next 30 days.</div>
    </div>
  </div>
</section>

<!-- RESULTS / TESTIMONIALS -->
<section id="results">
  <div class="proof-header">
    <div class="fade-up">
      <span class="section-eyebrow">What clinic owners say</span>
      <h2 class="section-title">Real results from<br/>real practices.</h2>
    </div>
    <div class="fade-up">
      <p class="section-body">We've helped clinics go from empty appointment slots to waitlists — across dental, family medicine, dermatology, and specialty practices.</p>
    </div>
  </div>

  <div class="testimonials">
    <div class="testimonial fade-up">
      <p>Within 60 days of working with All Edits Matter, our new patient calls doubled. Their Google Ads strategy was unlike anything we'd seen from previous agencies — surgical and effective.</p>
      <div class="testimonial-author">
        <div class="author-avatar">DR</div>
        <div>
          <div class="author-name">Dr. Rachel Kim</div>
          <div class="author-role">Owner, Bright Smile Dental — Austin, TX</div>
        </div>
      </div>
    </div>
    <div class="testimonial fade-up">
      <p>We went from 3.2 to 4.8 stars on Google in four months. The reputation management system they built is now running on autopilot. Patients mention our reviews constantly.</p>
      <div class="testimonial-author">
        <div class="author-avatar">MP</div>
        <div>
          <div class="author-name">Dr. Marcus Patel</div>
          <div class="author-role">Medical Director, ClearPath Family Clinic — Chicago, IL</div>
        </div>
      </div>
    </div>
    <div class="testimonial fade-up">
      <p>I was skeptical about social media for a medical practice. They proved me wrong. Our Instagram now generates more referrals than word-of-mouth used to. Remarkable work.</p>
      <div class="testimonial-author">
        <div class="author-avatar">SL</div>
        <div>
          <div class="author-name">Dr. Sophia Lane</div>
          <div class="author-role">Founder, LaneDerm Aesthetics — Miami, FL</div>
        </div>
      </div>
    </div>
    <div class="testimonial fade-up">
      <p>Their new website for our practice cut our bounce rate by 40% and tripled our online appointment bookings in the first month alone. Clean, fast, and it converts.</p>
      <div class="testimonial-author">
        <div class="author-avatar">JN</div>
        <div>
          <div class="author-name">Dr. James Nguyen</div>
          <div class="author-role">Co-founder, Northside Urgent Care — Seattle, WA</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CTA -->
<section class="cta-section" id="contact">
  <span class="section-eyebrow" style="color: var(--blue-accent);">Let's talk growth</span>
  <h2 class="section-title">Your next 100 patients<br/>are one audit away.</h2>
  <p class="section-body">Get a free, no-obligation audit of your clinic's online presence. We'll show you exactly where you're losing patients — and how to fix it.</p>
  <div class="cta-form">
    <input type="email" placeholder="Your email address" />
    <button type="button">Get Free Audit</button>
  </div>
  <p class="cta-note">No spam. No commitment. Just clarity on where your growth is hiding.</p>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div>
      <div class="footer-brand-name">All Edits Matter</div>
      <p class="footer-brand-desc">Premium digital marketing for dental clinics, medical practices, and hospitals across the United States.</p>
      <p style="font-size: 12px;">hello@alleditsmatter.com</p>
    </div>
    <div class="footer-col">
      <h4>Services</h4>
      <ul>
        <li><a href="#">SEO & Rankings</a></li>
        <li><a href="#">Social Media</a></li>
        <li><a href="#">Paid Ads</a></li>
        <li><a href="#">Website Design</a></li>
        <li><a href="#">Reputation Mgmt</a></li>
        <li><a href="#">Lead Generation</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Industries</h4>
      <ul>
        <li><a href="#">Dental Clinics</a></li>
        <li><a href="#">Medical Practices</a></li>
        <li><a href="#">Hospitals</a></li>
        <li><a href="#">Urgent Care</a></li>
        <li><a href="#">Specialty Clinics</a></li>
        <li><a href="#">Cosmetic Practices</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Company</h4>
      <ul>
        <li><a href="#">About</a></li>
        <li><a href="#">Case Studies</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Contact</a></li>
        <li><a href="#">Privacy Policy</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <span>© 2025 All Edits Matter. All rights reserved.</span>
    <span>Serving dental & medical practices across the United States</span>
  </div>
</footer>

<script>
  // Scroll fade-in
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(el => {
      if (el.isIntersecting) {
        el.target.classList.add('visible');
        observer.unobserve(el.target);
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

  // Smooth scroll for nav
  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      const target = document.querySelector(a.getAttribute('href'));
      if (target) {
        e.preventDefault();
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });
</script>
</body>
</html>
