---
layout: default
---

<div style="display:flex; align-items:center; gap:16px; margin-top:24px;">
  <img class="avatar" src="/assets/images/HeadShots097.jpg" alt="Mario Jimenez">
  <div>
    <h1 style="margin:0;">Mario Jimenez Illesca</h1>
    <p style="margin:4px 0 0 0;">CS @ SFSU · Full-stack dev · Interested in AI/VR and Biotech</p>
    <p style="margin:4px 0 0 0;">
      <a href="mailto:mariojillesca@gmail.com">Email</a> · 
      <a href="https://github.com/nochinxx">GitHub</a> · 
      <a href="https://www.linkedin.com/in/mario-jimenez-7b9683206/">LinkedIn</a> · 
      <a href="/blog/">Blog</a>
    </p>
  </div>
</div>

## Projects

<div class="grid">
  <div class="project-card">
    <h3><a href="/post/2025-06-20-dayton-sheets.html">Dayton Financial RFQ Tool</a> 
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

**Intern — Boyd Lighting**  
Digitized and structured a 1,000+ product archive to create a searchable internal knowledge base, improving sales enablement and accelerating design workflows. Proposed and designed concepts for a VR-powered virtual showroom and an AI-driven search tool to enhance product discovery, inspire design concepts, and support strategic sales initiatives.

**Software Developer @Dayton Financial (Contract) — June 2025**  
Shipped a production quoting platform with a 2-person team. Implemented auth, granular roles, and live UI for quotes.

## Skills

JavaScript/TypeScript, React/Next.js, Firebase/Firestore, Python, D3, Tailwind, Git, Jekyll.

## Résumé

<p>
  <a href="/documents/Aug-2.pdf">📄 Download PDF</a><br>
  <span>Email me for referrals</span>
</p>

