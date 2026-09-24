# 💻 Blueprint 04: Cyber-Minimalist Interactive CLI Terminal & CV

[![Category](https://img.shields.io/badge/Category-Interactive%20Terminal%20Resume-00F0FF?style=for-the-badge)](./04-interactive-terminal-resume-cv.md)
[![Standard](https://img.shields.io/badge/Standard-Staff%20Engineer%20%2F%20Kernel%20Hacker-10B981?style=for-the-badge)](./04-interactive-terminal-resume-cv.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-Phosphor%20Green%20Matrix%20CLI-22C55E?style=for-the-badge)](./04-interactive-terminal-resume-cv.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **Staff/Principal Software Engineers, Linux Kernel Developers, Cybersecurity Researchers, and DevOps/SRE Architects** who want to prove their technical depth by presenting their career as a fully functional, interactive in-browser bash terminal shell.

**Primary Objective:**  
To immediately signal deep systems competence, command-line mastery, and retro-futuristic hacker aesthetics to engineering VPs, CTOs, and technical hiring teams.

---

## 💡 Why To Use This Blueprint
Most software engineer resumes are boring PDF documents or generic React templates that feel childish:
- Standard progress bars showing "JavaScript: 90%" (meaningless, amateurish metric).
- Walls of unformatted text listing 50 frameworks.
- No interactive proof of actual coding capability.

**How This Blueprint Solves It:**
1. **Fully Functional Interactive Command Line:** Visitors can type real commands (`help`, `cat skills.txt`, `ls projects/`, `history`, `clear`, `sudo hire`).
2. **Tab-Completion & Command History:** Implements arrow key history (`↑` and `↓`) and `Tab` key auto-completion for an authentic UNIX developer experience.
3. **ASCII Art Avatar & System Specs:** Displays a stylized ASCII portrait alongside live browser telemetry (User Agent, Screen Resolution, Memory status, OS detection).
4. **1-Click Executive PDF Exporter:** For non-technical recruiters who just want a traditional resume, a dedicated `download-pdf` command triggers a clean print-ready document.

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[DEVELOPER_HANDLE]` with your terminal username (e.g. `root@valkyrie`).
- Replace `[CURRENT_ROLE]` with your senior title (e.g. *Principal Distributed Systems Architect*).
- Replace `[CORE_STACK]` with your core languages (e.g. *Rust, Go, eBPF, Kubernetes, C++*).
- Replace `[YEARS_EXP]` with your experience length (e.g. *11+ years*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Terminal Matrix Palette */
  --term-bg: #0C0D10;
  --term-chrome: #16181F;
  --term-green: #39FF14;
  --term-cyan: #00F0FF;
  --term-amber: #FFB000;
  --term-text: #E2E8F0;
  --term-dim: #64748B;

  /* Typography */
  --font-terminal: 'JetBrains Mono', 'Fira Code', 'Courier New', monospace;
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as a Principal Systems Engineer and Retro-Terminal UI Specialist.
Build a premier, fully interactive Web Terminal CV & Personal Shell for [DEVELOPER_HANDLE], [CURRENT_ROLE] specializing in [CORE_STACK].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER use fake non-functional terminal mockups. The command input MUST accept real typing, process commands, and print colored stdout.
- NEVER use generic percentage bars for skills ("Python 85%"). Skills must be organized by systems domain with real production accomplishments.
- NEVER break keyboard navigation. Users must be able to navigate using Tab for auto-completion and Arrow Up/Down for command history.
- NEVER use generic blinding green text everywhere. Use a nuanced phosphor palette (#39FF14 for prompt, #00F0FF for links, #FFB000 for warnings, #E2E8F0 for body text) on a deep obsidian terminal (#0C0D10).

CORE TERMINAL FEATURES & COMMANDS TO IMPLEMENT:
1. TERMINAL WINDOW CHROME:
   - Mac/Linux-style window header with Close, Minimize, Maximize dots.
   - Title bar: "[DEVELOPER_HANDLE]: ~/career_archive (bash - 80x24)".
   - Quick-action buttons in header: [Download PDF Resume] [Toggle Fullscreen] [Copy Email].

2. INITIAL BOOT SEQUENCE (ON PAGE LOAD):
   - Fast simulated kernel boot log:
     * "[OK] Initializing kernel subsystems..."
     * "[OK] Loading career modules: [CORE_STACK]"
     * "[OK] Network interfaces bound. Host: [DEVELOPER_HANDLE]"
   - ASCII Art Banner of developer's initials or handle.
   - Type `help` or click suggested commands below: `about`, `experience`, `projects`, `skills`, `contact`, `clear`.

3. COMMAND REGISTRY (PARSED BY JAVASCRIPT):
   - `help`: Lists all available commands with short descriptions.
   - `about`: Prints biographical summary, years of engineering, and architectural philosophy.
   - `experience`: Outputs career timeline in a clean formatted ASCII table with company names, roles, and impact metrics.
   - `projects`: Lists flagship open-source repositories and distributed systems with direct clickable URLs.
   - `skills`: Categorizes technical proficiencies (Distributed Systems, Low-Level, Cloud/Infra, Observability).
   - `sudo hire`: Playful Easter egg prompting for a recruiter confirmation, then reveals private contact scheduling link.
   - `clear`: Clears the screen buffer.

4. SUGGESTED COMMAND PILLS:
   - For mobile or non-keyboard users, provide clickable pills at the bottom (e.g. `[about]` `[experience]` `[projects]` `[contact]`) that auto-type and execute the command.
```

---

## ⚡ Runnable Starter Code Snippet: Interactive Bash Shell Engine

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Terminal Resume</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #08090C; color: #E2E8F0; font-family: 'Courier New', Courier, monospace; padding: 24px; min-height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; }
    .term-window { width: 100%; max-width: 820px; background: #0C0D10; border: 1px solid #1E222D; border-radius: 8px; box-shadow: 0 20px 50px rgba(0,0,0,0.8); overflow: hidden; display: flex; flex-direction: column; height: 520px; }
    .term-bar { background: #16181F; padding: 10px 14px; display: flex; align-items: center; gap: 8px; border-bottom: 1px solid #1E222D; }
    .dot { width: 10px; height: 10px; border-radius: 50%; display: inline-block; }
    .dot-red { background: #EF4444; } .dot-yellow { background: #F59E0B; } .dot-green { background: #10B981; }
    .term-title { margin-left: auto; margin-right: auto; font-size: 0.75rem; color: #64748B; letter-spacing: 0.05em; }
    .term-body { padding: 18px; flex: 1; overflow-y: auto; font-size: 0.9rem; line-height: 1.6; }
    .line-green { color: #39FF14; }
    .line-cyan { color: #00F0FF; }
    .line-dim { color: #64748B; }
    .input-line { display: flex; align-items: center; margin-top: 8px; }
    .prompt { color: #39FF14; font-weight: bold; margin-right: 8px; white-space: nowrap; }
    #cliInput { background: transparent; border: none; color: #FFFFFF; font-family: inherit; font-size: inherit; flex: 1; outline: none; }
    .quick-chips { display: flex; gap: 6px; padding: 10px 14px; background: #101217; border-top: 1px solid #1E222D; flex-wrap: wrap; }
    .chip { background: #1A1D26; color: #00F0FF; border: 1px solid #272B38; padding: 3px 10px; border-radius: 4px; font-size: 0.75rem; cursor: pointer; }
    .chip:hover { background: #00F0FF; color: #0C0D10; }
  </style>
</head>
<body>
  <div class="term-window">
    <div class="term-bar">
      <span class="dot dot-red"></span>
      <span class="dot dot-yellow"></span>
      <span class="dot dot-green"></span>
      <div class="term-title">alex@systems-host: ~/career (bash)</div>
    </div>
    <div class="term-body" id="termOutput">
      <div class="line-dim">[System Initialized - Linux 6.8.0-sys x86_64]</div>
      <div class="line-green">Alex Sterling // Principal Systems Engineer</div>
      <div class="line-dim">Type 'help' to inspect commands or click the chips below.</div>
      <br>
    </div>
    <div class="quick-chips">
      <button class="chip" onclick="runChip('about')">about</button>
      <button class="chip" onclick="runChip('experience')">experience</button>
      <button class="chip" onclick="runChip('skills')">skills</button>
      <button class="chip" onclick="runChip('contact')">contact</button>
      <button class="chip" onclick="runChip('clear')">clear</button>
    </div>
    <div style="padding: 0 18px 14px 18px;">
      <div class="input-line">
        <span class="prompt">guest@systems:~$</span>
        <input type="text" id="cliInput" autofocus autocomplete="off" spellcheck="false">
      </div>
    </div>
  </div>

  <script>
    const output = document.getElementById('termOutput');
    const input = document.getElementById('cliInput');

    const COMMANDS = {
      help: "Available commands:\n  about       - Biography and engineering philosophy\n  experience  - Career timeline and key roles\n  skills      - Technical proficiencies and systems\n  contact     - Reach out via encrypted channels\n  clear       - Clear the screen buffer",
      about: "Alex Sterling - 11+ years engineering high-throughput distributed systems.\nLead architect on consensus protocols and low-latency storage engines handling 4M+ ops/sec.",
      experience: "2023-Present: Principal Architect @ Sovereign Data (Rust, Raft, eBPF)\n2019-2023: Staff Infrastructure Engineer @ CloudScale (Go, Kubernetes, Envoy)\n2015-2019: Distributed Systems Engineer @ TelemetryCore",
      skills: "Languages: Rust, Go, C++, Zig, TypeScript\nSystems: Linux Kernel, eBPF, Raft/Paxos, RocksDB, DPDK, Kubernetes",
      contact: "Email: alex@sterling-systems.io\nPGP: 4A89 2F90 E12B 87CD\nGitHub: github.com/sterling-sys"
    };

    function execute(cmd) {
      cmd = cmd.trim().toLowerCase();
      if (!cmd) return;
      
      const cmdLine = document.createElement('div');
      cmdLine.innerHTML = `<span class="prompt">guest@systems:~$</span> ${cmd}`;
      output.appendChild(cmdLine);

      if (cmd === 'clear') {
        output.innerHTML = '';
      } else if (COMMANDS[cmd]) {
        const res = document.createElement('div');
        res.className = 'line-cyan';
        res.style.whiteSpace = 'pre-line';
        res.innerText = COMMANDS[cmd];
        output.appendChild(res);
      } else {
        const err = document.createElement('div');
        err.style.color = '#EF4444';
        err.innerText = `bash: command not found: ${cmd}. Type 'help' for available commands.`;
        output.appendChild(err);
      }
      output.scrollTop = output.scrollHeight;
    }

    input.addEventListener('keydown', (e) => {
      if (e.key === 'Enter') {
        execute(input.value);
        input.value = '';
      }
    });

    function runChip(cmd) {
      execute(cmd);
    }
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] Mobile users can navigate the terminal without needing to summon their software keyboard (via clickable command chips).
- [ ] Terminal auto-scrolls down smoothly when lengthy command outputs are rendered.
- [ ] No `eval()` or dangerous script execution in the command parser.
- [ ] High-contrast terminal green/cyan colors meet WCAG AAA requirements against `#0C0D10`.
