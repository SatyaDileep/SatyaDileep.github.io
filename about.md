---
layout: default
title: About
---

<style>
.timeline { position: relative; padding-left: 2.5rem; padding-bottom: 1rem; }
.timeline::before {
  content: ''; position: absolute; left: 5px; top: 4px; bottom: 4px;
  width: 2px; background: linear-gradient(to bottom, var(--primary), var(--border)); border-radius: 2px;
}
.timeline-item { position: relative; margin-bottom: 2rem; }
.timeline-item::before {
  content: ''; position: absolute; left: -2.5rem; top: 6px;
  width: 12px; height: 12px; border-radius: 50%;
  background: var(--surface); border: 2px solid var(--primary);
  transform: translateX(0); z-index: 1;
}
.timeline-item:first-child::before {
  background: var(--primary); border-color: var(--primary);
  box-shadow: 0 0 10px rgba(168,85,247,0.5), 0 0 20px rgba(168,85,247,0.3);
}
.timeline-date { font-size: 0.8rem; color: #9ca3af; margin-bottom: 0.2rem; text-transform: uppercase; letter-spacing: 0.4px; font-weight: 500; }
.timeline-title { margin: 0 0 0.15rem; font-size: 1.05rem; }
.timeline-company { color: var(--primary); font-weight: 600; margin-bottom: 0.3rem; font-size: 0.9rem; transition: all 0.2s; }
.timeline-company:hover { filter: brightness(1.3); text-decoration: underline; text-underline-offset: 3px; cursor: pointer; }
.timeline-desc { color: var(--muted); font-size: 0.9rem; margin: 0 0 0.5rem; line-height: 1.65; }
.timeline-location { font-size: 0.8rem; color: var(--muted); margin-bottom: 0.4rem; }
.timeline + .section-title { margin-top: 0; }
section { padding-bottom: 8rem; }
section:last-child { padding-bottom: 8rem; }
.page-header { margin-bottom: 1rem; }
.section-title { margin-top: 1.5rem; }
.tech-tag{ display:inline-block; padding:4px 12px; border-radius:6px; font-size:0.7rem; font-weight:600; letter-spacing:0.2px; background:rgba(88,28,135,0.3); color:var(--primary); border:1px solid rgba(139,92,246,0.2); margin-right:6px; margin-top:6px; }
</style>

<div class="page-header">
  <h1>About Me</h1>
  <p><strong><span id="exp-years"></span> years</strong> in enterprise software, including 2+ years in product management</p>
</div>

<section>
  <h2 class="section-title">Experience</h2>
  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-date">Sep 2025 &mdash; Present</div>
      <h3 class="timeline-title">Senior Product Manager</h3>
      <div class="timeline-company">Pegasystems</div>
      <div class="timeline-location">Hyderabad, Telangana</div>
      <p class="timeline-desc">Leading initiatives in LowCode, GenerativeAI and AgenticAI, focusing on creating intuitive, easy-to-use authoring experiences and boosting user adoption. Evangelizing ideas that boost adoption of Generative and Agentic AI across products.</p>
      <div><span class="tech-tag">Generative AI</span><span class="tech-tag">Agentic AI</span><span class="tech-tag">Product Management</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">May 2023 &mdash; Sep 2025</div>
      <h3 class="timeline-title">Product Manager</h3>
      <div class="timeline-company">Pegasystems</div>
      <div class="timeline-location">Hyderabad, Telangana</div>
      <p class="timeline-desc">Led transformation of complex ideas into intuitive, user-friendly features for Pega's Enterprise Low-Code Platform. Focused on leveraging Generative AI to simplify and accelerate development workflows for citizen and business developers.</p>
      <div><span class="tech-tag">Low-Code</span><span class="tech-tag">Generative AI</span><span class="tech-tag">Product Management</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Mar 2021 &mdash; May 2023</div>
      <h3 class="timeline-title">Principal Software Engineer</h3>
      <div class="timeline-company">Pegasystems</div>
      <div class="timeline-location">Hyderabad, Telangana</div>
      <p class="timeline-desc">Architected and delivered enterprise-scale features on Pega's Low-Code platform. Drove technical design for workflow automation and integration capabilities serving global clients.</p>
      <div><span class="tech-tag">Enterprise Software</span><span class="tech-tag">Pega Platform</span><span class="tech-tag">System Architecture</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Sep 2017 &mdash; Mar 2021</div>
      <h3 class="timeline-title">Senior Software Engineer</h3>
      <div class="timeline-company">Pegasystems</div>
      <div class="timeline-location">Hyderabad, Telangana</div>
      <p class="timeline-desc">Built and maintained core platform modules for enterprise workflow automation. Collaborated across teams to ship high-impact features improving developer productivity and runtime performance.</p>
      <div><span class="tech-tag">Enterprise Software</span><span class="tech-tag">Workflow Automation</span><span class="tech-tag">Platform Engineering</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">Oct 2016 &mdash; Sep 2017</div>
      <h3 class="timeline-title">Senior Development Engineer</h3>
      <div class="timeline-company">Pramati Technologies / Imaginea Technologies</div>
      <div class="timeline-location">Hyderabad Area</div>
      <p class="timeline-desc">Designed and delivered client solutions across cloud and enterprise stacks. Owned end-to-end delivery for multiple concurrent projects, from requirements to deployment.</p>
      <div><span class="tech-tag">Software Development</span><span class="tech-tag">Cloud Solutions</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">May 2015 &mdash; Oct 2016</div>
      <h3 class="timeline-title">Development Engineer</h3>
      <div class="timeline-company">Pramati Technologies / WaveMaker</div>
      <div class="timeline-location">Hyderabad</div>
      <p class="timeline-desc">Gathered requirements for Hybrid applications to be built on WaveMaker (A RAD tool), design, develop quality applications by powering them with Java logic for better computations. Developed and enhanced internal applications like Leave Management System.</p>
      <div><span class="tech-tag">Java</span><span class="tech-tag">RAD Tools</span></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date">May 2013 &mdash; May 2015</div>
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
      <div class="timeline-date">2008 &mdash; 2012</div>
      <h3 class="timeline-title">B.Tech, Computer Science</h3>
      <div class="timeline-company">Pragati Engineering College</div>
    </div>
    <div class="timeline-item">
      <div class="timeline-date">2006 &mdash; 2008</div>
      <h3 class="timeline-title">MPC (Maths, Physics, Chemistry)</h3>
      <div class="timeline-company">Sri Chaitanya Junior College</div>
    </div>
  </div>
</section>
