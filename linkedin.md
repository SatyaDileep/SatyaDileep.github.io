---
layout: default
title: LinkedIn Archive
permalink: /linkedin/
---

<style>
.linkedin-header{margin-bottom:1.25rem}
.linkedin-header h1{margin:0 0 0.35rem;font-size:1.7rem;letter-spacing:-0.4px}
.linkedin-header p{color:var(--muted);margin:0;font-size:0.92rem}
.linkedin-toolbar{display:flex;gap:0.6rem;flex-wrap:wrap;align-items:center;margin:1rem 0 1.1rem}
.search-wrap{flex:1;min-width:220px;position:relative}
.search-wrap input{width:100%;padding:0.65rem 0.9rem 0.65rem 2.2rem;border-radius:999px;border:1px solid var(--border);background:rgba(255,255,255,0.7);backdrop-filter:blur(8px);font-size:0.9rem;color:var(--text);outline:none}
body.dark .search-wrap input,body.dark-amber .search-wrap input,body.dark-purple .search-wrap input{background:rgba(255,255,255,0.06);border-color:rgba(255,255,255,0.08)}
.search-wrap::before{content:'⌕';position:absolute;left:12px;top:50%;transform:translateY(-50%);color:var(--muted);font-size:1rem}
.count-pill{font-size:0.75rem;font-weight:700;padding:0.4rem 0.8rem;border-radius:999px;background:var(--primary-dim);color:var(--primary);white-space:nowrap}
.tag-row{display:flex;gap:0.4rem;flex-wrap:wrap;margin:0 0 1rem}
.tag-pill{font-size:0.68rem;font-weight:600;padding:0.32rem 0.7rem;border-radius:999px;border:1px solid var(--border);background:rgba(255,255,255,0.5);color:var(--muted);cursor:pointer;transition:var(--transition)}
.tag-pill.active{background:var(--primary);color:#fff;border-color:var(--primary)}
.ln-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:0.9rem}
.ln-card{background:rgba(255,255,255,0.62);backdrop-filter:blur(12px) saturate(1.15);border:1px solid rgba(255,255,255,0.6);border-radius:16px;padding:1.1rem;transition:var(--transition);cursor:pointer;display:flex;flex-direction:column;min-height:160px}
body.dark .ln-card,body.dark-amber .ln-card,body.dark-purple .ln-card{background:rgba(22,18,36,0.45);border-color:rgba(255,255,255,0.07)}
.ln-card:hover{transform:translateY(-3px);box-shadow:var(--shadow-lg);border-color:var(--primary)}
.ln-card h3{margin:0 0 0.4rem;font-size:0.95rem;line-height:1.35}
.ln-card p{margin:0;color:var(--muted);font-size:0.82rem;line-height:1.5;display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden;flex:1}
.ln-meta{display:flex;gap:0.4rem;flex-wrap:wrap;margin-top:0.7rem}
.ln-tag{font-size:0.6rem;font-weight:700;padding:2px 7px;border-radius:999px;background:var(--primary-dim);color:var(--primary)}
.ln-foot{display:flex;justify-content:space-between;align-items:center;margin-top:0.6rem;font-size:0.7rem;color:var(--muted)}
.ln-foot a{font-weight:700}
</style>

<div class="linkedin-header">
  <h1>LinkedIn Archive — 14 posts</h1>
  <p>Your full public activity from <a href="https://www.linkedin.com/in/satya-dileep-kumar-thotakura-9b25021b/" target="_blank">linkedin.com/in/satya-dileep</a> — scraped via <code>Exa livecrawl</code> (full text, no 210-char cut). Search, filter by tag, and open any post. Clean 2026-only rebuild.</p>
</div>

<div class="linkedin-toolbar">
  <div class="search-wrap"><input id="ln-search" placeholder="Search posts… (e.g. Pega, GenAI, Blueprint)"></div>
  <span class="count-pill" id="ln-count">14 posts</span>
  <a href="https://www.linkedin.com/in/satya-dileep-kumar-thotakura-9b25021b/" target="_blank" class="btn" style="padding:0.45rem 0.9rem;font-size:0.8rem">Open LinkedIn →</a>
</div>

<div class="tag-row" id="tag-row"></div>
<div class="ln-grid" id="ln-grid"></div>

<div id="ln-modal" class="modal">
  <div class="modal-backdrop"></div>
  <div class="modal-content">
    <button class="modal-close" aria-label="Close">&times;</button>
    <div class="modal-body">
      <div class="modal-header"><div class="modal-date"></div><h2 class="modal-title"></h2></div>
      <div class="modal-text" style="white-space:pre-wrap"></div>
      <p style="margin-top:1rem"><a id="modal-link" target="_blank" style="font-weight:700">View on LinkedIn →</a></p>
    </div>
  </div>
</div>

<script>
const posts = {{ site.data.linkedin_posts | jsonify }};
const grid = document.getElementById('ln-grid');
const search = document.getElementById('ln-search');
const count = document.getElementById('ln-count');
const tagRow = document.getElementById('tag-row');
let activeTag = '';
const allTags = [...new Set(posts.flatMap(p=>p.tags))].sort().slice(0,12);
allTags.forEach(t=>{
  const b=document.createElement('button');
  b.className='tag-pill'; b.textContent='#'+t;
  b.onclick=()=>{
    activeTag = activeTag===t?'':t;
    document.querySelectorAll('.tag-pill').forEach(x=>x.classList.toggle('active', x.textContent==='#'+activeTag));
    render();
  };
  tagRow.appendChild(b);
});
function render(){
  const q=(search.value||'').toLowerCase();
  const filtered=posts.filter(p=>{
    const hay=(p.title+' '+p.excerpt+' '+p.tags.join(' ')).toLowerCase();
    if(q && !hay.includes(q)) return false;
    if(activeTag && !p.tags.includes(activeTag)) return false;
    return true;
  });
  count.textContent=filtered.length+' posts';
  grid.innerHTML='';
  filtered.forEach(p=>{
    const el=document.createElement('article');
    el.className='ln-card';
    el.innerHTML=`<h3>${p.title}</h3><p>${p.excerpt}</p><div class='ln-meta'>${p.tags.map(t=>`<span class='ln-tag'>#${t}</span>`).join('')}</div><div class='ln-foot'><span>${p.date} · ${p.chars} chars</span><a href='${p.url}' target='_blank' onclick='event.stopPropagation()'>LinkedIn ↗</a></div>`;
    el.onclick=()=>openModal(p);
    grid.appendChild(el);
  });
}
const modal=document.getElementById('ln-modal');
function openModal(p){
  modal.querySelector('.modal-title').textContent=p.title;
  modal.querySelector('.modal-date').textContent=p.date+' · '+p.tags.map(t=>'#'+t).join(' ');
  modal.querySelector('.modal-text').textContent=p.text;
  document.getElementById('modal-link').href=p.url;
  modal.classList.add('active'); document.body.style.overflow='hidden';
}
modal.querySelector('.modal-backdrop').onclick=()=>{modal.classList.remove('active');document.body.style.overflow=''};
modal.querySelector('.modal-close').onclick=()=>{modal.classList.remove('active');document.body.style.overflow=''};
search.addEventListener('input', render);
render();
</script>
