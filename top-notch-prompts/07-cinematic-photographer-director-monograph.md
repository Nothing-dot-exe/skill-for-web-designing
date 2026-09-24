# 🎞️ Blueprint 07: Cinematic Film Director & Fine Art Photographer Monograph

[![Category](https://img.shields.io/badge/Category-Cinematic%20Director%20Monograph-00F0FF?style=for-the-badge)](./07-cinematic-photographer-director-monograph.md)
[![Standard](https://img.shields.io/badge/Standard-A24%20%2F%20Nowness%20%2F%20Cannes%20Caliber-A855F7?style=for-the-badge)](./07-cinematic-photographer-director-monograph.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-Atmospheric%20Noir%20Film-E11D48?style=for-the-badge)](./07-cinematic-photographer-director-monograph.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **cinematographers, commercial film directors, editorial fashion photographers, and visual artists** (A24, Nowness, Vogue, Criterion Collection caliber) whose work demands supreme visual gravity and cinematic immersion.

**Primary Objective:**  
To mesmerize executive producers, brand creative directors, and gallery curators with full-bleed aspect ratios (2.39:1 anamorphic), analog film grain overlays, seamless horizontal exhibition scrolling, and real-time EXIF lens telemetry.

---

## 💡 Why To Use This Blueprint
Most photography portfolios look like generic Instagram feeds:
- Tiny thumbnail grids that destroy the emotional impact of high-resolution stills.
- Aggressive compression that ruins shadow detail and color grading.
- Zero audio or pacing; feels like scrolling through a boring digital photo album.

**How This Blueprint Solves It:**
1. **2.39:1 Anamorphic Letterbox Presentation:** Frames every project like a theatrical cinema still with subtle organic 35mm grain simulation.
2. **Horizontal Inertial Exhibition Scroll:** Replaces jarring vertical scroll with buttery-smooth horizontal momentum scrolling.
3. **Interactive Optical Lens & EXIF Telemetry Drawer:** Clicking any still reveals camera body, anamorphic lens focal length, aperture ($f/1.4$), ISO, and color LUT grade notes.
4. **Director's Commentary Audio Track:** Optional ambient score or subtle director voice track synchronized with project reveals.

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[DIRECTOR_NAME]` with your name (e.g. *Mateo Korda*).
- Replace `[DISCIPLINE]` with your focus (e.g. *Cinematographer & Commercial Director*).
- Replace `[REPRESENTATION_CITY]` with your agency hubs (e.g. *London // Paris // Tokyo*).
- Replace `[FLAGSHIP_FILM]` with your lead title (e.g. *Nocturne in Silver — 35mm Short*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Cinematic Palette */
  --film-black: #050505;
  --film-surface: #0E0E0E;
  --film-silver: #D4D4D8;
  --accent-amber: #F59E0B;
  --accent-crimson: #E11D48;
  --text-primary: #F4F4F5;
  --text-muted: #71717A;

  /* Typography */
  --font-serif: 'Playfair Display', Didot, serif;
  --font-sans: 'Syne', -apple-system, sans-serif;
  --font-mono: 'Space Mono', monospace;
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as an Executive Creative Director for high-fashion cinema and photography (A24 / Nowness / Criterion caliber).
Architect a breathtaking, immersive monograph portfolio for [DIRECTOR_NAME], [DISCIPLINE] represented in [REPRESENTATION_CITY].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER use standard 3-column square Instagram-style photo grids.
- NEVER use bright white backgrounds that bleed light and destroy black-point color contrast.
- NEVER compress images into tiny preview tiles. Treat every still as a museum gallery print with 2.39:1 or 4:3 artistic letterboxing.
- NEVER use default cursor shapes. Implement an optical crosshair or subtle focal ring.

CORE EXPERIENCE ARCHITECTURE:
1. THE THEATRICAL OVERLAY:
   - Fullscreen procedural 35mm film grain overlay using zero-asset SVG fractal noise with dynamic opacity (0.045).
   - Minimalist status bar: "[DIRECTOR_NAME] // REEL 2026 // [REPRESENTATION_CITY]".
   - Ambient Sound switch: "Soundtrack: Brian Eno Inspired Drone (Toggle ON/OFF)".

2. HERO STILL (THE PROLOGUE):
   - Full-bleed cinematic still with subtle slow parallax zoom (Ken Burns optical drift).
   - Monumental editorial typography: "[FLAGSHIP_FILM] — OFFICIAL SELECTION CANNES".
   - Lens telemetry badge: "ARRI Alexa Mini LF // Cooke Anamorphic /i 40mm // T2.3".

3. HORIZONTAL EXHIBITION GALLERY:
   - A buttery horizontal scroll strip showcasing 6 curated editorial stills/stills from commercial films (Nike, Saint Laurent, Apple, Independent Cinema).
   - Hovering over any still expands subtle metadata: Client, Director of Photography, Year, Aspect Ratio.

4. FULLSCREEN LIGHTBOX & EXIF DRAWER:
   - Clicking a still opens an edge-to-edge optical viewer.
   - Toggle "EXIF DATA": Slides open technical camera sheet (Shutter Angle: 180°, Sensor: 4.5K Open Gate, Color Space: ARRI LogC4, Location Coordinates).

5. REPRESENTATION & INQUIRY FOOTER:
   - Representation agency contacts across London, New York, and Tokyo.
   - Commercial booking contact form modal with direct agent phone and encrypted Signal link.
```

---

## ⚡ Runnable Starter Code Snippet: Full-Bleed Anamorphic Stills Viewer & EXIF Inspector

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Director Monograph</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #050505; color: #F4F4F5; font-family: -apple-system, sans-serif; overflow-x: hidden; }
    header { padding: 30px; display: flex; justify-content: space-between; align-items: center; position: fixed; top: 0; width: 100%; z-index: 50; background: linear-gradient(180deg, rgba(5,5,5,0.8) 0%, transparent 100%); }
    .director { font-family: 'Syne', sans-serif; font-size: 1.1rem; letter-spacing: 0.15em; text-transform: uppercase; font-weight: 700; }
    .status { font-family: monospace; font-size: 0.75rem; color: #71717A; }
    .gallery-container { height: 100vh; display: flex; align-items: center; padding: 0 60px; gap: 40px; overflow-x: auto; scroll-snap-type: x mandatory; }
    .film-card { flex: 0 0 70vw; max-width: 900px; height: 55vh; background: #111; border-radius: 4px; overflow: hidden; position: relative; scroll-snap-align: center; border: 1px solid rgba(255,255,255,0.08); transition: transform 0.3s; }
    .film-card:hover { transform: scale(1.01); border-color: rgba(255,255,255,0.25); }
    .film-visual { width: 100%; height: 100%; object-fit: cover; filter: contrast(1.1) brightness(0.9); }
    .film-info { position: absolute; bottom: 0; left: 0; right: 0; padding: 24px; background: linear-gradient(0deg, rgba(0,0,0,0.9) 0%, transparent 100%); display: flex; justify-content: space-between; align-items: flex-end; }
    .film-title { font-family: 'Playfair Display', serif; font-size: 1.8rem; font-style: italic; }
    .exif-btn { background: rgba(255,255,255,0.1); border: 1px solid rgba(255,255,255,0.2); color: #FFF; padding: 6px 14px; border-radius: 4px; font-family: monospace; font-size: 0.75rem; cursor: pointer; }
    .exif-btn:hover { background: #FFF; color: #000; }
    .exif-modal { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.85); z-index: 100; align-items: center; justify-content: center; }
    .exif-box { background: #111; border: 1px solid #333; padding: 30px; border-radius: 8px; width: 90%; max-width: 440px; font-family: monospace; }
  </style>
</head>
<body>
  <header>
    <div class="director">Mateo Korda</div>
    <div class="status">REPRESENTATION: LONDON // TOKYO</div>
  </header>

  <div class="gallery-container">
    <div class="film-card">
      <div style="width: 100%; height: 100%; background: linear-gradient(135deg, #1c1917, #0f172a); display: flex; align-items: center; justify-content: center; color: #475569; font-size: 2rem; font-family: serif;">
        [ Anamorphic Still: Nocturne in Silver ]
      </div>
      <div class="film-info">
        <div>
          <div style="font-size: 0.75rem; color: #E11D48; letter-spacing: 0.1em; text-transform: uppercase;">A24 Narrative Short</div>
          <div class="film-title">Nocturne in Silver (2025)</div>
        </div>
        <button class="exif-btn" onclick="openExif('Cooke Anamorphic 40mm T2.3', 'ARRI Alexa Mini LF', 'ISO 800 // 1/48s', 'Kodak 5219 Emulation')">Inspect Optics</button>
      </div>
    </div>
  </div>

  <div class="exif-modal" id="exifModal" onclick="closeExif()">
    <div class="exif-box" onclick="event.stopPropagation()">
      <h3 style="color: #E11D48; margin-bottom: 16px; font-size: 0.9rem;">OPTICAL & CAMERA TELEMETRY</h3>
      <p id="exifDetails" style="font-size: 0.85rem; line-height: 1.8; color: #D4D4D8;"></p>
      <button class="exif-btn" style="margin-top: 20px; width: 100%;" onclick="closeExif()">Close Telemetry</button>
    </div>
  </div>

  <script>
    function openExif(lens, camera, exp, lut) {
      document.getElementById('exifDetails').innerHTML = `
        <strong>LENS:</strong> ${lens}<br>
        <strong>SENSOR:</strong> ${camera}<br>
        <strong>EXPOSURE:</strong> ${exp}<br>
        <strong>COLOR PIPELINE:</strong> ${lut}
      `;
      document.getElementById('exifModal').style.display = 'flex';
    }
    function closeExif() {
      document.getElementById('exifModal').style.display = 'none';
    }
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] Images load via modern WebP / AVIF formats with responsive `srcset` resolutions.
- [ ] Horizontal gallery supports both mouse wheel horizontal panning and touch gestures.
- [ ] Film grain noise runs on GPU with CSS pseudo-elements to avoid CPU main-thread throttling.
