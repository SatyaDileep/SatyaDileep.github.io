---
layout: default
title: Micro-Apps
permalink: /micro-apps/
---

<div class="page-header">
  <h1>Builds & Prototypes</h1>
  <p>Shipped, live, and private-by-default — 3 featured builds plus earlier experiments I keep for reference.</p>
</div>

<section>
  <h2 class="section-title">Featured — Live on the Web</h2>
  <div class="bento-grid">
    <article class="featured-card">
      <div class="featured-top" style="background:linear-gradient(90deg,#0ea5e9,#6366f1)"></div>
      <span class="featured-num">01 — LIVE</span>
      <div class="featured-body">
        <h3>✨ Content Crafting Wand for LinkedIn</h3>
        <p>Feed-accurate 560px preview with 210-char cliff, Unicode formatting that survives paste, 20-gradient Image Card Studio, and pdfjs Document Visualizer. BYO Gemini/Groq/OpenAI key — stays in localStorage, no tracking.</p>
        <div class="featured-meta"><span class="mini-tag">React 19 + Vite</span><span class="mini-tag">Tailwind v4</span><span class="mini-tag">html-to-image 2×</span><span class="mini-tag">pdfjs-dist</span></div>
        <div class="featured-actions">
          <a class="primary" href="https://funny-belekoy-39b0f8.netlify.app/" target="_blank">Live →</a>
          <a class="ghost" href="https://github.com/SatyaDileep/Content-Crafting-Wand-For-LinkedIn" target="_blank">GitHub</a>
        </div>
      </div>
    </article>
    <article class="featured-card">
      <div class="featured-top" style="background:linear-gradient(90deg,#f59e0b,#ef4444)"></div>
      <span class="featured-num">02 — LIVE</span>
      <div class="featured-body">
        <h3>🇮🇳 DocBridge — One Upload Layer for India</h3>
        <p><strong>Hackathon:</strong> Next.js app with 3 real portal journeys (UPSC 20–200KB, Vahan 10–20KB, EPFO PDF 500KB) — Canvas + pdf-lib + pdfjs in-browser, DigiLocker mock, tricolor glass UI.<br><strong>Chrome Extension:</strong> same browser engine injected onto any gov portal upload field — placeholder URL, GitHub is source of truth for now.</p>
        <div class="featured-meta"><span class="mini-tag">Next.js 14</span><span class="mini-tag">Canvas/pdf-lib</span><span class="mini-tag">Chrome Extn</span><span class="mini-tag">Netlify</span></div>
        <div class="featured-actions">
          <a class="primary" href="https://incredible-taffy-db08a6.netlify.app" target="_blank">Live (Hackathon) →</a>
          <a class="ghost" href="https://github.com/SatyaDileep/Build-What-Moves-India-Hackathon" target="_blank">GitHub</a>
          <a class="ghost" href="https://github.com/SatyaDileep/Build-What-Moves-India-Hackathon" target="_blank">Extension (soon) ↗</a>
        </div>
      </div>
    </article>
    <article class="featured-card">
      <div class="featured-top" style="background:linear-gradient(90deg,#ec4899,#8b5cf6)"></div>
      <span class="featured-num">03 — LIVE</span>
      <div class="featured-body">
        <h3>🌼 Pregnancy Blossom Journal</h3>
        <p>Private PWA — week 4–40 guide, milestone pages, photo memories, drag-drop reorder, 6 global themes, carousel + stacked views, backup JSON + print keepsake. Blossom Baby AI (Gemini proxy, caps, BYOK). Works fully offline after Add to Home Screen.</p>
        <div class="featured-meta"><span class="mini-tag">PWA IndexedDB</span><span class="mini-tag">Express API</span><span class="mini-tag">Flutter (roadmap)</span><span class="mini-tag">Offline-first</span></div>
        <div class="featured-actions">
          <a class="primary" href="https://pregnancy-blossom-journal.netlify.app/" target="_blank">Live →</a>
          <a class="ghost" href="https://github.com/SatyaDileep/pregnancy-journal" target="_blank">GitHub</a>
        </div>
      </div>
    </article>
  </div>
</section>

<section>
  <details class="earlier-wrap">
    <summary>Earlier experiments — not deployed (kept for reference)</summary>
    <div class="earlier-grid">
      <div class="earlier-card">
        <h4>LinkedIn Card Creator (legacy)</h4>
        <p>Original HTML/CSS/JS card builder with live preview — evolved into Content Crafting Wand above. <a href="{{ '/apps/linkedin-card.html' | relative_url }}" target="_blank">Open legacy →</a></p>
      </div>
      <div class="earlier-card">
        <h4>TamilNadu Trip Planner</h4>
        <p>Google Canvas prototype — unstructured itinerary → local insights + translate tab. Built in 30 min via vibe coding. <em>Not deployed</em></p>
      </div>
      <div class="earlier-card">
        <h4>Healthcare Report Explainer</h4>
        <p>Empathetic AI agent — plain-English report explainer with PII redaction + multilingual follow-ups. <em>Not deployed</em></p>
      </div>
      <div class="earlier-card">
        <h4>Learning Artifact Hub</h4>
        <p>AI-driven learning prototype — content → retained structured knowledge. <em>Not deployed</em></p>
      </div>
    </div>
  </details>
</section>
