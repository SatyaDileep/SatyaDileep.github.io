---
layout: default
title: Home
---

<style>
.hero { padding: 3rem 0; }
.hero h1 { margin: 0 0 0.5rem 0; font-size: 2rem; }
.primary { color: #1a73e8; font-weight: 700; }
.subtitle { font-size: 1.1rem; color: #555; margin-bottom: 1rem; }

a.btn {
  display: inline-block;
  background: #1a73e8;
  color: #fff;
  padding: 0.6rem 1.2rem;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 600;
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
}
a.btn.secondary {
  background: #f1f3f4;
  color: #333;
}

.hero-flex { display: flex; gap: 2rem; align-items: center; flex-wrap: wrap; }
.hero-text { flex: 1; min-width: 280px; }
.hero-avatar { flex: 0 0 120px; }
.avatar { width: 120px; height: 120px; border-radius: 50%; object-fit: cover; }

.quick-links { margin-top: 2rem; padding-top: 2rem; border-top: 1px solid #eee; }
.quick-links h3 { margin-top: 0; }
</style>

<section class="hero">
  <div class="hero-flex">
    <div class="hero-text">
      <h1>Hi, I'm <span class="primary">Satya Dileep Kumar Thotakura</span></h1>
      <p class="subtitle">AI Product Manager — GenAI & agentic automation</p>
      <p>I build practical micro-apps and prototypes that ship. 13+ years in industry, 2+ years in PM focused on GenAI and applied automation.</p>
      <div>
        <a href="{{ '/micro-apps' | relative_url }}" class="btn">View My Work →</a>
        <a href="{{ '/blog' | relative_url }}" class="btn secondary">Read Blog</a>
      </div>
    </div>
    <div class="hero-avatar">
      <img src="{{ '/assets/dileep11.jpg' | relative_url }}" alt="Satya Dileep" class="avatar" loading="lazy">
    </div>
  </div>

  <div class="quick-links">
    <h3>What I'm Building</h3>
    <ul>
      <li><strong>PM Canvas Agent</strong> — transforms idea mind-dumps into canvases and lightweight mocks</li>
      <li><strong>VC Scout</strong> — vector matching, citations, and outreach tooling</li>
      <li><strong>Micro-apps</strong> — browser-first productivity tools (zero-setup)</li>
    </ul>
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
