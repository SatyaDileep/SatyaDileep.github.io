---
layout: default
title: Blog
---

<style>
.blog-header { margin-bottom: 1.5rem; }
.blog-header h1 { margin: 0 0 0.5rem; font-size: 1.5rem; }
.blog-header p { color: var(--muted); margin: 0; font-size: 0.9rem; }
</style>

<div class="blog-header">
  <h1>Insights & Reflections</h1>
  <p>Structured thoughts on Agentic AI, product strategy, and the shift from execution to orchestration.</p>
</div>

<div class="blog-grid">
  {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
  {% for post in sorted_posts %}
    <article class="blog-card"
      data-url="{{ post.url | relative_url }}"
      data-title="{{ post.title | escape }}"
      data-date="{{ post.date | date: '%b %d, %Y' }}">
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

      fetch(url)
        .then(res => res.text())
        .then(html => {
          const doc = new DOMParser().parseFromString(html, 'text/html');
          const main = doc.querySelector('main');
          const content = main ? main.innerHTML : '';
          loaded[url] = content;
          mText.innerHTML = content;
          spinner.style.display = 'none';
          mText.style.display = '';
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
