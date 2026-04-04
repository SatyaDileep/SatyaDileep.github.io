---
layout: default
title: Contact
---

<style>
.page-header { margin-bottom: 2rem; text-align: center; }
.page-header h1 { margin: 0 0 0.5rem 0; font-size: 2rem; }
.page-header p { color: var(--muted); margin: 0; }

.contact-grid { 
  display: grid; 
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); 
  gap: 1.5rem; 
  max-width: 800px;
  margin: 0 auto;
}

.contact-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 1.5rem;
  text-align: center;
  transition: transform 0.2s, box-shadow 0.2s;
}
.contact-card:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow);
}
.contact-icon {
  font-size: 2rem;
  margin-bottom: 0.75rem;
}
.contact-card h3 { margin: 0 0 0.25rem 0; font-size: 1rem; }
.contact-card p { margin: 0; color: var(--muted); }
.contact-card a { 
  color: var(--primary); 
  text-decoration: none; 
  font-weight: 600;
}
.contact-card a:hover { text-decoration: underline; }

.cta-box {
  max-width: 600px;
  margin: 3rem auto 0;
  text-align: center;
  padding: 2rem;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 12px;
}
.cta-box h2 { margin: 0 0 0.5rem 0; font-size: 1.5rem; }
.cta-box p { color: var(--muted); margin: 0 0 1.5rem 0; }
</style>

<div class="page-header">
  <h1>Get in Touch</h1>
  <p>Let's connect! I'm always open to discussing new opportunities and collaborations.</p>
</div>

<section>
  <div class="contact-grid">
    
    <div class="contact-card">
      <div class="contact-icon">📧</div>
      <h3>Email</h3>
      <p><a href="mailto:satyadileepkmr30@gmail.com">satyadileepkmr30@gmail.com</a></p>
    </div>

    <div class="contact-card">
      <div class="contact-icon">💼</div>
      <h3>LinkedIn</h3>
      <p><a href="https://www.linkedin.com/in/satya-dileepkumar-thotakura-9b25021b" target="_blank">linkedin.com/in/satya-dileep...</a></p>
    </div>

    <div class="contact-card">
      <div class="contact-icon">🗓️</div>
      <h3>Topmate</h3>
      <p><a href="https://topmate.io/satya_dileep_thotakura" target="_blank">Book a session</a></p>
    </div>

  </div>

  <div class="cta-box">
    <h2>Let's Build & Innovate</h2>
    <p>Whether you have a project in mind, want to collaborate on an Agentic AI workflow, or just want to say hi — drop me a message!</p>
    <a href="mailto:satyadileepkmr30@gmail.com" class="btn">Send Message</a>
  </div>
</section>
