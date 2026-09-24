# 📐 Blueprint 11: Avant-Garde Architectural & Spatial Designer Monograph

[![Category](https://img.shields.io/badge/Category-Architectural%20%26%20Spatial%20Monograph-00F0FF?style=for-the-badge)](./11-architect-spatial-designer-portfolio.md)
[![Standard](https://img.shields.io/badge/Standard-Zaha%20Hadid%20%2F%20BIG%20%2F%20Herzog%20%26%20de%20Meuron-A855F7?style=for-the-badge)](./11-architect-spatial-designer-portfolio.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-Brutalist%20Tectonic%20Blueprint-94A3B8?style=for-the-badge)](./11-architect-spatial-designer-portfolio.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **principal architects, computational spatial designers, parametric urbanists, and luxury interior architects** (Zaha Hadid Architects, BIG, Herzog & de Meuron alumni) who craft built environments.

**Primary Objective:**  
To win monumental civic commissions, luxury private residential commissions, and international design awards through interactive architectural blueprints, daylight sun-angle simulations, and physical material materiality inspectors.

---

## 💡 Why To Use This Blueprint
Most architectural portfolio websites are lifeless:
- Static galleries of rendered JPEGs that feel like generic interior design Pinterest boards.
- No sense of physical scale, solar orientation, or structural engineering.
- Blueprint technical drawings are buried or missing completely.

**How This Blueprint Solves It:**
1. **Interactive Render vs. Technical Blueprint Toggle:** Allows clients to toggle between photorealistic architectural renders and razor-sharp CAD vector line drawings.
2. **Interactive Solar Daylight Simulator:** A slider adjusting the sun angle ($0^\circ$ to $360^\circ$) casts dynamic soft shadows across 3D massing models.
3. **Physical Material Palette Inspector:** Interactive tactile swatches (Travertine marble, blackened steel, brushed fluted glass, charred cedar) with acoustic and tactile ratings.
4. **Parametric Blueprint Grid:** Subtle mathematical CAD coordinates and dimension lines that respond to mouse position.

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[ARCHITECT_NAME]` with your name or atelier (e.g. *Kaelen Vane Atelier*).
- Replace `[DISCIPLINE]` with your domain (e.g. *Parametric Architecture & Spatial Design*).
- Replace `[FLAGSHIP_STRUCTURE]` with your lead building (e.g. *The Obsidian Pavilion // Kyoto*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Tectonic Architecture Palette */
  --bg-concrete: #0D0E11;
  --bg-travertine: #16181E;
  --accent-cyan-cad: #00F0FF;
  --accent-stone: #CBD5E1;
  --text-main: #F1F5F9;
  --text-muted: #64748B;
  --border-cad: rgba(255, 255, 255, 0.12);

  /* Typography */
  --font-serif: 'Cinzel', 'Playfair Display', serif;
  --font-mono: 'JetBrains Mono', monospace;
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as a Principal Design Architect and Architectural Critic (Zaha Hadid / BIG / Foster+Partners caliber).
Design a museum-grade architectural monograph and spatial portfolio for [ARCHITECT_NAME], [DISCIPLINE].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER output generic interior design stock photos. Treat every project as an iconic, sculptural architectural monument.
- NEVER omit architectural metadata (Location, Area in m², Structural Engineering Partner, Structural Steel Tonnes, Solar Azimuth).
- NEVER use cartoonish rounded buttons. Use precise, crisp, tectonic 1px borders with CAD crosshairs and geometric coordinates.

CORE EXPERIENTIAL SECTIONS:
1. ARCHITECTURAL MASTHEAD & TECTONIC COORDINATES:
   - Atelier: "[ARCHITECT_NAME] // ATELIER OF PARAMETRIC ARCHITECTURE"
   - Live Cursor CAD Coordinates: Displaying X/Y viewport coordinates as mathematical millimeters (e.g. `X: 421.4mm | Y: 118.2mm`).

2. FLAGSHIP MONUMENT WITH BLUEPRINT / RENDER TOGGLE:
   - Structure: "[FLAGSHIP_STRUCTURE]"
   - Interactive View Toggle: [PHOTOREALISTIC RENDER] vs. [TECHNICAL CAD BLUEPRINT].
   - Architectural Specs Table: Gross Floor Area, Structural Material (Reinforced Basalt Concrete), Climate Category.

3. INTERACTIVE SOLAR DAYLIGHT SIMULATOR:
   - A daylight time-of-day slider (6:00 AM to 8:00 PM) that dynamically adjusts the lighting temperature, shadow length, and ambient occlusion across the building preview.

4. TACTILE MATERIALITY LAB:
   - Interactive tactile cards for physical materials:
     * Card 1: Roman Fluted Travertine Marble (Honed Finish)
     * Card 2: Blackened Anodized Aluminum
     * Card 3: Structural Low-Iron Triple-Glazed Glass
     * Card 4: Charred Yakisugi Japanese Cedar

5. CURATED COMMISSIONS CATALOG:
   - Project 2: High-Altitude Alpine Research Sanctuary (Switzerland).
   - Project 3: Sovereign Desalination Cultural Center (Doha).
   - Project 4: Cantilevered Desert Observatory (Atacama).

6. PRIVATE COMMISSION INQUIRY:
   - Private atelier consultation drawer with encrypted PDF monograph request.
```

---

## ⚡ Runnable Starter Code Snippet: Interactive Render vs Blueprint Toggle

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Architectural Monograph</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #0D0E11; color: #F1F5F9; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; padding: 40px 20px; max-width: 860px; margin: 0 auto; }
    header { display: flex; justify-content: space-between; align-items: baseline; border-bottom: 1px solid rgba(255, 255, 255, 0.1); padding-bottom: 20px; margin-bottom: 30px; }
    .atelier-title { font-family: 'Cinzel', serif, Georgia; font-size: 1.25rem; letter-spacing: 0.1em; text-transform: uppercase; }
    .cad-coords { font-family: monospace; font-size: 0.75rem; color: #64748B; }
    .project-header { margin-bottom: 24px; }
    .project-title { font-size: 2rem; font-weight: 700; margin-bottom: 6px; }
    .toggle-bar { display: flex; gap: 10px; margin-bottom: 20px; }
    .toggle-btn { background: #16181E; border: 1px solid #282C37; color: #94A3B8; padding: 8px 16px; border-radius: 4px; font-family: monospace; font-size: 0.8rem; cursor: pointer; }
    .toggle-btn.active { background: #00F0FF; color: #0D0E11; font-weight: bold; border-color: #00F0FF; }
    .viewport { width: 100%; height: 420px; border-radius: 8px; border: 1px solid rgba(255, 255, 255, 0.1); position: relative; overflow: hidden; display: flex; align-items: center; justify-content: center; }
    .render-view { position: absolute; inset: 0; background: linear-gradient(135deg, #1e293b, #0f172a); display: flex; flex-direction: column; align-items: center; justify-content: center; transition: opacity 0.3s; }
    .cad-view { position: absolute; inset: 0; background: #08090C; display: none; flex-direction: column; align-items: center; justify-content: center; border: 1px dashed #00F0FF; }
    .cad-grid { position: absolute; inset: 0; background-image: linear-gradient(to right, rgba(0, 240, 255, 0.08) 1px, transparent 1px), linear-gradient(to bottom, rgba(0, 240, 255, 0.08) 1px, transparent 1px); background-size: 30px 30px; }
  </style>
</head>
<body>
  <header>
    <div class="atelier-title">Kaelen Vane // Atelier</div>
    <div class="cad-coords" id="coords">CAD: 0.00mm // 0.00mm</div>
  </header>

  <div class="project-header">
    <div style="font-family: monospace; font-size: 0.75rem; color: #00F0FF;">KYOTO, JAPAN // 2026</div>
    <div class="project-title">The Obsidian Pavilion</div>
    <div style="color: #94A3B8; font-size: 0.95rem;">Parametric basalt cantilever hovering above thermal springs.</div>
  </div>

  <div class="toggle-bar">
    <button class="toggle-btn active" id="btnRender" onclick="setView('render')">Photorealistic Render</button>
    <button class="toggle-btn" id="btnCad" onclick="setView('cad')">Structural CAD Blueprint</button>
  </div>

  <div class="viewport" id="viewport">
    <div class="render-view" id="renderView">
      <div style="font-size: 1.5rem; font-family: serif; color: #CBD5E1;">[ Architectural Render View ]</div>
      <div style="font-family: monospace; font-size: 0.8rem; color: #64748B; margin-top: 8px;">Volumetric sunlight hitting travertine massing</div>
    </div>
    <div class="cad-view" id="cadView">
      <div class="cad-grid"></div>
      <div style="position: relative; z-index: 2; font-family: monospace; color: #00F0FF; text-align: center;">
        <div style="font-size: 1.3rem;">[ TECHNICAL VECTOR BLUEPRINT ]</div>
        <div style="font-size: 0.8rem; margin-top: 6px;">STRUCTURAL AXIS: A-14 // CANTILEVER: 18.4m // STEEL: ASTM A992</div>
      </div>
    </div>
  </div>

  <script>
    function setView(mode) {
      if (mode === 'render') {
        document.getElementById('renderView').style.display = 'flex';
        document.getElementById('cadView').style.display = 'none';
        document.getElementById('btnRender').classList.add('active');
        document.getElementById('btnCad').classList.remove('active');
      } else {
        document.getElementById('renderView').style.display = 'none';
        document.getElementById('cadView').style.display = 'flex';
        document.getElementById('btnRender').classList.remove('active');
        document.getElementById('btnCad').classList.add('active');
      }
    }

    window.addEventListener('mousemove', (e) => {
      document.getElementById('coords').innerText = `CAD: ${e.clientX}.00mm // ${e.clientY}.00mm`;
    });
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] Interactive Blueprint switch transitions instantaneously without layout flash.
- [ ] CAD grid scales cleanly across Retina and high-DPI displays.
- [ ] Architecture project data includes authentic structural metrics.
