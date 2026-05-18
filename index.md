---
layout: default
---

<link rel="stylesheet" href="/assets/style.css">

{% assign projects = site.data.projects | sort: "order" %}
{% assign featured_projects = projects | where: "featured", true %}
{% assign regular_projects = projects | where: "featured", false %}
{% assign writing = site.data.writing %}

<div style="display:flex; align-items:center; gap:16px; margin-top:12px;">
  <img class="avatar" src="/assets/images/mario.JPG" alt="Mario Jimenez Illesca">
  <div>
    <h1 style="margin:0;">Mario Jimenez Illesca</h1>
    <p style="margin:4px 0 0 0;">Full-stack software engineer building production-ready applications, frontend systems, and data-heavy product interfaces.</p>
    <p style="margin:4px 0 0 0;">Interested in product engineering, AI workflows, and fintech tools with real-world users and operational depth.</p>
    <p style="margin:4px 0 0 0;">
      <a href="mailto:mariojillesca@gmail.com">mariojillesca@gmail.com</a> · 
      <a href="https://github.com/nochinxx">GitHub</a> · 
      <a href="https://www.linkedin.com/in/mario-jimenez-7b9683206/">LinkedIn</a> · 
      <a href="/blog/">Blog</a>
    </p>
  </div>
</div>

## Featured Systems

<p class="section-note">
These are my strongest current systems projects: work that combines product thinking, technical architecture, and real-world workflows.
</p>

<div class="grid card-grid">
  {% for project in featured_projects %}
    <div class="project-card featured-card">
      <div class="media-frame">
        {% if project.image %}
          <img class="card-media card-media--{{ project.key }}" src="{{ project.image | relative_url }}" alt="{{ project.title }}">
        {% else %}
          <div class="media-placeholder">{{ project.placeholder }}</div>
        {% endif %}
      </div>

      <h3>
        {% if project.project_url %}
          <a href="{{ project.project_url | relative_url }}">{{ project.title }}</a>
        {% else %}
          {{ project.title }}
        {% endif %}
      </h3>

      <p class="card-description">{{ project.summary }}</p>

      <div class="tag-row">
        {% for tag in project.tags %}
          <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>

      <p class="card-links">
        {% if project.live_url %}<a href="{{ project.live_url }}">Live</a>{% endif %}
        {% if project.github_url %}<a href="{{ project.github_url }}">GitHub</a>{% endif %}
        {% if project.article_url %}<a href="{{ project.article_url | relative_url }}">{{ project.article_label }}</a>{% endif %}
      </p>
    </div>
  {% endfor %}
</div>

## Skills

TypeScript/JavaScript, React/Next.js, Firebase/Firestore, Python, Java, C++, Git, AI prototyping, dashboard-style product interfaces.

## Projects

<p class="section-note">
Broader shipped work, open-source contributions, and earlier projects that still show range across product, UI, and engineering foundations.
</p>

<div class="grid card-grid">
  {% for project in regular_projects %}
    <div class="project-card">
      {% if project.project_url %}
        <h3><a href="{{ project.project_url | relative_url }}">{{ project.title }}</a></h3>
      {% else %}
        <h3>{{ project.title }}</h3>
      {% endif %}

      <p class="card-description">{{ project.summary }}</p>

      <div class="tag-row">
        {% for tag in project.tags %}
          <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>

      <p class="card-links">
        {% if project.live_url %}<a href="{{ project.live_url }}">Live</a>{% endif %}
        {% if project.github_url %}<a href="{{ project.github_url }}">GitHub</a>{% endif %}
        {% if project.article_url %}<a href="{{ project.article_url | relative_url }}">{{ project.article_label }}</a>{% endif %}
      </p>
    </div>
  {% endfor %}
</div>

## Writing

<div class="grid card-grid">
  {% for item in writing %}
    <div class="project-card">
      <p class="card-date">{{ item.date }}</p>
      <h3>
        {% if item.internal_url %}
          <a href="{{ item.internal_url | relative_url }}">{{ item.title }}</a>
        {% else %}
          {{ item.title }}
        {% endif %}
      </h3>
      <p class="card-description">{{ item.summary }}</p>

      <div class="tag-row">
        {% for tag in item.tags %}
          <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>

      <p class="card-links">
        {% if item.internal_url %}<a href="{{ item.internal_url | relative_url }}">Read</a>{% endif %}
      </p>
    </div>
  {% endfor %}
</div>

## Experience

**Software Developer (Contract) — Dayton Financial** (April 2025 – June 2025)  
Designed and deployed a production-ready quoting platform replacing spreadsheet-based workflows.  
Built real-time dashboards, role-based access, and collaborative spreadsheet-style interfaces under tight delivery timelines.  
_Stack: Next.js, TypeScript, React, Firebase, TanStack Table._

**Software Intern — Boyd Lighting** (June 2025 – August 2025)  
Built internal web tools to upload, organize, and manage large datasets with authenticated access for internal teams.  
Collaborated with engineers on documentation, code review, and tooling improvements; supported testing and deployment.

**Coding Teacher — Marin Horizon Middle School** (September 2025 – Present)  
Designed and delivered a programming curriculum, translating technical concepts for a non-technical audience and iterating on UX based on direct feedback.

**Tutor — Computer Science, Mathematics & Statistics** (2023 – Present)  
Tutored undergraduates and high-schoolers in Python, statistics, and algorithms.

**Intern — University of California, Merced** (July 2024 – August 2024)  
Built Python-based data visualizations and educational tools using real-world scientific datasets through the CalTeach program.  
Worked on research-oriented technical material with an education focus.
