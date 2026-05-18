---
layout: post
title: "Multi-Agent Investment Research System"
date: 2026-04-05
permalink: /projects/multi-agent-investment-research/
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Tech Stack </h2>

<div class="tag-row">
  <span class="tag">Perplexity Computer</span>
  <span class="tag">Multi-agent orchestration</span>
  <span class="tag">Financial modeling</span>
  <span class="tag">Verification workflows</span>
  <span class="tag">Interactive thesis app</span>
</div>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

This project treats investment research as a systems problem rather than a single-prompt exercise. I built a multi-agent pipeline that generates competing hypotheses, checks factual claims across multiple runs, escalates disagreements for review, and compiles the result into an interactive thesis app.

The core idea is simple: in high-stakes research, disagreement is useful if the system is built to surface it, measure it, and resolve it against primary sources.

<img class="rounded-lg shadow-lg mt-6 mb-8" src="/assets/images/multi-agent/workflow.png" alt="Multi-agent investment research workflow">

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Workflow </h2>

<ul class="list-disc ml-6">
  <li><b>Strategy</b> — the orchestrator defines the research plan, screening criteria, and key questions.</li>
  <li><b>Hypothesis generation</b> — parallel agents explore macro, narrative, behavioral, and structural explanations for the stock.</li>
  <li><b>Truth verification</b> — five independent runs cross-check 26 facts, escalating disagreements into primary-source review.</li>
  <li><b>Financial modeling</b> — DCF, SOTP, and structural analysis translate validated findings into valuation work.</li>
  <li><b>Adversarial critique</b> — specialized critics challenge assumptions, pressure-test risks, and force revisions.</li>
  <li><b>Output</b> — the final thesis is delivered as an interactive app instead of a static memo.</li>
</ul>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Thesis outcome </h2>

The ELV thesis centered on a specific misclassification: the market was treating Elevance Health like a pure-play Medicare Advantage company and underweighting the role of Carelon, its fast-growing health services platform.

The more important result was how the system handled uncertainty. A precise DCF back-solve estimate was flagged because it could not be verified cleanly, and a structural FIDE-SNP positioning edge only stayed in the thesis after primary-source review.

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Why it matters </h2>

Most AI research tools optimize for speed and confidence. This system optimizes for coverage, visible uncertainty, and correction loops. That makes it more aligned with how rigorous analytical work should behave.

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Explore the Work </h2>

<ul class="list-disc ml-6">
  <li><a href="https://www.perplexity.ai/computer/a/elv-investment-thesis-stock-pi-hLArTzcNRfaEotogjuAjfQ">Open the ELV thesis app</a></li>
  <li><a href="https://www.perplexity.ai/computer/a/elv-agentworkflow-ai-investme-s5iPgti3TG2sQ3ipZqsnXQ">Open the interactive agent workflow</a></li>
  <li><a href="/posts/five-ai-agents-disagreed/">Read the article version</a></li>
</ul>
