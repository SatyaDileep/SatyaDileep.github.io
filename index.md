---
layout: default
title: Home
---

<style>
.hero {
  text-align: center;
  padding: 2rem 0 1rem;
}
.hero-avatar {
  width: 120px; height: 120px; margin: 0 auto 1.5rem;
  position: relative;
}
.hero-avatar::before {
  content: ''; position: absolute; inset: -10px; border-radius: 50%;
  background: radial-gradient(circle, var(--primary-dim) 0%, transparent 70%);
  animation: pulseGlow 4s ease-in-out infinite;
}
@keyframes pulseGlow { 0%, 50%, 100% { transform: scale(1); opacity: 0.5; } 70% { transform: scale(1.1); opacity: 1; } }
.avatar { width: 120px; height: 120px; border-radius: 50%; object-fit: cover; position: relative; z-index: 1; border: 2px solid var(--border); }
.hero h1 { font-size: clamp(1.5rem, 3.5vw, 2rem); letter-spacing: -0.5px; line-height: 1.25; margin: 0 0 0.35rem; }
.hero .name { color: var(--primary); font-weight: 800; }
.hero .subtitle { font-size: 1rem; color: var(--muted); margin: 0 0 0.75rem; font-weight: 500; }
.hero .tagline { color: var(--muted); margin: 0 auto 1.25rem; font-size: 0.92rem; line-height: 1.6; max-width: 520px; }
.hero-btns { display: flex; gap: 0.75rem; justify-content: center; flex-wrap: wrap; }

.quick-links { display: grid; grid-template-columns: repeat(2, 1fr); gap: 0.75rem; }
.quick-link-card {
  display: flex; flex-direction: column; align-items: center; gap: 0.4rem;
  padding: 1.25rem 0.75rem;
  background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius);
  text-decoration: none; text-align: center; transition: var(--transition);
}
.quick-link-card:hover { border-color: var(--primary); transform: translateY(-3px); box-shadow: var(--shadow-lg); }
.quick-link-card .qli { font-size: 1.6rem; line-height: 1; }
.quick-link-card h3 { margin: 0; font-size: 0.85rem; color: var(--text); font-weight: 600; }
.quick-link-card p { margin: 0; font-size: 0.7rem; color: var(--muted); }

@media (max-width: 480px) {
  .hero { padding: 1.5rem 0 0.5rem; }
  .hero-avatar { width: 100px; height: 100px; margin-bottom: 1rem; }
  .avatar { width: 100px; height: 100px; }
  .quick-links { gap: 0.5rem; }
  .quick-link-card { padding: 1rem 0.5rem; }
}
</style>

<section class="hero">
  <div class="hero-avatar">
    <img src="{{ '/assets/mypic.jfif' | relative_url }}" alt="Satya Dileep" class="avatar" loading="lazy">
  </div>
  <h1><span class="name">Satya Dileep Kumar Thotakura</span></h1>
  <p class="subtitle">AI Product Manager at Pegasystems</p>
  <p class="tagline">Blending Generative AI with LowCode to transform user experiences. <strong><span id="exp-years"></span> years</strong> in enterprise software, with the last 2+ years focused on product management.</p>
  <div class="hero-btns">
    <a href="{{ '/about' | relative_url }}" class="btn">About Me</a>
    <a href="{{ '/contact' | relative_url }}" class="btn secondary">Get in Touch</a>
  </div>
</section>

<section>
  <h2 class="section-title">Explore</h2>
  <div class="quick-links">
    <a href="{{ '/about' | relative_url }}" class="quick-link-card">
      <span class="qli">&#128218;</span>
      <h3>Experience</h3>
      <p>13+ year journey</p>
    </a>
    <a href="{{ '/skills' | relative_url }}" class="quick-link-card">
      <span class="qli">&#128640;</span>
      <h3>Skills</h3>
      <p>Certifications & tools</p>
    </a>
    <a href="{{ '/micro-apps/' | relative_url }}" class="quick-link-card">
      <span class="qli">&#128736;</span>
      <h3>Work</h3>
      <p>Micro-apps & prototypes</p>
    </a>
    <a href="{{ '/blog' | relative_url }}" class="quick-link-card">
      <span class="qli">&#9997;</span>
      <h3>Blog</h3>
      <p>Thoughts on AI & PM</p>
    </a>
  </div>
</section>
