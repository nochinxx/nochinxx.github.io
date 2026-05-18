---
layout: post
title: "PRs on Edge"
date: 2026-05-09
permalink: /posts/prs-on-edge/
---

<p>
  PRs on Edge is a generative UI agent that reads your open GitHub pull requests and dynamically renders the right interface for the moment: a swipe stack, a risk matrix, a contributor-focused view, a dependency graph, or a category-grouped board.
</p>

<p>
  There is no fixed dashboard to configure. The agent analyzes repository state and decides what to show, how to show it, and in what priority order.
</p>

<p>
  This is not a chatbot wrapped in a UI. It is a copilot that ships, rendering interactive components inline so you can confirm, tweak, and execute actions directly from a handheld or edge device.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> The Problem </h2>

<p>
  Pull request reviews are still stuck on desktop dashboards. Engineers context-switch between their IDE, GitHub, Slack, and email just to stay on top of open PRs. Reviews pile up, blockers go unnoticed, and high-risk changes get buried in routine noise.
</p>

<p>
  Existing tools give you a list. PRs on Edge tries to give you a decision interface.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> What We Built </h2>

<p>
  The agent reads your open PRs and chooses one of five generative views based on what it finds.
</p>

<ul class="list-disc ml-6">
  <li><b>SwipeStack</b> — used when there are fewer than 10 open PRs, enabling card-by-card review with approve, reject, or skip actions.</li>
  <li><b>RiskMatrix</b> — used when many high-risk PRs are detected, surfacing a color-coded grid sorted by risk.</li>
  <li><b>ContributorFocus</b> — used when one or two authors dominate the queue, grouping PRs by contributor and merge history.</li>
  <li><b>DependencyGraph</b> — used when merge order or linked pull requests matter more than raw queue length.</li>
  <li><b>CategoryGroup</b> — used when the fastest way to reduce noise is clustering PRs by feature, testing, maintenance, and similar classes.</li>
</ul>

<p>
  The user can still ask the agent to switch views or drill into a specific PR at any time, but the default surface is chosen by the system rather than configured manually.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> The Five Views </h2>

<p><b>SwipeStack</b> is the fastest review mode: one pull request at a time, with explicit approve, skip, or inspect actions.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-swipe.png" alt="PRs on Edge swipe mode">

<p><b>RiskMatrix</b> turns the queue into a severity surface so the reviewer can see whether the real problem is low-risk maintenance or a handful of changes that deserve immediate attention.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-risk-matrix.png" alt="PRs on Edge risk matrix mode">

<p><b>ContributorFocus</b> becomes useful when one contributor or team owns a disproportionate share of open work and the review bottleneck is coordination, not just prioritization.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-contributor-focus.png" alt="PRs on Edge contributor focus mode">

<p><b>DependencyGraph</b> is the structure-aware view: it shows whether PRs are independent or whether merge order matters because changes reference or block one another.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-dependency-graph.png" alt="PRs on Edge dependency graph mode">

<p><b>CategoryGroup</b> is the batching view, grouping PRs by feature, testing, maintenance, and similar patterns so reviewers can process like with like.</p>
<img class="rounded-lg shadow-lg mt-4 mb-8" src="/assets/images/projects/prs-edge-category-group.png" alt="PRs on Edge category group mode">

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Risk Scoring </h2>

<p>
  Every PR is scored from 0 to 100 using a lightweight runtime heuristic based on additions, deletions, number of changed files, and whether sensitive paths such as <code>auth/</code>, <code>billing/</code>, <code>payment/</code>, or <code>schema</code> are touched.
</p>

<ul class="list-disc ml-6">
  <li>Scores above 60 are flagged as high risk.</li>
  <li>Scores from 30 to 60 are treated as medium risk.</li>
  <li>Scores below 30 are treated as lower risk routine changes.</li>
</ul>

<p>
  No external scoring service and no heavy model are required. The point is to make risk visible fast enough to shape the interface in real time.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> PR Classification Parameters </h2>

<p>
  Before rendering any UI, the agent classifies pull requests across four dimensions:
</p>

<ol class="list-decimal ml-6">
  <li><b>Category grouping</b> — bug fix, refactor, maintenance, or new feature.</li>
  <li><b>Dependency graph</b> — identifies blocking chains so reviewers do not merge out of order.</li>
  <li><b>Priority ranking</b> — pushes older and unreviewed PRs upward so they do not disappear into backlog noise.</li>
  <li><b>Release targeting</b> — maps PRs to upcoming release targets and splits them by feature vs bug fix.</li>
</ol>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> GitHub API Surface </h2>

<p>
  The agent relies on a small, focused tool surface:
</p>

<ul class="list-disc ml-6">
  <li><b>get_open_prs</b> — title, author, additions, deletions, changed files, and URL for all open PRs.</li>
  <li><b>get_pr_files</b> — changed files and patch content for a specific PR.</li>
  <li><b>get_contributor_history</b> — recent PR history for a contributor in the same repo.</li>
  <li><b>risk_score</b> — an inline 0–100 score built from size, file count, and sensitive path detection.</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Why This Matters </h2>

<p>
  Most AI tools stop at recommendation text: “you have 12 open PRs” or “this change looks risky.”
</p>

<p>
  PRs on Edge tries to go one step further. The output is not just analysis. It is an interface the user can act on directly: swipe, filter, inspect, approve, or merge. The UI is generated by the agent, not preconfigured by the user.
</p>

<p>
  That is the core idea behind the project: replacing static dashboards with review interfaces that emerge from context.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Explore the Work </h2>

<ul class="list-disc ml-6">
  <li><a href="/projects/prs-on-edge-swipr/">View the full SwiPR / PRs on Edge project page</a></li>
  <li><a href="https://github.com/nochinxx/PRs-on-edge">Open the PRs on Edge repo</a></li>
  <li><a href="https://www.linkedin.com/pulse/prs-edge-mario-jimenez-illesca-tk94c/">Read the original LinkedIn article</a></li>
</ul>
