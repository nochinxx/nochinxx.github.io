---
layout: post
title: "Dayton Financial RFQ Tool"
date: 2025-06-20
permalink: /projects/dayton-sheets/
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

Built for Dayton Financial, this production quoting platform replaced spreadsheet-based RFQ workflows with a structured multi-user system for buyers and sellers.  

The product centered on data-heavy dashboards, spreadsheet-style editing, role-based access, and real-time collaboration across shared quote workflows. The result was a faster operational process with less manual reconciliation and clearer system visibility for internal users.

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Screenshots & Demo </h2>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
  <img class="rounded-lg shadow-lg" src="/assets/images/dayton/spreadsheet.png" alt="Original Spreadsheet">
  <img class="rounded-lg shadow-lg" src="/assets/images/dayton/webapp.png" alt="Dayton Webapp">
</div>

<div class="flex flex-col md:flex-row gap-6 mb-8">
  <div class="flex-1">
    <video
      class="rounded-lg shadow-lg w-full"
      controls
      muted
      loop
      playsinline
      preload="metadata"
      poster="/assets/images/dayton/webapp.png">
      <source src="/assets/videos/dayton/demo.mp4" type="video/mp4">
      <source src="/assets/videos/dayton/demo.mov" type="video/quicktime">
      Your browser does not support the video tag.
    </video>
    <p class="mt-2 text-sm text-slate-600">
      If the embedded video does not play in your browser, <a href="/assets/videos/dayton/demo.mp4">open the MP4 directly</a>.
    </p>
  </div>
  <div class="flex-1 flex flex-col justify-center">
    <h3 class="text-l font-semibold mb-2">Private/Internal build</h3>
    <p class="mb-2">
      The platform translated a laborious spreadsheet process into a purpose-built quoting system with shared state, cleaner permissions, and more reliable operations.
    </p>
    <p>
      Sellers could update quotes directly, buyers could review aggregated views, and the system kept everyone working from the same data model instead of separate sheets.
    </p>
  </div>
</div>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Tech Stack </h2>

<div class="flex flex-wrap gap-2">
  <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Next.js</span>
  <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">TypeScript</span>
  <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">React</span>
  <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Firebase</span>
  <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">Firestore</span>
  <span class="bg-indigo-100 text-indigo-800 px-3 py-1 rounded-full text-sm">TanStack Table</span>
</div>

<p class="mt-6 text-sm text-slate-600">
  Public screenshots are available here, but the full product and repository are private/internal.
</p>
