---
layout: default
title: Home
---

<style>
.hero-wrap {
  display: flex; gap: 2.5rem; align-items: center;
  padding: 0.5rem 0;
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
.hero-text { flex: 1; min-width: 240px; }
.hero-text h1 { font-size: clamp(1.4rem, 3vw, 1.8rem); letter-spacing: -0.5px; line-height: 1.2; margin: 0 0 0.25rem; }
.hero-text .name { color: var(--primary); font-weight: 800; }
.hero-text .subtitle { font-size: 0.95rem; color: var(--muted); margin: 0 0 0.6rem; font-weight: 500; }
.hero-text .tagline { color: var(--muted); margin: 0 0 1rem; font-size: 0.9rem; line-height: 1.6; }
.hero-btns { display: flex; gap: 0.6rem; flex-wrap: wrap; }

.grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem; }
.card-link {
  display: flex; flex-direction: column; align-items: center; gap: 0.35rem;
  padding: 1.15rem 0.75rem;
  background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius);
  text-decoration: none; text-align: center; transition: var(--transition);
}
.card-link:hover { border-color: var(--primary); transform: translateY(-3px); box-shadow: var(--shadow-lg); }
.card-link .ico { font-size: 1.5rem; line-height: 1; }
.card-link h3 { margin: 0; font-size: 0.85rem; color: var(--text); font-weight: 600; }
.card-link p { margin: 0; font-size: 0.7rem; color: var(--muted); }
.hero-wrap + section .section-title { margin-top: 1.5rem; }

@media (max-width: 640px) {
  .hero-wrap { flex-direction: column; text-align: center; gap: 1.5rem; min-height: 0; }
  .hero-avatar { flex: 0 0 130px; }
  .avatar { width: 130px; height: 130px; }
  .hero-btns { justify-content: center; }
}
</style>

<section class="hero-wrap">
  <div class="hero-avatar">
    <img src="{{ '/assets/mypic.jfif' | relative_url }}" alt="Satya Dileep" class="avatar" loading="lazy">
  </div>
  <div class="hero-text">
    <h1><span class="name">Satya Dileep Kumar Thotakura</span></h1>
    <p class="subtitle">AI Product Manager at Pegasystems</p>
    <p class="tagline">Blending Generative AI with LowCode to transform user experiences. <strong><span id="exp-years"></span> years</strong> in enterprise software, with the last 2+ years focused on product management.</p>
    <div class="hero-btns">
      <a href="{{ '/about' | relative_url }}" class="btn">About Me</a>
      <a href="{{ '/contact' | relative_url }}" class="btn secondary">Get in Touch</a>
    </div>
  </div>
</section>

<section>
  <h2 class="section-title">Explore</h2>
  <div class="grid-2">
    <a href="{{ '/about' | relative_url }}" class="card-link">
      <span class="ico">&#128218;</span>
      <h3>Experience</h3>
      <p>13+ year journey</p>
    </a>
    <a href="{{ '/skills' | relative_url }}" class="card-link">
      <span class="ico">&#128640;</span>
      <h3>Skills</h3>
      <p>Certifications & tools</p>
    </a>
    <a href="{{ '/micro-apps/' | relative_url }}" class="card-link">
      <span class="ico">&#128736;</span>
      <h3>Work</h3>
      <p>Micro-apps & prototypes</p>
    </a>
    <a href="{{ '/blog' | relative_url }}" class="card-link">
      <span class="ico">&#9997;</span>
      <h3>Blog</h3>
      <p>Thoughts on AI & PM</p>
    </a>
  </div>
</section>
