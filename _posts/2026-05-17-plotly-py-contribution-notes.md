---
layout: post
title: "Plotly.py contribution notes"
date: 2026-01-20
permalink: /posts/plotly-py-contribution-notes/
---

<p>
  Plotly.py is an open-source Python library for creating interactive browser-based visualizations. Because it wraps Plotly.js, users can build high-quality charts in Python without needing to touch JavaScript directly.
</p>

<p>
  My contribution focused on a bug and refactor path around labeled autoshapes, especially <code>add_vline()</code> on datetime axes.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> The Issue </h2>

<p>
  Historically, Plotly.py created two separate objects whenever a user added a labeled line or rectangle:
</p>

<ol class="list-decimal ml-6">
  <li>a shape</li>
  <li>an annotation</li>
</ol>

<p>
  That worked until users plotted datetime data and called <code>add_vline(x="2020-09-24", annotation_text="Test")</code>. The old code tried to compute the mean of x-coordinates to decide where to place the annotation, but dates cannot be averaged with integers, which caused a hard crash.
</p>

<p>
  The real issue was architectural. Plotly.py was duplicating annotation behavior that Plotly.js already supports natively through <code>shape.label</code>.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Why I Started With add_vline() </h2>

<p>
  I intentionally started with <code>add_vline()</code> because the datetime-axis crash was easiest to reproduce there. That made it the best entry point for validating whether the move to <code>shape.label</code> actually fixed the real user-facing failure mode.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> What I Learned from Debugging </h2>

<p>
  The old approach:
</p>

<ul class="list-disc ml-6">
  <li>computed averages and min/max values over user coordinates</li>
  <li>built annotations manually</li>
  <li>did not account cleanly for datetimes or mixed data types</li>
  <li>duplicated logic that Plotly.js already handled correctly</li>
</ul>

<p>
  By shifting toward <code>shape.label</code>, that fragile arithmetic disappears. The label becomes part of the shape, and Plotly.js handles placement more consistently across axis types.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Progress </h2>

<ul class="list-disc ml-6">
  <li>Built <code>_coerceshape_label_from_legacy_annotation_kwargs</code> to map legacy annotation args into label fields.</li>
  <li>Updated <code>_process_multiple_axis_spanning_shapes()</code> so <code>add_vline()</code> can produce a single labeled shape.</li>
  <li>Validated that the datetime-axis crash no longer occurs.</li>
  <li>Pushed the work to a shared branch and opened a draft PR.</li>
  <li>Outlined the next test and refactor targets for <code>add_hline()</code>, <code>add_vrect()</code>, and <code>add_hrect()</code>.</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Why it mattered </h2>

<p>
  This contribution helped me understand how architectural decisions inside large libraries can create subtle but real failures for users. It also reinforced the importance of aligning abstractions across language boundaries when working on wrapper libraries like Plotly.py.
</p>

<p>
  <a href="/projects/plotly-py-contribution/">Related project</a> ·
  <a href="https://github.com/plotly/plotly.py">Plotly.py repository</a> ·
  <a href="https://www.linkedin.com/pulse/fixing-plot-labels-plotlypy-how-i-improved-addvline-using-jimenez-p78rc/">Original LinkedIn article</a>
</p>
