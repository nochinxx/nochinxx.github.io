---
layout: post
title: "Plotly.py contribution"
date: 2026-05-17
permalink: /projects/plotly-py-contribution/
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Tech Stack </h2>

<div class="tag-row">
  <span class="tag">Python</span>
  <span class="tag">Plotly.py</span>
  <span class="tag">Open source</span>
  <span class="tag">Debugging</span>
  <span class="tag">Data visualization</span>
</div>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

This contribution focused on a real bug inside Plotly.py’s autoshape helpers: labeled vertical lines on datetime axes could crash because the library tried to compute annotation placement with arithmetic that did not generalize beyond numeric coordinates.

The deeper architectural issue was that Plotly.py was manually building annotations for shapes even though Plotly.js already supports labels natively through <code>shape.label</code>. Moving toward that path makes the behavior more robust, more consistent across axis types, and less dependent on fragile placement logic.

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Focus </h2>

<ul class="list-disc ml-6">
  <li>Reproducing the datetime-axis crash triggered by <code>add_vline(x="2020-09-24", annotation_text="Test")</code>.</li>
  <li>Tracing the call path through Plotly.py’s autoshape helpers and internal annotation logic.</li>
  <li>Refactoring labeled shapes toward <code>shape.label</code> instead of manual annotation placement.</li>
  <li>Preserving compatibility while preparing the code and tests for a cleaner long-term migration.</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> What I Changed </h2>

<ul class="list-disc ml-6">
  <li>Worked on the issue around refactoring <code>add_vline()</code>, <code>add_hline()</code>, <code>add_vrect()</code>, and <code>add_hrect()</code> to use Plotly.js <code>shape.label</code>.</li>
  <li>Built a compatibility helper to map legacy <code>annotation_*</code> kwargs into shape label fields safely.</li>
  <li>Updated the internal autoshape processing path so labeled vertical lines no longer crash on datetime axes.</li>
  <li>Opened a draft PR while the codebase remained in a transition phase between legacy annotations and native labels.</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Why it matters </h2>

This work was valuable not just because of one bug fix, but because it touched the boundary between Plotly.py and Plotly.js. It was a good example of how wrapper libraries can drift into duplicated abstractions, and how aligning them back to the underlying platform can remove subtle user-facing failures.

<p>
  <a href="https://github.com/plotly/plotly.py">Plotly.py repository</a> ·
  <a href="/posts/plotly-py-contribution-notes/">Related article</a>
</p>
