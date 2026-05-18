---
layout: default
title: Blog
---

<link rel="stylesheet" href="/assets/style.css">
{% assign writing = site.data.writing %}

<header class="bg-[#111827] text-white p-6 flex justify-between items-center">
  <div>
    <h1 class="text-3xl font-semibold">Blog</h1>
  </div>
</header>

<main class="p-6">
  <p class="section-note">
    Notes, project writeups, and reflections connected to systems, interfaces, AI workflows, and software engineering.
  </p>

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

  <h2>Archive</h2>
  <ul class="space-y-2">
    {% for post in site.posts %}
      <li>
        <a href="{{ post.url }}" class="text-indigo-600 hover:underline">{{ post.title }}</a>
        <small class="text-gray-500">— {{ post.date | date: "%b %d, %Y" }}</small>
      </li>
    {% endfor %}
  </ul>

  <div class="flex justify-between items-center mb-6">
    <a href="/" class="text-white-600 hover:text-indigo-800 font-semibold flex items-center">
      ← Back
    </a>
  </div>
</main>
