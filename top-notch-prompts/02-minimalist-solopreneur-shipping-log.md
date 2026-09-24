# ⚡ Blueprint 02: Minimalist Solopreneur & Indie Hacker Ship Log

[![Category](https://img.shields.io/badge/Category-Indie%20Hacker%20%26%20Founder-00F0FF?style=for-the-badge)](./02-minimalist-solopreneur-shipping-log.md)
[![Standard](https://img.shields.io/badge/Standard-Levels.io%20%2F%20Linear%20Speed-10B981?style=for-the-badge)](./02-minimalist-solopreneur-shipping-log.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-High--Velocity%20Brutalist-FF6B00?style=for-the-badge)](./02-minimalist-solopreneur-shipping-log.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **indie hackers, bootstrapper founders, solopreneurs, and micro-SaaS builders** (similar to Pieter Levels, Danny Postma, Marc Lou, and Tony Dinh) who ship multiple revenue-generating products in public.

**Primary Objective:**  
To establish raw founder credibility and authentic transparency through live revenue telemetry, chronological public shipping logs, and zero-bullshit minimalist design.

---

## 💡 Why To Use This Blueprint
Standard AI models fail catastrophically when generating founder personal sites:
- They write pretentious corporate mission statements: *"Synergizing digital transformations through agile paradigms."*
- They hide metrics behind buzzwords instead of showing real shipped products, user counts, and revenue.
- They generate slow, bloated templates loaded with 10MB of stock illustrations.

**How This Blueprint Solves It:**
1. **Live Business Telemetry Ribbon:** Displays verified live MRR (Monthly Recurring Revenue), total active customers, and uptime.
2. **Chronological "Ship Log" Matrix:** An interactive changelog timeline tracking every product release, pivot, and milestone with status tags (`#SHIPPED`, `#BETA`, `#ACQUIRED`, `#SUNSET`).
3. **Keyboard Quick-Jump Command Menu:** Press `Cmd+K` / `Ctrl+K` to instantly filter products by stack (Next.js, Python, Mobile, Chrome Extension).
4. **Stark High-Contrast Typography:** High-speed monochromatic brutalism with zero bloat and near-instant sub-50ms page load times.

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[YOUR_HANDLE]` with your online alias or name (e.g. `@founder_dev`).
- Replace `[TOTAL_MRR]` with your current recurring revenue (e.g. `$42,800/mo`).
- Replace `[FLAGSHIP_PRODUCT]` with your top product (e.g. *AutoDoc AI*).
- Replace `[PRODUCTS_SHIPPED_COUNT]` with total projects built (e.g. *14 products in 24 months*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Palette Tokens */
  --bg-canvas: #0A0A0C;
  --bg-card: #121215;
  --bg-badge: #1A1A1F;
  --accent-green: #22C55E;
  --accent-amber: #F59E0B;
  --text-main: #FAFAFA;
  --text-dim: #71717A;
  --border-subtle: #27272A;

  /* Typography */
  --font-display: 'Inter', -apple-system, sans-serif;
  --font-mono: 'JetBrains Mono', 'SF Mono', monospace;

  /* Elevation */
  --card-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as a Principal Design Technologist specializing in ultra-fast, high-velocity indie hacker personal sites (Levels.io / Dan Abramov / Linear caliber).
Create a high-impact, transparent personal portfolio and public ship log for [YOUR_HANDLE], a solo founder who has built [PRODUCTS_SHIPPED_COUNT].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER write corporate buzzwords ("synergy", "paradigm", "passionate problem solver").
- NEVER use cartoon illustrations, stock vectors, or rounded playful candy buttons.
- NEVER hide metrics. Every product card must display either revenue, user count, or launch status.
- NEVER build a bloated multi-page site. Everything must be accessible on one blazing-fast, keyboard-navigable single-page document.
- NEVER use slow JavaScript animations that cause layout shifts (CLS).

REQUIRED CORE SECTIONS:
1. RAW HEADER & LIVE TELEMETRY BAR:
   - Left: [YOUR_HANDLE] with a glowing green status dot: "ONLINE // CODING NEW FEATURE".
   - Right: Live counter pills:
     * "LIVE MRR: [TOTAL_MRR]"
     * "TOTAL CUSTOMERS: 18,400+"
     * "BOOTSTRAPPED: 100% INDEPENDENT"

2. CANDID FOUNDER ELEVATOR NOTE:
   - 2-sentence candid statement: "I build software that makes money while solving specific problems. No venture capital, no 50-person meetings, just code shipped directly to users."
   - Action Links: "Read My Rules of Bootstrapping", "Subscribe to Ship RSS", "Follow on X/Twitter".

3. INTERACTIVE PRODUCT FLEET (FILTERABLE BENTO):
   - Interactive Stack Filter: [ALL] [SAAS] [DEV TOOLS] [MOBILE] [OPEN SOURCE].
   - Product Card 1 (Flagship): [FLAGSHIP_PRODUCT] - Metrics ($18k MRR, 4,200 users), Tech Stack badges (TypeScript, PostgreSQL, Stripe), direct 1-click external link icon.
   - Product Card 2: Micro-SaaS tool (Status: $6.4k MRR, acquired or growing).
   - Product Card 3: Free viral open-source tool (Status: 12k GitHub Stars).
   - Product Card 4: Sunsetted experiment (Status: FAILED // Post-mortem notes linked).

4. CHRONOLOGICAL PUBLIC SHIP LOG (CHANGELOG STYLE):
   - A timeline table of recent releases with dates, version tags (e.g. v2.4.0), and 1-line release summaries.
   - Clickable row expansion showing release highlights.

5. KEYBOARD COMMAND PALETTE (CMD+K / CTRL+K):
   - Pressing Cmd+K opens a clean modal to search shipped projects, copy founder email, or jump to social links.

6. TACTILE FOOTER:
   - "Built with pure HTML/CSS/JS. Zero trackers. Page size < 80kb. Deployed to edge."
   - 1-click "Copy Contact Info" button with animated checkmark toast.
```

---

## ⚡ Runnable Starter Code Snippet: Interactive Public Ship Log & Telemetry

Paste this code into an `index.html` to test the live telemetry counters and interactive filterable ship log:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Indie Founder Ship Log</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #0A0A0C; color: #FAFAFA; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; padding: 40px 20px; max-width: 860px; margin: 0 auto; line-height: 1.5; }
    header { display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid #27272A; padding-bottom: 24px; margin-bottom: 32px; flex-wrap: wrap; gap: 16px; }
    .brand { font-size: 1.25rem; font-weight: 700; font-family: monospace; display: flex; align-items: center; gap: 10px; }
    .status-dot { width: 8px; height: 8px; border-radius: 50%; background: #22C55E; box-shadow: 0 0 10px #22C55E; }
    .telemetry { display: flex; gap: 12px; font-family: monospace; font-size: 0.8rem; }
    .telemetry-item { background: #18181B; border: 1px solid #27272A; padding: 6px 12px; border-radius: 6px; }
    .telemetry-item span { color: #22C55E; font-weight: bold; }
    .intro { margin-bottom: 40px; font-size: 1.15rem; color: #A1A1AA; }
    .filter-tabs { display: flex; gap: 8px; margin-bottom: 24px; }
    .filter-btn { background: #121215; border: 1px solid #27272A; color: #71717A; padding: 6px 14px; border-radius: 6px; cursor: pointer; font-size: 0.85rem; font-family: monospace; transition: all 0.2s; }
    .filter-btn.active, .filter-btn:hover { background: #27272A; color: #FAFAFA; border-color: #3F3F46; }
    .products-grid { display: flex; flex-direction: column; gap: 12px; }
    .product-row { background: #121215; border: 1px solid #27272A; border-radius: 8px; padding: 18px 20px; display: flex; justify-content: space-between; align-items: center; transition: transform 0.15s, border-color 0.15s; text-decoration: none; color: inherit; }
    .product-row:hover { transform: translateY(-2px); border-color: #52525B; }
    .product-info h3 { font-size: 1.05rem; font-weight: 600; display: flex; align-items: center; gap: 10px; }
    .product-info p { font-size: 0.85rem; color: #71717A; margin-top: 4px; }
    .pill { font-size: 0.7rem; font-family: monospace; padding: 3px 8px; border-radius: 4px; text-transform: uppercase; }
    .pill-live { background: rgba(34, 197, 94, 0.12); color: #22C55E; border: 1px solid rgba(34, 197, 94, 0.3); }
    .pill-sunset { background: rgba(239, 68, 68, 0.12); color: #EF4444; border: 1px solid rgba(239, 68, 68, 0.3); }
    .product-metrics { text-align: right; font-family: monospace; font-size: 0.9rem; }
    .product-metrics .mrr { color: #22C55E; font-weight: bold; }
    .product-metrics .users { color: #71717A; font-size: 0.75rem; margin-top: 2px; }
  </style>
</head>
<body>
  <header>
    <div class="brand"><span class="status-dot"></span> @levels_shipper</div>
    <div class="telemetry">
      <div class="telemetry-item">MRR: <span>$48,200</span></div>
      <div class="telemetry-item">ACTIVE USERS: <span>34,100</span></div>
    </div>
  </header>

  <p class="intro">Building independent web applications without funding or employees. Every project is bootstrapped and documented in public.</p>

  <div class="filter-tabs">
    <button class="filter-btn active" onclick="filterCategory('all')">ALL (4)</button>
    <button class="filter-btn" onclick="filterCategory('saas')">SAAS (2)</button>
    <button class="filter-btn" onclick="filterCategory('tools')">TOOLS (2)</button>
  </div>

  <div class="products-grid" id="productGrid">
    <a href="#" class="product-row" data-cat="saas">
      <div class="product-info">
        <h3>AutoInvoice AI <span class="pill pill-live">PROFITABLE</span></h3>
        <p>Zero-effort PDF invoice parsing for European VAT compliance.</p>
      </div>
      <div class="product-metrics">
        <div class="mrr">$31,500/mo</div>
        <div class="users">2,410 paying teams</div>
      </div>
    </a>

    <a href="#" class="product-row" data-cat="saas">
      <div class="product-info">
        <h3>SubPulse <span class="pill pill-live">GROWING</span></h3>
        <p>Stripe churn early-warning telemetry engine for bootstrappers.</p>
      </div>
      <div class="product-metrics">
        <div class="mrr">$14,200/mo</div>
        <div class="users">890 customers</div>
      </div>
    </a>

    <a href="#" class="product-row" data-cat="tools">
      <div class="product-info">
        <h3>CSS Mesh Studio <span class="pill pill-live">FREE TOOL</span></h3>
        <p>In-browser SVG gradient mesh generator. 40k monthly visitors.</p>
      </div>
      <div class="product-metrics">
        <div class="mrr">$2,500/mo (Sponsors)</div>
        <div class="users">38,000 MAU</div>
      </div>
    </a>

    <a href="#" class="product-row" data-cat="tools">
      <div class="product-info">
        <h3>CryptoTaxBot <span class="pill pill-sunset">SUNSETTED</span></h3>
        <p>Automated DeFi transaction ledger. Archived after API deprecations.</p>
      </div>
      <div class="product-metrics">
        <div class="mrr">$0</div>
        <div class="users">Post-Mortem Published</div>
      </div>
    </a>
  </div>

  <script>
    function filterCategory(cat) {
      document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
      event.target.classList.add('active');
      const rows = document.querySelectorAll('.product-row');
      rows.forEach(row => {
        if (cat === 'all' || row.dataset.cat === cat) {
          row.style.display = 'flex';
        } else {
          row.style.display = 'none';
        }
      });
    }
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] Complete page weight under 100 KB total assets.
- [ ] First Contentful Paint (FCP) under 300ms on 4G cellular connections.
- [ ] Keyboard accessible: users can cycle through products using `Tab` and filter using hotkeys.
- [ ] Every external product link opens securely with `rel="noopener noreferrer"`.
- [ ] All revenue and user metrics are clearly differentiated from marketing claims.
