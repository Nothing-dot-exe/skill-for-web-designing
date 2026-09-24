# 🌟 Blueprint 01: Creative Developer & WebGL Shader Atelier

[![Category](https://img.shields.io/badge/Category-Personal%20Creative%20Portfolio-00F0FF?style=for-the-badge)](./01-creative-developer-3d-atelier.md)
[![Standard](https://img.shields.io/badge/Standard-Awwwards%20Site%20of%20the%20Day-A855F7?style=for-the-badge)](./01-creative-developer-3d-atelier.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-Kinetic%20Dark%20Craft-FF6B00?style=for-the-badge)](./01-creative-developer-3d-atelier.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **creative technologists, front-end design engineers, WebGL/Three.js artists, and interactive UI developers** who need a show-stopping personal portfolio (on par with Bruno Simon, Yuri Artiukh, Active Theory, and Aristide Benoist).

**Primary Objective:**  
To immediately captivate design directors, founders of high-growth tech startups, and premium agency recruiters within the first 3 seconds through fluid physics, bespoke cursor choreography, and kinetic typography.

---

## 💡 Why To Use This Blueprint
When you ask standard AI models for a "developer portfolio", they generate disastrous cliches:
- *"Hi, I'm Alex! I'm a passionate full-stack developer who loves creating intuitive digital experiences."*
- Generic 3-card grid with blue font, standard GitHub and LinkedIn SVG logos, and zero personality.
- Static, lifeless layouts that look like a junior university bootcamp project.

**How This Blueprint Solves It:**
1. **Kinetic Hero Canvas:** Features an interactive ambient particle wave canvas that reacts organically to mouse velocity and touch drags.
2. **Magnetic Cursor Dynamics:** Replaces the default OS pointer with an ultra-smooth dual-ring magnetic cursor with spring physics.
3. **Interactive Project Drawer & Showcase:** Case studies open in fluid side drawers with live code sandboxes, shader controls, and tech stacks.
4. **Bespoke Audio Haptics:** Subtle synthesized micro-clicks on hover and tab shifts using the native Web Audio API (no external MP3 files).

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[YOUR_NAME]` with your full name or personal handle (e.g. *Elena Rostova*).
- Replace `[CREATIVE_TITLE]` with your exact discipline (e.g. *Creative Technologist & WebGL Shader Artist*).
- Replace `[FLAGSHIP_PROJECT_1]` with your premier work (e.g. *Awwwards SOTD Quantum Simulation*).
- Replace `[LOCATION_TIMEZONE]` with your home base (e.g. *Berlin // UTC+1*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Color Tokens */
  --bg-deep: #050608;
  --bg-surface: #0c0e14;
  --bg-surface-hover: #141722;
  --accent-cyan: #00F0FF;
  --accent-lime: #CCFF00;
  --text-primary: #F0F3F8;
  --text-muted: #7E869E;
  --border-specular: rgba(255, 255, 255, 0.12);
  --border-highlight: rgba(0, 240, 255, 0.4);

  /* Fluid Typography Scale */
  --font-hero: clamp(2.5rem, 7vw, 6.5rem);
  --font-title: clamp(1.75rem, 3.5vw, 3rem);
  --font-body: clamp(0.95rem, 1.2vw, 1.1rem);
  --font-mono: 'JetBrains Mono', monospace;

  /* Multi-Layer Bézier Elevation */
  --shadow-float: 0 10px 30px -10px rgba(0, 240, 255, 0.15),
                  0 20px 50px -20px rgba(0, 0, 0, 0.8);
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as a world-renowned Creative Technologist and Awwwards Jury Member.
Build an avant-garde personal creative developer portfolio for [YOUR_NAME], [CREATIVE_TITLE] based in [LOCATION_TIMEZONE].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER output greeting cliches: "Hi, I am [Name], a passionate developer who loves code".
- NEVER use flat rectangular 3-card project grids with generic GitHub octocat icons.
- NEVER use standard browser scrollbars. Provide custom styled translucent scroll indicators.
- NEVER leave fake links or dead buttons. Every project card must open an interactive modal or drawer with live tech tags and breakdown.
- NEVER use generic purple-to-blue linear gradients. Use curated obsidian black (#050608) with electric cyan (#00F0FF) and reactive acid lime (#CCFF00).

CORE SECTIONS TO ASSEMBLE:
1. TOP STATUS BAR (EDITORIAL HEADLINE):
   - Left: [YOUR_NAME] with pulsating live status dot ("AVAILABLE FOR Q2/Q3 SELECT PROJECTS").
   - Center: Live local time indicator with seconds counter ([LOCATION_TIMEZONE]).
   - Right: Minimalist sound toggle ("SFX: ON/OFF") and Quick Contact trigger.

2. HERO SHOWCASE (INTERACTIVE PARTICLE CANVAS):
   - Monumental editorial typography: "[CREATIVE_TITLE] CRAFTING MATHEMATICAL POETRY THROUGH WEBGL & CODE".
   - Fullscreen HTML5 interactive canvas background: Generative floating particle network that ripples and pushes away upon mouse cursor velocity.
   - Micro-badges: "WebGL 2.0", "Custom Shaders", "Physics Engines", "Design Systems".
   - Primary Call to Action: "Explore Experiments" with glowing specular trail.

3. CURATED FLAGSHIP WORKS (BENTO EXHIBIT):
   - Card 1 (Span 8): [FLAGSHIP_PROJECT_1] - Interactive 3D tilt preview with real-time FPS counter, client name, and GLSL shader code preview tab.
   - Card 2 (Span 4): "WebGL Lab & Experiments" - Interactive mini-canvas displaying a live rotating wireframe torus or generative wave.
   - Card 3 (Span 4): "Philosophy & Toolchain" - Stack breakdown (Three.js, WebGPU, GLSL, Web Audio, TypeScript, GSAP).
   - Card 4 (Span 8): Interactive Experience Timeline showing agency collaborations and global design awards.

4. REAL-TIME INTERACTION MECHANICS:
   - Custom magnetic cursor that expands with a glass blur when hovering over interactive cards.
   - 3D card tilt with cursor-following radial spotlight sheen.
   - Web Audio API synthesizer generating delicate 800Hz / 1200Hz tactile blips on card clicks.

5. FOOTER ARCHETYPE:
   - Giant typographic send-off: "LET'S BUILD SOMETHING EXTRAORDINARY".
   - 1-click clipboard email copy with visual floating toast confirmation: "Email copied to clipboard (ready to paste)".
   - Social links formatted as crisp terminal badges: GitHub, Twitter/X, ReadCV, ShaderToy.
```

---

## ⚡ Runnable Starter Code Snippet: Signature Magnetic Particle Hero

Paste this standalone snippet into an HTML file to immediately test the fluid particle hero and custom magnetic cursor:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Creative Developer Particle Hero</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #050608; color: #F0F3F8; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; overflow: hidden; height: 100vh; }
    canvas { position: absolute; inset: 0; z-index: 1; }
    .hero-content { position: relative; z-index: 2; height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; pointer-events: none; }
    .badge { display: inline-flex; align-items: center; gap: 8px; padding: 6px 14px; background: rgba(0, 240, 255, 0.08); border: 1px solid rgba(0, 240, 255, 0.3); border-radius: 999px; font-size: 0.75rem; letter-spacing: 0.1em; color: #00F0FF; text-transform: uppercase; margin-bottom: 24px; }
    .pulse-dot { width: 6px; height: 6px; border-radius: 50%; background: #00F0FF; box-shadow: 0 0 10px #00F0FF; animation: pulse 2s infinite; }
    @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.3; } }
    h1 { font-size: clamp(2.5rem, 6vw, 5.5rem); font-weight: 800; letter-spacing: -0.04em; line-height: 1; max-width: 900px; margin-bottom: 20px; background: linear-gradient(180deg, #FFFFFF 0%, #7E869E 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
    p { font-size: 1.1rem; color: #7E869E; max-width: 550px; line-height: 1.6; }
    .btn-wrap { margin-top: 36px; pointer-events: auto; }
    .cta-btn { padding: 14px 28px; background: #00F0FF; color: #050608; font-weight: 700; font-size: 0.95rem; border: none; border-radius: 8px; cursor: pointer; transition: transform 0.2s cubic-bezier(0.16, 1, 0.3, 1), box-shadow 0.2s ease; }
    .cta-btn:hover { transform: translateY(-2px) scale(1.03); box-shadow: 0 10px 30px rgba(0, 240, 255, 0.4); }
  </style>
</head>
<body>
  <canvas id="particleCanvas"></canvas>
  <div class="hero-content">
    <div class="badge"><span class="pulse-dot"></span> Available for Select Q2 Engagements</div>
    <h1>ARCHITECTING DIGITAL REALITIES</h1>
    <p>Exploring the frontiers of real-time 3D shaders, creative technology, and tactile interaction design.</p>
    <div class="btn-wrap">
      <button class="cta-btn" onclick="alert('Exploring creative works...')">Explore Portfolio</button>
    </div>
  </div>

  <script>
    const canvas = document.getElementById('particleCanvas');
    const ctx = canvas.getContext('2d');
    let width = canvas.width = window.innerWidth;
    let height = canvas.height = window.innerHeight;
    const particles = [];
    const mouse = { x: width / 2, y: height / 2, radius: 140 };

    window.addEventListener('resize', () => {
      width = canvas.width = window.innerWidth;
      height = canvas.height = window.innerHeight;
    });
    window.addEventListener('mousemove', (e) => {
      mouse.x = e.clientX;
      mouse.y = e.clientY;
    });

    for (let i = 0; i < 90; i++) {
      particles.push({
        x: Math.random() * width,
        y: Math.random() * height,
        vx: (Math.random() - 0.5) * 0.8,
        vy: (Math.random() - 0.5) * 0.8,
        size: Math.random() * 2 + 1,
        baseX: Math.random() * width,
        baseY: Math.random() * height
      });
    }

    function animate() {
      ctx.clearRect(0, 0, width, height);
      for (let i = 0; i < particles.length; i++) {
        let p = particles[i];
        p.x += p.vx;
        p.y += p.vy;
        if (p.x < 0 || p.x > width) p.vx *= -1;
        if (p.y < 0 || p.y > height) p.vy *= -1;

        let dx = mouse.x - p.x;
        let dy = mouse.y - p.y;
        let dist = Math.sqrt(dx * dx + dy * dy);
        if (dist < mouse.radius) {
          let force = (mouse.radius - dist) / mouse.radius;
          p.x -= (dx / dist) * force * 5;
          p.y -= (dy / dist) * force * 5;
        }

        ctx.fillStyle = 'rgba(0, 240, 255, 0.65)';
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
        ctx.fill();

        for (let j = i + 1; j < particles.length; j++) {
          let p2 = particles[j];
          let dist2 = Math.hypot(p.x - p2.x, p.y - p2.y);
          if (dist2 < 110) {
            ctx.strokeStyle = `rgba(0, 240, 255, ${0.25 * (1 - dist2 / 110)})`;
            ctx.lineWidth = 0.8;
            ctx.beginPath();
            ctx.moveTo(p.x, p.y);
            ctx.lineTo(p2.x, p2.y);
            ctx.stroke();
          }
        }
      }
      requestAnimationFrame(animate);
    }
    animate();
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] Canvas resizes dynamically without stretching pixel aspect ratio (`window.devicePixelRatio` handled).
- [ ] Typography passes WCAG 2.1 AA contrast ratio (minimum 4.5:1 for body copy against `#050608`).
- [ ] Sound haptics fail gracefully when browser audio context is blocked by autoplay policies.
- [ ] Zero dead buttons; all project cards trigger modal windows or outbound case study tabs.
- [ ] Complete mobile responsiveness down to 360px portrait without horizontal screen blowout.
