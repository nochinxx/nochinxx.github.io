---
layout: post
title: "Building Dayton Sheets — RFQ Tool"
date: 2025-06-20
---

<style>
/* Container for each section */
.block {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
  margin-bottom: 32px;
  align-items: flex-start;
}

/* Images/Videos */
.block img, .block video {
  flex: 1 1 300px;
  max-width: 45%;
  border-radius: 12px;
  object-fit: cover;
}

/* Text content */
.block .content {
  flex: 1 1 300px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

/* Optional: badges for tech stack */
.badge {
  display: inline-block;
  background-color: #eef2ff;
  color: #3730a3;
  padding: 2px 8px;
  border-radius: 999px;
  font-size: 0.8rem;
  margin-left: 4px;
  margin-bottom: 4px;
}
</style>

## Overview

We built a multi-tenant RFQ and quoting platform featuring buyer/seller dashboards, 
role-based access, spreadsheet UI, seller magic links, batch updates, and buyer aggregation views.  

This replaced a messy workflow in Google Sheets and saved thousands in operational costs.

## Screenshots & Demo

<div class="block">
  <img src="/assets/images/dayton/spreadsheet.png" alt="Original Spreadsheet">
  <img src="/assets/images/dayton/webapp.png" alt="Dayton Webapp">
</div>

<div class="block">
  <video src="/assets/images/dayton/demo.mov" autoplay muted controls></video>
  <div class="content">
    <h3>Dayton Sheets</h3>
    <p>
      We converted their laborious process from entering seller data in a buyer sheet into a streamlined full-stack web app.
    </p>
    <p>
      The vision was to have a master sheet with products where sellers could enter quotes and updates would sync in real-time. Private sheets, master sheet aggregation, and live dashboards made it all possible.
    </p>
  </div>
</div>

## Tech Stack

Next.js · TypeScript · React · Firebase · Firestore · TanStack Table

