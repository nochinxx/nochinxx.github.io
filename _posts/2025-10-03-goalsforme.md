---
layout: post
title: "goalsforme.com"
date: 2025-10-03
tags: [ai, development, apps, webapps, selfhelp]
permalink: /projects/goalsforme/
---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Overview </h2>

**goalsforme.com** is a full-stack web app I built to help users set, track, and share personal goals in an intelligent and structured way.  
It combines **AI-assisted planning**, **habit tracking**, and **collaboration tools** — designed to act as a “personal progress system” rather than just a to-do list.

Technically, the app is powered by **Next.js (React)** on the frontend, **Firebase** for authentication and data persistence, and **Firestore** as a real-time database.  
The system uses **AI prompting pipelines** (Gemini 2.5 Flash) to expand short user goal inputs into structured projects, tasks, and due dates automatically.

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Architecture & Features </h2>

<ul class="list-disc ml-6">
  <li><b>AI Goal Planner</b> — Parses natural-language goals (e.g. “write my research paper by Nov 1”) into JSON trees of projects and tasks.  
      Uses Gemini’s structured output to assign deadlines, subtasks, and priorities dynamically.</li>

  <li><b>AI Integration Pipeline</b> — Back-end routes build contextual prompts including current date and goal metadata before passing them to Gemini for schedule planning.</li>

  <li><b>Serverless Deployment</b> — Hosted on <b>Vercel</b>; leverages edge-functions for API routes and Firebase for real-time sync.</li>

  <li><b>Habit Engine</b> — Every day there is a habit card that logs progress and generate completion analytics.  
      Uses Firestore timestamps and Pacific Time utilities to record streaks.</li>

  <li><b>Dashboard & Visualization</b> — Unified dashboard displays both personal and shared goals.  
      Includes filters, project progress bars, and due-dates.</li>

  <li><b>Shared Goals & Collaboration</b> — Currently implementing a modular “shared” space where users can invite others via email (Resend API + Firebase Admin).  
      New users can accept invitations even before registering, making it ideal for clubs or teams.</li>

</ul>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Technical Stack </h2>

- **Frontend:** Next.js (App Router), React, TailwindCSS  
- **Backend:** Firebase Auth + Firestore (modular collections for goals, projects, tasks, habits)  
- **AI Integration:** Gemini 2.5 Flash for structured goal planning  
- **Email Infrastructure:** Resend API for invite & notification delivery  
- **Hosting:** Vercel 
- **Languages:** TypeScript, JavaScript  

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Skills </h2>

- Full-stack TypeScript development with React & Firebase  
- Real-time data modeling and Firestore security rules  
- Serverless API design and environment management on Vercel  
- AI prompt engineering and JSON schema validation  
- Authentication, invite flows, and transactional email (Resend API)  
- Modular architecture planning for scalable features (shared goals, habits, AI pipelines)

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Coming up </h2>
<ul class="list-disc ml-6">
<li>Email invite & shared goal infrastructure  </li>
<li>Integrate cross-user dashboards and AI-assisted team planning </li>
<li>Implement analytics dashboard: habit streaks, project progress forecasting </li>
</ul>

---

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2"> Reflection </h2>

Building *goalsforme.com* has been a great experience in **production-ready full-stack web development.** To find the balance in database design, UX, and AI-driven automation has been super fun.  
The project demonstrates how large-scale personal productivity tools can be built using modern frameworks with minimal infrastructure, and it continues to evolve as I refine the collaborative and AI components.

The best part is that I use it everyday, and I am happy to have a few users who like it.


