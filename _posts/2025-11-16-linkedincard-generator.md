---
layout: default
title: "A Fully Customizable LinkedIn Card Generator"
description: "A zero‑setup browser micro‑app to design branded LinkedIn cards, export Markdown, and post in seconds."
tags: [micro-apps, generative-ai, design, linkedin]
---

### Why this exists
Creating a clean, on‑brand LinkedIn card should be fast, repeatable, and not tied to heavyweight design tools or local setups.  
Personal branding benefits from consistent color, typography, and a recognizable footer, and a single micro‑app can enforce that consistently across posts.  

### What it does
- Live preview while you type titles, subtitles, bullet lists, and call‑to‑action text.  
- Theme controls for colors and accent gradients, plus a personal footer block.  
- One‑click export to Markdown so the result pastes directly into a LinkedIn post editor.  
- Zero setup: pure HTML/CSS/JS, runs on GitHub Pages under apps/linkedin-card.html.  

### How to use
1. Open {{ '/apps/linkedin-card.html' | relative_url }} in a new tab.  
2. Enter Title, Subtitle, optional Image URL, Link URL/Text, and pick the Button Color.  
3. Copy the generated Markdown and paste it into your LinkedIn post.  
4. Optional: save a few presets as snippets to keep a consistent brand voice.  

### Under the hood
- The app is a small DOM builder: it renders a card preview and in parallel composes a Markdown string, keeping WYSIWYG and final output in sync.  
- Pure client‑side code means no dependencies, no tracking, and instant hosting from this repo.  

### Roadmap
- Built‑in templates for announcement, recap, and “how‑to” post formats.  
- Image upload to repo assets with automatic URL insertion.  
- Saved presets keyed to themes (glass, dark, electrify) for one‑tap styling.  
