---
layout: page
permalink: /gamedevbench/
title: GameDevBench
description: "Evaluating Agentic Capabilities Through Game Development"
nav: false
nav_order: 100
---

<style>
  /* Override page layout for wider content */
  .post {
    max-width: 980px;
    margin: 0 auto;
  }
  .post-header {
    display: none;
  }

  /* Hero Section */
  .gdb-hero {
    text-align: center;
    padding: 30px 0 10px;
  }
  .gdb-hero h1 {
    font-size: 2.8em;
    font-weight: 800;
    margin-bottom: 10px;
    line-height: 1.2;
    letter-spacing: -0.5px;
    color: var(--global-text-color);
  }
  .gdb-hero .subtitle {
    font-size: 1.1em;
    color: var(--global-text-color-light);
    margin-bottom: 12px;
    font-weight: 400;
    letter-spacing: 0.2px;
  }
  .gdb-hero .venue {
    font-size: 1.0em;
    margin-bottom: 24px;
    letter-spacing: 0.5px;
  }

  /* Stats strip */
  .gdb-stats {
    display: flex;
    justify-content: center;
    gap: 0;
    flex-wrap: wrap;
    border: 1px solid #d8d8d8;
    margin-bottom: 48px;
  }
  .gdb-stat {
    flex: 1 1 140px;
    text-align: center;
    padding: 18px 10px;
    border-right: 1px solid #e4e4e4;
  }
  .gdb-stat:last-child {
    border-right: none;
  }
  .gdb-stat .num {
    font-size: 1.6em;
    font-weight: 800;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    color: var(--global-text-color);
    line-height: 1.2;
  }
  .gdb-stat .label {
    font-size: 0.72em;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: var(--global-text-color-light);
    margin-top: 4px;
  }
  html[data-theme='dark'] .gdb-stats {
    border-color: #3a3a3a;
  }
  html[data-theme='dark'] .gdb-stat {
    border-right-color: #2e2e2e;
  }

  /* Author List */
  .gdb-authors {
    text-align: center;
    margin-bottom: 8px;
    font-size: 1.05em;
    line-height: 1.8;
  }
  .gdb-authors a {
    text-decoration: none;
    color: inherit;
  }
  .gdb-authors a:hover {
    text-decoration: underline;
  }
  .gdb-authors sup {
    font-size: 0.7em;
    margin-left: 1px;
  }
  .gdb-affiliations {
    text-align: center;
    color: var(--global-text-color-light);
    font-size: 0.9em;
    margin-bottom: 28px;
  }

  /* Buttons */
  .gdb-buttons {
    text-align: center;
    margin-bottom: 40px;
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
  }
  .gdb-btn {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 9px 22px;
    border-radius: 3px;
    font-size: 0.88em;
    font-weight: 600;
    text-decoration: none !important;
    transition: opacity 0.15s ease;
    border: 1px solid;
    letter-spacing: 0.3px;
    text-transform: uppercase;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
  }
  .gdb-btn-primary {
    background: var(--global-text-color);
    color: var(--global-bg-color) !important;
    border-color: var(--global-text-color);
  }
  .gdb-btn-primary:hover {
    opacity: 0.75;
  }
  .gdb-btn-outline {
    background: transparent;
    color: var(--global-text-color) !important;
    border-color: #b0b0b0;
  }
  .gdb-btn-outline:hover {
    border-color: var(--global-text-color);
    opacity: 0.75;
  }

  /* Section Styling */
  .gdb-section {
    margin-bottom: 48px;
  }
  .gdb-section h2 {
    font-size: 0.78em;
    font-weight: 700;
    margin-bottom: 20px;
    padding-bottom: 10px;
    text-transform: uppercase;
    letter-spacing: 1.5px;
    color: var(--global-text-color);
    border-bottom: 1px solid #d0d0d0;
    display: block;
  }

  /* Abstract */
  .gdb-abstract {
    font-size: 1.05em;
    line-height: 1.8;
    text-align: justify;
  }
  .gdb-abstract p {
    margin-bottom: 12px;
  }

  /* TL;DR finding cards */
  .gdb-tldr-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
  }
  @media (max-width: 640px) {
    .gdb-tldr-grid { grid-template-columns: 1fr; }
  }
  .gdb-card {
    border: 1px solid #d8d8d8;
    padding: 20px 22px 18px;
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  .gdb-card .card-title {
    font-size: 0.72em;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1.2px;
    color: var(--global-text-color-light);
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .gdb-card .card-title i {
    font-size: 1.15em;
    color: var(--global-text-color);
  }
  .gdb-card .card-text {
    font-size: 0.9em;
    line-height: 1.6;
    color: var(--global-text-color);
    margin: 0;
  }
  .gdb-card .big-num {
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    font-size: 2.6em;
    font-weight: 800;
    line-height: 1.1;
    color: var(--global-text-color);
  }
  .gdb-card .big-num .sub {
    font-size: 0.32em;
    font-weight: 600;
    color: var(--global-text-color-light);
    text-transform: uppercase;
    letter-spacing: 1px;
    display: block;
    margin-top: 2px;
  }
  /* segmented distribution bar */
  .gdb-seg-bar {
    display: flex;
    height: 14px;
    border-radius: 2px;
    overflow: hidden;
  }
  .gdb-seg-legend {
    display: flex;
    flex-wrap: wrap;
    gap: 6px 14px;
    font-size: 0.74em;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    color: var(--global-text-color-light);
  }
  .gdb-seg-legend span {
    display: inline-flex;
    align-items: center;
    gap: 5px;
  }
  .gdb-seg-legend .sw {
    width: 9px;
    height: 9px;
    border-radius: 2px;
    display: inline-block;
  }
  /* mini bar rows */
  .gdb-mini-row {
    display: grid;
    grid-template-columns: 78px 1fr 44px;
    align-items: center;
    gap: 8px;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    font-size: 0.76em;
  }
  .gdb-mini-row .lbl { color: var(--global-text-color-light); white-space: nowrap; }
  .gdb-mini-row .val { text-align: right; font-weight: 700; color: var(--global-text-color); }
  .gdb-mini-track {
    height: 10px;
    background: #f4f4f4;
    border-radius: 2px;
    position: relative;
  }
  .gdb-mini-fill {
    position: absolute;
    left: 0; top: 0; height: 100%;
    border-radius: 2px;
  }
  /* before/after arrow */
  .gdb-lift {
    display: flex;
    align-items: baseline;
    gap: 12px;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
  }
  .gdb-lift .from {
    font-size: 1.7em;
    font-weight: 600;
    color: var(--global-text-color-light);
    text-decoration: line-through;
    text-decoration-thickness: 2px;
    text-decoration-color: #c0392b88;
  }
  .gdb-lift .arrow { font-size: 1.3em; color: var(--global-text-color-light); }
  .gdb-lift .to {
    font-size: 2.3em;
    font-weight: 800;
    color: #1a9e5c;
  }
  .gdb-lift .delta {
    font-size: 0.84em;
    font-weight: 700;
    color: #1a9e5c;
    background: rgba(26,158,92,0.1);
    padding: 3px 8px;
    border-radius: 3px;
  }
  html[data-theme='dark'] .gdb-card { border-color: #3a3a3a; }
  html[data-theme='dark'] .gdb-mini-track { background: #242424; }

  /* Teaser */
  .gdb-teaser img {
    width: 100%;
    border: 1px solid #e0e0e0;
  }
  .gdb-teaser .caption {
    font-size: 0.82em;
    color: var(--global-text-color-light);
    text-align: center;
    margin-top: 8px;
    letter-spacing: 0.1px;
  }

  /* Example image */
  .gdb-example-img {
    width: 100%;
    border: 1px solid #e0e0e0;
  }

  /* Leaderboard bar chart */
  .gdb-leaderboard-section {
    width: min(960px, calc(100vw - 48px));
    margin-left: 50%;
    transform: translateX(-50%);
  }
  .gdb-chart {
    border: 1px solid #d8d8d8;
    background: var(--global-bg-color, #fff);
    padding: 18px 22px 12px;
  }
  .gdb-bar-row {
    display: grid;
    grid-template-columns: minmax(280px, 370px) minmax(240px, 1fr) 118px;
    align-items: center;
    gap: 14px;
    padding: 9px 0;
    border-bottom: 1px solid #efefef;
  }
  .gdb-bar-row.new {
    margin: 0 -8px;
    padding: 9px 8px;
    background: rgba(15, 118, 110, 0.06);
    border-left: 3px solid #0f766e;
  }
  .gdb-bar-row:last-of-type {
    border-bottom: none;
  }
  .gdb-bar-label {
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    font-size: 0.8em;
    font-weight: 600;
    color: var(--global-text-color);
    display: flex;
    align-items: center;
    gap: 8px;
    white-space: nowrap;
    overflow: hidden;
    min-width: 0;
  }
  .gdb-bar-label .logo {
    width: 16px;
    height: 16px;
    flex-shrink: 0;
  }
  .gdb-rank {
    width: 1.5em;
    flex-shrink: 0;
    text-align: right;
    color: var(--global-text-color-light);
    font-weight: 700;
  }
  .gdb-model-name {
    min-width: 0;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .gdb-bar-label .harness {
    font-weight: 400;
    color: var(--global-text-color-light);
    font-size: 0.88em;
  }
  .gdb-new-badge {
    flex-shrink: 0;
    border: 1px solid rgba(15, 118, 110, 0.35);
    background: rgba(15, 118, 110, 0.1);
    color: #0f766e;
    border-radius: 3px;
    padding: 1px 5px;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    font-size: 0.68em;
    font-weight: 700;
    text-transform: uppercase;
  }
  .gdb-bar-track {
    position: relative;
    height: 16px;
    background: #f4f4f4;
    border-radius: 2px;
  }
  .gdb-bar-fill {
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    border-radius: 2px;
  }
  .gdb-bar-err {
    position: absolute;
    top: 50%;
    height: 1.5px;
    background: rgba(0,0,0,0.65);
    transform: translateY(-50%);
  }
  .gdb-bar-err::before,
  .gdb-bar-err::after {
    content: "";
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 1.5px;
    height: 9px;
    background: rgba(0,0,0,0.65);
  }
  .gdb-bar-err::before { left: 0; }
  .gdb-bar-err::after { right: 0; }
  .gdb-bar-score {
    text-align: right;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    font-size: 0.86em;
    font-weight: 700;
    color: var(--global-text-color);
    white-space: nowrap;
  }
  .gdb-bar-score .ci {
    font-weight: 400;
    color: var(--global-text-color-light);
    font-size: 0.88em;
  }
  .gdb-axis {
    display: grid;
    grid-template-columns: minmax(280px, 370px) minmax(240px, 1fr) 118px;
    gap: 14px;
    padding-top: 8px;
  }
  .gdb-axis-scale {
    position: relative;
    height: 16px;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    font-size: 0.7em;
    color: var(--global-text-color-light);
  }
  .gdb-axis-scale span {
    position: absolute;
    transform: translateX(-50%);
  }
  @media (max-width: 640px) {
    .gdb-leaderboard-section {
      width: calc(100vw - 30px);
    }
    .gdb-chart {
      padding: 14px 14px 12px;
    }
    .gdb-bar-row {
      grid-template-columns: minmax(0, 1fr) auto;
      gap: 7px 10px;
      padding: 10px 0;
    }
    .gdb-bar-row.new {
      margin: 0 -6px;
      padding: 10px 6px;
    }
    .gdb-bar-label {
      grid-column: 1;
      grid-row: 1;
    }
    .gdb-bar-track {
      grid-column: 1 / -1;
      grid-row: 2;
    }
    .gdb-bar-score {
      grid-column: 2;
      grid-row: 1;
      font-size: 0.82em;
    }
    .gdb-axis {
      display: block;
      padding-top: 8px;
    }
    .gdb-axis > div:first-child,
    .gdb-axis > div:last-child {
      display: none;
    }
    .gdb-axis-scale span:nth-child(2),
    .gdb-axis-scale span:nth-child(4) {
      display: none;
    }
    .gdb-bar-label .harness { display: none; }
  }

  /* BibTeX */
  .gdb-bibtex {
    position: relative;
  }
  .gdb-bibtex pre {
    background: #f4f4f4;
    border: 1px solid #d8d8d8;
    border-radius: 0;
    padding: 24px;
    font-size: 0.84em;
    overflow-x: auto;
    line-height: 1.6;
  }
  .gdb-bibtex .copy-btn {
    position: absolute;
    top: 12px;
    right: 12px;
    background: var(--global-text-color);
    color: var(--global-bg-color);
    border: none;
    border-radius: 2px;
    padding: 5px 13px;
    font-size: 0.76em;
    font-weight: 600;
    cursor: pointer;
    transition: opacity 0.15s;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    letter-spacing: 0.3px;
    text-transform: uppercase;
  }
  .gdb-bibtex .copy-btn:hover {
    opacity: 0.7;
  }

  /* Dark mode */
  html[data-theme='dark'] .gdb-chart {
    border-color: #3a3a3a;
  }
  html[data-theme='dark'] .gdb-bar-row {
    border-bottom-color: #282828;
  }
  html[data-theme='dark'] .gdb-bar-row.new {
    background: rgba(20, 184, 166, 0.1);
    border-left-color: #14b8a6;
  }
  html[data-theme='dark'] .gdb-new-badge {
    border-color: rgba(20, 184, 166, 0.45);
    background: rgba(20, 184, 166, 0.14);
    color: #5eead4;
  }
  html[data-theme='dark'] .gdb-bar-track {
    background: #242424;
  }
  html[data-theme='dark'] .gdb-bar-err,
  html[data-theme='dark'] .gdb-bar-err::before,
  html[data-theme='dark'] .gdb-bar-err::after {
    background: rgba(255,255,255,0.75);
  }
  html[data-theme='dark'] .gdb-section h2 {
    border-bottom-color: #3a3a3a;
  }
  html[data-theme='dark'] .gdb-bibtex pre {
    background: #1c1c1c;
    border-color: #3a3a3a;
  }
  html[data-theme='dark'] .gdb-teaser img,
  html[data-theme='dark'] .gdb-example-img {
    border-color: #3a3a3a;
  }
</style>

<!-- Hero -->
<div class="gdb-hero">
  <h1>GameDevBench</h1>
  <p class="subtitle">Evaluating Agentic Capabilities Through Game Development</p>
  <p class="venue"><strong>ICML 2026</strong></p>
</div>

<!-- Authors -->
<div class="gdb-authors">
  <a href="https://waynchi.github.io/">Wayne Chi</a><sup>1</sup>,
  <a href="https://kigb.github.io/">Yixiong Fang</a><sup>1</sup>,
  Arnav Yayavaram<sup>1</sup>,
  Siddharth Yayavaram<sup>1</sup>,
  <a href="https://sethkarten.ai/">Seth Karten</a><sup>2</sup>,
  <a href="https://qiuhongannawei.me/">Qiuhong Anna Wei</a><sup>1</sup>,
  Runkun Chen<sup>1</sup>,
  Alexander Wang<sup>1</sup>,
  <a href="https://valeriechen.github.io/">Valerie Chen</a><sup>1</sup>,
  <a href="https://www.cs.cmu.edu/~atalwalk/">Ameet Talwalkar</a><sup>1</sup>,
  <a href="https://chrisdonahue.com/">Chris Donahue</a><sup>1</sup>
</div>
<div class="gdb-affiliations">
  <sup>1</sup>Carnegie Mellon University &nbsp;&nbsp; <sup>2</sup>Princeton University
</div>

<!-- Buttons -->
<div class="gdb-buttons">
  <a href="https://arxiv.org/abs/2602.11103" class="gdb-btn gdb-btn-primary" target="_blank">
    <i class="fas fa-file-pdf"></i> Paper
  </a>
  <a href="https://github.com/waynchi/gamedevbench" class="gdb-btn gdb-btn-outline" target="_blank">
    <i class="fab fa-github"></i> Code
  </a>
</div>

<!-- Leaderboard -->
<div class="gdb-section gdb-leaderboard-section">
  <h2 id="leaderboard">Leaderboard</h2>
  <div class="gdb-chart">
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">1</span><img class="logo" src="/assets/img/logos/anthropic.svg" alt="anthropic"><span class="gdb-model-name">claude-fable-5 (xhigh)</span><span class="harness">[Claude Code]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:67.3%;background:#d97757;"></div>
        <div class="gdb-bar-err" style="left:62.2%;width:10.1%;"></div>
      </div>
      <div class="gdb-bar-score">67.3% <span class="ci">±5.0</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">2</span><img class="logo" src="/assets/img/logos/openai.svg" alt="openai"><span class="gdb-model-name">gpt-5.6-sol (xhigh)</span><span class="harness">[Codex]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:63.7%;background:#10a37f;"></div>
        <div class="gdb-bar-err" style="left:58.5%;width:10.3%;"></div>
      </div>
      <div class="gdb-bar-score">63.7% <span class="ci">±5.2</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">3</span><img class="logo" src="/assets/img/logos/openai.svg" alt="openai"><span class="gdb-model-name">gpt-5.6-sol (high)</span><span class="harness">[Codex]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:63.1%;background:#10a37f;"></div>
        <div class="gdb-bar-err" style="left:57.9%;width:10.4%;"></div>
      </div>
      <div class="gdb-bar-score">63.1% <span class="ci">±5.2</span></div>
    </div>
    <div class="gdb-bar-row new">
      <div class="gdb-bar-label"><span class="gdb-rank">4</span><img class="logo" src="/assets/img/logos/meta.svg" alt="meta"><span class="gdb-model-name">muse-spark-1.2 [high]</span><span class="harness">[Muse Code]</span><span class="gdb-new-badge">New</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:63.1%;background:#0668e1;"></div>
        <div class="gdb-bar-err" style="left:57.9%;width:10.4%;"></div>
      </div>
      <div class="gdb-bar-score">63.1% <span class="ci">±5.2</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">5</span><img class="logo" src="/assets/img/logos/openai.svg" alt="openai"><span class="gdb-model-name">gpt-5.6-sol (medium)</span><span class="harness">[Codex]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:58.6%;background:#10a37f;"></div>
        <div class="gdb-bar-err" style="left:53.3%;width:10.6%;"></div>
      </div>
      <div class="gdb-bar-score">58.6% <span class="ci">±5.3</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">6</span><img class="logo" src="/assets/img/logos/moonshot.svg" alt="moonshot"><span class="gdb-model-name">kimi-k3</span><span class="harness">[Kimi Code]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:58.0%;background:#cf3e3e;"></div>
        <div class="gdb-bar-err" style="left:52.7%;width:10.6%;"></div>
      </div>
      <div class="gdb-bar-score">58.0% <span class="ci">±5.3</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">7</span><img class="logo" src="/assets/img/logos/anthropic.svg" alt="anthropic"><span class="gdb-model-name">claude-opus-4-8</span><span class="harness">[Claude Code]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:55.9%;background:#d97757;"></div>
        <div class="gdb-bar-err" style="left:50.6%;width:10.6%;"></div>
      </div>
      <div class="gdb-bar-score">55.9% <span class="ci">±5.3</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">8</span><img class="logo" src="/assets/img/logos/openai.svg" alt="openai"><span class="gdb-model-name">gpt-5.5</span><span class="harness">[Codex]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:54.7%;background:#10a37f;"></div>
        <div class="gdb-bar-err" style="left:49.4%;width:10.6%;"></div>
      </div>
      <div class="gdb-bar-score">54.7% <span class="ci">±5.3</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">9</span><img class="logo" src="/assets/img/logos/gemini.svg" alt="gemini">gemini-3-pro-preview&nbsp;<span class="harness">[Gemini CLI]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:53.8%;background:#4285f4;"></div>
        <div class="gdb-bar-err" style="left:48.4%;width:10.8%;"></div>
      </div>
      <div class="gdb-bar-score">53.8% <span class="ci">±5.4</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">10</span><img class="logo" src="/assets/img/logos/openai.svg" alt="openai">gpt-5.4&nbsp;<span class="harness">[Codex]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:52.0%;background:#10a37f;"></div>
        <div class="gdb-bar-err" style="left:46.6%;width:10.8%;"></div>
      </div>
      <div class="gdb-bar-score">52.0% <span class="ci">±5.4</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">11</span><img class="logo" src="/assets/img/logos/gemini.svg" alt="gemini">gemini-3-flash-preview&nbsp;<span class="harness">[Gemini CLI]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:46.8%;background:#4285f4;"></div>
        <div class="gdb-bar-err" style="left:41.4%;width:10.8%;"></div>
      </div>
      <div class="gdb-bar-score">46.8% <span class="ci">±5.4</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">12</span><img class="logo" src="/assets/img/logos/openai.svg" alt="openai">gpt-5.4-mini&nbsp;<span class="harness">[Codex]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:43.2%;background:#10a37f;"></div>
        <div class="gdb-bar-err" style="left:37.9%;width:10.6%;"></div>
      </div>
      <div class="gdb-bar-score">43.2% <span class="ci">±5.3</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">13</span><img class="logo" src="/assets/img/logos/zai.svg" alt="Z.ai"><span class="gdb-model-name">glm-5.2</span><span class="harness">[OpenCode]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:38.4%;background:#0f766e;"></div>
        <div class="gdb-bar-err" style="left:33.2%;width:10.4%;"></div>
      </div>
      <div class="gdb-bar-score">38.4% <span class="ci">±5.2</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">14</span><img class="logo" src="/assets/img/logos/anthropic.svg" alt="anthropic">claude-sonnet-4-5&nbsp;<span class="harness">[Claude Code]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:34.8%;background:#d97757;"></div>
        <div class="gdb-bar-err" style="left:29.7%;width:10.2%;"></div>
      </div>
      <div class="gdb-bar-score">34.8% <span class="ci">±5.1</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">15</span><img class="logo" src="/assets/img/logos/moonshot.svg" alt="moonshot">kimi-k2.5&nbsp;<span class="harness">[OpenHands]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:20.7%;background:#cf3e3e;"></div>
        <div class="gdb-bar-err" style="left:16.3%;width:8.8%;"></div>
      </div>
      <div class="gdb-bar-score">20.7% <span class="ci">±4.4</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">16</span><img class="logo" src="/assets/img/logos/anthropic.svg" alt="anthropic">claude-haiku-4-5&nbsp;<span class="harness">[Claude Code]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:18.6%;background:#d97757;"></div>
        <div class="gdb-bar-err" style="left:14.4%;width:8.4%;"></div>
      </div>
      <div class="gdb-bar-score">18.6% <span class="ci">±4.2</span></div>
    </div>
    <div class="gdb-bar-row">
      <div class="gdb-bar-label"><span class="gdb-rank">17</span><img class="logo" src="/assets/img/logos/qwen.svg" alt="qwen">qwen3.5-397b&nbsp;<span class="harness">[OpenHands]</span></div>
      <div class="gdb-bar-track">
        <div class="gdb-bar-fill" style="width:5.4%;background:#7952b3;"></div>
        <div class="gdb-bar-err" style="left:3.0%;width:4.8%;"></div>
      </div>
      <div class="gdb-bar-score">5.4% <span class="ci">±2.4</span></div>
    </div>
    <div class="gdb-axis">
      <div></div>
      <div class="gdb-axis-scale">
        <span style="left:0;transform:none;">0%</span>
        <span style="left:25%;">25%</span>
        <span style="left:50%;">50%</span>
        <span style="left:75%;">75%</span>
        <span style="right:0;transform:none;">100%</span>
      </div>
      <div></div>
    </div>
  </div>
  <p style="font-size: 0.83em; color: var(--global-text-color-light); margin-top: 10px;">
    * <code>pass@1</code> (%) on all 333 tasks &mdash; best multimodal feedback configuration per model, in its best harness (ICML 2026 camera-ready results). Error bars are 95% confidence intervals.
  </p>
</div>

<!-- Stats strip -->
<div class="gdb-stats">
  <div class="gdb-stat">
    <div class="num">333</div>
    <div class="label">Tasks</div>
  </div>
  <div class="gdb-stat">
    <div class="num">88</div>
    <div class="label">Tutorials</div>
  </div>
  <div class="gdb-stat">
    <div class="num">4</div>
    <div class="label">Skill Categories</div>
  </div>
  <div class="gdb-stat">
    <div class="num">63.7%</div>
    <div class="label">Best Agent Score</div>
  </div>
</div>

<!-- TL;DR -->
<div class="gdb-section">
  <h2>TL;DR</h2>
  <div class="gdb-tldr-grid">

    <div class="gdb-card">
      <div class="card-title"><i class="fas fa-gamepad"></i> The first game-dev benchmark for agents</div>
      <div class="gdb-seg-bar">
        <div style="width:33.3%;background:#4285f4;"></div>
        <div style="width:26.7%;background:#10a37f;"></div>
        <div style="width:20.1%;background:#d97757;"></div>
        <div style="width:19.8%;background:#7952b3;"></div>
      </div>
      <div class="gdb-seg-legend">
        <span><span class="sw" style="background:#4285f4;"></span>2D Graphics 33%</span>
        <span><span class="sw" style="background:#10a37f;"></span>3D Graphics 27%</span>
        <span><span class="sw" style="background:#d97757;"></span>UI 20%</span>
        <span><span class="sw" style="background:#7952b3;"></span>Gameplay 20%</span>
      </div>
      <p class="card-text">333 real tasks in the Godot engine &mdash; shaders, sprites, animations, and scenes, not just code.</p>
    </div>

    <div class="gdb-card">
      <div class="card-title"><i class="fas fa-triangle-exclamation"></i> Agents struggle</div>
      <div class="big-num">63.7%<span class="sub">best agent score</span></div>
      <p class="card-text">Even the strongest agent fails nearly half the benchmark.</p>
    </div>

    <div class="gdb-card">
      <div class="card-title"><i class="fas fa-eye"></i> Multimodality is the bottleneck</div>
      <div style="display:flex;flex-direction:column;gap:7px;">
        <div class="gdb-mini-row"><span class="lbl">Gameplay</span><div class="gdb-mini-track"><div class="gdb-mini-fill" style="width:51.4%;background:#1a9e5c;"></div></div><span class="val">51.4%</span></div>
        <div class="gdb-mini-row"><span class="lbl">3D Graphics</span><div class="gdb-mini-track"><div class="gdb-mini-fill" style="width:38.4%;background:#e8a33d;"></div></div><span class="val">38.4%</span></div>
        <div class="gdb-mini-row"><span class="lbl">2D Graphics</span><div class="gdb-mini-track"><div class="gdb-mini-fill" style="width:33.0%;background:#c0392b;"></div></div><span class="val">33.0%</span></div>
        <div class="gdb-mini-row"><span class="lbl">UI</span><div class="gdb-mini-track"><div class="gdb-mini-fill" style="width:32.0%;background:#c0392b;"></div></div><span class="val">32.0%</span></div>
      </div>
      <p class="card-text">The more visual understanding a task demands, the more agents fail.</p>
    </div>

    <div class="gdb-card">
      <div class="card-title"><i class="fas fa-video"></i> Visual feedback works</div>
      <div class="gdb-lift">
        <span class="from">41.1%</span>
        <span class="arrow">&rarr;</span>
        <span class="to">52.0%</span>
        <span class="delta">+10.9</span>
      </div>
      <p class="card-text">Letting agents see screenshots and gameplay video consistently boosts performance (GPT-5.4 shown).</p>
    </div>

  </div>
</div>

<!-- Example Case -->
<div class="gdb-section">
  <h2>Example Task</h2>
  <p style="margin-bottom: 16px; line-height: 1.7;">
    In this example, the goal is to populate an empty 3D scene with a water depth visualization, including environment lighting, shader-driven water plane, background spheres, and a camera.
    This is a <strong>3D graphics and animations</strong> task that focuses on the <strong>scene editor</strong>. The figure shows both the editor-based and code-based solution approaches.
  </p>
  <img class="gdb-example-img" src="/assets/img/gamedevbench-3d-example.png" alt="GameDevBench 3D example: water depth visualization task showing editor and code solutions">
</div>

<!-- BibTeX -->
<div class="gdb-section">
  <h2>Citation</h2>
  <div class="gdb-bibtex">
    <button class="copy-btn" onclick="navigator.clipboard.writeText(document.getElementById('bibtex-text').innerText)">
      <i class="fas fa-copy"></i> Copy
    </button>
    <pre><code id="bibtex-text">@inproceedings{chi2026gamedevbenchevaluatingagenticcapabilities,
      title={GameDevBench: Evaluating Agentic Capabilities Through Game Development},
      author={Wayne Chi and Yixiong Fang and Arnav Yayavaram and Siddharth Yayavaram and Seth Karten and Qiuhong Anna Wei and Runkun Chen and Alexander Wang and Valerie Chen and Ameet Talwalkar and Chris Donahue},
      booktitle={International Conference on Machine Learning (ICML)},
      year={2026},
      eprint={2602.11103},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2602.11103},
}</code></pre>
  </div>
</div>
