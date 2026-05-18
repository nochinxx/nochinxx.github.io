---
layout: post
title: "SwiPR / PRs on Edge"
date: 2026-05-09
permalink: /projects/prs-on-edge-swipr/
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Tech Stack </h2>

<div class="tag-row">
  <span class="tag">Next.js</span>
  <span class="tag">React</span>
  <span class="tag">TypeScript</span>
  <span class="tag">CopilotKit</span>
  <span class="tag">GitHub API</span>
  <span class="tag">Generative UI</span>
  <span class="tag">pgvector</span>
</div>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

SwiPR / PRs on Edge captures two iterations of the same core idea: using AI to make pull request review faster, safer, and more context-aware.

SwiPR started as context infrastructure for the merge decision. PRs on Edge later focused on the interface layer, using generative UI to decide how PR review should look on mobile and edge devices.

<img class="rounded-lg shadow-lg mt-6 mb-8" src="/assets/images/projects/swipr-review.png" alt="SwiPR review screen">

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Two Iterations </h2>

<ul class="list-disc ml-6">
  <li><b>SwiPR</b> explored retrieval and memory for PR review using vector search over repo and pull request context.</li>
  <li><b>PRs on Edge</b> focused on the interface layer: dynamically rendering SwipeStack, RiskMatrix, ContributorFocus, DependencyGraph, or CategoryGroup depending on repository state.</li>
  <li>Together, they explore the same core question: how can AI make PR review faster, safer, and more context-aware?</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> SwiPR </h2>

<ul class="list-disc ml-6">
  <li><b>Swipe review UI</b> — a card-based interface for triaging open-source pull requests quickly.</li>
  <li><b>AI context panel</b> — surfaces risk score, contributor history, similar past changes, and PR summaries alongside the diff.</li>
  <li><b>Repo memory</b> — stores and embeds PR and file context so both humans and agents can retrieve related changes later.</li>
  <li><b>MCP server</b> — exposes the same PR context layer to Claude Desktop, Cursor, and other MCP-compatible clients.</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> PRs on Edge </h2>

<ul class="list-disc ml-6">
  <li><b>Dynamic view selection</b> — switches between SwipeStack, RiskMatrix, ContributorFocus, DependencyGraph, or CategoryGroup based on queue shape and repository state.</li>
  <li><b>Inline risk scoring</b> — scores PRs using diff size, changed files, and sensitive path heuristics without requiring a separate ML model.</li>
  <li><b>Queue classification</b> — groups pull requests by type, age, contributor concentration, and dependency chains before rendering.</li>
  <li><b>Generative UI focus</b> — the main output is not a static dashboard or plain chat answer, but an interface the agent chooses at runtime.</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Interface Modes </h2>

<p><b>Swipe</b> — a card-by-card review surface for fast triage when the queue is still small enough for direct approve, skip, or inspect actions.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-swipe.png" alt="PRs on Edge swipe mode">

<p><b>Risk Matrix</b> — a severity-oriented view that groups pull requests by runtime risk so the reviewer can attack the highest-signal items first.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-risk-matrix.png" alt="PRs on Edge risk matrix mode">

<p><b>Contributor Focus</b> — a grouped view for author-heavy queues, useful when one contributor or one team owns a large share of open work.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-contributor-focus.png" alt="PRs on Edge contributor focus mode">

<p><b>Dependency Graph</b> — a structure-aware view that surfaces merge ordering and cross-references so related pull requests do not get merged out of sequence.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-dependency-graph.png" alt="PRs on Edge dependency graph mode">

<p><b>Category Group</b> — a batching view that clusters pull requests into feature, testing, maintenance, and similar classes to reduce queue noise.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-category-group.png" alt="PRs on Edge category group mode">

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Explore the Work </h2>

<p>
  <a href="https://github.com/nochinxx/SwiPR">Open the SwiPR repo</a> ·
  <a href="https://github.com/nochinxx/PRs-on-edge">Open the PRs on Edge repo</a> ·
  <a href="/posts/prs-on-edge/">Read the article version</a>
</p>
