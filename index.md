---
layout: default
title: Home
---

<style>
/* Minimal, focused styles for a cleaner, professional landing hero + cards */
.hero.hero-with-avatar {
  display: flex;
  gap: 2rem;
  align-items: center;
  justify-content: space-between;
  padding: 3.2rem 0;
}
.hero-text { flex: 1; min-width: 0; }
.hero-text h1 { margin: 0 0 0.5rem 0; font-size: 2rem; line-height: 1.1; }
.primary { color: #1a73e8; font-weight: 700; }

.hero-avatar { display:flex; align-items:center; justify-content:center; }
.avatar {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid rgba(0,0,0,0.06);
  box-shadow: 0 8px 20px rgba(15, 23, 42, 0.06);
}

a.btn {
  display: inline-block;
  margin-top: 0.6rem;
  background: #1a73e8;
  color: #fff;
  padding: 0.55rem 1rem;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 600;
  box-shadow: 0 6px 18px rgba(26,115,232,0.16);
}

.grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px,1fr)); gap: 1rem; margin-top: 2rem; }
.card { background: #fff; padding: 1.25rem; border-radius: 8px; border: 1px solid rgba(0,0,0,0.03); box-shadow: 0 8px 20px rgba(12,13,14,0.04); }
.card h3 { margin-top: 0; font-size: 1.05rem; font-weight:700; color:#111; }

/* Responsive */
@media (max-width: 720px) {
  .hero.hero-with-avatar { flex-direction: column; text-align: center; }
  .hero-avatar { margin-top: 1rem; }
}
</style>

<section class="hero hero-with-avatar">
  <div class="hero-text">
    <h1>Hi, I’m <span class="primary">Satya Dileep Kumar Thotakura</span></h1>
    <p class="subtitle">AI Product Manager — GenAI & agentic automation. I build practical micro‑apps and prototypes that ship.</p>
    <p><a href="{{ '/micro-apps' | relative_url }}" class="btn">Explore my micro‑apps →</a></p>
  </div>
  <div class="hero-avatar">
    <img
      src="{{ '/assets/dileep11.jpg' | relative_url }}"
      alt="Satya Dileep Kumar Thotakura"
      class="avatar"
      loading="lazy" />
  </div>
</section>

<section id="about" class="grid">
  <div class="card">
    <h3>About</h3>
    <p>I’m an AI Product Manager who turns ideas into production-ready software using agentic patterns, micro‑apps, and rapid feedback loops.</p>
    <p>13+ years in industry, 2+ years in product management, focused on GenAI and applied automation.</p>
  </div>

  <div class="card">
    <h3>What I’m building</h3>
    <ul>
      <li>PM Canvas Agent — transforms idea mind‑dumps into canvases and lightweight mocks.</li>
      <li>VC Scout prototype — vector matching, citations, and outreach tooling.</li>
      <li>Browser‑first micro‑apps — zero‑setup HTML/CSS/JS productivity tools.</li>
    </ul>
  </div>

  <div class="card">
    <h3>Stack & strengths</h3>
    <ul>
      <li>Google Cloud, serverless, and API orchestration.</li>
      <li>Pega integration and workflow automation.</li>
      <li>Rapid prototyping in Python & JS with reusable UI snippets.</li>
    </ul>
  </div>
</section>
