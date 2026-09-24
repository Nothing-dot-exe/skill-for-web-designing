# 🎛️ Blueprint 10: Interactive Audio Engineer & Game Sound Designer Reel

[![Category](https://img.shields.io/badge/Category-Sound%20Designer%20%26%20Audio%20Portfolio-00F0FF?style=for-the-badge)](./10-audio-sound-designer-interactive-reel.md)
[![Standard](https://img.shields.io/badge/Standard-Ableton%20%2F%20Teenage%20Engineering%20Caliber-A855F7?style=for-the-badge)](./10-audio-sound-designer-interactive-reel.md)
[![Aesthetic](https://img.shields.io/badge/Aesthetic-Tactile%20Hardware%20Groovebox-EC4899?style=for-the-badge)](./10-audio-sound-designer-interactive-reel.md)

---

## 🎯 For What This Blueprint Is Built
This blueprint is engineered for **interactive audio directors, game sound designers, synthesizer patch designers, and film composers** (working in AAA games, spatial audio, and cinematic scoring) who need an audio reel that visitors can play with hands-on.

**Primary Objective:**  
To blow away audio directors at PlayStation, EA, Kojima Productions, and film studios by letting them dynamically solo/mute individual audio stems (Drums, Bass, Synths, Foley, Ambience) in real-time in the browser.

---

## 💡 Why To Use This Blueprint
Most composer/sound designer websites are terrible:
- They just embed an ugly SoundCloud widget.
- Visitors can't isolate the sound effects from the music to evaluate technical foley craft.
- No visual correlation between acoustic frequency and screen dynamics.

**How This Blueprint Solves It:**
1. **Interactive Multi-Track Stem Mixer Reel:** Real-time in-browser Web Audio mixer with Mute, Solo, and Volume faders for 4 separate audio layers.
2. **Live Canvas Audio Frequency Oscilloscope:** Visualizes live frequency spectrums (FFT analysis) in real-time with neon waveform blooms.
3. **Tactile Hardware Aesthetic:** Inspired by Teenage Engineering OP-1 and vintage Neve consoles with knurled knobs and mechanical toggles.
4. **Bespoke SFX Soundboard:** A 9-pad playable sampler allowing recruiters to tap custom UI clicks, creature vocalizations, and cinematic laser hits.

---

## 🛠️ How To Use This Blueprint (Vibe Coding Playbook)

### 1. Tool Compatibility
Run this prompt in **Antigravity IDE**, **Cursor**, **Claude 3.7 Sonnet**, **v0.dev**, or **Windsurf**.

### 2. Customization Parameters
- Replace `[SOUND_DESIGNER_NAME]` with your name (e.g. *Lyra Vance*).
- Replace `[PRIMARY_SPECIALTY]` with your domain (e.g. *Sci-Fi Weapon Foley & Procedural Audio DSP*).
- Replace `[FLAGSHIP_GAME]` with your premier title (e.g. *Cyberpunk: Phantom Echoes — Lead Foley Artist*).

---

## 🎨 Design System & Visual Specification

```css
:root {
  /* Hardware Console Palette */
  --console-bg: #0B0D12;
  --console-surface: #141720;
  --console-fader: #1C212E;
  --accent-pink: #EC4899;
  --accent-cyan: #06B6D4;
  --meter-green: #10B981;
  --text-main: #F8FAFC;
  --text-dim: #64748B;

  /* Typography */
  --font-hardware: 'Space Grotesk', -apple-system, sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
}
```

---

## 📋 The Copy-Paste Production Mega-Prompt

```markdown
Act as a Principal Interactive Audio Director and Creative Technologist (Ableton / Teenage Engineering caliber).
Build a tactile, interactive personal audio portfolio and stem mixer reel for [SOUND_DESIGNER_NAME], specializing in [PRIMARY_SPECIALTY].

CRITICAL NEGATIVE CONSTRAINTS (ZERO TOLERANCE):
- NEVER just paste an iframe to SoundCloud or Spotify. The visitor MUST have tactile, in-browser playback controls.
- NEVER use flat modern generic design. Emulate a tactile Scandinavian hardware instrument with knurled aluminum knobs and LED peak meters.
- NEVER play audio without user interaction (strictly respect browser autoplay security policies).

CORE SECTIONS & FUNCTIONALITY:
1. HARDWARE MASTHEAD & MASTER BUS:
   - Name & Discipline: "[SOUND_DESIGNER_NAME] // [PRIMARY_SPECIALTY]"
   - Master Transport Bar: [PLAY/PAUSE] [STOP] [BPM: 128] [MASTER VOLUME SLIDER].
   - Live Master VU Meter: Dual stereo LED bars with green/yellow/red peak indicators.

2. INTERACTIVE 4-TRACK STEM MIXER:
   - Track 1: FOLEY & IMPACTS (Swords, explosions, metallic weapon clatter).
   - Track 2: PROCEDURAL AMBIENCE (Dystopian rain, wind howl, alien ventilation).
   - Track 3: BASS & SUB-SYNTH (Analog Moog drone, 808 sub rumble).
   - Track 4: ORCHESTRAL CINEMATIC SCORE (Strings, brass stabs).
   - Each track features: Mute [M], Solo [S], Volume Slider, and real-time waveform activity bar.

3. REAL-TIME CANVAS OSCILLOSCOPE:
   - Full-width HTML5 canvas visualizing the active audio spectrum using Web Audio API AnalyserNode.

4. 9-PAD INTERACTIVE SOUNDBOARD:
   - 3x3 grid of tactile MPC-style drumpads. Pressing keys [Q, W, E, A, S, D, Z, X, C] or tapping pads triggers instant synthesized sound design effects (Laser, Cyber Shield, Mech Step, Menu Click, Drone).

5. CREDITS & STUDIO INQUIRY:
   - Interactive project list with game client logos, release dates, and DAW tools (Pro Tools, Wwise, FMOD, Reaper).
   - Direct audio lead booking calendar.
```

---

## ⚡ Runnable Starter Code Snippet: Interactive 9-Pad Synthesized Soundboard

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Audio Soundboard</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #0B0D12; color: #F8FAFC; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; padding: 40px 20px; display: flex; flex-direction: column; align-items: center; justify-content: center; min-height: 100vh; }
    .header { text-align: center; margin-bottom: 28px; }
    .badge { font-family: monospace; font-size: 0.75rem; color: #EC4899; background: rgba(236, 72, 153, 0.1); border: 1px solid rgba(236, 72, 153, 0.3); padding: 4px 10px; border-radius: 4px; display: inline-block; margin-bottom: 8px; }
    h1 { font-size: 1.8rem; font-weight: 700; }
    p { font-size: 0.85rem; color: #64748B; margin-top: 4px; }
    .soundboard { display: grid; grid-template-columns: repeat(3, 110px); gap: 14px; background: #141720; padding: 20px; border-radius: 12px; border: 1px solid rgba(255, 255, 255, 0.08); box-shadow: 0 20px 40px rgba(0,0,0,0.8); }
    .pad { height: 110px; background: #1C212E; border: 1px solid #2B3346; border-radius: 8px; display: flex; flex-direction: column; align-items: center; justify-content: center; cursor: pointer; user-select: none; transition: all 0.1s; }
    .pad:hover { border-color: #EC4899; background: #23293A; }
    .pad:active, .pad.active { transform: scale(0.94); background: #EC4899; color: #0B0D12; border-color: #EC4899; box-shadow: 0 0 20px #EC4899; }
    .pad-key { font-size: 0.7rem; font-family: monospace; color: #64748B; margin-top: 4px; }
    .pad:active .pad-key, .pad.active .pad-key { color: #0B0D12; }
    .pad-label { font-size: 0.8rem; font-weight: 600; }
  </style>
</head>
<body>
  <div class="header">
    <span class="badge">LYRA VANCE // AUDIO LAB</span>
    <h1>Interactive SFX Soundboard</h1>
    <p>Tap pads or use keyboard keys [Q, W, E, A, S, D, Z, X, C] to synthesize real-time audio.</p>
  </div>

  <div class="soundboard">
    <div class="pad" data-key="q" onclick="triggerSynth(440, 'sine', this)"><span class="pad-label">Laser</span><span class="pad-key">[Q]</span></div>
    <div class="pad" data-key="w" onclick="triggerSynth(180, 'square', this)"><span class="pad-label">Sub Drop</span><span class="pad-key">[W]</span></div>
    <div class="pad" data-key="e" onclick="triggerSynth(880, 'sawtooth', this)"><span class="pad-label">Chirp</span><span class="pad-key">[E]</span></div>
    <div class="pad" data-key="a" onclick="triggerSynth(220, 'triangle', this)"><span class="pad-label">Impact</span><span class="pad-key">[A]</span></div>
    <div class="pad" data-key="s" onclick="triggerSynth(600, 'sine', this)"><span class="pad-label">Blip</span><span class="pad-key">[S]</span></div>
    <div class="pad" data-key="d" onclick="triggerSynth(320, 'square', this)"><span class="pad-label">Pulse</span><span class="pad-key">[D]</span></div>
    <div class="pad" data-key="z" onclick="triggerSynth(120, 'sine', this)"><span class="pad-label">Sub Thump</span><span class="pad-key">[Z]</span></div>
    <div class="pad" data-key="x" onclick="triggerSynth(940, 'triangle', this)"><span class="pad-label">Glitch</span><span class="pad-key">[X]</span></div>
    <div class="pad" data-key="c" onclick="triggerSynth(520, 'sawtooth', this)"><span class="pad-label">Warp</span><span class="pad-key">[C]</span></div>
  </div>

  <script>
    let audioCtx = null;
    function triggerSynth(freq, type, el) {
      if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      const osc = audioCtx.createOscillator();
      const gain = audioCtx.createGain();
      
      osc.type = type;
      osc.frequency.setValueAtTime(freq, audioCtx.currentTime);
      osc.frequency.exponentialRampToValueAtTime(40, audioCtx.currentTime + 0.35);

      gain.gain.setValueAtTime(0.3, audioCtx.currentTime);
      gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 0.35);

      osc.connect(gain);
      gain.connect(audioCtx.destination);
      osc.start();
      osc.stop(audioCtx.currentTime + 0.35);

      if (el) {
        el.classList.add('active');
        setTimeout(() => el.classList.remove('active'), 120);
      }
    }

    window.addEventListener('keydown', (e) => {
      const key = e.key.toLowerCase();
      const pad = document.querySelector(`.pad[data-key="${key}"]`);
      if (pad) pad.click();
    });
  </script>
</body>
</html>
```

---

## ✅ Production QA Verification Checklist

- [ ] AudioContext initiates only after first user tap/keypress to avoid browser autoplay warnings.
- [ ] Gain nodes safely clamped to avoid clipping or distortion exceeding 0 dBFS.
- [ ] Soundboard responds reliably on iOS Safari and Android Chrome touch devices.
