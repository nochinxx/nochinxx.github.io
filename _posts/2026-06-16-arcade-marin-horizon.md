---
layout: post
title: "Building an Arcade Cabinet at Marin Horizon School"
date: 2026-06-16
permalink: /posts/arcade-marin-horizon/
tags: [raspberry-pi, pygame, hardware, education]
---

<p>
  This past semester I built a full arcade cabinet from scratch for the students at Marin Horizon School. It runs on a Raspberry Pi, uses Pygame for the game layer, and has a custom control panel with arcade buttons wired directly to the GPIO pins. The whole thing is self-contained — plug it in and it boots straight into the game menu.
</p>

<p>
  I had a great time building it. Hardware and software meeting in one box is a different kind of satisfaction than shipping a web app. Every bug has a physical symptom.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2">Why an Arcade Cabinet</h2>

<p>
  Marin Horizon is a school that values hands-on learning. The idea was to build something the students could actually play — something tangible that made the underlying technology visible. A Raspberry Pi hidden inside a cabinet that plays games is a much better introduction to embedded systems than a slide deck.
</p>

<p>
  Kids would walk up, play a game, and then ask: how does this work? That question is the whole point.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2">How It Was Built</h2>

<p>
  The stack is deliberately minimal. A Raspberry Pi 4 runs a lightweight Linux image. Pygame handles the display and input loop. Arcade buttons connect through the GPIO pins — each button maps to a keyboard event so the game layer doesn't need to know anything about hardware.
</p>

<ul class="list-disc ml-6 mb-6">
  <li><b>Compute:</b> Raspberry Pi 4 — boots straight to the game menu via a systemd service</li>
  <li><b>Display:</b> HDMI monitor mounted inside the cabinet frame</li>
  <li><b>Controls:</b> Arcade joystick + buttons wired to GPIO via a USB encoder board</li>
  <li><b>Software:</b> Pygame game loop, custom menu system, config files for adding new games</li>
  <li><b>Cabinet:</b> Custom-built frame — cut, assembled, and painted by hand</li>
</ul>

<p>
  The hardest part was the physical build — cutting the cabinet to the right dimensions, routing the wiring cleanly, and making sure the screen mount was solid enough that students couldn't rattle it loose. Software bugs are easier to fix than a crooked monitor.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2">What I Learned</h2>

<p>
  Building for a school is different from building for the internet. There is no error page. There is no retry button. If the cabinet crashes during recess, that is the whole experience.
</p>

<p>
  That constraint forced good engineering: clean boot sequences, graceful error recovery, a config system that doesn't require a terminal to update. The final version boots in under 20 seconds and has run without a restart for the remainder of the semester.
</p>

<p>
  It also reminded me that the best products are the ones that disappear into their context. The students don't think about Raspberry Pi or GPIO. They think about the game. Getting out of the way is the hardest design decision.
</p>

<h2 class="text-2xl font-bold mt-8 mb-4 border-b-2 border-indigo-200 pb-2">The Semester</h2>

<p>
  This was a semester-long project alongside coursework. I designed it, sourced the parts, built the cabinet, wrote the software, and installed it at the school. It is still running there.
</p>

<p>
  If you want to build something similar, I am happy to share the parts list and config. Message me at mariojillesca@gmail.com.
</p>
