# 🎨 Blueprint 05: Lead Product Designer & Design Systems Portfolio

[![Category](https://img.shields.io/badge/Category-Lead%20Product%20Designer%20Portfolio-00F0FF?style=for-the-badge)](./05-lead-product-designer-case-study.md)
[![Standard](https://img.shields.io/badge/Standard-Apple%20%2F%20Linear%20%2F%20Figma%20Caliber-A855F7?style=for-the-badge)](./05-lead-product-designer-case-study.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-Tactile%20Dark%20System-FF6B00?style=for-the-badge)](./05-lead-product-designer-case-study.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **Staff/Principal Product Designers, Design Systems Architects, and UI/UX Directors** (working at or aiming for Linear, Apple, Figma, Stripe, or Airbnb) who need to present their design craftsmanship through deep, rigorous interactive case studies.

**Primary Objective:**  
To win over Chief Design Officers, VP of Product leads, and discerning startup founders by demonstrating true systems thinking, component token rigor, and measurable product business impact.

---

## 💡 Why To Use This Blueprint
Most designer portfolios are superficial Dribbble mockups:
- Pretty screenshots with zero context or business metrics.
- Wall-of-text case studies that nobody has time to read.
- Generic Behance templates that fail to show how components behave interactively.

**How This Blueprint Solves It:**
1. **Interactive Before-and-After Redesign Splitter:** Allows recruiters to slide between the legacy enterprise UI and the designer's refined design system.
2. **Interactive Design Token & Component Inspector:** A live widget demonstrating token variables (color contrast, spring transitions, spacing scales).
3. **Business Impact Telemetry:** Prominently highlights conversion uplifts, task-completion speed improvements, and reduction in engineering sprint cycles.
4. **Micro-Motion Polish:** Silky spring transitions, subtle card elevation on cursor hover, and tactile haptic feedback.

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[DESIGNER_NAME]` with your full name (e.g. *Kaelen Vance*).
- Replace `[CURRENT_TITLE]` with your leadership title (e.g. *Principal Design Systems Architect*).
- Replace `[FLAGSHIP_PRODUCT]` with your premier case study (e.g. *Next-Gen Enterprise Analytics Redesign*).
- Replace `[KEY_IMPACT_METRIC]` with your measurable result (e.g. *+34% task completion velocity, 420 components unified*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Design System Tokens */
  --canvas-dark: #090A0F;
  --surface-1: #11131A;
  --surface-2: #1A1D27;
  --brand-violet: #8B5CF6;
  --brand-cyan: #06B6D4;
  --text-primary: #F8FAFC;
  --text-secondary: #94A3B8;
  --border-specular: rgba(255, 255, 255, 0.08);

  /* Typography */
  --font-heading: 'Plus Jakarta Sans', -apple-system, sans-serif;
  --font-mono: 'JetBrains Mono', monospace;

  /* Spring Physics */
  --transition-spring: 0.35s cubic-bezier(0.16, 1, 0.3, 1);
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as a Principal Design Systems Architect and Executive Design Director (Linear / Apple / Stripe caliber).
Design an elite product design portfolio and interactive case study platform for [DESIGNER_NAME], [CURRENT_TITLE].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER show static flat Dribbble mockups without real product context.
- NEVER write passive fluff ("I helped brainstorm with the team"). Use decisive product design vocabulary ("Architected multi-brand token engine", "Refactored navigational information architecture", "Eliminated modal cognitive friction").
- NEVER use generic purple gradient hero cards. Use deep obsidian surfaces (#090A0F) with razor-sharp 1px border specular sheens.
- NEVER omit business outcomes. Every case study must lead with verified quantitative impact.

CORE SECTIONS TO ASSEMBLE:
1. DESIGNER HERO & CRAFT MANIFESTO:
   - Name & Role: "[DESIGNER_NAME] // [CURRENT_TITLE]"
   - Craft Manifesto: "Translating extreme complexity into effortless, tactile digital instruments. Focused on design systems, information architecture, and micro-interactions."
   - Experience Badges: Former Lead at Tier-1 tech companies, 10+ design systems shipped.

2. FLAGSHIP CASE STUDY WITH INTERACTIVE BEFORE/AFTER SLIDER:
   - Case Title: "[FLAGSHIP_PRODUCT]"
   - Impact Telemetry: "[KEY_IMPACT_METRIC]"
   - Interactive Before/After Splitter: An interactive image/mockup slider allowing visitors to drag left/right to contrast the bloated legacy enterprise screen vs. the streamlined minimalist redesign.
   - Design System Artifacts: Expandable tabs showing Typography Scale, Spacing Grid, and Color Contrast tokens.

3. COMPONENT ATOM & MOLECULE PLAYGROUND:
   - An interactive live sandbox where visitors can test actual buttons, segmented controls, dropdowns, and toggle switches built by the designer.
   - Toggle dark/light mode token shifts in real-time.

4. SECONDARY CASE STUDIES (BENTO MATRIX):
   - Case 2: B2B Enterprise Data Visualization Engine (3D charts, keyboard navigation).
   - Case 3: Mobile Native Design System (iOS & Android token synchronization).
   - Case 4: Zero-Friction Checkout & Onboarding Funnel (+22% conversion).

5. INTERVIEW AVAILABILITY & DIRECT INQUIRY DRAWER:
   - Clean calendar availability badge: "OPEN TO ADVISORY & SELECT DESIGN LEADERSHIP ROLES".
   - 1-click email copy with animated toast notification.
```

---

## ⚡ Runnable Starter Code Snippet: Interactive Before/After Splitter Component

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Design Case Study - Before/After Comparison</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #090A0F; color: #F8FAFC; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; padding: 40px 20px; display: flex; flex-direction: column; align-items: center; }
    .container { width: 100%; max-width: 800px; }
    .header { margin-bottom: 30px; }
    .tag { font-family: monospace; font-size: 0.75rem; color: #8B5CF6; letter-spacing: 0.1em; text-transform: uppercase; }
    h1 { font-size: 2rem; margin: 8px 0; }
    p { color: #94A3B8; font-size: 0.95rem; }
    .slider-box { position: relative; width: 100%; height: 380px; border-radius: 12px; overflow: hidden; border: 1px solid rgba(255, 255, 255, 0.1); user-select: none; }
    .slide-layer { position: absolute; inset: 0; display: flex; flex-direction: column; justify-content: center; align-items: center; padding: 30px; text-align: center; }
    .before-layer { background: #1E222D; color: #94A3B8; }
    .after-layer { background: #0D111A; color: #F8FAFC; width: 50%; border-right: 2px solid #8B5CF6; overflow: hidden; }
    .after-content { position: absolute; width: 800px; height: 380px; left: 0; top: 0; display: flex; flex-direction: column; justify-content: center; align-items: center; padding: 30px; }
    .handle { position: absolute; top: 0; bottom: 0; width: 40px; margin-left: -20px; display: flex; align-items: center; justify-content: center; cursor: ew-resize; z-index: 10; left: 50%; }
    .handle-circle { width: 34px; height: 34px; border-radius: 50%; background: #8B5CF6; color: #FFFFFF; font-size: 0.8rem; display: flex; align-items: center; justify-content: center; box-shadow: 0 4px 15px rgba(139, 92, 246, 0.5); }
    .badge { padding: 4px 10px; border-radius: 6px; font-size: 0.75rem; font-family: monospace; margin-bottom: 12px; }
    .badge-legacy { background: #EF4444; color: #FFF; }
    .badge-modern { background: #8B5CF6; color: #FFF; }
  </style>
</head>
<body>
  <div class="container">
    <div class="header">
      <div class="tag">Case Study Redesign</div>
      <h1>Enterprise Analytics Redesign</h1>
      <p>Drag the slider to compare the legacy cluttered interface with the modern, high-contrast design system.</p>
    </div>

    <div class="slider-box" id="sliderContainer">
      <div class="slide-layer before-layer">
        <span class="badge badge-legacy">LEGACY ENTERPRISE UI (2022)</span>
        <h2 style="font-size: 1.4rem; color: #CBD5E1;">Cluttered 14-Column Grid</h2>
        <p style="max-width: 450px; margin-top: 10px;">High cognitive fatigue, inconsistent button colors, 8 different font weights, zero dark mode support.</p>
      </div>

      <div class="slide-layer after-layer" id="afterLayer">
        <div class="after-content">
          <span class="badge badge-modern">REFINED SYSTEM (2026)</span>
          <h2 style="font-size: 1.4rem; color: #FFFFFF;">Streamlined Bento Architecture</h2>
          <p style="max-width: 450px; margin-top: 10px;">Strict 8pt spacing grid, WCAG AAA contrast, keyboard shortcuts, and 45% faster task completion time.</p>
        </div>
      </div>

      <div class="handle" id="sliderHandle">
        <div class="handle-circle">↔</div>
      </div>
    </div>
  </div>

  <script>
    const container = document.getElementById('sliderContainer');
    const afterLayer = document.getElementById('afterLayer');
    const handle = document.getElementById('sliderHandle');
    let isDragging = false;

    function updateSlider(x) {
      const rect = container.getBoundingClientRect();
      let pos = (x - rect.left) / rect.width;
      if (pos < 0.05) pos = 0.05;
      if (pos > 0.95) pos = 0.95;
      const pct = pos * 100;
      afterLayer.style.width = pct + '%';
      handle.style.left = pct + '%';
    }

    container.addEventListener('mousedown', () => isDragging = true);
    window.addEventListener('mouseup', () => isDragging = false);
    window.addEventListener('mousemove', (e) => {
      if (!isDragging) return;
      updateSlider(e.clientX);
    });

    container.addEventListener('touchstart', () => isDragging = true);
    window.addEventListener('touchend', () => isDragging = false);
    window.addEventListener('touchmove', (e) => {
      if (!isDragging) return;
      updateSlider(e.touches[0].clientX);
    });
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] Touch gestures on mobile devices support smooth drag tracking without interfering with page scroll.
- [ ] Before/After images or mockups load with blur-up progressive rendering.
- [ ] Quantitative metrics cite real measurable benchmarks rather than vague percentages.
- [ ] Color tokens conform to WCAG 2.1 AA/AAA contrast ratios across both dark and light modes.
