---
layout: default
title: Blog
---

<style>
.blog-hero{position:relative;overflow:hidden;background:rgba(255,255,255,0.52);backdrop-filter:blur(16px) saturate(1.25);border:1px solid rgba(255,255,255,0.6);border-radius:20px;padding:1.4rem 1.5rem 1.1rem;margin-bottom:1.5rem;box-shadow:0 8px 32px rgba(37,99,235,0.06)}
body.dark .blog-hero{background:rgba(18,22,34,0.42);border-color:rgba(255,255,255,0.06)}
.blog-hero .mesh::before{content:'';position:absolute;width:280px;height:280px;right:-60px;top:-80px;background:radial-gradient(circle, rgba(37,99,235,0.12), transparent 70%);filter:blur(8px);pointer-events:none}
.blog-hero h1{margin:0 0 0.3rem;font-size:1.55rem;letter-spacing:-0.4px;position:relative}
.blog-hero p{color:var(--muted);margin:0;font-size:0.9rem;line-height:1.6;position:relative}
.blog-hero .cta-row{margin-top:0.9rem;display:flex;gap:0.6rem;flex-wrap:wrap;position:relative}
.pill{font-size:0.7rem;font-weight:700;padding:0.3rem 0.7rem;border-radius:999px;background:var(--primary-dim);color:var(--primary)}
.blog-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1rem}
.blog-card{position:relative;overflow:hidden;background:rgba(255,255,255,0.62);backdrop-filter:blur(12px) saturate(1.15);border:1px solid rgba(255,255,255,0.58);border-radius:16px;padding:1.2rem;cursor:pointer;transition:var(--transition);display:flex;flex-direction:column;min-height:170px}
body.dark .blog-card{background:rgba(22,18,36,0.42);border-color:rgba(255,255,255,0.07)}
.blog-card:hover{transform:translateY(-3px);box-shadow:var(--shadow-lg);border-color:var(--primary)}
.blog-card .card-date{font-size:0.68rem;color:var(--muted);letter-spacing:0.5px;text-transform:uppercase;margin-bottom:0.35rem}
.blog-card .card-title{margin:0 0 0.4rem;font-size:1rem;line-height:1.35}
.blog-card .card-desc{margin:0;color:var(--muted);font-size:0.83rem;line-height:1.55;display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden;flex:1}
.blog-card .card-tags{margin-top:0.7rem;display:flex;flex-wrap:wrap;gap:0.35rem}
.blog-card .tag{font-size:0.6rem;font-weight:700;padding:2px 7px;border-radius:999px;background:var(--primary-dim);color:var(--primary)}
.card-top{height:3px;background:linear-gradient(90deg,var(--primary),var(--accent));border-radius:4px;margin:-1.2rem -1.2rem 0.9rem -1.2rem;opacity:0}
.blog-card:hover .card-top{opacity:1}
</style>

<div class="blog-hero">
  <div class="mesh"></div>
  <h1>Insights & Reflections</h1>
  <p>Curated long-form thinking on Agentic AI, product strategy, and the shift from execution to orchestration. <span class="pill">12 articles</span> · For the full 53-post LinkedIn history, see the archive.</p>
  <div class="cta-row">
    <a href="{{ '/linkedin/' | relative_url }}" class="btn" style="padding:0.45rem 0.95rem;font-size:0.85rem">LinkedIn Archive (53) →</a>
    <span style="align-self:center;font-size:0.78rem;color:var(--muted)">Pure posts only — no reactions, full text even >210 chars</span>
  </div>
</div>

<div class="blog-grid">
  {% assign curated = site.posts | where_exp: "p", "p.source != 'linkedin'" | sort: 'date' | reverse %}
  {% for post in curated %}
    <article class="blog-card"
      data-url="{{ post.url | relative_url }}"
      data-title="{{ post.title | escape }}"
      data-date="{{ post.date | date: '%b %d, %Y' }}">
      <div class="card-top"></div>
      <div class="card-date">{{ post.date | date: "%b %d, %Y" }}</div>
      <h2 class="card-title">{{ post.title }}</h2>
      <p class="card-desc">{{ post.description }}</p>
      {% if post.tags %}
      <div class="card-tags">
        {% for tag in post.tags limit:4 %}
          <span class="tag">#{{ tag }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </article>
  {% endfor %}
</div>

<div id="post-modal" class="modal">
  <div class="modal-backdrop"></div>
  <div class="modal-content">
    <button class="modal-close" aria-label="Close">&times;</button>
    <div id="modal-spinner" class="spinner active"></div>
    <div class="modal-body">
      <div class="modal-header">
        <div class="modal-date"></div>
        <h2 class="modal-title"></h2>
      </div>
      <div class="modal-text"></div>
    </div>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const modal = document.getElementById('post-modal');
  const cards = document.querySelectorAll('.blog-card');
  const spinner = document.getElementById('modal-spinner');
  const mTitle = modal.querySelector('.modal-title');
  const mDate = modal.querySelector('.modal-date');
  const mText = modal.querySelector('.modal-text');
  const mHeader = modal.querySelector('.modal-header');
  let loaded = {};
  cards.forEach(card => {
    card.addEventListener('click', () => {
      const url = card.dataset.url;
      const title = card.dataset.title;
      const date = card.dataset.date;
      mTitle.textContent = title;
      mDate.textContent = date;
      mText.innerHTML = '';
      mText.style.display = 'none';
      mHeader.style.display = '';
      spinner.style.display = 'block';
      modal.classList.add('active');
      document.body.style.overflow = 'hidden';
      if (loaded[url]) {
        spinner.style.display = 'none';
        mText.innerHTML = loaded[url];
        mText.style.display = '';
        return;
      }
      fetch(url).then(res => res.text()).then(html => {
        const s = '<main class="container" id="page-content">';
        const e = '</main>';
        const a = html.indexOf(s);
        const b = html.indexOf(e, a);
        let content = '';
        if (a !== -1 && b !== -1) content = html.slice(a + s.length, b).trim();
        loaded[url] = content;
        mText.innerHTML = content;
        spinner.style.display = 'none';
        mText.style.display = '';
      });
    });
  });
  const closeBtn = modal.querySelector('.modal-close');
  const backdrop = modal.querySelector('.modal-backdrop');
  function closeModal(){ modal.classList.remove('active'); document.body.style.overflow=''; setTimeout(()=>{mText.innerHTML='';},300); }
  closeBtn.addEventListener('click', closeModal);
  backdrop.addEventListener('click', closeModal);
  document.addEventListener('keydown', e=>{ if(e.key==='Escape') closeModal(); });
});
</script>
