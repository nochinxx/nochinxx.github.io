---
layout: post
title: "TravelClaim AI"
date: 2026-05-17
permalink: /projects/travelclaim-ai/
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

**TravelClaim AI** is a **hackathon prototype** exploring agentic AI workflows for military travel reimbursement. The idea was to let service members describe travel in plain English, ask policy questions against the **Joint Travel Regulations**, auto-fill **DD Form 1351-2**, and validate uploaded receipts before the package reaches finance review.

This was built as a concept prototype rather than a deployed production system. The focus was reducing administrative friction in a workflow that is both high-frequency and regulation-heavy.

<img class="rounded-lg shadow-lg mt-6 mb-8" src="/assets/images/projects/travelclaim-claim-new.png" alt="TravelClaim AI authorization workflow">

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Problem </h2>

Military travel reimbursement is slow and painful because service members have to navigate **JTR rules, DTS, per diem rules, receipts, and DD Form 1351-2** all at once. Even a relatively standard TDY trip can become a long administrative task with multiple failure points before reimbursement is approved.

The opportunity behind TravelClaim AI was not just answering policy questions, but turning that knowledge into concrete workflow actions: structured claim data, form fill, receipt checks, and a cleaner handoff to reviewers.

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Validation </h2>

The team validated the problem through Reddit analysis across military communities. The pitch deck surfaced:

<ul class="list-disc ml-6">
  <li><b>822 posts</b> across military subreddits discussing reimbursement and voucher pain.</li>
  <li><b>9,754 total upvotes</b>, showing that the frustration is widely recognized and shared.</li>
  <li>Repeated complaints around delayed reimbursement, DTS friction, confusing policy interpretation, and waiting weeks or months to get paid back.</li>
</ul>

This mattered because it grounded the prototype in a real administrative pain point rather than a generic “AI assistant” idea.

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> System </h2>

<ul class="list-disc ml-6">
  <li><b>RAG assistant over Joint Travel Regulations</b> — soldiers or reviewers can ask policy questions and get regulation-grounded answers with citations.</li>
  <li><b>Natural-language travel input</b> — conversational travel descriptions get converted into structured claim fields.</li>
  <li><b>DD Form 1351-2 PDF autofill</b> — the system generates a filled voucher preview and PDF rather than leaving users with a blank form.</li>
  <li><b>Receipt upload / vision extraction concept</b> — receipt images can be parsed into structured expense data for review and claim packaging.</li>
  <li><b>Finance NCO review queue concept</b> — the prototype direction included a cleaner downstream review flow for flagged claims.</li>
</ul>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8 mt-6">
  <img class="rounded-lg shadow-lg" src="/assets/images/projects/travelclaim-rag.png" alt="TravelClaim AI regulations retrieval interface">
  <img class="rounded-lg shadow-lg" src="/assets/images/projects/travelclaim-dd1351.png" alt="TravelClaim AI DD Form 1351-2 preview">
</div>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Stack </h2>

- **Prototype stack direction:** Next.js, Tailwind, Supabase, pgvector or ChromaDB, OpenAI embeddings, Claude, pdf-lib or PyMuPDF, Vercel/Railway/Render  
- **Repo implementation:** Next.js, Supabase, pgvector, Gemini, Google Vision OCR, Python PDF filling

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> My Role </h2>

I contributed to the agentic workflow design, product framing, research validation, and technical architecture for the prototype.

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> What I Learned </h2>

<ul class="list-disc ml-6">
  <li>Agentic systems are strongest when they take concrete actions, not just answer questions.</li>
  <li>RAG needs citations and uncertainty handling for regulatory workflows.</li>
  <li>Form automation is valuable when it reduces real administrative pain.</li>
  <li>User research can come from messy public data when handled carefully.</li>
</ul>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Links </h2>

- [Project repository](https://github.com/nochinxx/travelclaimAI)
- [Hackathon pitch deck](/assets/documents/travelclaim-ai-pitch.pdf)
