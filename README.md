[academic-website (1).html](https://github.com/user-attachments/files/26942435/academic-website.1.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Wilson Turner — Materials Chemistry</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500&family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Source+Sans+3:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --navy: #7a1c2e;
    --navy-light: #9e2a3f;
    --gold: #7a9490;
    --gold-light: #96aaa6;
    --cream: #f7f5f0;
    --cream-dark: #eae7e0;
    --text: #1e1a18;
    --text-mid: #48423e;
    --text-muted: #7a7470;
    --rule: #c8c3bc;
    --white: #ffffff;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 18px;
    line-height: 1.75;
    color: var(--text);
    background: var(--cream);
  }

  /* ── NAV ── */
  nav {
    position: sticky;
    top: 0;
    z-index: 100;
    background: var(--navy);
    border-bottom: 3px solid var(--gold);
  }
  .nav-inner {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 54px;
  }
  .nav-brand {
    font-family: 'Libre Baskerville', serif;
    font-size: 15px;
    color: var(--cream);
    letter-spacing: 0.04em;
    text-decoration: none;
    white-space: nowrap;
  }
  .nav-links {
    display: flex;
    gap: 0;
    list-style: none;
  }
  .nav-links a {
    display: block;
    padding: 0 1rem;
    font-family: 'Source Sans 3', sans-serif;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: rgba(247,244,239,0.75);
    text-decoration: none;
    line-height: 54px;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold-light); }

  /* ── HERO ── */
  #hero {
    background: var(--navy);
    color: var(--cream);
    padding: 5rem 2rem 4.5rem;
    border-bottom: 1px solid var(--navy-light);
  }
  .hero-inner {
    max-width: 1100px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 200px 1fr;
    gap: 3rem;
    align-items: center;
  }
  .hero-photo {
    width: 200px;
    height: 200px;
    border-radius: 4px;
    background: var(--navy-light);
    border: 3px solid var(--gold);
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    flex-shrink: 0;
  }
  .hero-photo-placeholder {
    font-family: 'Libre Baskerville', serif;
    font-size: 64px;
    color: var(--gold);
    opacity: 0.6;
  }
  .hero-text h1 {
    font-family: 'Libre Baskerville', serif;
    font-size: 2.6rem;
    font-weight: 400;
    line-height: 1.2;
    color: var(--white);
    margin-bottom: 0.4rem;
  }
  .hero-text .title {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 1rem;
    font-weight: 400;
    letter-spacing: 0.06em;
    color: var(--gold-light);
    text-transform: uppercase;
    margin-bottom: 1.25rem;
  }
  .hero-text .tagline {
    font-size: 1.15rem;
    color: rgba(247,244,239,0.8);
    font-style: italic;
    margin-bottom: 1.5rem;
    max-width: 560px;
  }
  .hero-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
  }
  .btn {
    display: inline-block;
    padding: 0.5rem 1.25rem;
    font-family: 'Source Sans 3', sans-serif;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 2px;
    transition: background 0.2s, color 0.2s;
  }
  .btn-gold {
    background: var(--gold);
    color: var(--white);
    border: 1.5px solid var(--gold);
  }
  .btn-gold:hover { background: var(--gold-light); border-color: var(--gold-light); }
  .btn-outline {
    background: transparent;
    color: var(--cream);
    border: 1.5px solid rgba(247,244,239,0.4);
  }
  .btn-outline:hover { border-color: var(--cream); }

  /* ── MAIN LAYOUT ── */
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  section {
    padding: 4rem 0;
    border-bottom: 1px solid var(--rule);
  }
  section:last-child { border-bottom: none; }

  .section-label {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 0.5rem;
  }
  h2 {
    font-family: 'Libre Baskerville', serif;
    font-size: 1.9rem;
    font-weight: 400;
    color: var(--navy);
    margin-bottom: 2rem;
    padding-bottom: 0.75rem;
    border-bottom: 2px solid var(--navy);
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 3.5rem;
    align-items: start;
  }
  .about-body p {
    margin-bottom: 1.1rem;
    color: var(--text-mid);
  }
  .about-body p:last-child { margin-bottom: 0; }

  .info-block {
    background: var(--white);
    border: 1px solid var(--rule);
    border-top: 3px solid var(--navy);
    padding: 1.5rem;
  }
  .info-block h3 {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 1rem;
  }
  .info-item {
    display: flex;
    gap: 0.6rem;
    align-items: flex-start;
    margin-bottom: 0.9rem;
    font-size: 16px;
  }
  .info-item:last-child { margin-bottom: 0; }
  .info-icon {
    width: 18px;
    height: 18px;
    flex-shrink: 0;
    margin-top: 2px;
    opacity: 0.55;
  }
  .info-item a { color: var(--navy); text-decoration: underline; text-decoration-color: transparent; }
  .info-item a:hover { text-decoration-color: var(--gold); }

  /* ── RESEARCH ── */
  .research-intro {
    font-size: 1.05rem;
    color: var(--text-mid);
    margin-bottom: 2.5rem;
    max-width: 680px;
  }
  .research-areas {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    margin-bottom: 2.5rem;
  }
  .area-card {
    background: var(--white);
    border: 1px solid var(--rule);
    padding: 1.5rem;
    position: relative;
  }
  .area-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: var(--navy);
  }
  .area-card h3 {
    font-family: 'Libre Baskerville', serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 0.6rem;
  }
  .area-card p {
    font-size: 16px;
    color: var(--text-muted);
    line-height: 1.6;
  }
  .area-number {
    font-family: 'Libre Baskerville', serif;
    font-size: 2.5rem;
    color: var(--cream-dark);
    font-style: italic;
    position: absolute;
    top: 0.75rem;
    right: 1rem;
    line-height: 1;
    pointer-events: none;
  }

  .funding-note {
    background: var(--navy);
    color: rgba(247,244,239,0.85);
    padding: 1.25rem 1.5rem;
    font-size: 16px;
    display: flex;
    gap: 1rem;
    align-items: flex-start;
  }
  .funding-note strong { color: var(--gold-light); }

  /* ── PUBLICATIONS ── */
  .pub-filters {
    display: flex;
    gap: 0.5rem;
    margin-bottom: 2rem;
    flex-wrap: wrap;
  }
  .filter-btn {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 13px;
    padding: 0.3rem 1rem;
    border: 1px solid var(--rule);
    background: var(--white);
    color: var(--text-muted);
    cursor: pointer;
    border-radius: 2px;
    transition: all 0.15s;
  }
  .filter-btn.active, .filter-btn:hover {
    background: var(--navy);
    color: var(--cream);
    border-color: var(--navy);
  }

  .pub-list { display: flex; flex-direction: column; gap: 0; }
  .pub-item {
    padding: 1.4rem 0;
    border-bottom: 1px solid var(--cream-dark);
    display: grid;
    grid-template-columns: 48px 1fr;
    gap: 1rem;
    align-items: start;
  }
  .pub-item:last-child { border-bottom: none; }
  .pub-year {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 13px;
    font-weight: 600;
    color: var(--text-muted);
    padding-top: 3px;
  }
  .pub-content { }
  .pub-title {
    font-size: 1rem;
    font-weight: 600;
    color: var(--navy);
    margin-bottom: 0.2rem;
    font-style: italic;
    font-family: 'Libre Baskerville', serif;
  }
  .pub-authors {
    font-size: 15px;
    color: var(--text-muted);
    margin-bottom: 0.2rem;
  }
  .pub-authors strong { color: var(--text); font-weight: 600; }
  .pub-journal {
    font-size: 15px;
    color: var(--text-mid);
  }
  .pub-journal em { font-style: italic; }
  .pub-badge {
    display: inline-block;
    font-family: 'Source Sans 3', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    padding: 1px 7px;
    margin-left: 0.5rem;
    border-radius: 2px;
    vertical-align: middle;
  }
  .badge-selected { background: #e8f0e0; color: #3a6018; border: 1px solid #a8c87a; }
  .badge-cover { background: #e8eef6; color: #1a4070; border: 1px solid #7aaad4; }

  /* ── CV ── */
  .cv-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
  }
  .cv-section h3 {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1rem;
    padding-bottom: 0.4rem;
    border-bottom: 1px solid var(--rule);
  }
  .cv-entry {
    margin-bottom: 1.4rem;
  }
  .cv-entry-head {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 1rem;
    margin-bottom: 0.15rem;
  }
  .cv-entry-title {
    font-size: 17px;
    font-weight: 600;
    color: var(--text);
    font-family: 'Libre Baskerville', serif;
  }
  .cv-entry-date {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 13px;
    color: var(--text-muted);
    white-space: nowrap;
    flex-shrink: 0;
  }
  .cv-entry-sub {
    font-size: 15px;
    color: var(--text-mid);
    font-style: italic;
  }
  .cv-entry-detail {
    font-size: 15px;
    color: var(--text-muted);
    margin-top: 0.2rem;
  }

  .cv-download {
    margin-top: 2rem;
    padding: 1.25rem 1.5rem;
    background: var(--cream-dark);
    border: 1px solid var(--rule);
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
  }
  .cv-download p {
    font-size: 16px;
    color: var(--text-mid);
  }

  /* ── TEACHING ── */
  .teaching-intro {
    font-size: 1.05rem;
    color: var(--text-mid);
    margin-bottom: 2.5rem;
    max-width: 680px;
  }
  .teaching-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    margin-bottom: 2.5rem;
  }
  .course-card {
    padding: 1.4rem 1.5rem;
    background: var(--white);
    border: 1px solid var(--rule);
    border-left: 4px solid var(--navy);
  }
  .course-code {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.1em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 0.25rem;
  }
  .course-name {
    font-family: 'Libre Baskerville', serif;
    font-size: 1.05rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 0.4rem;
  }
  .course-meta {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 14px;
    color: var(--text-muted);
    margin-bottom: 0.6rem;
  }
  .course-desc {
    font-size: 15px;
    color: var(--text-mid);
    line-height: 1.6;
  }

  .mentoring-block {
    background: var(--white);
    border: 1px solid var(--rule);
    padding: 1.75rem 2rem;
  }
  .mentoring-block h3 {
    font-family: 'Libre Baskerville', serif;
    font-size: 1.2rem;
    color: var(--navy);
    margin-bottom: 1rem;
  }
  .mentee-list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
  }
  .mentee {
    font-size: 15px;
  }
  .mentee-name {
    font-weight: 600;
    color: var(--text);
    display: block;
  }
  .mentee-role {
    color: var(--text-muted);
    font-size: 14px;
    font-style: italic;
  }

  /* ── CONTACT ── */
  #contact { background: var(--white); }
  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
  }
  .contact-info h3 {
    font-family: 'Libre Baskerville', serif;
    font-size: 1.3rem;
    color: var(--navy);
    margin-bottom: 1.25rem;
  }
  .contact-row {
    display: flex;
    gap: 1rem;
    align-items: flex-start;
    margin-bottom: 1rem;
    font-size: 17px;
  }
  .contact-label {
    font-family: 'Source Sans 3', sans-serif;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--text-muted);
    min-width: 80px;
    padding-top: 2px;
  }
  .contact-val { color: var(--text-mid); }
  .contact-val a { color: var(--navy); }

  .contact-form h3 {
    font-family: 'Libre Baskerville', serif;
    font-size: 1.3rem;
    color: var(--navy);
    margin-bottom: 1.25rem;
  }
  .form-field { margin-bottom: 1.1rem; }
  .form-field label {
    display: block;
    font-family: 'Source Sans 3', sans-serif;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 0.35rem;
  }
  .form-field input,
  .form-field textarea {
    width: 100%;
    padding: 0.6rem 0.85rem;
    font-family: 'Source Sans 3', sans-serif;
    font-size: 15px;
    border: 1px solid var(--rule);
    background: var(--cream);
    color: var(--text);
    border-radius: 0;
    outline: none;
    transition: border-color 0.2s;
  }
  .form-field input:focus,
  .form-field textarea:focus { border-color: var(--navy); background: var(--white); }
  .form-field textarea { resize: vertical; min-height: 110px; }
  .form-submit {
    background: var(--navy);
    color: var(--cream);
    border: none;
    padding: 0.65rem 2rem;
    font-family: 'Source Sans 3', sans-serif;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    cursor: pointer;
    border-radius: 2px;
    transition: background 0.2s;
  }
  .form-submit:hover { background: var(--navy-light); }

  /* ── FOOTER ── */
  footer {
    background: var(--navy);
    color: rgba(247,244,239,0.5);
    padding: 2rem;
    text-align: center;
    font-family: 'Source Sans 3', sans-serif;
    font-size: 13px;
    letter-spacing: 0.04em;
  }
  footer a { color: rgba(247,244,239,0.7); }

  /* ── RESPONSIVE ── */
  @media (max-width: 800px) {
    .hero-inner { grid-template-columns: 1fr; text-align: center; }
    .hero-photo { margin: 0 auto; }
    .hero-links { justify-content: center; }
    .about-grid, .cv-grid, .contact-grid, .teaching-grid { grid-template-columns: 1fr; }
    .research-areas { grid-template-columns: 1fr; }
    .mentee-list { grid-template-columns: 1fr 1fr; }
    .nav-links a { padding: 0 0.6rem; font-size: 11px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a href="#hero" class="nav-brand">Wilson Turner</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#research">Research</a></li>
      <li><a href="#publications">Publications</a></li>
      <li><a href="#cv">CV</a></li>
      <li><a href="#teaching">Teaching</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-inner">
    <div class="hero-photo">
      <span class="hero-photo-placeholder">◎</span>
      <!-- Replace with: <img src="photo.jpg" alt="Dr. [Your Name]" style="width:100%;height:100%;object-fit:cover;"> -->
    </div>
    <div class="hero-text">
      <h1>Wilson Turner</h1>
      <p class="title">Ph.D. Candidate · Bao Research Group · Stanford University</p>
      <p class="tagline">Functional materials designed from atoms upwards.</p>
      <div class="hero-links">
        <a href="#research" class="btn btn-gold">View Research</a>
        <a href="#publications" class="btn btn-outline">Publications</a>
        <a href="cv.pdf" class="btn btn-outline">Download CV</a>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="container">
    <div class="section-label">About</div>
    <h2>Biography</h2>
    <div class="about-grid">
      <div class="about-body">
        <p>I am a polymer chemist and engineer interested in making things that have never before existed. My graduate work, conducted in the Bao Research Group at Stanford University, focuses on the design, synthesis, and engineering of shape-memory materials — functional polymers able to reversibly transform between multiple programmed states. This work bridges organic synthesis, materials characterization, and device fabrication to create fundamentally new functional materials.</p>
        <p>I completed my B.S. in Molecular Engineering with a specialization in polymeric materials engineering at the University of Chicago. My undergraduate thesis was performed under Prof. Stuart Rowan, where I developed a class of previously inaccessible doubly-threaded poly[3]rotaxane networks and studied their unique rheological properties.</p>
        <p>My graduate research is supported by the NSF Graduate Research Fellowship and the Stanford EDGE Fellowship. During my undergraduate studies I was supported by the Odyssey Scholarship, the Barry Goldwater Scholarship, and the Astronaut Scholarship.</p>
      </div>
      <div>
        <div class="info-block">
          <h3>Contact & Links</h3>
          <div class="info-item">
            <svg class="info-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
              <path d="M4 4h16v16H4z" rx="2"/><path d="M22 6l-10 7L2 6"/>
            </svg>
            <span><a href="/cdn-cgi/l/email-protection#90e7e2e4e5e2fef5e2d0e3e4f1fef6ffe2f4bef5f4e5"><span class="__cf_email__" data-cfemail="80f7f2f4f5f2eee5f2c0f3f4e1eee6eff2e4aee5e4f5">[email&#160;protected]</span></a></span>
          </div>
          <div class="info-item">
            <svg class="info-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
              <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7z"/>
              <circle cx="12" cy="9" r="2.5"/>
            </svg>
            <span>Bao Research Group, Stanford University</span>
          </div>
          <div class="info-item">
            <svg class="info-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
              <path d="M12 2a10 10 0 1 0 0 20A10 10 0 0 0 12 2z"/>
              <path d="M12 6v6l4 2"/>
            </svg>
            <span><a href="https://scholar.google.com/citations?user=LiA8b3YAAAAJ&hl=en" target="_blank">Google Scholar</a></span>
          </div>
          <div class="info-item">
            <svg class="info-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
              <rect x="2" y="2" width="20" height="20" rx="5"/>
              <path d="M16 8h-2a4 4 0 0 0-4 4v8M8 12h8"/>
            </svg>
            <span><a href="https://orcid.org/0000-0002-3279-2749" target="_blank">ORCID: 0000-0002-3279-2749</a></span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- RESEARCH -->
<section id="research">
  <div class="container">
    <div class="section-label">Research</div>
    <h2>Research Overview</h2>
    <p class="research-intro">My research spans the design and synthesis of polymer systems with programmable mechanical properties, the chemistry of mechanically interlocked molecules, and the fabrication of gold-based nanomaterials for chemical sensing applications.</p>
    <div class="research-areas" style="grid-template-columns:1fr;gap:1.25rem;">
      <div class="area-card">
        <span class="area-number">I</span>
        <h3>High Energy-Density Shape Memory Materials</h3>
        <p>Design and synthesis of novel, energy-dense shape memory actuator materials capable of reversibly transforming between multiple programmed states. <em>This work is ongoing. Stay tuned for publications!</em></p>
      </div>

      <div class="area-card">
        <span class="area-number">II</span>
        <h3>Mechanically Interlocked Materials</h3>
        <p>Synthesis and characterization of previously inaccessible molecular topologies — including doubly-threaded poly[3]rotaxane networks — and study of their unique mechanical and rheological properties.</p>
        <div style="margin-top:1.25rem;padding-top:1rem;border-top:1px solid var(--rule);">
          <p style="font-family:'Source Sans 3',sans-serif;font-size:11px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;color:var(--gold);margin-bottom:0.75rem;">Selected Publications</p>
          <div style="display:grid;grid-template-columns:44px 1fr;gap:0.75rem;align-items:start;">
            <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;font-weight:600;color:var(--text-muted);">2023</span>
            <div>
              <p style="font-size:15px;font-weight:600;color:var(--navy);font-style:italic;font-family:'Libre Baskerville',serif;margin-bottom:0.2rem;">Doubly threaded slide-ring polycatenane networks</p>
              <p style="font-size:14px;color:var(--text-muted);margin-bottom:0.2rem;">L. F. Hart, W. R. Lenart, J. E. Hertzog, J. Oh, <strong style="color:var(--text);">W. R. Turner</strong>, J. M. Dennis, and S. J. Rowan</p>
              <p style="font-size:14px;color:var(--text-mid);"><em>Journal of the American Chemical Society</em>, 145 (22), 12315–12323. <a href="https://pubs.acs.org/doi/full/10.1021/jacs.3c02837" target="_blank" style="color:var(--navy);">DOI: 10.1021/jacs.3c02837</a></p>
            </div>
          </div>
        </div>
      </div>

      <div class="area-card">
        <span class="area-number">III</span>
        <h3>Gold-Based Functional Nanomaterials</h3>
        <p>Synthesis, characterization, and application of gold-based nanoparticles for the surface-enhanced Raman scattering (SERS) sensing of water contaminants and volatile organics.</p>
        <div style="margin-top:1.25rem;padding-top:1rem;border-top:1px solid var(--rule);">
          <p style="font-family:'Source Sans 3',sans-serif;font-size:11px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;color:var(--gold);margin-bottom:0.75rem;">Selected Publications</p>
          <div style="display:flex;flex-direction:column;gap:0.9rem;">
            <div style="display:grid;grid-template-columns:44px 1fr;gap:0.75rem;align-items:start;">
              <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;font-weight:600;color:var(--text-muted);">2024</span>
              <div>
                <p style="font-size:15px;font-weight:600;color:var(--navy);font-style:italic;font-family:'Libre Baskerville',serif;margin-bottom:0.2rem;">Surface-enhanced Raman scattering gold nanoplatelets synthesized using extracts of the <em>Cercis Canadensis</em> flower</p>
                <p style="font-size:14px;color:var(--text-muted);margin-bottom:0.2rem;"><strong style="color:var(--text);">W. R. Turner</strong>†, D. Aligholizadeh†, L. Bechdel, K. Langford, M. Zhukovskyi, and M. S. Devadas</p>
                <p style="font-size:14px;color:var(--text-mid);"><em>Journal of Nanoparticle Research</em>, 26, 253. <a href="https://link.springer.com/article/10.1007/s11051-024-06170-5" target="_blank" style="color:var(--navy);">DOI: 10.1007/s11051-024-06170-5</a></p>
              </div>
            </div>
            <div style="display:grid;grid-template-columns:44px 1fr;gap:0.75rem;align-items:start;padding-top:0.9rem;border-top:1px solid var(--cream-dark);">
              <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;font-weight:600;color:var(--text-muted);">2019</span>
              <div>
                <p style="font-size:15px;font-weight:600;color:var(--navy);font-style:italic;font-family:'Libre Baskerville',serif;margin-bottom:0.2rem;">Signal detection limit of a portable Raman spectrometer for the SERS detection of gunshot residue</p>
                <p style="font-size:14px;color:var(--text-muted);margin-bottom:0.2rem;">E. Thayer, <strong style="color:var(--text);">W. Turner</strong>, S. Blama, M. S. Devadas, and E. M. Hondrogiannis</p>
                <p style="font-size:14px;color:var(--text-mid);"><em>MRS Communications</em>, 9 (3), 948–955. <a href="https://www.cambridge.org/core/journals/mrs-communications/article/signal-detection-limit-of-a-portable-raman-spectrometer-for-the-sers-detection-of-gunshot-residue/BB444992838F623EA141BDBAF6BFF435" target="_blank" style="color:var(--navy);">DOI: 10.1557/mrc.2019.100</a></p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="funding-note">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" style="flex-shrink:0;margin-top:2px;opacity:0.7">
        <circle cx="12" cy="12" r="10"/><path d="M12 8v4m0 4h.01"/>
      </svg>
      <p>Graduate research supported by the <strong>NSF Graduate Research Fellowship (NSF-GRFP)</strong> and the <strong>Stanford EDGE Fellowship</strong>.</p>
    </div>
  </div>
</section>

<!-- PUBLICATIONS -->
<section id="publications">
  <div class="container">
    <div class="section-label">Scholarship</div>
    <h2>Publications</h2>

    <div class="pub-filters">
      <button class="filter-btn active" onclick="filterPubs('all', this)">All</button>
      <button class="filter-btn" onclick="filterPubs('2024', this)">2024</button>
      <button class="filter-btn" onclick="filterPubs('2023', this)">2023</button>
      <button class="filter-btn" onclick="filterPubs('2019', this)">2019</button>
    </div>

    <div class="pub-list" id="pub-list">

      <div class="pub-item" data-year="2024">
        <div class="pub-year">2024</div>
        <div class="pub-content">
          <p class="pub-title">Boosting the oxygen evolution reaction performance of Ni–Fe electrodes by tailored conditioning</p>
          <p class="pub-authors">C. M. Gohlke, J. Gallenberger, <strong>W. R. Turner</strong>, N. Niederprüm, H. Ingendae, J. Kautz, J. P. Hofmann, and A. K. Mechler</p>
          <p class="pub-journal"><em>ChemElectroChem</em>, 2024, 11 (18), e202400318. <a href="https://chemistry-europe.onlinelibrary.wiley.com/doi/full/10.1002/celc.202400318" target="_blank" style="color:var(--navy);">DOI: 10.1002/celc.202400318</a></p>
        </div>
      </div>

      <div class="pub-item" data-year="2024">
        <div class="pub-year">2024</div>
        <div class="pub-content">
          <p class="pub-title">Surface-enhanced Raman scattering gold nanoplatelets synthesized using extracts of the <em>Cercis Canadensis</em> flower</p>
          <p class="pub-authors"><strong>W. R. Turner</strong>†, D. Aligholizadeh†, L. Bechdel, K. Langford, M. Zhukovskyi, and M. S. Devadas</p>
          <p class="pub-journal"><em>Journal of Nanoparticle Research</em>, 2024, 26, 253. <a href="https://link.springer.com/article/10.1007/s11051-024-06170-5" target="_blank" style="color:var(--navy);">DOI: 10.1007/s11051-024-06170-5</a></p>
        </div>
      </div>

      <div class="pub-item" data-year="2023">
        <div class="pub-year">2023</div>
        <div class="pub-content">
          <p class="pub-title">Doubly threaded slide-ring polycatenane networks</p>
          <p class="pub-authors">L. F. Hart, W. R. Lenart, J. E. Hertzog, J. Oh, <strong>W. R. Turner</strong>, J. M. Dennis, and S. J. Rowan</p>
          <p class="pub-journal"><em>Journal of the American Chemical Society</em>, 2023, 145 (22), 12315–12323. <a href="https://pubs.acs.org/doi/full/10.1021/jacs.3c02837" target="_blank" style="color:var(--navy);">DOI: 10.1021/jacs.3c02837</a></p>
        </div>
      </div>

      <div class="pub-item" data-year="2019">
        <div class="pub-year">2019</div>
        <div class="pub-content">
          <p class="pub-title">Signal detection limit of a portable Raman spectrometer for the SERS detection of gunshot residue</p>
          <p class="pub-authors">E. Thayer, <strong>W. Turner</strong>, S. Blama, M. S. Devadas, and E. M. Hondrogiannis</p>
          <p class="pub-journal"><em>MRS Communications</em>, 2019, 9 (3), 948–955. <a href="https://www.cambridge.org/core/journals/mrs-communications/article/signal-detection-limit-of-a-portable-raman-spectrometer-for-the-sers-detection-of-gunshot-residue/BB444992838F623EA141BDBAF6BFF435" target="_blank" style="color:var(--navy);">DOI: 10.1557/mrc.2019.100</a></p>
        </div>
      </div>

    </div>

    <p style="margin-top:1.5rem;font-size:15px;color:var(--text-muted);">
      For a complete list, see my <a href="https://scholar.google.com/citations?user=LiA8b3YAAAAJ&hl=en" target="_blank" style="color:var(--navy);">Google Scholar profile</a> or <a href="cv.pdf" style="color:var(--navy);">full CV</a>.
    </p>
  </div>
</section>

<!-- CV -->
<section id="cv">
  <div class="container">
    <div class="section-label">Curriculum Vitae</div>
    <h2>Academic Record</h2>
    <div class="cv-grid">

      <div>
        <div class="cv-section">
          <h3>Education</h3>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Ph.D., Chemical Engineering</span>
              <span class="cv-entry-date">2024–2029</span>
            </div>
            <div class="cv-entry-sub">Stanford University, Stanford, CA</div>
            <div class="cv-entry-detail">Advisor: Prof. Zhenan Bao · NSF-GRFP Graduate Fellow</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">B.S. (Hons.) Molecular Engineering &amp; B.A. Chemistry</span>
              <span class="cv-entry-date">2019–2023</span>
            </div>
            <div class="cv-entry-sub">University of Chicago, Chicago, IL</div>
            <div class="cv-entry-detail">Advisor: Prof. Stuart Rowan · GPA: 3.93 · Thesis: "Doubly-Threaded Poly[3]Rotaxane Slide-Ring Networks"</div>
          </div>
        </div>

        <div class="cv-section" style="margin-top:2rem;">
          <h3>Professional Experience</h3>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Launchpad Engineer</span>
              <span class="cv-entry-date">2023–2024</span>
            </div>
            <div class="cv-entry-sub">Space Exploration Technologies (SpaceX)</div>
            <div class="cv-entry-detail">Launchpad cryogenic systems design · Weld engineering · Launch operations</div>
          </div>
        </div>

        <div class="cv-section" style="margin-top:2rem;">
          <h3>Awards &amp; Honors</h3>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">NSF Graduate Research Fellowship</span>
              <span class="cv-entry-date">2024–2027</span>
            </div>
            <div class="cv-entry-sub">National Science Foundation</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Stanford EDGE Fellowship</span>
              <span class="cv-entry-date">2024</span>
            </div>
            <div class="cv-entry-sub">Stanford University</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Rhodes Scholarship — National Finalist</span>
              <span class="cv-entry-date">2023</span>
            </div>
            <div class="cv-entry-sub">Rhodes Trust</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Barry M. Goldwater Scholarship</span>
              <span class="cv-entry-date">2022</span>
            </div>
            <div class="cv-entry-sub">Barry Goldwater Scholarship &amp; Excellence in Education Foundation</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Astronaut Scholarship</span>
              <span class="cv-entry-date">2022</span>
            </div>
            <div class="cv-entry-sub">Astronaut Scholarship Foundation</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">NSF IRES / DAAD-RISE Summer Research Scholarship</span>
              <span class="cv-entry-date">2021</span>
            </div>
            <div class="cv-entry-sub">National Science Foundation / DAAD</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">ACS National Undergraduate Award in Physical Chemistry</span>
              <span class="cv-entry-date">2021</span>
            </div>
            <div class="cv-entry-sub">American Chemical Society</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Odyssey Scholarship — Trautschold Family Endowed Scholar</span>
              <span class="cv-entry-date">2019–2023</span>
            </div>
            <div class="cv-entry-sub">University of Chicago</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Phi Beta Kappa</span>
              <span class="cv-entry-date">2023</span>
            </div>
            <div class="cv-entry-sub">University of Chicago Chapter</div>
          </div>
        </div>
      </div>

      <div>
        <div class="cv-section">
          <h3>Service &amp; Leadership</h3>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Peer Reviewer</span>
              <span class="cv-entry-date">2022–present</span>
            </div>
            <div class="cv-entry-sub"><em>Advanced Functional Materials · Journal of the American Chemical Society</em></div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Dean's Graduate Student Advisory Committee</span>
              <span class="cv-entry-date">2024–present</span>
            </div>
            <div class="cv-entry-sub">Stanford University · Board Member</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">ChemE Graduate Student Advisory Council</span>
              <span class="cv-entry-date">2024–present</span>
            </div>
            <div class="cv-entry-sub">Stanford University · Colloquium Chair</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Summer First FLI &amp; URM Program</span>
              <span class="cv-entry-date">2024–present</span>
            </div>
            <div class="cv-entry-sub">Stanford University · Student Mentor</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Odyssey Scholarship Community Fellowship</span>
              <span class="cv-entry-date">2019–2023</span>
            </div>
            <div class="cv-entry-sub">University of Chicago · Inaugural Fellow</div>
          </div>
          <div class="cv-entry">
            <div class="cv-entry-head">
              <span class="cv-entry-title">Pritzker School of Molecular Engineering DEI Board</span>
              <span class="cv-entry-date">2021–2023</span>
            </div>
            <div class="cv-entry-sub">University of Chicago · Board Member</div>
          </div>
        </div>
      </div>

    </div>

    <div class="cv-download">
      <p>Full curriculum vitae including all publications, presentations, and service activities.</p>
      <a href="cv.pdf" class="btn btn-gold">Download Full CV (PDF)</a>
    </div>

  </div>
</section>

<!-- TEACHING -->
<section id="teaching">
  <div class="container">
    <div class="section-label">Teaching</div>
    <h2>Teaching &amp; Invited Talks</h2>
    <p class="teaching-intro">I am committed to making science accessible and engaging at every level — from designing an original biology curriculum for middle schoolers to supporting graduate-level instruction in nanofabrication and medical devices.</p>

    <div class="teaching-grid">
      <div class="course-card">
        <div class="course-code">Stanford · 2026</div>
        <div class="course-name">Micro and Nano Processing Technologies for Medical Electronics</div>
        <div class="course-meta">Teaching Assistant · Instructor: Prof. Zhenan Bao</div>
        <p class="course-desc">Assisted with course materials preparation, grading, and discussion facilitation covering fundamentals of patterning and processing of electrical devices, with special emphasis on medical devices, wearables, and human–computer interaction.</p>
      </div>
      <div class="course-card">
        <div class="course-code">Khan Lab School · 2025</div>
        <div class="course-name">Eighth Grade Biology</div>
        <div class="course-meta">Instructor · Khan Laboratory School</div>
        <p class="course-desc">Worked with Khan Academy founder Salman Khan to design and teach a one-semester biology crash course for eighth graders matriculating into Advanced Placement biology the following year. Sole instructor of record alongside Mr. Khan.</p>
      </div>
    </div>

    <div class="mentoring-block">
      <h3>Invited Talks &amp; Presentations</h3>
      <div style="display:flex;flex-direction:column;gap:0.75rem;">
        <div style="display:grid;grid-template-columns:90px 1fr;gap:1rem;font-size:15px;">
          <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;color:var(--text-muted);padding-top:2px;">Feb. 2026</span>
          <span><em>"3D Printing Methods for Medical Devices"</em> — Guest Lecturer, Micro and Nano Processing Technologies for Medical Electronics, Stanford University</span>
        </div>
        <div style="display:grid;grid-template-columns:90px 1fr;gap:1rem;font-size:15px;">
          <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;color:var(--text-muted);padding-top:2px;">Jan. 2025</span>
          <span><em>"Young Minds, Big Visions: Astronaut Scholars and the Dynamic Technologies Shaping the World"</em> — Space Congress National Convention, Orlando, FL</span>
        </div>
        <div style="display:grid;grid-template-columns:90px 1fr;gap:1rem;font-size:15px;">
          <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;color:var(--text-muted);padding-top:2px;">May 2024</span>
          <span><em>"ASF Scholars at Work: Panel Discussion with Alumni Working in Space"</em> — Astronaut Hall of Fame Induction Ceremony, Kennedy Space Center, FL</span>
        </div>
        <div style="display:grid;grid-template-columns:90px 1fr;gap:1rem;font-size:15px;">
          <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;color:var(--text-muted);padding-top:2px;">May 2023</span>
          <span><em>"Directed Synthesis of Slide-Ring Polycatenane Networks"</em> — UChicago Undergraduate Research Symposium · <strong>Awarded Gold</strong></span>
        </div>
        <div style="display:grid;grid-template-columns:90px 1fr;gap:1rem;font-size:15px;">
          <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;color:var(--text-muted);padding-top:2px;">Mar. 2022</span>
          <span><em>"Methodology &amp; Evaluation of the Oxygen Evolution Reaction in a 3D-Printed Electrochemical Flow Cell"</em> — ACS National Conference, San Diego, CA</span>
        </div>
        <div style="display:grid;grid-template-columns:90px 1fr;gap:1rem;font-size:15px;">
          <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;color:var(--text-muted);padding-top:2px;">May 2021</span>
          <span><em>"Utilizing Polymer Soft Confinement for Novel De-Icing Surfaces"</em> — UChicago Undergraduate Research Symposium · <strong>Awarded Gold</strong></span>
        </div>
        <div style="display:grid;grid-template-columns:90px 1fr;gap:1rem;font-size:15px;">
          <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;color:var(--text-muted);padding-top:2px;">Apr. 2020</span>
          <span><em>"Undulated Gold Nanoplates — A Green Approach"</em> — American Vacuum Society National Poster Competition (Virtual)</span>
        </div>
        <div style="display:grid;grid-template-columns:90px 1fr;gap:1rem;font-size:15px;">
          <span style="font-family:'Source Sans 3',sans-serif;font-size:13px;color:var(--text-muted);padding-top:2px;">2019</span>
          <span><em>"Green Synthesis and Characterization of Serrated Gold Nanoplates"</em> — UMBC Undergraduate Research Symposium for the Chemical and Biological Sciences, Baltimore, MD · <strong>Awarded First Overall</strong></span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="container">
    <div class="section-label">Get in Touch</div>
    <h2>Contact</h2>
    <div class="contact-grid">
      <div class="contact-info">
        <h3>Office &amp; Correspondence</h3>
        <div class="contact-row">
          <span class="contact-label">Email</span>
          <span class="contact-val"><a href="mailto:wrturner@stanford.edu">wrturner@stanford.edu</a></span>
        </div>
        <div class="contact-row">
          <span class="contact-label">Office</span>
          <span class="contact-val">Shriram Center for Bioengineering &amp; Chemical Engineering<br>Department of Chemical Engineering<br>Stanford University, Stanford, CA</span>
        </div>
        <div class="contact-row">
          <span class="contact-label">Scholar</span>
          <span class="contact-val"><a href="https://scholar.google.com/citations?user=LiA8b3YAAAAJ&hl=en" target="_blank">Google Scholar Profile</a></span>
        </div>
        <div class="contact-row">
          <span class="contact-label">ORCID</span>
          <span class="contact-val"><a href="https://orcid.org/0000-0002-3279-2749" target="_blank">0000-0002-3279-2749</a></span>
        </div>
        <p style="margin-top:1.5rem;font-size:15px;color:var(--text-muted);font-style:italic;">I welcome inquiries from prospective collaborators and colleagues.</p>
      </div>
      <div class="contact-form">
        <h3>Send a Message</h3>
        <div class="form-field">
          <label>Name</label>
          <input type="text" placeholder="Your full name">
        </div>
        <div class="form-field">
          <label>Email</label>
          <input type="email" placeholder="your@email.com">
        </div>
        <div class="form-field">
          <label>Subject</label>
          <input type="text" placeholder="e.g. Collaboration inquiry, Prospective student">
        </div>
        <div class="form-field">
          <label>Message</label>
          <textarea placeholder="Your message..."></textarea>
        </div>
        <button class="form-submit">Send Message</button>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2026 Wilson R. Turner · Chemical Engineering · Stanford University · Last updated March 2026</p>
  <p style="margin-top:0.4rem;font-size:12px;opacity:0.6;">Built with HTML/CSS · Hoste
