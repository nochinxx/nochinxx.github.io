---
layout: default
title: Blog
---

<link rel="stylesheet" href="/assets/style.css">

<header class="bg-[#111827] text-white p-6 flex justify-between items-center">
  <div>
    <h1 class="text-3xl font-semibold">All posts</h1>
  </div>
</header>

<main class="p-6">
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
