---
layout: default
---

<link rel="stylesheet" href="/assets/style.css">


<div style="display:flex; align-items:center; gap:16px; margin-top:24px;">
  <img class="avatar" src="/assets/images/HeadShots097.jpg" alt="Mario Jimenez">
  <div>
    <h1 style="margin:0;">Mario Jimenez Illesca</h1>
    <p style="margin:4px 0 0 0;">CS @ SFSU · Full-stack dev · Interested in Machine Learning, AI/VR and Biotech</p>
    <p style="margin:4px 0 0 0;">
      <a href="mailto:mariojillesca@gmail.com">mariojillesca@gmail.com</a> · 
      <a href="https://github.com/nochinxx">GitHub</a> · 
      <a href="https://www.linkedin.com/in/mario-jimenez-7b9683206/">LinkedIn</a> · 
      <a href="/blog/">Blog</a>
    </p>
  </div>
</div>

## Skills

C++, Python, Java, JavaScript/TypeScript, React/Next.js, Firebase/Firestore, Tailwind, Git.

## Projects

<div class="grid">
  <div class="project-card">
    <h3><a href="{{ '/projects/ucsd-data-structures/' | relative_url }}">
      UCSD Data Structures & Performance
    </a>
      <span class="badge">Java · Algorithms · Data Structures</span>
    </h3>
    <p>
      A series of five CS projects covering linked lists, tries, autocomplete, text analysis, performance benchmarking, 
      and spelling suggestion engines. Focused on implementing core data structures from scratch, optimizing algorithms, 
      and validating correctness with JUnit tests. 
    </p>
    <p>
      <a href="https://github.com/nochinxx/ucsd-data-structures">Code</a>
    </p>
  </div>
</div>


<div class="grid">
  <div class="project-card">
    <h3><a href="{{ '/projects/dayton-sheets/' | relative_url }}">Dayton Financial RFQ Tool</a> 
      <span class="badge">Next.js · Firebase · Firestore · TanStack</span>
    </h3>
    <p>
      Multi-tenant RFQ and quoting platform featuring real-time buyer/seller dashboards, role-based access, interactive spreadsheet UI, seller magic links, batch updates, and buyer aggregation views. 
      Replaced complex spreadsheets and saved thousands in operational costs.
    </p>
    <p>
      <a href="https://github.com/nima64/Dayton-Sheets">Code</a> · 
      <a href="https://dayton-sheets-git-main-rintarouokabe12gmailcoms-projects.vercel.app/">Live</a>
    </p>
  </div>

  <div class="project-card">
    <h3>Nutrition Tracker <span class="badge">React · Firebase</span></h3>
    <p>
      USDA API integration to scrape all the nutrients from different foods, charts, role-based access, and daily macro insights with clean UI.
    </p>
    <p>
      <a href="https://github.com/nima64/nutrition-nextjs">Code</a> · 
      <a href="https://nutrition-nextjs.vercel.app/">Live</a>
    </p>
  </div>
</div>

## Blog Highlights

<ul>
  {% for post in site.posts limit:3 %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br>
    </li>
  {% endfor %}
</ul>

## Experience

**Software Developer (Contract) — Dayton Financial** (Apr–Jun 2025)  
Designed and deployed a production-ready quoting platform replacing complex spreadsheet workflows, saving thousands in operational costs.  
Built real-time buyer-seller dashboards with interactive spreadsheet UIs featuring live updates, cell-level editing, and secure role-based access.  
*Stack: Next.js, TypeScript, React, Firebase, TanStack Table.*

**Intern — Boyd Lighting** (Jun–Aug 2025)  
Digitized and structured a 1,000+ product archive into a searchable knowledge base, improving sales enablement.  
Proposed VR-powered virtual showroom and AI-driven search tool concepts to enhance product discovery.  

**Coding Teacher — Marin Horizon Middle School** (Sep 2025–Present)  
Designed and delivered a custom coding curriculum (Scratch) for 6th–8th graders.  
Taught problem decomposition, logic, and computational thinking, guiding students in building interactive projects.  

**Intern — UC Merced CalTeach Program** (Jul–Aug 2024)  
Developed Python/Jupyter-based visualizations of dark matter data with Astropy and Matplotlib.  
Collaborated with faculty to improve K-12 STEM education materials and strategies.  

## Résumé

<p>
  <a href="assets/documents/SepResume.pdf">📄 Download PDF</a><br>
  <span>Email me for referrals</span>
</p>

