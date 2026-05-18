---
layout: post
title: "SwiPR / PRs on Edge"
date: 2026-05-09
permalink: /projects/prs-on-edge-swipr/
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

SwiPR / PRs on Edge captures two iterations of the same core idea: using AI to make pull request review faster, safer, and more context-aware.

SwiPR started as context infrastructure for the merge decision. PRs on Edge later focused on the interface layer, using generative UI to decide how PR review should look on mobile and edge devices.

<img class="rounded-lg shadow-lg mt-6 mb-8" src="/assets/images/projects/swipr-review.png" alt="SwiPR review screen">

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Two Iterations </h2>

<ul class="list-disc ml-6">
  <li><b>SwiPR</b> explored retrieval and memory for PR review using vector search over repo and pull request context.</li>
  <li><b>PRs on Edge</b> focused on the interface layer: dynamically rendering SwipeStack, RiskMatrix, or ContributorFocus depending on repository state.</li>
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
  <li><b>Dynamic view selection</b> — switches between SwipeStack, RiskMatrix, or ContributorFocus based on queue shape and repository state.</li>
  <li><b>Inline risk scoring</b> — scores PRs using diff size, changed files, and sensitive path heuristics without requiring a separate ML model.</li>
  <li><b>Queue classification</b> — groups pull requests by type, age, contributor concentration, and dependency chains before rendering.</li>
  <li><b>Generative UI focus</b> — the main output is not a static dashboard or plain chat answer, but an interface the agent chooses at runtime.</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Stack </h2>

Across both iterations: Next.js, React, TypeScript, GitHub API integrations, CopilotKit, vector retrieval patterns, and runtime interface selection.

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Explore the Work </h2>

<p>
  <a href="https://github.com/nochinxx/SwiPR">Open the SwiPR repo</a> ·
  <a href="https://github.com/nochinxx/PRs-on-edge">Open the PRs on Edge repo</a> ·
  <a href="/posts/prs-on-edge/">Read the article version</a>
</p>
