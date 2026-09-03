---
layout: default
title: Blog
---

<style>
.blog-hero{position:relative;overflow:hidden;background:rgba(255,255,255,0.52);backdrop-filter:blur(16px) saturate(1.25);border:1px solid rgba(255,255,255,0.6);border-radius:20px;padding:1.4rem 1.5rem 1.1rem;margin-bottom:1.2rem;box-shadow:0 8px 32px rgba(37,99,235,0.06)}
body.dark .blog-hero,body.dark-amber .blog-hero,body.dark-purple .blog-hero{background:rgba(22,16,36,0.55);border-color:rgba(255,255,255,0.1);box-shadow:0 8px 32px rgba(0,0,0,0.35),inset 0 1px 0 rgba(255,255,255,0.06)}
.blog-hero .mesh::before{content:'';position:absolute;width:420px;height:420px;right:-80px;top:-100px;background:radial-gradient(circle at 30% 30%, rgba(139,92,246,0.18), transparent 65%);filter:blur(12px);pointer-events:none}
.blog-hero .mesh::after{content:'';position:absolute;width:340px;height:340px;left:-60px;bottom:-90px;background:radial-gradient(circle at 70% 70%, rgba(245,158,11,0.08), transparent 65%);filter:blur(10px);pointer-events:none}
body.dark-purple .blog-hero .mesh::before{background:radial-gradient(circle at 30% 30%, rgba(139,92,246,0.25), transparent 65%)}
.blog-hero h1{margin:0 0 0.3rem;font-size:1.55rem;letter-spacing:-0.4px;position:relative}
.blog-hero p{color:var(--muted);margin:0;font-size:0.9rem;line-height:1.6;position:relative}
.blog-hero .cta-row{margin-top:0.9rem;display:flex;gap:0.6rem;flex-wrap:wrap;position:relative}
.pill{font-size:0.7rem;font-weight:700;padding:0.3rem 0.7rem;border-radius:999px;background:var(--primary-dim);color:var(--primary)}
.blog-tabs{display:flex;gap:0.5rem;justify-content:center;margin:0 0 1.2rem}
.tab-btn{padding:0.45rem 1rem;border-radius:999px;border:1px solid var(--border);background:rgba(255,255,255,0.6);color:var(--muted);font-weight:600;font-size:0.82rem;cursor:pointer;transition:all 0.3s}
body.dark .tab-btn{background:rgba(255,255,255,0.05);border-color:rgba(255,255,255,0.1)}
.tab-btn.active{background:var(--primary);color:#fff;border-color:var(--primary)}
.blog-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1rem;padding-bottom:10rem}
.blog-card{position:relative;overflow:hidden;background:rgba(255,255,255,0.05);backdrop-filter:blur(12px) saturate(1.15);border:1px solid rgba(255,255,255,0.1);border-radius:16px;padding:1.2rem;cursor:pointer;transition:all 300ms cubic-bezier(0.4,0,0.2,1);display:flex;flex-direction:column;min-height:170px}
body.dark .blog-card,body.dark-amber .blog-card,body.dark-purple .blog-card{background:rgba(255,255,255,0.05);border-color:rgba(255,255,255,0.1)}
.blog-card:hover{transform:translateY(-4px);box-shadow:0 12px 40px rgba(0,0,0,0.4);border-color:rgba(139,92,246,0.3)}
.blog-card .card-date{font-size:0.68rem;color:var(--muted);letter-spacing:0.5px;text-transform:uppercase;margin-bottom:0.35rem}
.blog-card .card-title{margin:0 0 0.45rem;font-size:1rem;line-height:1.35;font-weight:600;color:#f3f4f6}
.blog-card .card-desc{margin:0;color:#9ca3af;font-size:0.83rem;line-height:1.7;display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden;flex:1}
.blog-card .card-tags{margin-top:0.75rem;display:flex;flex-wrap:wrap;gap:0.35rem}
.blog-card .tag{font-size:0.68rem;font-weight:600;padding:4px 8px;border-radius:6px;background:rgba(139,92,246,0.1);color:#c4b5fd;border:1px solid rgba(139,92,246,0.15)}
.card-top{height:3px;background:linear-gradient(90deg,var(--primary),var(--accent));border-radius:4px;margin:-1.2rem -1.2rem 0.9rem -1.2rem;opacity:0;transition:opacity 300ms}
.blog-card:hover .card-top{opacity:1}
</style>

<div class="blog-hero">
  <div class="mesh"></div>
  <h1>Blog & Feed</h1>
  <p>Curated long-form articles on Agentic AI and product strategy, alongside real-time professional updates and thoughts.</p>
  <div class="cta-row">
    <a href="https://satyadileep.github.io/linkedin/" class="btn" style="padding:0.45rem 0.95rem;font-size:0.85rem">View LinkedIn Feed →</a>
  </div>
</div>

<div class="blog-tabs">
  <button class="tab-btn active" data-tab="articles">Long-form Articles</button>
  <button class="tab-btn" data-tab="feed">Short-form Feed</button>
</div>

<div id="articles-grid" class="blog-grid">
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

<div id="feed-grid" class="blog-grid" style="display:none">
  {% for post in site.data.linkedin_posts %}
    <article class="blog-card feed-card"
      data-text="{{ post.text | escape }}"
      data-title="{{ post.title | escape }}"
      data-date="{{ post.date }}"
      data-url="{{ post.url }}">
      <div class="card-top"></div>
      <div class="card-date">{{ post.date }} · {{ post.chars }} chars</div>
      <h2 class="card-title">{{ post.title }}</h2>
      <p class="card-desc">{{ post.excerpt }}</p>
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
  const tabs = document.querySelectorAll('.tab-btn');
  const articlesGrid = document.getElementById('articles-grid');
  const feedGrid = document.getElementById('feed-grid');
  tabs.forEach(btn => {
    btn.addEventListener('click', () => {
      tabs.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const tab = btn.dataset.tab;
      if (tab === 'articles') { articlesGrid.style.display = 'grid'; feedGrid.style.display = 'none'; }
      else { articlesGrid.style.display = 'none'; feedGrid.style.display = 'grid'; }
    });
  });

  const modal = document.getElementById('post-modal');
  const spinner = document.getElementById('modal-spinner');
  const mTitle = modal.querySelector('.modal-title');
  const mDate = modal.querySelector('.modal-date');
  const mText = modal.querySelector('.modal-text');
  const mHeader = modal.querySelector('.modal-header');
  let loaded = {};
  document.querySelectorAll('#articles-grid .blog-card').forEach(card => {
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
  document.querySelectorAll('#feed-grid .blog-card').forEach(card => {
    card.addEventListener('click', () => {
      mTitle.textContent = card.dataset.title;
      mDate.textContent = card.dataset.date;
      mText.innerHTML = '<p style="white-space:pre-wrap;line-height:1.7">' + card.dataset.text + '</p><p style="margin-top:1rem"><a href="' + card.dataset.url + '" target="_blank" style="font-weight:700">View on LinkedIn →</a></p>';
      mText.style.display = '';
      mHeader.style.display = '';
      spinner.style.display = 'none';
      modal.classList.add('active');
      document.body.style.overflow = 'hidden';
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
