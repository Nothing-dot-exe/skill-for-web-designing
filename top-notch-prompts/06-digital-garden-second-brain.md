# 🌿 Blueprint 06: Bespoke Digital Garden & Evergreen Second Brain

[![Category](https://img.shields.io/badge/Category-Digital%20Garden%20%26%20Second%20Brain-00F0FF?style=for-the-badge)](./06-digital-garden-second-brain.md)
[![Standard](https://img.shields.io/badge/Standard-Andy%20Matuschak%20%2F%20Maggie%20Appleton-10B981?style=for-the-badge)](./06-digital-garden-second-brain.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-Organic%20Evergreen%20Graph-10B981?style=for-the-badge)](./06-digital-garden-second-brain.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **knowledge workers, researchers, system thinkers, technical writers, and software philosophers** who prefer a living "Digital Garden" over a static linear blog.

**Primary Objective:**  
To publish interconnected, evolving thoughts with bidirectional wiki-links (`[[Note Name]]`), note maturity stages (Seedling 🌱, Budding 🌿, Evergreen 🌲), and a live interactive 2D force-directed knowledge graph.

---

## 💡 Why To Use This Blueprint
Traditional blogging formats fail modern deep thinkers:
- Reverse-chronological blog posts force old ideas to die regardless of relevance.
- Static posts don't show how concepts connect or evolve over years.
- Readers get lost with no mental map of how ideas cross-pollinate.

**How This Blueprint Solves It:**
1. **Interactive 2D Canvas Knowledge Graph:** Visualizes nodes and edges connecting thoughts, allowing readers to explore the mental network dynamically.
2. **Note Growth Stages:** Explicit status markers:
   - 🌱 **Seedling:** Raw, unpolished thought or question.
   - 🌿 **Budding:** Developing idea with empirical citations.
   - 🌲 **Evergreen:** Mature, deeply refined conceptual framework.
3. **Stacked Sliding Note Panes (Andy Matuschak Style):** Clicking a wiki-link slides open the new note horizontally without losing the reader's current place.
4. **Bidirectional Backlinks Drawer:** Automatically displays every note that references the current document.

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[GARDENER_NAME]` with your name (e.g. *Julian Chen*).
- Replace `[CORE_RESEARCH_FIELDS]` with your themes (e.g. *Distributed Systems, Epistemology, Human-Computer Interaction*).
- Replace `[KEY_NOTE_1]` with your premier evergreen thought (e.g. *Tools for Thought and Spatial Memory*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Digital Garden Palette */
  --bg-botanical: #0B0E0C;
  --surface-leaf: #121714;
  --accent-emerald: #10B981;
  --accent-lime: #84CC16;
  --text-primary: #ECFDF5;
  --text-muted: #6EE7B7;
  --border-organic: rgba(16, 185, 129, 0.2);

  /* Typography */
  --font-content: 'Newsreader', Georgia, serif;
  --font-interface: 'Inter', -apple-system, sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as a Principal Design Engineer and Digital Epistemologist (Andy Matuschak / Maggie Appleton caliber).
Create a living, bespoke personal Digital Garden and Evergreen Second Brain for [GARDENER_NAME] researching [CORE_RESEARCH_FIELDS].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER treat this as a standard blog with "Published on Date" as the main hierarchy. Ideas must be sorted by conceptual connectivity and growth stage.
- NEVER omit bidirectional links. Notes must feature inline [[wiki-style links]] that show live hover previews.
- NEVER use flat sterile gray cards. Use an organic botanical dark palette (#0B0E0C base, #121714 surface, with vibrant emerald green #10B981 accents).
- NEVER use dead placeholders in the interactive knowledge graph. The canvas graph must have physics nodes that bounce and tether.

CORE ARCHITECTURAL FEATURES:
1. GARDEN STATUS & PHILOSOPHY BANNER:
   - "This is a digital garden, not a blog. Notes are planted as seedlings, pruned as they grow, and maintained as evergreens."
   - Live Garden Telemetry: 142 Notes, 380 Bidirectional Connections, 18 Evergreen Monographs.
   - Growth Stage Legend: 🌱 Seedling (Idea) | 🌿 Budding (Developing) | 🌲 Evergreen (Mature).

2. INTERACTIVE 2D KNOWLEDGE GRAPH CANVAS:
   - An interactive HTML5 canvas displaying nodes (notes) connected by luminous spring edges.
   - Dragging a node moves connected thoughts with spring tension.
   - Clicking a node navigates to or preview-expands the corresponding note.

3. RECENTLY CULTIVATED THOUGHTS (HORIZONTAL CAROUSEL OR MASONRY):
   - Note Card 1: "[KEY_NOTE_1]" (🌲 Evergreen) - Last pruned 3 days ago. Read time: 8 min.
   - Note Card 2: "The Paradox of Tool Fluidity" (🌿 Budding) - 4 backlinks.
   - Note Card 3: "Memory as a Kinetic Medium" (🌱 Seedling) - Quick hypothesis.

4. ANDY MATUSCHAK HORIZONTAL STACKING PANES:
   - Clicking any internal note link slides open a new column next to the active note, preserving continuous reading context across multiple connected thoughts.

5. BACKLINKS & MENTIONS ACCORDION:
   - At the bottom of each note: "4 notes reference this idea", showing previews of inbound thoughts.
```

---

## ⚡ Runnable Starter Code Snippet: Interactive Knowledge Graph Canvas

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Digital Garden Knowledge Graph</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #0B0E0C; color: #ECFDF5; font-family: -apple-system, sans-serif; overflow: hidden; height: 100vh; }
    #graphCanvas { position: absolute; inset: 0; }
    .overlay { position: relative; z-index: 10; padding: 24px; pointer-events: none; }
    .badge { display: inline-flex; align-items: center; gap: 6px; padding: 4px 10px; background: rgba(16, 185, 129, 0.1); border: 1px solid rgba(16, 185, 129, 0.3); border-radius: 6px; font-size: 0.75rem; color: #10B981; font-family: monospace; }
    h1 { font-size: 1.5rem; margin-top: 8px; font-weight: 700; color: #FFFFFF; }
    p { font-size: 0.85rem; color: #6EE7B7; max-width: 400px; margin-top: 4px; }
  </style>
</head>
<body>
  <div class="overlay">
    <div class="badge">🌿 Digital Garden Graph v2.4</div>
    <h1>Julian's Second Brain</h1>
    <p>Drag nodes to explore semantic gravity between evolving notes.</p>
  </div>
  <canvas id="graphCanvas"></canvas>

  <script>
    const canvas = document.getElementById('graphCanvas');
    const ctx = canvas.getContext('2d');
    let width = canvas.width = window.innerWidth;
    let height = canvas.height = window.innerHeight;

    window.addEventListener('resize', () => {
      width = canvas.width = window.innerWidth;
      height = canvas.height = window.innerHeight;
    });

    const nodes = [
      { id: 1, label: "Spatial Memory", x: width * 0.4, y: height * 0.4, vx: 0, vy: 0, stage: "🌲" },
      { id: 2, label: "Tools for Thought", x: width * 0.5, y: height * 0.5, vx: 0, vy: 0, stage: "🌲" },
      { id: 3, label: "Canvas UI", x: width * 0.6, y: height * 0.45, vx: 0, vy: 0, stage: "🌿" },
      { id: 4, label: "Epistemic Agency", x: width * 0.45, y: height * 0.65, vx: 0, vy: 0, stage: "🌱" },
      { id: 5, label: "Local-First Software", x: width * 0.58, y: height * 0.6, vx: 0, vy: 0, stage: "🌲" },
      { id: 6, label: "CRDTs & Synergy", x: width * 0.68, y: height * 0.65, vx: 0, vy: 0, stage: "🌿" },
    ];

    const links = [
      { source: 0, target: 1 },
      { source: 1, target: 2 },
      { source: 1, target: 3 },
      { source: 1, target: 4 },
      { source: 4, target: 5 },
      { source: 2, target: 4 }
    ];

    let dragNode = null;
    window.addEventListener('mousedown', (e) => {
      nodes.forEach(n => {
        if (Math.hypot(n.x - e.clientX, n.y - e.clientY) < 25) {
          dragNode = n;
        }
      });
    });
    window.addEventListener('mousemove', (e) => {
      if (dragNode) {
        dragNode.x = e.clientX;
        dragNode.y = e.clientY;
      }
    });
    window.addEventListener('mouseup', () => dragNode = null);

    function loop() {
      ctx.clearRect(0, 0, width, height);

      // Draw links
      ctx.strokeStyle = "rgba(16, 185, 129, 0.25)";
      ctx.lineWidth = 1.5;
      links.forEach(l => {
        const s = nodes[l.source];
        const t = nodes[l.target];
        ctx.beginPath();
        ctx.moveTo(s.x, s.y);
        ctx.lineTo(t.x, t.y);
        ctx.stroke();
      });

      // Draw nodes
      nodes.forEach(n => {
        ctx.fillStyle = "#121714";
        ctx.strokeStyle = "#10B981";
        ctx.lineWidth = 2;
        ctx.beginPath();
        ctx.arc(n.x, n.y, 18, 0, Math.PI * 2);
        ctx.fill();
        ctx.stroke();

        ctx.font = "12px sans-serif";
        ctx.fillStyle = "#FFFFFF";
        ctx.textAlign = "center";
        ctx.fillText(n.stage, n.x, n.y + 4);

        ctx.font = "11px monospace";
        ctx.fillStyle = "#6EE7B7";
        ctx.fillText(n.label, n.x, n.y + 32);
      });

      requestAnimationFrame(loop);
    }
    loop();
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] Force simulation dampens naturally to avoid infinite jitter or CPU spin.
- [ ] Bidirectional wiki-links parse correctly without breaking nested brackets.
- [ ] Stacking panes work responsively on tablets and desktop monitors.
- [ ] Offline reading supported via Service Worker caching.
