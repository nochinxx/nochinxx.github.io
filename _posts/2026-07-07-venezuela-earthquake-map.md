---
layout: post
title: "Venezuela Earthquake Map"
date: 2026-07-07
permalink: /projects/venezuela-earthquake-map/
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Tech Stack </h2>

<div class="tag-row">
  <span class="tag">Next.js 15</span>
  <span class="tag">Mapbox GL JS</span>
  <span class="tag">Supabase + PostGIS</span>
  <span class="tag">Python scrapers</span>
  <span class="tag">Playwright</span>
  <span class="tag">Whisper</span>
  <span class="tag">Gemma 3 (local)</span>
  <span class="tag">Vercel</span>
</div>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

On June 24, 2026, a **M7.2 earthquake struck near Yumare, Venezuela**. Within hours, official channels were overwhelmed and families had no reliable way to find damage reports, shelter locations, or missing persons information.

I built a real-time damage map the same day — aggregating reports from YouTube, X/Twitter, and Instagram every 10 minutes and plotting them on an interactive heatmap. The app reached **4,000+ people** in the days following the earthquake.

<a href="https://sismovenezuela.com">sismovenezuela.com</a>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> What it does </h2>

<ul class="list-disc ml-6">
  <li><strong>Damage heatmap</strong> — weighted by report credibility and damage severity, updated every 10 minutes</li>
  <li><strong>Drill-down reports</strong> — click any zone to see the underlying videos, tweets, and posts that generated the signal</li>
  <li><strong>Relief centers</strong> — verified centros de acopio with addresses and accepted items</li>
  <li><strong>Missing persons</strong> — community-submitted reports plotted on the map</li>
  <li><strong>Emergency directory</strong> — 30+ Caracas hospitals, ambulances, bomberos, and rescue teams</li>
  <li><strong>USGS PAGER</strong> — live fatality projection pulled from official seismic data</li>
</ul>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Data pipeline </h2>

The system ran three parallel scraper processes on a local Mac Mini, each on a 10-minute interval:

<ul class="list-disc ml-6">
  <li><strong>YouTube</strong> — 6 search queries, auto-subtitles with Whisper fallback for Spanish transcription</li>
  <li><strong>X/Twitter</strong> — 13 Playwright searches including verified accounts (convzlacomando, MariaCorinaYA)</li>
  <li><strong>Instagram</strong> — 5 hashtags via saved session</li>
  <li><strong>Geo-extraction</strong> — Gemma 3 4b running locally via Ollama to extract location references from Spanish text, zero API cost</li>
  <li><strong>PostGIS</strong> — geospatial queries for clustering and heatmap generation</li>
</ul>

The architecture was deliberately built to run without cloud compute costs during the acute phase — everything ran on a Mac Mini with local inference.

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Why I built it </h2>

Venezuela is where I'm from. When the earthquake hit, the information fragmentation was immediate — reports scattered across WhatsApp groups, YouTube livestreams, and Twitter threads with no unified picture of where damage was worst or where relief was going.

The tools I had — Mapbox, Supabase PostGIS, Python scrapers, local LLM inference — were exactly what was needed to build a real signal out of that noise. So I built it.

This project is an example of what I think software can do at its best: respond to a real crisis with real infrastructure, fast enough to matter.

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Impact </h2>

<ul class="list-disc ml-6">
  <li>4,000+ page views in the days following the earthquake</li>
  <li>Used by families searching for missing persons and damage information</li>
  <li>Relief center data surfaced donation drop-off points across Caracas</li>
</ul>

<p class="mt-6">
  <a href="https://sismovenezuela.com">Live site</a> ·
  <a href="https://github.com/nochinxx/venezuela-earthquake-map">GitHub</a>
</p>
