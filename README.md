[aboutme.html](https://github.com/user-attachments/files/35496195/aboutme.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>LUKE SABLE // Voice Actor &amp; Narrator</title>
  <style>
    :root {
      /* HIM 'Dark Light' + 'Razorblade' inspired alt-emo palette */
      --bg-deep: #090a0d;
      --bg-panel: #101218;
      --bg-card: #151821;
      --bg-hover: #1b1f2b;
      --border: #262b38;
      --border-glow: #3b465c;
      --text-main: #e6e9ef;
      --text-dim: #8b93a6;
      --text-faint: #586073;
      --ice: #84a9c9;        /* Dark Light slate-blue */
      --crimson: #b8425e;    /* Razorblade dried-crimson */
      --crimson-dim: rgba(184, 66, 94, 0.14);
      --ice-dim: rgba(132, 169, 201, 0.12);
      --online: #4ec98b;
      --mono: "JetBrains Mono", "Cascadia Code", Consolas, monospace;
      --sans: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background-color: var(--bg-deep);
      background-image:
        radial-gradient(circle at 18% 12%, rgba(132, 169, 201, 0.08), transparent 42%),
        radial-gradient(circle at 85% 85%, rgba(184, 66, 94, 0.08), transparent 45%),
        radial-gradient(rgba(255, 255, 255, 0.03) 1px, transparent 1px);
      background-size: 100% 100%, 100% 100%, 24px 24px;
      color: var(--text-main);
      font-family: var(--sans);
      font-size: 14px;
      line-height: 1.55;
      padding: 28px 16px 48px;
      min-height: 100vh;
    }

    a { color: var(--ice); text-decoration: none; transition: 0.2s ease; }
    a:hover { color: #b6d3ec; }

    .shell {
      max-width: 960px;
      margin: 0 auto;
      background: var(--bg-panel);
      border: 1px solid var(--border);
      box-shadow: 0 24px 70px rgba(0, 0, 0, 0.75);
      border-radius: 6px;
      overflow: hidden;
    }

    /* Subtle retro-modern top window bar */
    .topbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 10px;
      padding: 10px 18px;
      background: #0c0e13;
      border-bottom: 1px solid var(--border);
      font-family: var(--mono);
      font-size: 11px;
      color: var(--text-dim);
      letter-spacing: 0.06em;
    }

    .topbar-left {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .status-pill {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      padding: 3px 9px;
      border: 1px solid rgba(78, 201, 139, 0.25);
      background: rgba(78, 201, 139, 0.07);
      border-radius: 999px;
      color: #bcebd2;
      font-size: 10.5px;
    }

    .status-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: var(--online);
      box-shadow: 0 0 8px var(--online);
    }

    /* Atmospheric Banner Header */
    .hero {
      position: relative;
      padding: 26px 24px 22px;
      border-bottom: 1px solid var(--border);
      background:
        linear-gradient(125deg, rgba(16, 18, 24, 0.94) 10%, rgba(18, 23, 34, 0.9) 60%, rgba(38, 18, 26, 0.86) 100%);
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      flex-wrap: wrap;
      gap: 16px;
    }

    .hero-title h1 {
      font-size: clamp(1.7rem, 3.5vw, 2.35rem);
      font-weight: 700;
      letter-spacing: -0.02em;
      line-height: 1.1;
      color: #ffffff;
    }

    .hero-title h1 span {
      color: var(--crimson);
      font-weight: 400;
      font-family: var(--mono);
      font-size: 0.65em;
      margin-left: 6px;
    }

    .hero-sub {
      margin-top: 6px;
      color: var(--text-dim);
      font-size: 13.5px;
    }

    .hero-sub strong { color: var(--ice); font-weight: 500; }

    .hero-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 7px;
      font-family: var(--mono);
      font-size: 11px;
    }

    .badge {
      padding: 4px 10px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid var(--border-glow);
      border-radius: 4px;
      color: var(--text-main);
    }

    .badge.accent {
      border-color: rgba(184, 66, 94, 0.5);
      background: var(--crimson-dim);
      color: #f3b5c4;
    }

    /* Main 2-column MySpace-inspired grid */
    .layout {
      display: grid;
      grid-template-columns: 300px 1fr;
      gap: 18px;
      padding: 20px;
    }

    @media (max-width: 780px) {
      .layout { grid-template-columns: 1fr; }
    }

    .col { display: flex; flex-direction: column; gap: 16px; }

    .card {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 5px;
      overflow: hidden;
    }

    .card-head {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 8px 13px;
      background: rgba(0, 0, 0, 0.28);
      border-bottom: 1px solid var(--border);
      font-family: var(--mono);
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--ice);
    }

    .card-head.crimson { color: #e28aa0; }
    .card-head small { color: var(--text-faint); font-weight: 400; }

    .card-body { padding: 14px; }

    /* Landscape-friendly Profile Pic Frame */
    .pfp-wrap {
      width: 100%;
      aspect-ratio: 16 / 10;
      background: #0b0d12;
      border: 1px solid var(--border);
      border-radius: 4px;
      overflow: hidden;
      margin-bottom: 12px;
      position: relative;
    }

    .pfp-wrap img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
      display: block;
      filter: contrast(1.04) saturate(0.9);
    }

    .pfp-fallback {
      width: 100%;
      height: 100%;
      display: none;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: var(--text-faint);
      font-family: var(--mono);
      font-size: 11px;
      text-align: center;
      padding: 12px;
      background: linear-gradient(145deg, #0d0f15, #17141c);
    }

    /* Key-value MySpace blurb rows */
    .kv-list { display: flex; flex-direction: column; gap: 8px; font-size: 13px; }
    .kv-row {
      display: flex;
      justify-content: space-between;
      gap: 10px;
      border-bottom: 1px dashed rgba(255, 255, 255, 0.06);
      padding-bottom: 6px;
    }
    .kv-row:last-child { border-bottom: none; padding-bottom: 0; }
    .kv-label {
      color: var(--text-dim);
      font-family: var(--mono);
      font-size: 11.5px;
      flex-shrink: 0;
    }
    .kv-val { text-align: right; color: var(--text-main); }
    .kv-val.highlight { color: var(--ice); }

    /* Social Icon Dock */
    .socials-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 8px;
    }

    .social-btn {
      display: flex;
      align-items: center;
      gap: 9px;
      padding: 9px 10px;
      background: #101219;
      border: 1px solid var(--border);
      border-radius: 4px;
      color: var(--text-main);
      font-size: 12.5px;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.18s ease;
    }

    .social-btn:hover {
      background: var(--bg-hover);
      border-color: var(--ice);
      color: #ffffff;
      transform: translateY(-1px);
    }

    .social-btn.crimson-hover:hover { border-color: var(--crimson); }

    .social-btn svg {
      width: 16px;
      height: 16px;
      flex-shrink: 0;
      fill: currentColor;
      color: var(--ice);
    }

    .social-btn.muted-soon {
      opacity: 0.72;
    }

    .contact-copy {
      margin-top: 10px;
      width: 100%;
      padding: 9px 12px;
      background: var(--crimson-dim);
      border: 1px solid rgba(184, 66, 94, 0.4);
      border-radius: 4px;
      color: #f3c4cf;
      font-family: var(--mono);
      font-size: 11.5px;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: 0.18s ease;
    }

    .contact-copy:hover {
      background: rgba(184, 66, 94, 0.24);
      border-color: var(--crimson);
      color: #ffffff;
    }

    /* Custom Sleek Dark Alt-Emo Audio Player */
    .player-deck {
      background: linear-gradient(180deg, #10131c 0%, #0d0f16 100%);
      border: 1px solid var(--border-glow);
      border-radius: 5px;
      padding: 15px;
      margin-bottom: 12px;
    }

    .now-playing-top {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 12px;
      margin-bottom: 12px;
    }

    .np-kicker {
      font-family: var(--mono);
      font-size: 10px;
      color: var(--crimson);
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 3px;
    }

    .np-title {
      font-size: 16px;
      font-weight: 600;
      color: #ffffff;
    }

    .np-desc {
      font-size: 12.5px;
      color: var(--text-dim);
      margin-top: 2px;
    }

    /* Subtle animated EQ bars */
    .eq-bars {
      display: flex;
      align-items: flex-end;
      gap: 3px;
      height: 22px;
      padding-top: 4px;
    }

    .eq-bars span {
      width: 3px;
      height: 5px;
      background: var(--text-faint);
      border-radius: 2px;
      transition: height 0.2s ease;
    }

    .eq-bars.playing span {
      background: var(--crimson);
      animation: eqPulse 0.8s ease-in-out infinite alternate;
    }
    .eq-bars.playing span:nth-child(2) { animation-delay: 0.2s; background: var(--ice); }
    .eq-bars.playing span:nth-child(3) { animation-delay: 0.4s; }
    .eq-bars.playing span:nth-child(4) { animation-delay: 0.15s; background: var(--ice); }

    @keyframes eqPulse {
      0% { height: 4px; }
      100% { height: 20px; }
    }

    .controls-row {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .ctrl-btn {
      background: #1b202d;
      border: 1px solid var(--border-glow);
      color: #ffffff;
      border-radius: 4px;
      width: 34px;
      height: 34px;
      display: grid;
      place-items: center;
      cursor: pointer;
      flex-shrink: 0;
      transition: 0.15s ease;
    }

    .ctrl-btn:hover { border-color: var(--ice); background: #232a3b; }

    .ctrl-btn.play-main {
      width: 40px;
      height: 40px;
      background: var(--crimson);
      border-color: #d35472;
    }

    .ctrl-btn.play-main:hover { background: #cc4c6b; }

    .scrubber-wrap {
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 4px;
    }

    input[type="range"] {
      -webkit-appearance: none;
      appearance: none;
      width: 100%;
      height: 5px;
      background: #232836;
      border-radius: 99px;
      outline: none;
      cursor: pointer;
    }

    input[type="range"]::-webkit-slider-thumb {
      -webkit-appearance: none;
      appearance: none;
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: var(--ice);
      border: 2px solid #090a0d;
      cursor: pointer;
    }

    input[type="range"]::-moz-range-thumb {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: var(--ice);
      border: 2px solid #090a0d;
      cursor: pointer;
    }

    .time-row {
      display: flex;
      justify-content: space-between;
      font-family: var(--mono);
      font-size: 10.5px;
      color: var(--text-dim);
    }

    .vol-wrap {
      display: flex;
      align-items: center;
      gap: 6px;
      width: 84px;
    }

    @media (max-width: 520px) { .vol-wrap { display: none; } }

    .player-alert {
      display: none;
      margin-top: 9px;
      padding: 6px 10px;
      background: rgba(184, 66, 94, 0.12);
      border: 1px solid rgba(184, 66, 94, 0.35);
      border-radius: 4px;
      font-family: var(--mono);
      font-size: 11px;
      color: #f0b6c4;
    }

    /* Tracklist */
    .tracklist { display: flex; flex-direction: column; gap: 6px; }

    .track-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      padding: 10px 12px;
      background: #10131a;
      border: 1px solid var(--border);
      border-radius: 4px;
      cursor: pointer;
      transition: 0.15s ease;
      text-align: left;
      width: 100%;
      color: inherit;
    }

    .track-item:hover {
      background: var(--bg-hover);
      border-color: var(--border-glow);
    }

    .track-item.active {
      background: rgba(132, 169, 201, 0.08);
      border-color: var(--ice);
    }

    .track-num {
      font-family: var(--mono);
      font-size: 11px;
      color: var(--crimson);
      margin-right: 8px;
    }

    .track-name { font-weight: 600; color: var(--text-main); font-size: 13.5px; }
    .track-sub { font-size: 12px; color: var(--text-dim); margin-top: 1px; }

    .track-tag {
      font-family: var(--mono);
      font-size: 10.5px;
      padding: 3px 8px;
      border-radius: 3px;
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid var(--border);
      color: var(--text-dim);
      white-space: nowrap;
    }

    .track-item.active .track-tag {
      border-color: rgba(132, 169, 201, 0.4);
      color: var(--ice);
    }

    /* Tags Matrix */
    .tag-group { margin-bottom: 12px; }
    .tag-group:last-child { margin-bottom: 0; }
    .tag-label {
      font-family: var(--mono);
      font-size: 10.5px;
      text-transform: uppercase;
      letter-spacing: 0.07em;
      color: var(--text-dim);
      margin-bottom: 6px;
      display: block;
    }

    .tags { display: flex; flex-wrap: wrap; gap: 6px; }

    .tag {
      font-size: 12px;
      padding: 4px 9px;
      border-radius: 4px;
      background: #10131a;
      border: 1px solid var(--border);
      color: var(--text-main);
    }

    .tag.yes { border-color: rgba(132, 169, 201, 0.35); background: var(--ice-dim); color: #cde2f5; }
    .tag.no { border-color: rgba(184, 66, 94, 0.3); color: #c78b9a; text-decoration: line-through; text-decoration-color: rgba(184, 66, 94, 0.5); }

    /* Culture & Interests MySpace Touch */
    .culture-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
      gap: 12px;
    }

    .culture-box {
      background: #10131a;
      border: 1px solid var(--border);
      border-radius: 4px;
      padding: 10px 12px;
    }

    .culture-box h4 {
      font-family: var(--mono);
      font-size: 10.5px;
      color: var(--ice);
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 6px;
    }

    .culture-box p {
      font-size: 12.5px;
      color: var(--text-dim);
      line-height: 1.5;
    }

    .culture-box strong { color: var(--text-main); font-weight: 500; }

    /* Log / Credits box */
    .log-line {
      font-family: var(--mono);
      font-size: 12px;
      color: var(--text-dim);
      padding: 5px 0;
      border-bottom: 1px dashed rgba(255, 255, 255, 0.05);
    }
    .log-line:last-child { border-bottom: none; }
    .log-line span { color: var(--crimson); margin-right: 8px; }

    .footer {
      padding: 11px 20px;
      background: #0c0e13;
      border-top: 1px solid var(--border);
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 8px;
      font-family: var(--mono);
      font-size: 11px;
      color: var(--text-faint);
    }
  </style>
</head>
<body>

  <div class="shell">
    <!-- Top Window Status Bar -->
    <div class="topbar">
      <div class="topbar-left">
        <span>SABLE // AUDIO_PROFILE.HTML</span>
        <span class="status-pill"><span class="status-dot"></span> OPEN FOR ROLES</span>
      </div>
      <div>AUSTRALIA (AEST/ACDT) &bull; 12–24HR TURNAROUND</div>
    </div>

    <!-- Header -->
    <header class="hero">
      <div class="hero-title">
        <h1>Luke Sable <span>// VO</span></h1>
        <p class="hero-sub">
          <strong>Deep, calm &amp; composed voice.</strong> Built for narration, podcasts, horror &amp; grounded characters.
        </p>
      </div>
      <div class="hero-badges">
        <span class="badge">Sounds Mid-20s</span>
        <span class="badge">Maono PD200X</span>
        <span class="badge accent">Indie / Micro-Budget ($0–$10)</span>
      </div>
    </header>

    <!-- Main Content Grid -->
    <main class="layout">

      <!-- LEFT COLUMN (MySpace Sidebar Vibe) -->
      <aside class="col">

        <!-- Profile Pic + Quick Status -->
        <section class="card">
          <div class="card-head">
            <span>Profile</span>
            <small>ID #001</small>
          </div>
          <div class="card-body">
            <div class="pfp-wrap">
              <!-- TODO: Upload your selfie to your GitHub folder named pfp.jpg -->
              <img src="pfp.jpg" alt="Luke Sable" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
              <div class="pfp-fallback">
                [ pfp.jpg ]<br />
                Drop your photo in the repo folder to display here
              </div>
            </div>

            <div class="kv-list">
              <div class="kv-row">
                <span class="kv-label">Pronouns</span>
                <span class="kv-val">He / Him</span>
              </div>
              <div class="kv-row">
                <span class="kv-label">Vocal Age</span>
                <span class="kv-val highlight">Mid-20s (18 IRL)</span>
              </div>
              <div class="kv-row">
                <span class="kv-label">Mood</span>
                <span class="kv-val">composed / late-night</span>
              </div>
              <div class="kv-row">
                <span class="kv-label">Vibe</span>
                <span class="kv-val">downtown after dark</span>
              </div>
              <div class="kv-row">
                <span class="kv-label">Spinning</span>
                <span class="kv-val highlight">HIM — Killing Loneliness</span>
              </div>
            </div>
          </div>
        </section>

        <!-- Studio Rig & Turnaround -->
        <section class="card">
          <div class="card-head">
            <span>Studio Rig</span>
            <small>CLEAN AUDIO</small>
          </div>
          <div class="card-body">
            <div class="kv-list">
              <div class="kv-row">
                <span class="kv-label">Mic</span>
                <span class="kv-val highlight">Maono PD200X</span>
              </div>
              <div class="kv-row">
                <span class="kv-label">Space</span>
                <span class="kv-val">Padded room (0 noise)</span>
              </div>
              <div class="kv-row">
                <span class="kv-label">DAW</span>
                <span class="kv-val">Audacity (WAV / MP3)</span>
              </div>
              <div class="kv-row">
                <span class="kv-label">Delivery</span>
                <span class="kv-val">12–24 hrs (US-friendly)</span>
              </div>
              <div class="kv-row">
                <span class="kv-label">Rates</span>
                <span class="kv-val">Free to &lt;$10 / Flexible</span>
              </div>
            </div>
          </div>
        </section>

        <!-- Social Links & Contact -->
        <section class="card">
          <div class="card-head crimson">
            <span>Links &amp; Booking</span>
            <small>DM OPEN</small>
          </div>
          <div class="card-body">
            <div class="socials-grid">
              <!-- TODO: Replace YOUR_DISCORD_USER_ID with your numeric Discord ID (see guide!) -->
              <a class="social-btn" href="https://discord.com/users/YOUR_DISCORD_USER_ID" target="_blank" rel="noopener">
                <svg viewBox="0 0 24 24"><path d="M20.3 4.4A19.8 19.8 0 0 0 15.4 3a14 14 0 0 0-.6 1.3 18.4 18.4 0 0 0-5.6 0A13.7 13.7 0 0 0 8.6 3a19.8 19.8 0 0 0-4.9 1.4C.6 9.1-.3 13.7.2 18.2a20 20 0 0 0 6 3 14.7 14.7 0 0 0 1.3-2.1 12.8 12.8 0 0 1-2-.9l.5-.4a14.2 14.2 0 0 0 12 0l.5.4a12.8 12.8 0 0 1-2 .9 14.7 14.7 0 0 0 1.3 2.1 20 20 0 0 0 6-3c.6-5.2-.9-9.8-3.5-13.8zM8 15.4c-1.2 0-2.1-1.1-2.1-2.4s.9-2.4 2.1-2.4c1.2 0 2.2 1.1 2.1 2.4 0 1.3-.9 2.4-2.1 2.4zm8 0c-1.2 0-2.1-1.1-2.1-2.4s.9-2.4 2.1-2.4c1.2 0 2.2 1.1 2.1 2.4 0 1.3-.9 2.4-2.1 2.4z"/></svg>
                Discord
              </a>

              <!-- TODO: Replace with your Casting Call Club profile URL -->
              <a class="social-btn" href="https://www.castingcall.club/YOUR_HANDLE" target="_blank" rel="noopener">
                <svg viewBox="0 0 24 24"><path d="M12 2a4 4 0 0 1 4 4v6a4 4 0 0 1-8 0V6a4 4 0 0 1 4-4zm-7 9a1 1 0 0 1 1 1 6 6 0 0 0 12 0 1 1 0 1 1 2 0 8 8 0 0 1-7 7.9V22h3a1 1 0 1 1 0 2H8a1 1 0 1 1 0-2h3v-2.1A8 8 0 0 1 4 12a1 1 0 0 1 1-1z"/></svg>
                Casting Call
              </a>

              <!-- TODO: Replace with your TikTok URL -->
              <a class="social-btn" href="https://www.tiktok.com/@YOUR_TIKTOK" target="_blank" rel="noopener">
                <svg viewBox="0 0 24 24"><path d="M19.6 6.7a4.8 4.8 0 0 1-3.8-4.2V2h-3.4v13.7a2.9 2.9 0 1 1-2-2.7V9.5a6.3 6.3 0 1 0 5.4 6.2V8.8a8.2 8.2 0 0 0 4.8 1.5V6.9l-1-.2z"/></svg>
                TikTok
              </a>

              <!-- TODO: Replace with your Patreon URL -->
              <a class="social-btn crimson-hover" href="https://www.patreon.com/YOUR_PATREON" target="_blank" rel="noopener">
                <svg viewBox="0 0 24 24"><path d="M15.4 2.5a6.5 6.5 0 1 0 0 13 6.5 6.5 0 0 0 0-13zM2.5 2.5v19h3.4v-19H2.5z"/></svg>
                Patreon
              </a>

              <!-- TODO: Replace with your Instagram URL when ready -->
              <a class="social-btn muted-soon" href="https://www.instagram.com/YOUR_IG" target="_blank" rel="noopener">
                <svg viewBox="0 0 24 24"><path d="M7.5 2h9A5.5 5.5 0 0 1 22 7.5v9a5.5 5.5 0 0 1-5.5 5.5h-9A5.5 5.5 0 0 1 2 16.5v-9A5.5 5.5 0 0 1 7.5 2zm0 2A3.5 3.5 0 0 0 4 7.5v9A3.5 3.5 0 0 0 7.5 20h9a3.5 3.5 0 0 0 3.5-3.5v-9A3.5 3.5 0 0 0 16.5 4h-9zM12 7a5 5 0 1 1 0 10 5 5 0 0 1 0-10zm0 2a3 3 0 1 0 0 6 3 3 0 0 0 0-6zm5.3-2.6a1.1 1.1 0 1 1 0 2.2 1.1 1.1 0 0 1 0-2.2z"/></svg>
                Instagram
              </a>

              <!-- Copy Discord username fallback (works even if not in shared server) -->
              <button class="social-btn" type="button" onclick="copyText('YOUR_DISCORD_USERNAME', this)">
                <svg viewBox="0 0 24 24"><path d="M16 1H4a2 2 0 0 0-2 2v14h2V3h12V1zm3 4H8a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h11a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zm0 16H8V7h11v14z"/></svg>
                <span>Copy Tag</span>
              </button>
            </div>

            <!-- TODO: Replace with your VA email -->
            <button class="contact-copy" type="button" onclick="copyText('lukesable.vo@gmail.com', this)">
              <span>lukesable.vo@gmail.com</span>
              <strong>COPY</strong>
            </button>
          </div>
        </section>

      </aside>

      <!-- RIGHT COLUMN (Audio Samples, Accents, Culture, Bookings) -->
      <div class="col">

        <!-- Custom Alt-Emo Audio Player -->
        <section class="card">
          <div class="card-head crimson">
            <span>Voice Samples // 4 Accents</span>
            <small>CLICK TRACK TO PLAY</small>
          </div>
          <div class="card-body">

            <div class="player-deck">
              <div class="now-playing-top">
                <div>
                  <div class="np-kicker" id="npKicker">TRACK 01 // LOADED</div>
                  <div class="np-title" id="npTitle">Australian (Native)</div>
                  <div class="np-desc" id="npDesc">Natural mid-20s baritone. Calm, soothing &amp; podcast-ready.</div>
                </div>
                <div class="eq-bars" id="eqBars">
                  <span></span><span></span><span></span><span></span>
                </div>
              </div>

              <div class="controls-row">
                <button class="ctrl-btn" type="button" id="prevBtn" title="Previous">&#9664;</button>
                <button class="ctrl-btn play-main" type="button" id="playBtn" title="Play / Pause">&#9654;</button>
                <button class="ctrl-btn" type="button" id="nextBtn" title="Next">&#9654;&#9654;</button>

                <div class="scrubber-wrap">
                  <input type="range" id="seekBar" min="0" max="100" value="0" step="0.1" />
                  <div class="time-row">
                    <span id="curTime">0:00</span>
                    <span id="durTime">0:00</span>
                  </div>
                </div>

                <div class="vol-wrap">
                  <span style="font-family:var(--mono); font-size:10px; color:var(--text-dim);">VOL</span>
                  <input type="range" id="volBar" min="0" max="1" step="0.05" value="0.9" />
                </div>
              </div>

              <div class="player-alert" id="playerAlert"></div>
            </div>

            <!-- 4 Accent Tracklist -->
            <div class="tracklist" id="tracklist">
              <button class="track-item active" type="button" data-index="0">
                <div>
                  <div class="track-name"><span class="track-num">01</span>Australian (Native)</div>
                  <div class="track-sub">Natural mid-20s baritone &mdash; calm, conversational, podcast &amp; narration.</div>
                </div>
                <span class="track-tag">NATURAL</span>
              </button>

              <button class="track-item" type="button" data-index="1">
                <div>
                  <div class="track-name"><span class="track-num">02</span>Fancy English (RP)</div>
                  <div class="track-sub">Composed, articulate, dry authority &mdash; horror, essays &amp; stoic roles.</div>
                </div>
                <span class="track-tag">CALM / FORMAL</span>
              </button>

              <button class="track-item" type="button" data-index="2">
                <div>
                  <div class="track-name"><span class="track-num">03</span>Southern American</div>
                  <div class="track-sub">Warm drawl &amp; gritty storyteller cadence &mdash; Western/horror NPCs &amp; tales.</div>
                </div>
                <span class="track-tag">CHARACTER</span>
              </button>

              <button class="track-item" type="button" data-index="3">
                <div>
                  <div class="track-name"><span class="track-num">04</span>Slavic / Eastern European</div>
                  <div class="track-sub">Authentic cadence &amp; syntax drop (&ldquo;My name Luke. Want get in car?&rdquo;).</div>
                </div>
                <span class="track-tag">CHARACTER</span>
              </button>
            </div>

            <audio id="audioCore" preload="metadata"></audio>
          </div>
        </section>

        <!-- Vocal Profile & Sweet Spot -->
        <section class="card">
          <div class="card-head">
            <span>Vocal Range &amp; Fit</span>
            <small>WHAT I DO BEST</small>
          </div>
          <div class="card-body">
            <div class="tag-group">
              <span class="tag-label">Tone &amp; Delivery</span>
              <div class="tags">
                <span class="tag yes">Deep &amp; Soothing</span>
                <span class="tag yes">Calm &amp; Deadpan</span>
                <span class="tag yes">Mid-20s Maturity</span>
                <span class="tag">Light Scottish</span>
                <span class="tag">Goofy / Offbeat Bits</span>
              </div>
            </div>

            <div class="tag-group">
              <span class="tag-label">Best Roles For Me</span>
              <div class="tags">
                <span class="tag yes">Podcasts &amp; Co-Hosting</span>
                <span class="tag yes">Horror Narration</span>
                <span class="tag yes">YouTube / Reddit Reads</span>
                <span class="tag yes">Grounded RPG NPCs</span>
                <span class="tag yes">Long-Term Projects</span>
              </div>
            </div>

            <div class="tag-group">
              <span class="tag-label">Not My Lane (Honest Check)</span>
              <div class="tags">
                <span class="tag no">Neutral American</span>
                <span class="tag no">High-Pitched Voices</span>
                <span class="tag no">Heavy Screaming</span>
              </div>
            </div>
          </div>
        </section>

        <!-- Non-Corny MySpace Culture Strip -->
        <section class="card">
          <div class="card-head">
            <span>Rotation &amp; Taste</span>
            <small>NO LARP // JUST STUFF I ACTUALLY LIKE</small>
          </div>
          <div class="card-body">
            <div class="culture-grid">
              <div class="culture-box">
                <h4>Heavy Rotation</h4>
                <p>
                  <strong>HIM</strong> (<em>Dark Light</em>, <em>Razorblade Romance</em>),
                  <strong>Violent Vira</strong>,
                  <strong>Overgrown</strong> (<em>Waiting Room</em> / <em>Escape</em>),
                  <strong>whatsaheart</strong>,
                  <strong>Amira Elfeky</strong>,
                  <strong>chauncy</strong> (<em>stay</em>)
                </p>
              </div>
              <div class="culture-box">
                <h4>Watchlist &amp; Pod Fit</h4>
                <p>
                  Films &amp; TV: <strong>Obsession</strong>, <strong>The Mentalist</strong>.<br />
                  Pod Vibe: <strong>Knifepoint Horror</strong> (minimalist, late-night storytelling).
                </p>
              </div>
            </div>
          </div>
        </section>

        <!-- Credits / Project Log -->
        <section class="card">
          <div class="card-head">
            <span>Project Log</span>
            <small>UPDATED REGULARLY</small>
          </div>
          <div class="card-body">
            <div class="log-line"><span>[2026]</span> Rig dialed in (Maono PD200X + padded room) &mdash; booking first projects.</div>
            <div class="log-line"><span>[OPEN]</span> Taking free &amp; micro-budget indie games, mods, YouTube &amp; podcasts.</div>
          </div>
        </section>

      </div>
    </main>

    <footer class="footer">
      <span>LUKE SABLE // VOICE &amp; NARRATION</span>
      <span>NO AUTOPLAY &bull; CLEAN AUDIO DELIVERED FAST</span>
    </footer>
  </div>

  <script>
    // TODO: Upload these 4 MP3 files into an "audio" folder in your GitHub repo!
    const tracks = [
      {
        title: "Australian (Native)",
        desc: "Natural mid-20s baritone. Calm, soothing & podcast-ready.",
        src: "audio/australian.mp3"
      },
      {
        title: "Fancy English (RP)",
        desc: "Composed, articulate, dry authority. Ideal for horror & essays.",
        src: "audio/english.mp3"
      },
      {
        title: "Southern American",
        desc: "Warm drawl & grizzled storyteller cadence. Great for characters.",
        src: "audio/southern-us.mp3"
      },
      {
        title: "Slavic / Eastern European",
        desc: "Heavy cadence with authentic broken-English phrasing shifts.",
        src: "audio/slavic.mp3"
      }
    ];

    const audio = document.getElementById("audioCore");
    const playBtn = document.getElementById("playBtn");
    const prevBtn = document.getElementById("prevBtn");
    const nextBtn = document.getElementById("nextBtn");
    const seekBar = document.getElementById("seekBar");
    const volBar = document.getElementById("volBar");
    const curTime = document.getElementById("curTime");
    const durTime = document.getElementById("durTime");
    const npKicker = document.getElementById("npKicker");
    const npTitle = document.getElementById("npTitle");
    const npDesc = document.getElementById("npDesc");
    const eqBars = document.getElementById("eqBars");
    const playerAlert = document.getElementById("playerAlert");
    const trackItems = document.querySelectorAll(".track-item");

    let currentIndex = 0;
    audio.volume = parseFloat(volBar.value);

    function formatTime(sec) {
      if (!isFinite(sec) || sec < 0) return "0:00";
      const m = Math.floor(sec / 60);
      const s = Math.floor(sec % 60);
      return m + ":" + (s < 10 ? "0" : "") + s;
    }

    function loadTrack(idx, autoPlay = false) {
      currentIndex = (idx + tracks.length) % tracks.length;
      const t = tracks[currentIndex];
      playerAlert.style.display = "none";

      audio.src = t.src;
      seekBar.value = 0;
      curTime.textContent = "0:00";
      durTime.textContent = "0:00";

      npKicker.textContent = `TRACK 0${currentIndex + 1} // ${autoPlay ? "PLAYING" : "READY"}`;
      npTitle.textContent = t.title;
      npDesc.textContent = t.desc;

      trackItems.forEach((btn, i) => {
        btn.classList.toggle("active", i === currentIndex);
      });

      if (autoPlay) {
        audio.play().catch(() => showMissingFile(t.src));
      } else {
        setPlayingUI(false);
      }
    }

    function setPlayingUI(isPlaying) {
      playBtn.innerHTML = isPlaying ? "&#10074;&#10074;" : "&#9654;";
      eqBars.classList.toggle("playing", isPlaying);
      npKicker.textContent = `TRACK 0${currentIndex + 1} // ${isPlaying ? "PLAYING" : "PAUSED"}`;
    }

    function showMissingFile(path) {
      setPlayingUI(false);
      playerAlert.style.display = "block";
      playerAlert.textContent = `Audio file not uploaded yet — add "${path}" to your repo folder.`;
    }

    playBtn.addEventListener("click", () => {
      if (!audio.src) loadTrack(currentIndex, false);
      if (audio.paused) {
        audio.play().catch(() => showMissingFile(tracks[currentIndex].src));
      } else {
        audio.pause();
      }
    });

    prevBtn.addEventListener("click", () => loadTrack(currentIndex - 1, true));
    nextBtn.addEventListener("click", () => loadTrack(currentIndex + 1, true));

    trackItems.forEach((btn) => {
      btn.addEventListener("click", () => {
        const idx = parseInt(btn.dataset.index, 10);
        if (idx === currentIndex && !audio.paused) {
          audio.pause();
        } else {
          loadTrack(idx, true);
        }
      });
    });

    audio.addEventListener("play", () => {
      playerAlert.style.display = "none";
      setPlayingUI(true);
    });
    audio.addEventListener("pause", () => setPlayingUI(false));
    audio.addEventListener("error", () => {
      if (audio.getAttribute("src")) showMissingFile(tracks[currentIndex].src);
    });

    audio.addEventListener("loadedmetadata", () => {
      durTime.textContent = formatTime(audio.duration);
    });

    audio.addEventListener("timeupdate", () => {
      if (isFinite(audio.duration) && audio.duration > 0) {
        seekBar.value = (audio.currentTime / audio.duration) * 100;
        curTime.textContent = formatTime(audio.currentTime);
      }
    });

    audio.addEventListener("ended", () => loadTrack(currentIndex + 1, true));

    seekBar.addEventListener("input", () => {
      if (isFinite(audio.duration) && audio.duration > 0) {
        audio.currentTime = (seekBar.value / 100) * audio.duration;
      }
    });

    volBar.addEventListener("input", () => {
      audio.volume = parseFloat(volBar.value);
    });

    function copyText(text, btn) {
      navigator.clipboard.writeText(text).then(() => {
        const original = btn.innerHTML;
        btn.innerHTML = btn.classList.contains("contact-copy")
          ? `<span>${text}</span><strong>COPIED!</strong>`
          : `<span>Copied!</span>`;
        setTimeout(() => { btn.innerHTML = original; }, 1400);
      });
    }

    loadTrack(0, false);
  </script>
</body>
</html>
