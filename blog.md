---
layout: default
title: Blog
---

<style>
.blog-header { margin-bottom: 2rem; }
.blog-header h1 { margin: 0 0 0.5rem 0; }
.blog-header p { color: var(--muted); margin: 0; }

.blog-grid { 
  display: grid; 
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); 
  gap: 1.5rem; 
}

.blog-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 1.5rem;
  cursor: pointer;
  transition: transform 0.2s, box-shadow 0.2s, border-color 0.2s;
}
.blog-card:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow);
  border-color: var(--primary);
}

.blog-card .card-date { 
  font-size: 0.8rem; 
  color: var(--muted); 
  margin-bottom: 0.5rem; 
}
.blog-card .card-title { 
  margin: 0 0 0.5rem 0; 
  font-size: 1.15rem; 
  line-height: 1.4;
}
.blog-card .card-desc { 
  margin: 0; 
  color: var(--muted); 
  font-size: 0.9rem;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
.blog-card .card-tags {
  margin-top: 1rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}
.blog-card .tag {
  font-size: 0.7rem;
  background: var(--border);
  color: var(--muted);
  padding: 2px 8px;
  border-radius: 4px;
}
</style>

<div class="blog-header">
  <h1>Blog</h1>
  <p>Thoughts on product management, GenAI, agentic automation, and prototyping.</p>
</div>

<div class="blog-grid">
  {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
  {% for post in sorted_posts %}
    <article class="blog-card" data-url="{{ post.url | relative_url }}">
      <div class="card-date">{{ post.date | date: "%b %d, %Y" }}</div>
      <h2 class="card-title">{{ post.title }}</h2>
      <p class="card-desc">{{ post.description }}</p>
      {% if post.tags %}
      <div class="card-tags">
        {% for tag in post.tags %}
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
    <div class="modal-body">
      <div class="modal-header">
        <div class="modal-date"></div>
        <h2 class="modal-title"></h2>
      </div>
      <div class="modal-text"></div>
    </div>
  </div>
</div>

<style>
.modal {
  display: none;
  position: fixed;
  inset: 0;
  z-index: 100;
  align-items: center;
  justify-content: center;
  padding: 1rem;
}
.modal.active { display: flex; }

.modal-backdrop {
  position: absolute;
  inset: 0;
  background: rgba(0,0,0,0.6);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
}

.modal-content {
  position: relative;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 16px;
  max-width: 720px;
  width: 100%;
  max-height: 85vh;
  overflow-y: auto;
  box-shadow: 0 25px 50px rgba(0,0,0,0.25);
}

.modal-close {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background: var(--border);
  border: none;
  width: 36px;
  height: 36px;
  border-radius: 50%;
  font-size: 1.5rem;
  cursor: pointer;
  color: var(--text);
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
}
.modal-close:hover { background: var(--muted); color: #fff; }

.modal-body { padding: 2rem; }

.modal-header { margin-bottom: 1.5rem; }
.modal-date { font-size: 0.85rem; color: var(--muted); margin-bottom: 0.5rem; }
.modal-title { margin: 0; font-size: 1.5rem; line-height: 1.3; }
.modal-text { color: var(--text); line-height: 1.7; }
.modal-text h3 { margin: 1.5rem 0 0.5rem 0; font-size: 1.1rem; }
.modal-text p { margin: 0 0 1rem 0; }
.modal-text ul, .modal-text ol { margin: 0 0 1rem 0; padding-left: 1.5rem; }
.modal-text li { margin-bottom: 0.5rem; }
.modal-text strong { color: var(--text); }
.modal-text .badge {
  display: inline-block;
  background: var(--primary);
  color: #fff;
  font-size: 0.7rem;
  padding: 2px 8px;
  border-radius: 4px;
  margin-bottom: 0.5rem;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const modal = document.getElementById('post-modal');
  const cards = document.querySelectorAll('.blog-card');
  
  cards.forEach(card => {
    card.addEventListener('click', () => {
      const url = card.dataset.url;
      fetch(url)
        .then(res => res.text())
        .then(html => {
          const parser = new DOMParser();
          const doc = parser.parseFromString(html, 'text/html');
          
          const title = doc.querySelector('h1, h2')?.textContent || '';
          const date = doc.querySelector('.timeline-date, .card-date')?.textContent || '';
          const content = doc.querySelector('section, main, .post-content, article')?.innerHTML || doc.body.innerHTML;
          
          modal.querySelector('.modal-title').textContent = title;
          modal.querySelector('.modal-date').textContent = doc.querySelector('[class*="date"]')?.textContent || '';
          modal.querySelector('.modal-text').innerHTML = content;
          
          modal.classList.add('active');
          document.body.style.overflow = 'hidden';
        });
    });
  });
  
  const closeBtn = modal.querySelector('.modal-close');
  const backdrop = modal.querySelector('.modal-backdrop');
  
  function closeModal() {
    modal.classList.remove('active');
    document.body.style.overflow = '';
  }
  
  closeBtn.addEventListener('click', closeModal);
  backdrop.addEventListener('click', closeModal);
  document.addEventListener('keydown', e => {
    if (e.key === 'Escape') closeModal();
  });
});
</script>
