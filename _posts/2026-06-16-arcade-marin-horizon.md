---
layout: post
title: "Building an Arcade Cabinet at Marin Horizon School"
date: 2026-06-16
permalink: /posts/arcade-marin-horizon/
tags: [raspberry-pi, pygame, hardware, teaching]
---

<p>
  This past semester I taught coding at Marin Horizon Middle School. We started with Scratch and JavaScript with p5.js — visual, immediate, forgiving languages for students who had never written a line of code. By the end of the semester, the class capstone was a full-size arcade cabinet, built by hand and running games the students wrote themselves.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2">The Build</h2>

<p>
  The cabinet runs on a Raspberry Pi Zero 2 W. Students wrote games in Pygame — a 2D sports game was the one that made it onto the machine. We also loaded classic NES ROMs: Super Mario Bros, Tetris, a bike game. The control panel has a red arcade joystick and six buttons, wired through a USB encoder board to GPIO. I soldered the connections by hand.
</p>

<img src="/assets/images/projects/arcade/arcade-soldering.jpeg" alt="Soldering the GPIO controls" style="width:100%;border-radius:8px;margin:16px 0;">

<p>
  The cabinet itself is plywood. A Philips monitor sits inside the frame. It boots straight into the game menu off a systemd service.
</p>

<img src="/assets/images/projects/arcade/arcade-testing-backyard.jpeg" alt="Testing the cabinet during build" style="width:100%;border-radius:8px;margin:16px 0;">

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2">Why This Project</h2>

<p>
  Teaching middle schoolers to code means navigating a gap between what they can imagine and what they can build. Scratch closes that gap fast. p5.js is close to magic for students who care about visuals. But the question that came up every week was: <em>does this connect to something real?</em>
</p>

<p>
  The arcade cabinet was the answer to that question. It is real. You can touch it. The games running on it were written by students in the same room. That connection — between code on a screen and something you can walk up to and play — is what I wanted them to carry out of the semester.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2">What I Learned Teaching</h2>

<p>
  Debugging with a 12-year-old is different from debugging alone. They do not read error messages. They do not google first. They either ask immediately or give up. The job is to slow that cycle down — to make the error message interesting rather than alarming, and to make the fix feel like theirs, not yours.
</p>

<p>
  That constraint made me a better explainer. You cannot hide behind jargon with a middle schooler. If you cannot say it plainly, you do not understand it well enough.
</p>

<img src="/assets/images/projects/arcade/arcade-mario-pointing.jpeg" alt="Running the student Pygame game at school" style="width:100%;border-radius:8px;margin:16px 0;">

<p>
  The machine is at the school.
</p>

<img src="/assets/images/projects/arcade/arcade-cabinet-school.jpeg" alt="The finished cabinet at Marin Horizon" style="width:100%;border-radius:8px;margin:16px 0;">
