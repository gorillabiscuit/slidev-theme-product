---
theme: ./
title: "slidev-theme-product — examples"
colorSchema: light
transition: fade
lineNumbers: false
fonts:
  sans: Inter
  weights: '400,500,600,700'
  provider: google
layout: intro-image-right
image: https://images.unsplash.com/photo-1486325212027-8081e485255e?w=1200&q=80
---

# Product Name

One-line value proposition.

<div style="margin-top:48px; font-size:13px; color:#86868b">Company · Date</div>

---
layout: section
---

## Chapter title.

---
layout: fact
---

## 98.2%

The headline number. One per slide. Let it breathe.

<div class="source-line">Source · Year · Grade</div>

---
layout: default
---

<div class="eyebrow">Context</div>

## Why this. Why now.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:80px; margin-top:32px">

<div>
<div style="font-size:var(--product-body); color:var(--product-ink)">
  Left column content. Keep each item to one line. Use opacity to
  dim secondary items.
</div>
</div>

<div>
<div style="font-size:var(--product-body); color:var(--product-ink)">
  Right column content. The gap between columns does the work —
  no dividers needed.
</div>
</div>

</div>

---
layout: two-cols
---

<div class="eyebrow">For</div>

<div v-click style="padding:10px 0; font-size:15px; line-height:1.3">First benefit — revealed on click</div>
<div v-click style="padding:10px 0; font-size:15px; line-height:1.3">Second benefit</div>
<div v-click style="padding:10px 0; font-size:15px; line-height:1.3">Third benefit</div>

::right::

<div class="eyebrow">Against</div>

<div v-click style="padding:10px 0; font-size:15px; line-height:1.3">First concern — revealed on click</div>
<div v-click style="padding:10px 0; font-size:15px; line-height:1.3">Second concern</div>

---
layout: default
---

<!--
  BAR CHART SLIDE
  Bar colours: --product-blue, --product-green, --product-gray, --product-red
  Use ONE colour per chart. Mix only when data is semantically different.
  Set max-width inline. bar-grow animation fires on slide entry.
-->

<div class="eyebrow mt-8">Comparison</div>

<div style="margin-top:32px; display:flex; flex-direction:column; gap:12px">

<div class="bar-row">
  <div class="bar-label" style="width:180px">Label A</div>
  <div class="bar-track" style="height:36px">
    <div class="bar" style="max-width:75%; background:var(--product-blue)">75%</div>
  </div>
  <div class="bar-note">Source · Grade B</div>
</div>

<div class="bar-row">
  <div class="bar-label" style="width:180px">Label B</div>
  <div class="bar-track" style="height:36px">
    <div class="bar" style="max-width:52%; background:var(--product-gray)">52%</div>
  </div>
  <div class="bar-note">Benchmark</div>
</div>

</div>

<div class="source-line">Data source · Year</div>

---
layout: statement
---

## We recommend<br><span class="text-accent">the thing.</span>

One supporting sentence. Short. Confident.

---
layout: section
---

## Sources.

N items · evidence grades A through D

---
layout: default
---

<div class="eyebrow mt-2">All sources by evidence grade</div>
<div style="font-size:12px; color:var(--product-muted); margin-bottom:16px">Grade A and B = primary evidence · C and D = context only</div>

<div style="display:grid; grid-template-columns:1fr 1fr; gap:40px">
<div>
  <div style="font-size:11px; font-weight:600; color:var(--product-accent); margin-bottom:6px">Grade A — Peer-reviewed academic</div>
  <div style="font-size:11px; color:var(--product-muted); line-height:1.6">
    Author et al. — Title, Year<br>
    Author et al. — Title, Year
  </div>
  <div style="font-size:11px; font-weight:600; color:var(--product-accent); margin:14px 0 6px">Grade B — Credible industry body</div>
  <div style="font-size:11px; color:var(--product-muted); line-height:1.6">
    Organisation — Report Name Year<br>
    Organisation — Report Name Year
  </div>
</div>
<div>
  <div style="font-size:11px; font-weight:600; color:var(--product-accent); margin-bottom:6px">Grade C — Operator / provider marketing</div>
  <div style="font-size:11px; color:var(--product-muted); line-height:1.6">
    Company — Publication Year
  </div>
  <div style="font-size:11px; font-weight:600; color:var(--product-accent); margin:14px 0 6px">Grade D — Anecdotal</div>
  <div style="font-size:11px; color:var(--product-muted); line-height:1.6">
    Source — Description
  </div>
  <div style="margin-top:16px; padding-top:14px; border-top:1px solid rgba(0,0,0,0.08); font-size:11px; color:var(--product-muted)">Full dataset available on request.</div>
</div>
</div>
