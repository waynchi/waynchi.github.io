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

  /* Leaderboard */
  .gdb-leaderboard {
    border: 1px solid #d8d8d8;
    overflow: hidden;
    background: var(--global-bg-color, #fff);
  }
  .gdb-lb-table {
    width: 100%;
    border-collapse: collapse;
  }
  .gdb-lb-table th {
    padding: 9px 16px;
    text-align: left;
    font-weight: 700;
    font-size: 0.72em;
    text-transform: uppercase;
    letter-spacing: 0.8px;
    color: #555;
    border-bottom: 2px solid #d0d0d0;
    border-right: 1px solid #e4e4e4;
    background: #f2f2f2;
    white-space: nowrap;
  }
  .gdb-lb-table th:first-child {
    width: 52px;
    text-align: center;
  }
  .gdb-lb-table th:last-child {
    text-align: right;
    border-right: none;
  }
  .gdb-lb-table td {
    padding: 10px 16px;
    border-bottom: 1px solid #eeeeee;
    border-right: 1px solid #eeeeee;
    font-size: 0.91em;
    font-variant-numeric: tabular-nums;
  }
  .gdb-lb-table td:last-child {
    border-right: none;
  }
  .gdb-lb-table tr:last-child td {
    border-bottom: none;
  }
  .gdb-lb-table tr:hover {
    background: rgba(0,0,0,0.025);
  }
  .gdb-lb-table .rank {
    text-align: center;
    font-weight: 700;
    font-size: 0.95em;
    color: #aaa;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
  }
  .gdb-lb-table .rank-top {
    color: #444;
  }
  .gdb-lb-table .model-name {
    font-weight: 600;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    font-size: 0.88em;
    color: var(--global-text-color);
  }
  .gdb-lb-table .model-name-top {
    font-weight: 700;
  }
  .gdb-lb-table .framework {
    font-size: 0.87em;
    color: var(--global-text-color-light);
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
  }
  .gdb-lb-table .score-cell {
    text-align: right;
    font-weight: 700;
    font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
    font-size: 0.95em;
    letter-spacing: 0.3px;
  }
  .gdb-lb-table .score-hi  { color: #1a9e5c; }
  .gdb-lb-table .score-mid { color: #2a7ab8; }
  .gdb-lb-table .score-lo  { color: #c0392b; }
  .gdb-lb-table .row-top-1 {
    background: rgba(26,158,92,0.05);
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
  html[data-theme='dark'] .gdb-leaderboard {
    border-color: #3a3a3a;
  }
  html[data-theme='dark'] .gdb-lb-table th {
    background: #1c1c1c;
    color: #aaa;
    border-bottom-color: #3a3a3a;
    border-right-color: #2e2e2e;
  }
  html[data-theme='dark'] .gdb-lb-table td {
    border-bottom-color: #282828;
    border-right-color: #282828;
  }
  html[data-theme='dark'] .gdb-lb-table tr:hover {
    background: rgba(255,255,255,0.04);
  }
  html[data-theme='dark'] .gdb-lb-table .row-top-1 {
    background: rgba(26,158,92,0.08);
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

<!-- Teaser -->
<div class="gdb-teaser" style="margin-bottom: 48px;">
  <img src="/assets/img/gamedevbench-teaser.png" alt="GameDevBench task examples across 3D Graphics, 2D Graphics, Gameplay, and UI categories">
  <p class="caption">
    Example tasks from GameDevBench spanning 3D Graphics, 2D Graphics, Gameplay, and UI categories in the Godot engine.
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
    <div class="num">114</div>
    <div class="label">Avg. LOC / Solution</div>
  </div>
  <div class="gdb-stat">
    <div class="num">53.8%</div>
    <div class="label">Best Agent Score</div>
  </div>
</div>

<!-- TL;DR -->
<div class="gdb-section">
  <h2>TL;DR</h2>
  <div class="gdb-abstract">
    <ul style="line-height: 1.8;">
      <li>GameDevBench is the first benchmark for evaluating LM agents on game development tasks.</li>
      <li>GameDevBench features 333 tasks set in the Godot engine, collected from web and video tutorials across four skill categories: gameplay logic (collision detectors, character controllers), 3D graphics and animation (material tuning, skeletal animation), 2D graphics and animation (sprite animation, TileMap setup), and user interface (HUD layout, menu navigation).</li>
      <li>Tasks require agents to navigate large codebases and manipulate multimodal assets such as shaders, sprites, and animations &mdash; the average solution requires over 3&times; the lines of code and file changes of prior software development benchmarks.</li>
      <li>Game development is hard for agents: the best agent and method solves only 53.8% of tasks, and success drops sharply on multimodally demanding tasks (51.4% on gameplay vs. 33.0% on 2D graphics).</li>
      <li>Two simple image and video-based feedback mechanisms consistently improve performance &mdash; visual feedback lifts GPT-5.4 from 41.1% to 52.0%.</li>
    </ul>
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

<!-- Leaderboard -->
<div class="gdb-section">
  <h2>Leaderboard</h2>
  <div class="gdb-leaderboard">
    <table class="gdb-lb-table">
      <thead>
        <tr>
          <th>Rank</th>
          <th>Model</th>
          <th>Org</th>
          <th>Harness</th>
          <th>Feedback</th>
          <th style="text-align: right;">Score</th>
        </tr>
      </thead>
      <tbody>
        <tr class="row-top-1">
          <td class="rank rank-top">1</td>
          <td class="model-name model-name-top">gemini-3-pro-preview</td>
          <td class="framework">Google</td>
          <td class="framework">Gemini CLI</td>
          <td class="framework">Screenshot + Video</td>
          <td class="score-cell score-hi">53.8</td>
        </tr>
        <tr>
          <td class="rank rank-top">2</td>
          <td class="model-name">gpt-5.4</td>
          <td class="framework">OpenAI</td>
          <td class="framework">Codex</td>
          <td class="framework">Screenshot + Video</td>
          <td class="score-cell score-hi">52.0</td>
        </tr>
        <tr>
          <td class="rank rank-top">3</td>
          <td class="model-name">gemini-3-flash-preview</td>
          <td class="framework">Google</td>
          <td class="framework">Gemini CLI</td>
          <td class="framework">Video</td>
          <td class="score-cell score-hi">46.9</td>
        </tr>
        <tr>
          <td class="rank">4</td>
          <td class="model-name">gpt-5.4-mini</td>
          <td class="framework">OpenAI</td>
          <td class="framework">Codex</td>
          <td class="framework">Video</td>
          <td class="score-cell score-mid">43.2</td>
        </tr>
        <tr>
          <td class="rank">5</td>
          <td class="model-name">gpt-5.4-mini</td>
          <td class="framework">OpenAI</td>
          <td class="framework">OpenHands</td>
          <td class="framework">Baseline</td>
          <td class="score-cell score-mid">38.4</td>
        </tr>
        <tr>
          <td class="rank">6</td>
          <td class="model-name">claude-sonnet-4-5</td>
          <td class="framework">Anthropic</td>
          <td class="framework">Claude Code</td>
          <td class="framework">Screenshot + Video</td>
          <td class="score-cell score-mid">34.8</td>
        </tr>
        <tr>
          <td class="rank">7</td>
          <td class="model-name">gemini-3-flash-preview</td>
          <td class="framework">Google</td>
          <td class="framework">OpenHands</td>
          <td class="framework">Screenshot + Video</td>
          <td class="score-cell score-mid">31.8</td>
        </tr>
        <tr>
          <td class="rank">8</td>
          <td class="model-name">kimi-k2.5</td>
          <td class="framework">Moonshot AI</td>
          <td class="framework">OpenHands</td>
          <td class="framework">Screenshot + Video</td>
          <td class="score-cell score-lo">20.7</td>
        </tr>
        <tr>
          <td class="rank">9</td>
          <td class="model-name">claude-haiku-4-5</td>
          <td class="framework">Anthropic</td>
          <td class="framework">Claude Code</td>
          <td class="framework">Video</td>
          <td class="score-cell score-lo">18.6</td>
        </tr>
        <tr>
          <td class="rank">10</td>
          <td class="model-name">claude-haiku-4-5</td>
          <td class="framework">Anthropic</td>
          <td class="framework">OpenHands</td>
          <td class="framework">Screenshot + Video</td>
          <td class="score-cell score-lo">17.7</td>
        </tr>
        <tr>
          <td class="rank">11</td>
          <td class="model-name">qwen3.5-397b</td>
          <td class="framework">Alibaba</td>
          <td class="framework">OpenHands</td>
          <td class="framework">Baseline</td>
          <td class="score-cell score-lo">5.4</td>
        </tr>
      </tbody>
    </table>
  </div>
  <p style="font-size: 0.83em; color: var(--global-text-color-light); margin-top: 10px;">
    * <code>pass@1</code> (%) on all 333 tasks. Each row shows the best-performing multimodal feedback configuration for that model + harness pair (ICML 2026 camera-ready results). Screenshot = editor screenshot MCP server; Video = runtime gameplay video instructions.
  </p>
</div>

<!-- BibTeX -->
<div class="gdb-section">
  <h2>Citation</h2>
  <div class="gdb-bibtex">
    <button class="copy-btn" onclick="navigator.clipboard.writeText(document.getElementById('bibtex-text').innerText)">
      <i class="fas fa-copy"></i> Copy
    </button>
    <pre><code id="bibtex-text">@misc{chi2026gamedevbenchevaluatingagenticcapabilities,
      title={GameDevBench: Evaluating Agentic Capabilities Through Game Development},
      author={Wayne Chi and Yixiong Fang and Arnav Yayavaram and Siddharth Yayavaram and Seth Karten and Qiuhong Anna Wei and Runkun Chen and Alexander Wang and Valerie Chen and Ameet Talwalkar and Chris Donahue},
      year={2026},
      eprint={2602.11103},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2602.11103},
}</code></pre>
  </div>
</div>
