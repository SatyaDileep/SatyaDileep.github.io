---
layout: default
title: Home
---

<style>
.hero-flex { display: flex; gap: 2rem; align-items: center; flex-wrap: wrap; justify-content: space-between; }
.hero-text { flex: 1; min-width: 240px; }
.hero h1 { font-size: clamp(1.6rem, 4vw, 2.2rem); letter-spacing: -0.5px; line-height: 1.2; margin: 0 0 0.5rem; }
.hero .primary { color: var(--primary); font-weight: 800; }
.hero .subtitle { font-size: 1rem; color: var(--muted); margin-bottom: 0.75rem; font-weight: 500; }
.hero p { color: var(--muted); margin: 0 0 1rem; font-size: 0.95rem; line-height: 1.6; }
.hero-avatar { flex: 0 0 90px; position: relative; }
.hero-avatar::before {
  content: ''; position: absolute; inset: -6px; border-radius: 50%;
  background: radial-gradient(circle, var(--primary-dim) 0%, transparent 70%);
  animation: pulseGlow 3s ease-in-out infinite;
}
@keyframes pulseGlow { 0%, 100% { transform: scale(1); opacity: 0.6; } 50% { transform: scale(1.08); opacity: 1; } }
.avatar { width: 90px; height: 90px; border-radius: 50%; object-fit: cover; position: relative; z-index: 1; border: 2px solid var(--border); }
.status-dot { display: inline-block; width: 8px; height: 8px; border-radius: 50%; background: #22c55e; margin-right: 6px; vertical-align: middle; }
.status-text { display: inline-flex; align-items: center; gap: 6px; font-size: 0.8rem; color: var(--muted); margin-bottom: 1rem; }
.quick-links { display: grid; grid-template-columns: repeat(2, 1fr); gap: 0.75rem; margin-top: 0.5rem; }
.quick-link-card {
  display: flex; align-items: center; gap: 0.75rem; padding: 0.85rem 1rem;
  background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius-sm);
  text-decoration: none; transition: var(--transition);
}
.quick-link-card:hover { border-color: var(--primary); transform: translateY(-2px); box-shadow: var(--shadow); }
.quick-link-card .qli { font-size: 1.2rem; flex-shrink: 0; }
.quick-link-card .qlb { display: flex; flex-direction: column; }
.quick-link-card h3 { margin: 0; font-size: 0.85rem; color: var(--text); font-weight: 600; }
.quick-link-card p { margin: 0; font-size: 0.7rem; color: var(--muted); }
@media (max-width: 480px) {
  .hero-flex { flex-direction: column; text-align: center; gap: 1.25rem; }
  .hero-avatar { flex: 0 0 80px; }
  .avatar { width: 80px; height: 80px; }
  .quick-links { grid-template-columns: 1fr 1fr; gap: 0.5rem; }
  .quick-link-card { flex-direction: column; text-align: center; padding: 0.75rem; }
  .quick-link-card .qlb { align-items: center; }
}
</style>

<section class="hero">
  <div class="hero-flex">
    <div class="hero-text">
      <div class="status-text"><span class="status-dot"></span> Currently at Pegasystems</div>
      <h1>Hi, I'm <span class="primary">Satya Dileep Kumar Thotakura</span></h1>
      <p class="subtitle">AI Product Manager</p>
      <p>I blend Generative AI with LowCode to transform user experiences. <strong><span id="exp-years"></span> years</strong> in enterprise software, 2+ years shipping PM-led AI initiatives.</p>
      <div style="margin-top:1.25rem">
        <a href="{{ '/about' | relative_url }}" class="btn">About Me</a>
        <a href="{{ '/contact' | relative_url }}" class="btn secondary">Get in Touch</a>
      </div>
    </div>
    <div class="hero-avatar">
      <img src="{{ '/assets/mypic.jfif' | relative_url }}" alt="Satya Dileep" class="avatar" loading="lazy">
    </div>
  </div>
</section>

<section>
  <h2 class="section-title">Explore</h2>
  <div class="quick-links">
    <a href="{{ '/about' | relative_url }}" class="quick-link-card">
      <span class="qli">&#128218;</span>
      <div class="qlb">
        <h3>Experience</h3>
        <p>13+ year journey</p>
      </div>
    </a>
    <a href="{{ '/skills' | relative_url }}" class="quick-link-card">
      <span class="qli">&#128640;</span>
      <div class="qlb">
        <h3>Skills</h3>
        <p>Certifications & tools</p>
      </div>
    </a>
    <a href="{{ '/micro-apps' | relative_url }}" class="quick-link-card">
      <span class="qli">&#128736;</span>
      <div class="qlb">
        <h3>Work</h3>
        <p>Micro-apps & prototypes</p>
      </div>
    </a>
    <a href="{{ '/blog' | relative_url }}" class="quick-link-card">
      <span class="qli">&#9997;</span>
      <div class="qlb">
        <h3>Blog</h3>
        <p>Thoughts on AI & PM</p>
      </div>
    </a>
  </div>
</section>
