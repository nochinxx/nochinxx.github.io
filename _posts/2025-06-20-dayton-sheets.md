---
layout: post
title: "Building Dayton Sheets — RFQ Tool"
date: 2025-06-20
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

We built a multi-tenant RFQ and quoting platform featuring buyer/seller dashboards, role-based access, spreadsheet UI, seller magic links, batch updates, and buyer aggregation views.  

This replaced a messy workflow in Google Sheets and saved thousands in operational costs.

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Screenshots & Demo </h2>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
  <img class="rounded-lg shadow-lg" src="/assets/images/dayton/spreadsheet.png" alt="Original Spreadsheet">
  <img class="rounded-lg shadow-lg" src="/assets/images/dayton/webapp.png" alt="Dayton Webapp">
</div>

<div class="flex flex-col md:flex-row gap-6 mb-8">
  <video class="rounded-lg shadow-lg flex-1" controls autoplay muted loop>
  <source src="/assets/images/dayton/demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
    </video>
  <div class="flex-1 flex flex-col justify-center">
    <h3 class="text-l font-semibold mb-2">Dayton Sheets</h3>
    <p class="mb-2">
      We converted their laborious process from entering seller data in a buyer sheet into a streamlined full-stack web app.
    </p>
    <p>
      The vision was to have a master sheet with products where sellers could enter quotes and updates would sync in real-time. Private sheets, master sheet aggregation, and live dashboards made it all possible.
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


