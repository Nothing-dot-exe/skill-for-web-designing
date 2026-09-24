# 🔬 Blueprint 08: Frontier AI Scientist & ML Research Fellow Portfolio

[![Category](https://img.shields.io/badge/Category-AI%20Scientist%20%26%20Researcher-00F0FF?style=for-the-badge)](./08-ai-researcher-academic-papers-archive.md)
[![Standard](https://img.shields.io/badge/Standard-DeepMind%20%2F%20OpenAI%20%2F%20NeurIPS%20Caliber-A855F7?style=for-the-badge)](./08-ai-researcher-academic-papers-archive.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-Rigorous%20Mathematical%20Obsidian-6366F1?style=for-the-badge)](./08-ai-researcher-academic-papers-archive.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **frontier artificial intelligence researchers, deep learning scientists, postdocs, and ML research fellows** (publishing at NeurIPS, ICML, ICLR, CVPR, and Nature) who need to present their publications, mathematical foundations, and model weights with supreme scientific rigor.

**Primary Objective:**  
To establish undeniable scientific eminence for peer review committees, academic tenure boards, elite research lab recruiters (DeepMind, FAIR, Anthropic, OpenAI), and grant allocators.

---

## 💡 Why To Use This Blueprint
Most academic researcher websites are abysmal:
- Static HTML pages from 2004 that look like a raw directory listing.
- Broken links to PDFs hosted on obscure university servers.
- No interactive way to explore model architectures, loss curves, or citation trees.

**How This Blueprint Solves It:**
1. **Interactive LaTeX & Equation Visualizer:** High-fidelity KaTeX/MathJax rendering of core transformer theorems, loss functions, and diffusion proofs.
2. **Interactive Citation & arXiv Matrix:** Live citation counters (h-index, total citations) with 1-click BibTeX clipboard copy.
3. **Interactive Weights & Model Playground:** Live in-browser inference demo or interactive architecture DAG (Multi-Head Latent Attention, Mixture-of-Experts routing).
4. **Peer Review & Conference Timeline:** Chronological archive filterable by conference tier (Oral Presentation, Spotlight, Poster).

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[RESEARCHER_NAME]` with your name (e.g. *Dr. Aris Thorne*).
- Replace `[LAB_INSTITUTION]` with your lab (e.g. *Frontier Alignment Lab // Stanford & DeepMind Fellow*).
- Replace `[PRIMARY_FOCUS]` with your subfield (e.g. *Mechanistic Interpretability & Latent Reasoning in Large Transformers*).
- Replace `[FLAGSHIP_PAPER]` with your top paper (e.g. *Dissecting Attention Superposition in Sparse Mixture-of-Experts*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Scientific Obsidian Palette */
  --bg-deep: #07080B;
  --bg-panel: #0E1017;
  --accent-indigo: #6366F1;
  --accent-cyan: #06B6D4;
  --text-main: #F1F5F9;
  --text-math: #E2E8F0;
  --text-dim: #64748B;
  --border-glass: rgba(99, 102, 241, 0.18);

  /* Typography */
  --font-math: 'KaTeX_Math', 'Latin Modern Math', 'Computer Modern', serif;
  --font-sans: 'Inter', -apple-system, sans-serif;
  --font-code: 'JetBrains Mono', monospace;
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as a Principal Research Scientist and Academic Web Architect (DeepMind / NeurIPS caliber).
Build a premier, mathematically rigorous personal research archive and paper catalog for [RESEARCHER_NAME], [LAB_INSTITUTION] researching [PRIMARY_FOCUS].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER use generic tech icons (like generic gears or lightbulbs).
- NEVER display papers without essential scientific metadata (arXiv ID, Conference Tier, BibTeX citation block, Code repository, Model weights link).
- NEVER write marketing fluff. Use rigorous academic prose: "Investigating representation geometry, linear representation hypothesis, mechanistic circuits, and sparse autoencoder feature dictionaries."
- NEVER omit mobile-friendly mathematical rendering.

REQUIRED CORE SECTIONS:
1. SCIENTIFIC MASTHEAD:
   - Name & Affiliation: "[RESEARCHER_NAME] — [LAB_INSTITUTION]"
   - Live Telemetry Ribbon:
     * "h-index: 28"
     * "Citations: 4,820+"
     * "NeurIPS / ICML Publications: 14"
   - Quick Links: [Google Scholar] [arXiv Author Link] [GitHub] [HuggingFace Profile].

2. RESEARCH THESIS & MATHEMATICAL FOUNDATION:
   - Statement: "[PRIMARY_FOCUS]"
   - Interactive Formula Box: Display the flagship loss function or attention formula rendered with LaTeX styling, with clickable terms explaining hyperparameter intuition.

3. FEATURED PAPERS WITH 1-CLICK BIBTEX EXPORT:
   - Paper 1 (Oral / Spotlight): "[FLAGSHIP_PAPER]" (NeurIPS 2025)
     * Abstract toggle
     * [PDF Link] [arXiv] [Code / GitHub] [HuggingFace Weights] [Copy BibTeX]
   - Paper 2: "Sparse Autoencoders for Feature Decomposition in 70B Parameter Models" (ICML 2024)
   - Paper 3: "Provable Bounds on Alignment Drift Under Continuous Fine-Tuning" (ICLR 2024)

4. INTERACTIVE MODEL ARCHITECTURE OR ATTENTION VISUALIZER:
   - A live interactive widget showing transformer attention heads or token routing activations.

5. ACADEMIC SERVICE & TEACHING:
   - Program Committee / Area Chair service for major conferences.
   - PhD and Master students mentored.
   - Keynote and invited talk recordings.
```

---

## ⚡ Runnable Starter Code Snippet: Interactive Academic Paper Card with BibTeX Copy

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>AI Researcher Archive</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #07080B; color: #F1F5F9; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; padding: 40px 20px; max-width: 840px; margin: 0 auto; line-height: 1.6; }
    header { border-bottom: 1px solid #1E222D; padding-bottom: 24px; margin-bottom: 36px; }
    .name { font-size: 1.8rem; font-weight: 700; color: #FFFFFF; }
    .affiliation { color: #6366F1; font-family: monospace; font-size: 0.9rem; margin-top: 4px; }
    .metrics { display: flex; gap: 16px; margin-top: 16px; font-family: monospace; font-size: 0.8rem; }
    .metric-badge { background: #0E1017; border: 1px solid #1E222D; padding: 6px 12px; border-radius: 6px; }
    .paper-card { background: #0E1017; border: 1px solid #1E222D; border-radius: 8px; padding: 24px; margin-bottom: 20px; transition: border-color 0.2s; }
    .paper-card:hover { border-color: #6366F1; }
    .conf-tag { display: inline-block; background: rgba(99, 102, 241, 0.15); color: #818CF8; border: 1px solid rgba(99, 102, 241, 0.3); padding: 3px 8px; border-radius: 4px; font-size: 0.75rem; font-family: monospace; margin-bottom: 10px; }
    .paper-title { font-size: 1.2rem; font-weight: 600; color: #FFFFFF; }
    .authors { font-size: 0.9rem; color: #94A3B8; margin: 6px 0 12px 0; }
    .authors strong { color: #F1F5F9; }
    .actions { display: flex; gap: 8px; flex-wrap: wrap; margin-top: 14px; }
    .btn { background: #161922; border: 1px solid #272B38; color: #CBD5E1; padding: 6px 12px; border-radius: 6px; font-size: 0.8rem; font-family: monospace; cursor: pointer; text-decoration: none; transition: all 0.2s; }
    .btn:hover { background: #6366F1; color: #FFF; border-color: #6366F1; }
    .bibtex-box { display: none; background: #07080B; border: 1px solid #272B38; padding: 14px; border-radius: 6px; font-family: monospace; font-size: 0.75rem; color: #94A3B8; margin-top: 14px; white-space: pre-wrap; }
    .toast { position: fixed; bottom: 24px; right: 24px; background: #6366F1; color: #FFF; padding: 10px 18px; border-radius: 6px; font-family: monospace; font-size: 0.8rem; display: none; }
  </style>
</head>
<body>
  <header>
    <div class="name">Dr. Aris Thorne</div>
    <div class="affiliation">Frontier AI Fellow // DeepMind & Stanford AI Lab</div>
    <div class="metrics">
      <div class="metric-badge">Citations: <strong>4,820</strong></div>
      <div class="metric-badge">h-index: <strong>28</strong></div>
      <div class="metric-badge">NeurIPS/ICML: <strong>14</strong></div>
    </div>
  </header>

  <div class="paper-card">
    <span class="conf-tag">NeurIPS 2025 // ORAL PRESENTATION</span>
    <div class="paper-title">Dissecting Attention Superposition in Sparse Mixture-of-Experts</div>
    <div class="authors"><strong>Aris Thorne</strong>, Elena Rostova, Marcus Sterling, David Silver</div>
    <p style="font-size: 0.9rem; color: #94A3B8;">We prove that transformer routing circuits collapse representation rank under deep gradient flow, and propose orthogonal gating projectors that recover full rank representation.</p>
    
    <div class="actions">
      <a href="#" class="btn">[PDF arXiv]</a>
      <a href="#" class="btn">[Code / GitHub]</a>
      <a href="#" class="btn">[HuggingFace Weights]</a>
      <button class="btn" onclick="toggleBibtex('bib1')">[BibTeX]</button>
      <button class="btn" onclick="copyBibtex()">[Copy Citation]</button>
    </div>

    <div class="bibtex-box" id="bib1">@inproceedings{thorne2025dissecting,
  title={Dissecting Attention Superposition in Sparse Mixture-of-Experts},
  author={Thorne, Aris and Rostova, Elena and Sterling, Marcus and Silver, David},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  year={2025}
}</div>
  </div>

  <div class="toast" id="toast">BibTeX copied to clipboard!</div>

  <script>
    function toggleBibtex(id) {
      const el = document.getElementById(id);
      el.style.display = el.style.display === 'block' ? 'none' : 'block';
    }
    function copyBibtex() {
      const text = document.getElementById('bib1').innerText;
      navigator.clipboard.writeText(text);
      const toast = document.getElementById('toast');
      toast.style.display = 'block';
      setTimeout(() => toast.style.display = 'none', 2500);
    }
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] LaTeX math blocks render without horizontal page overflow on small smartphone screens.
- [ ] 1-click BibTeX copy triggers visual feedback and copies valid syntax.
- [ ] External PDF and code repository links are actively validated without 404 dead links.
