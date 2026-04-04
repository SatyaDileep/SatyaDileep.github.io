---
layout: default
title: About
---

<style>
.page-header { margin-bottom: 2rem; }
.page-header h1 { margin: 0 0 0.5rem 0; font-size: 2rem; }
.page-header p { color: var(--muted); margin: 0; }

.timeline { position: relative; padding-left: 2rem; }
.timeline::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 2px;
  background: var(--border);
}

.timeline-item { position: relative; margin-bottom: 2rem; }
.timeline-item::before {
  content: '';
  position: absolute;
  left: -2rem;
  top: 6px;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: var(--primary);
  transform: translateX(-4px);
}

.timeline-date { 
  font-size: 0.85rem; 
  color: var(--muted); 
  margin-bottom: 0.25rem; 
}
.timeline-title { margin: 0 0 0.25rem 0; font-size: 1.1rem; }
.timeline-company { color: var(--primary); font-weight: 600; margin-bottom: 0.5rem; }
.timeline-desc { color: var(--muted); font-size: 0.95rem; margin: 0; }
.timeline-location { font-size: 0.85rem; color: var(--muted); margin-bottom: 0.5rem;}

.tech-tag {
  display: inline-block;
  background: var(--surface);
  border: 1px solid var(--border);
  padding: 2px 8px;
  border-radius: 4px;
  font-size: 0.75rem;
  color: var(--muted);
  margin-right: 4px;
  margin-top: 4px;
}

.section-title { font-size: 1.25rem; margin: 2.5rem 0 1.5rem 0; }
</style>

<div class="page-header">
  <h1>About Me</h1>
  <p>8+ years building enterprise products, 2+ years in product management</p>
</div>

<section>
  <h2 class="section-title">Experience</h2>
  <div class="timeline">
    
    <div class="timeline-item">
      <div class="timeline-date">Sep 2025 - Present</div>
      <h3 class="timeline-title">Senior Product Manager</h3>
      <div class="timeline-company">Pegasystems</div>
      <div class="timeline-location">Hyderabad, Telangana</div>
      <p class="timeline-desc">Leading initiatives in LowCode, GenerativeAI and AgenticAI, focusing on creating intuitive, easy-to-use authoring experiences and boosting user adoption. Evangelizing ideas that boost adoption of Generative & Agentic AI across products.</p>
      <div><span class="tech-tag">Generative AI</span><span class="tech-tag">Agentic AI</span><span class="tech-tag">Product Management</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">May 2023 - Sep 2025</div>
      <h3 class="timeline-title">Product Manager</h3>
      <div class="timeline-company">Pegasystems</div>
      <div class="timeline-location">Hyderabad, Telangana</div>
      <p class="timeline-desc">Led transformation of complex ideas into intuitive, user-friendly features for Pega's Enterprise Low-Code Platform. Focused on leveraging Generative AI to simplify and accelerate development workflows for citizen and business developers.</p>
      <div><span class="tech-tag">Low-Code</span><span class="tech-tag">Generative AI</span><span class="tech-tag">Product Management</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Mar 2021 - May 2023</div>
      <h3 class="timeline-title">Principal Software Engineer</h3>
      <div class="timeline-company">Pegasystems</div>
      <div class="timeline-location">Hyderabad, Telangana</div>
      <div><span class="tech-tag">Enterprise Software</span><span class="tech-tag">Pega Platform</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Sep 2017 - Mar 2021</div>
      <h3 class="timeline-title">Senior Software Engineer</h3>
      <div class="timeline-company">Pegasystems</div>
      <div class="timeline-location">Hyderabad, Telangana</div>
      <div><span class="tech-tag">Enterprise Software</span><span class="tech-tag">Workflow Automation</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Oct 2016 - Sep 2017</div>
      <h3 class="timeline-title">Senior Development Engineer</h3>
      <div class="timeline-company">Pramati Technologies / Imaginea Technologies</div>
      <div class="timeline-location">Hyderabad Area</div>
      <p class="timeline-desc">Design, develop and deliver best possible solutions for clients.</p>
      <div><span class="tech-tag">Software Development</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">May 2015 - Oct 2016</div>
      <h3 class="timeline-title">Development Engineer</h3>
      <div class="timeline-company">Pramati Technologies / WaveMaker</div>
      <div class="timeline-location">Hyderabad</div>
      <p class="timeline-desc">Gathered requirements for Hybrid applications to be built on WaveMaker (A RAD tool), design, develop quality applications by powering them with Java logic for better computations. Developed and enhanced internal applications like Leave Management System.</p>
      <div><span class="tech-tag">Java</span><span class="tech-tag">RAD Tools</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">May 2013 - May 2015</div>
      <h3 class="timeline-title">Assistant Systems Engineer</h3>
      <div class="timeline-company">Tata Consultancy Services</div>
      <div class="timeline-location">Chennai</div>
      <p class="timeline-desc">Key Developer for Dashboards, Reports, Charts modules for MasterCraft Service Governance Manager.</p>
      <div><span class="tech-tag">JavaScript</span><span class="tech-tag">API Design</span></div>
    </div>

  </div>

  <h2 class="section-title">Education</h2>
  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-date">2008 - 2012</div>
      <h3 class="timeline-title">B.Tech, Computer Science</h3>
      <div class="timeline-company">Pragati Engineering College</div>
    </div>
    <div class="timeline-item">
      <div class="timeline-date">2006 - 2008</div>
      <h3 class="timeline-title">MPC (Maths, Physics, Chemistry)</h3>
      <div class="timeline-company">Sri Chaitanya Junior College</div>
    </div>
  </div>
</section>
