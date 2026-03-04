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

.section-title { font-size: 1.1rem; margin: 2rem 0 1rem 0; }
.quick-links { display: flex; gap: 1rem; flex-wrap: wrap; margin-top: 1.5rem; }
.quick-link-card {
  flex: 1;
  min-width: 140px;
  padding: 1rem;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 10px;
  text-decoration: none;
  text-align: center;
}
.quick-link-card:hover { border-color: var(--primary); }
.quick-link-card h3 { margin: 0 0 0.25rem 0; font-size: 0.95rem; color: var(--text); }
.quick-link-card p { margin: 0; font-size: 0.8rem; color: var(--muted); }
</style>

<section class="hero">
  <div class="hero-flex">
    <div class="hero-text">
      <h1>Hi, I'm <span class="primary">Satya Dileep Kumar Thotakura</span></h1>
      <p class="subtitle">AI Product Manager at Pegasystems</p>
      <p>I blend Generative AI with LowCode to transform user experiences. 8+ years in enterprise software, 2+ years shipping PM-led AI initiatives.</p>
      <div>
        <a href="{{ '/about' | relative_url }}" class="btn">About Me</a>
        <a href="{{ '/contact' | relative_url }}" class="btn secondary">Get in Touch</a>
      </div>
    </div>
    <div class="hero-avatar">
      <img src="{{ '/assets/dileep11.jpg' | relative_url }}" alt="Satya Dileep" class="avatar" loading="lazy">
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
      <p>Certifications & expertise</p>
    </a>
    <a href="{{ '/micro-apps' | relative_url }}" class="quick-link-card">
      <h3>Work</h3>
      <p>Micro-apps & tools</p>
    </a>
    <a href="{{ '/blog' | relative_url }}" class="quick-link-card">
      <h3>Blog</h3>
      <p>Thoughts & case studies</p>
    </a>
  </div>
</section>
