---
layout: post
title: "How Five AI Agents Disagreed, and Why That Was the Point"
date: 2026-04-05
permalink: /posts/five-ai-agents-disagreed/
---

<p>
  As a CS student, I wanted to test whether the same system architectures we use in software engineering could be applied to investment research with real rigor.
</p>

<p>
  Orchestrators. Parallel workers. Evaluation and critique loops. Same underlying patterns, different domain.
</p>

<p>
  So, using Perplexity Computer, I built a 12-agent system to pitch a stock.
</p>

<p>
  Five agents. One question:<br>
  What did ELV’s stock do on January 28th, 2026?
</p>

<p>
  The answers ranged from -6.7% to +5.9%. The correct answer was +5.86% close-to-close. Two agents got the direction wrong.
</p>

<p>
  That disagreement was not a failure. It is exactly what the system is designed to surface.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> The Problem with Single-Agent Research </h2>

<p>
  Most people use AI like a faster Google: one prompt, one answer, move on.
</p>

<p>
  The issue is structural.
</p>

<p>
  Language models are probabilistic. The same prompt can produce different outputs because each run samples from a distribution over possible tokens. That is usually fine for casual use. But in financial research, it is dangerous.
</p>

<p>
  A wrong number does not stay isolated. It propagates into your model, into your peer comparisons, and into your price target. By the time you notice, the entire thesis can be built on a faulty assumption.
</p>

<p>
  With a single agent, you get one sample. With multiple independent agents, you get a distribution of answers, and the variance tells you exactly where uncertainty exists.
</p>

<p>
  There is a second issue too: narrow framing. One agent, or one analyst, tends to reinforce its own assumptions. Contradictory evidence often never shows up because it was never searched for in the first place.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> The Architecture </h2>

<p>
  I built a six-stage pipeline with 12+ agents. Each stage has a specific job, and outputs are gated before moving to the next stage.
</p>

<p>
  At a high level:<br>
  Strategy → Hypothesis Generation → Verification → Modeling → Critique → Output
</p>

<p>
  Under the hood, each stage is powered by multiple specialized agents.
</p>

<img class="rounded-lg shadow-lg" src="/assets/images/multi-agent/workflow.png" alt="Multi-agent investment research workflow">

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Multi-Agent Investment Research Pipeline </h2>

<ol class="list-decimal ml-6">
  <li>
    <b>Strategy (Orchestrator)</b><br>
    Defines the research plan and key questions.
  </li>
  <li>
    <b>Hypothesis Generation (Parallel Agents)</b><br>
    Multiple agents explore different explanations for the stock in parallel: macro, narrative, behavioral, and structural. The goal here is not agreement. It is coverage.
  </li>
  <li>
    <b>Truth Verification (Ensemble System)</b><br>
    Five independent runs cross-check 26 discrete facts. When agents agree, confidence increases. When they disagree, it triggers an investigation. Every conflict is resolved using primary sources such as SEC filings, transcripts, or raw market data. This is where the system becomes reliable.
  </li>
  <li>
    <b>Financial Modeling (Quant Layer)</b><br>
    DCF, SOTP, and structural analysis translate insights into valuation.
  </li>
  <li>
    <b>Adversarial Critique (Red Team)</b><br>
    Specialized agents are designed to challenge the thesis, not validate it. They look for flawed assumptions, missing risks, and overstated claims.
  </li>
  <li>
    <b>Output (Product)</b><br>
    The final result is compiled into an interactive thesis app.
  </li>
</ol>

<p>
  Under the hood, the system behaves like a directed pipeline. Each phase produces structured output that must be reviewed before the next stage begins.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> What the System Found </h2>

<p>
  The company is Elevance Health (formerly Anthem), ticker ELV.
</p>

<p>
  The mispricing is specific: the market is treating ELV like a pure-play Medicare Advantage company during a regulatory pressure cycle. But that framing is incomplete.
</p>

<p>
  A significant portion of ELV’s business comes from Carelon, its health services platform, which has been growing rapidly and now represents a substantial share of total revenue. This segment is less visible in the headline narrative, but it changes how the business should be evaluated.
</p>

<p>
  Two insights that emerged from the multi-agent process:
</p>

<ol class="list-decimal ml-6">
  <li>
    <b>DCF back-solve.</b> One of the agents produced a precise estimate of the negative long-term growth implied by the current price. That number could not be cleanly verified. Which is exactly the point. Without a verification layer, that figure would have made it into the thesis as fact. Instead, it was flagged, investigated, and reduced to a directional conclusion: at current prices, the market is effectively pricing in little to no long-term growth.
  </li>
  <li>
    <b>FIDE-SNP positioning advantage.</b> ELV’s Medicaid footprint across multiple states gives it stronger access to fully integrated dual-eligible plans. While competitors like Humana and Centene participate in dual-eligible programs, ELV appears better positioned to integrate Medicaid and Medicare services at scale. This creates a structural advantage that is not immediately visible in standard peer comparisons.
  </li>
</ol>

<p>
  Finding these insights was not the hard part. Making sure they were actually true was.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> What the Critic Layer Caught </h2>

<p>
  The thesis underwent multiple rounds of adversarial review before publication. These were not superficial checks. They found real issues.
</p>

<ul class="list-disc ml-6">
  <li>The Bear Analyst pointed out that I treated key risks as independent. They were actually correlated.</li>
  <li>A CMS rate timeline error was corrected using primary sources.</li>
  <li>The claim about Humana’s exclusion from FIDE-SNPs was too strong and was revised.</li>
  <li>Settlement figures were verified against DOJ releases.</li>
</ul>

<p>
  The system did not just generate ideas. It forced corrections.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> The Lesson </h2>

<p>
  The most valuable thing about multi-agent systems is not that they produce answers. It is that they disagree.
</p>

<p>
  A single agent gives you an output. Multiple agents give you a distribution, visible uncertainty, and clear signals on where to investigate.
</p>

<p>
  The real work happens in resolving those disagreements using primary sources.
</p>

<p>
  The system is built around a simple assumption: the first answer is a hypothesis, not a conclusion.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Explore the Work </h2>

<ul class="list-disc ml-6">
  <li><a href="https://www.perplexity.ai/computer/a/elv-investment-thesis-stock-pi-hLArTzcNRfaEotogjuAjfQ">Open the ELV thesis app</a></li>
  <li><a href="/projects/multi-agent-investment-research/">View the full project page</a></li>
  <li><a href="https://www.linkedin.com/pulse/how-five-ai-agents-disagreed-why-point-mario-jimenez-illesca-igibc/">Read the original LinkedIn article</a></li>
</ul>
