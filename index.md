---
layout: default
title: Home
---

<style>
.hero-wrap {
  display: flex; gap: 2rem; align-items: center;
  position: relative; z-index: 1;
}
.hero-avatar {
  flex: 0 0 160px; position: relative;
}
.hero-avatar::before {
  content: ''; position: absolute; inset: -10px; border-radius: 50%;
  background: radial-gradient(circle, var(--primary-dim) 0%, transparent 70%);
  animation: pulseGlow 4s ease-in-out infinite;
}
.avatar {
  width: 160px; height: 160px; border-radius: 50%; object-fit: cover;
  position: relative; z-index: 1; border: 2px solid var(--border);
}
.hero-text { flex: 1; min-width: 240px; position: relative; z-index: 1; }
.hero-text h1 { font-size: clamp(1.4rem, 3vw, 1.85rem); letter-spacing: -0.5px; line-height: 1.2; margin: 0 0 0.25rem; }
.hero-text .name { color: var(--primary); font-weight: 800; }
.hero-text .subtitle { font-size: 0.95rem; color: var(--muted); margin: 0 0 0.6rem; font-weight: 500; }
.hero-text .tagline { color: var(--muted); margin: 0 0 1rem; font-size: 0.9rem; line-height: 1.6; }
.hero-btns { display: flex; gap: 0.6rem; flex-wrap: wrap; }
.hero-glass + .bento-section { margin-top: 1.5rem; }

@media (max-width: 640px) {
  .hero-wrap { flex-direction: column; text-align: center; gap: 1.5rem; }
  .hero-avatar { flex: 0 0 130px; }
  .avatar { width: 130px; height: 130px; }
  .hero-btns { justify-content: center; }
}
</style>

<section class="hero-glass">
  <div class="hero-mesh"></div>
  <div class="hero-wrap">
    <div class="hero-avatar">
      <img src="{{ '/assets/mypic.jfif' | relative_url }}" alt="Satya Dileep" class="avatar" loading="lazy">
    </div>
    <div class="hero-text">
      <h1><span class="name">Satya Dileep Kumar Thotakura</span></h1>
      <p class="subtitle">AI Product Manager at Pegasystems — Pragmatic Builder</p>
      <p class="tagline">I turn complex AI capabilities into intuitive products. With <strong><span id="exp-years"></span> years</strong> in enterprise software, I build generative and agentic AI solutions trusted by Fortune 500 teams.</p>
      <div class="hero-btns">
        <a href="{{ '/product-portfolio/' | relative_url }}" class="btn">Explore Projects →</a>
        <a href="{{ '/linkedin/' | relative_url }}" class="btn secondary">Read My Insights →</a>
      </div>
    </div>
  </div>
</section>

<section class="bento-section">
  <h2 class="section-title">Featured Projects</h2>
  <p style="color:var(--muted);margin:-0.5rem 0 1rem;font-size:0.88rem">Production-ready applications demonstrating applied AI, open-source architecture, and intuitive design.</p>
  <div class="bento-grid">
    <article class="featured-card">
      <div class="featured-body">
        <h3>Content Crafting Wand for LinkedIn</h3>
        <p>Optimize LinkedIn content formatting with high-fidelity feed previews and durable styling tools. Local-first architecture ensuring API key privacy.</p>
        <div class="featured-meta"><span class="mini-tag">React</span><span class="mini-tag">Vite</span><span class="mini-tag">Tailwind</span><span class="mini-tag">Document Preview</span></div>
        <div class="featured-actions">
          <a class="primary" href="https://funny-belekoy-39b0f8.netlify.app/" target="_blank">View Project</a>
          <a class="ghost" href="https://github.com/SatyaDileep/Content-Crafting-Wand-For-LinkedIn" target="_blank">Source Code</a>
        </div>
      </div>
    </article>
    <article class="featured-card">
      <div class="featured-body">
        <h3>DocBridge — Universal Upload Layer</h3>
        <p>Citizen-centric upload solution that normalizes government portal requirements for photos and documents. Integrates DigiLocker with on-device processing to prevent rejections without exposing sensitive files.</p>
        <div class="featured-meta"><span class="mini-tag">Next.js</span><span class="mini-tag">DigiLocker</span><span class="mini-tag">Browser Processing</span><span class="mini-tag">Chrome Extension</span></div>
        <div class="featured-actions">
          <a class="primary" href="https://incredible-taffy-db08a6.netlify.app" target="_blank">View Project</a>
          <a class="ghost" href="https://github.com/SatyaDileep/Build-What-Moves-India-Hackathon" target="_blank">Source Code</a>
          <a class="ghost" href="https://github.com/SatyaDileep/Build-What-Moves-India-Hackathon" target="_blank">Coming Soon</a>
        </div>
      </div>
    </article>
    <article class="featured-card">
      <div class="featured-body">
        <h3>Pregnancy Blossom Journal</h3>
        <p>Private, offline-capable journaling platform for expectant families. Supports week-by-week milestones, photo memories, and AI-assisted reflections with on-device data retention.</p>
        <div class="featured-meta"><span class="mini-tag">PWA</span><span class="mini-tag">Offline-first</span><span class="mini-tag">AI Reflections</span><span class="mini-tag">Privacy-first</span></div>
        <div class="featured-actions">
          <a class="primary" href="https://pregnancy-blossom-journal.netlify.app/" target="_blank">View Project</a>
          <a class="ghost" href="https://github.com/SatyaDileep/pregnancy-journal" target="_blank">Source Code</a>
        </div>
      </div>
    </article>
  </div>
  <p style="text-align:center;margin:0.25rem 0 0"><a href="{{ '/product-portfolio/' | relative_url }}" style="font-weight:700;font-size:0.88rem">View portfolio →</a></p>
</section>

<section>
  <h2 class="section-title">Explore</h2>
  <div class="grid-2" style="display:grid;grid-template-columns:1fr 1fr;gap:0.75rem">
    <a href="{{ '/about' | relative_url }}" class="card-link" style="display:flex;flex-direction:column;align-items:center;gap:0.35rem;padding:1.15rem 0.75rem;background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);text-decoration:none;text-align:center">
      <span class="ico" style="font-size:1.5rem">📚</span>
      <h3 style="margin:0;font-size:0.85rem;color:var(--text)">Experience</h3>
      <p style="margin:0;font-size:0.7rem;color:var(--muted)">13+ year journey</p>
    </a>
    <a href="{{ '/skills' | relative_url }}" class="card-link" style="display:flex;flex-direction:column;align-items:center;gap:0.35rem;padding:1.15rem 0.75rem;background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);text-decoration:none;text-align:center">
      <span class="ico" style="font-size:1.5rem">🚀</span>
      <h3 style="margin:0;font-size:0.85rem;color:var(--text)">Skills</h3>
      <p style="margin:0;font-size:0.7rem;color:var(--muted)">Certifications & tools</p>
    </a>
     <a href="{{ '/product-portfolio/' | relative_url }}" class="card-link" style="display:flex;flex-direction:column;align-items:center;gap:0.35rem;padding:1.15rem 0.75rem;background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);text-decoration:none;text-align:center">
      <span class="ico" style="font-size:1.5rem">🛠️</span>
      <h3 style="margin:0;font-size:0.85rem;color:var(--text)">Work</h3>
      <p style="margin:0;font-size:0.7rem;color:var(--muted)">Product portfolio</p>
    </a>
    <a href="{{ '/linkedin/' | relative_url }}" class="card-link" style="display:flex;flex-direction:column;align-items:center;gap:0.35rem;padding:1.15rem 0.75rem;background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);text-decoration:none;text-align:center;background:linear-gradient(135deg, rgba(37,99,235,0.06), rgba(139,92,246,0.06))">
      <span class="ico" style="font-size:1.5rem">💼</span>
      <h3 style="margin:0;font-size:0.85rem;color:var(--text)">LinkedIn</h3>
      <p style="margin:0;font-size:0.7rem;color:var(--muted)">90 posts archive</p>
    </a>
  </div>
</section>
