---
layout: default
title: Home
---

<style>
.hero { padding: 2rem 0; }
.hero h1 { margin: 0 0 0.5rem 0; font-size: 2.2rem; }
.primary { color: var(--primary); font-weight: 700; }
.subtitle { font-size: 1.15rem; color: var(--muted); margin-bottom: 1rem; }
.hero p { color: var(--muted); margin: 0 0 1rem 0; }

a.btn {
  display: inline-block;
  background: var(--primary);
  color: #fff;
  padding: 0.6rem 1.2rem;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 600;
  margin-right: 0.5rem;
}
a.btn:hover { opacity: 0.9; }
a.btn.secondary {
  background: var(--border);
  color: var(--text);
}

.hero-flex { display: flex; gap: 2rem; align-items: center; flex-wrap: wrap; }
.hero-text { flex: 1; min-width: 280px; }
.hero-avatar { flex: 0 0 100px; }
.avatar { width: 100px; height: 100px; border-radius: 50%; object-fit: cover; }

.section-title { font-size: 1.1rem; margin: 2rem 0 1rem 0; color: var(--text); }
.project-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 1rem; }
.project-card { 
  padding: 1.25rem; border-radius: 12px; border: 1px solid var(--border);
  background: var(--surface); 
}
.project-card h3 { margin: 0 0 0.5rem 0; font-size: 1rem; }
.project-card p { margin: 0; font-size: 0.9rem; color: var(--muted); }

.stack-list { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-top: 1rem; }
.stack-tag {
  background: var(--border);
  color: var(--text);
  padding: 4px 10px;
  border-radius: 6px;
  font-size: 0.8rem;
}
</style>

<section class="hero">
  <div class="hero-flex">
    <div class="hero-text">
      <h1>Hi, I'm <span class="primary">Satya Dileep Kumar Thotakura</span></h1>
      <p class="subtitle">AI Product Manager — GenAI & agentic automation</p>
      <p>I build practical micro-apps and prototypes that ship. 13+ years in industry, 2+ years in PM focused on GenAI and applied automation.</p>
      <div>
        <a href="{{ '/micro-apps' | relative_url }}" class="btn">View My Work</a>
        <a href="{{ '/blog' | relative_url }}" class="btn secondary">Read Blog</a>
      </div>
    </div>
    <div class="hero-avatar">
      <img src="{{ '/assets/dileep11.jpg' | relative_url }}" alt="Satya Dileep" class="avatar" loading="lazy">
    </div>
  </div>
</section>

<section>
  <h2 class="section-title">What I'm Building</h2>
  <div class="project-grid">
    <div class="project-card">
      <h3>PM Canvas Agent</h3>
      <p>Transforms idea mind-dumps into canvases and lightweight mocks</p>
    </div>
    <div class="project-card">
      <h3>VC Scout</h3>
      <p>Vector matching, citations, and outreach tooling for investors</p>
    </div>
    <div class="project-card">
      <h3>Micro-Apps</h3>
      <p>Browser-first productivity tools with zero setup</p>
    </div>
  </div>

  <h2 class="section-title">Stack</h2>
  <div class="stack-list">
    <span class="stack-tag">Google Cloud</span>
    <span class="stack-tag">Serverless</span>
    <span class="stack-tag">Pega</span>
    <span class="stack-tag">Python</span>
    <span class="stack-tag">JavaScript</span>
    <span class="stack-tag">GenAI</span>
    <span class="stack-tag">Agentic AI</span>
  </div>
</section>
