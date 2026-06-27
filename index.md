---
layout: default
title: Home
---

<style>
.hero { padding: 1.5rem 0; }
.hero h1 { margin: 0 0 0.5rem 0; font-size: 1.8rem; }
.primary { color: var(--primary); font-weight: 700; }
.subtitle { font-size: 1rem; color: var(--muted); margin-bottom: 0.75rem; }
.hero p { color: var(--muted); margin: 0 0 0.75rem 0; font-size: 0.95rem; }

a.btn {
  display: inline-block;
  background: var(--primary);
  color: #fff;
  padding: 0.5rem 1rem;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 600;
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
}
a.btn:hover { opacity: 0.9; }
a.btn.secondary {
  background: var(--border);
  color: var(--text);
}

.hero-flex { display: flex; gap: 1.5rem; align-items: center; flex-wrap: wrap; }
.hero-text { flex: 1; min-width: 200px; }
.hero-avatar { flex: 0 0 80px; }
.avatar { width: 80px; height: 80px; border-radius: 50%; object-fit: cover; }

.section-title { font-size: 1rem; margin: 1.5rem 0 0.75rem 0; }
.quick-links { display: grid; grid-template-columns: repeat(2, 1fr); gap: 0.75rem; margin-top: 1rem; }
.quick-link-card {
  padding: 0.85rem;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 10px;
  text-decoration: none;
  text-align: center;
}
.quick-link-card:hover { border-color: var(--primary); }
.quick-link-card h3 { margin: 0 0 0.2rem 0; font-size: 0.9rem; color: var(--text); }
.quick-link-card p { margin: 0; font-size: 0.75rem; color: var(--muted); }

@media (max-width: 480px) {
  .hero { padding: 1rem 0; }
  .hero h1 { font-size: 1.5rem; }
  .hero-flex { flex-direction: column; text-align: center; gap: 1rem; }
  .hero-avatar { flex: 0 0 70px; }
  .avatar { width: 70px; height: 70px; }
  .quick-links { grid-template-columns: 1fr 1fr; gap: 0.5rem; }
}
</style>

<section class="hero">
  <div class="hero-flex">
    <div class="hero-text">
      <h1>Hi, I'm <span class="primary">Satya Dileep Kumar Thotakura</span></h1>
      <p class="subtitle">AI Product Manager at Pegasystems</p>
      <p>I blend Generative AI with LowCode to transform user experiences. <strong><span id="exp-years"></span> years</strong> in enterprise software, 2+ years shipping PM-led AI initiatives.</p>
      <div>
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
      <h3>Experience</h3>
      <p>My journey</p>
    </a>
    <a href="{{ '/skills' | relative_url }}" class="quick-link-card">
      <h3>Skills</h3>
      <p>Certifications</p>
    </a>
    <a href="{{ '/micro-apps' | relative_url }}" class="quick-link-card">
      <h3>Work</h3>
      <p>Micro-apps</p>
    </a>
    <a href="{{ '/blog' | relative_url }}" class="quick-link-card">
      <h3>Blog</h3>
      <p>Thoughts</p>
    </a>
  </div>
</section>