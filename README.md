# MyBeautifulPortfolio
Portfolio
<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<meta name="description" content="A playful, pixel‑art themed portfolio website. Single file. Drop into any static host." />
<title>👾 Pixelated Portfolio</title>
<!-- Pixel/arcade fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=VT323&display=swap" rel="stylesheet">
<style>
/* ==========================
PIXELATED PORTFOLIO CSS
Single file, responsive, accessible
========================== */


/* ---- Color tokens (themes) ---- */
:root {
--bg: #f5f7ff;
--panel: #ffffff;
--ink: #13141a;
--muted: #3a3d4a;
--accent: #0078ff;
--accent-2: #ff2f92;
--grid: rgba(0,0,0,0.06);
--shadow: #1a1a1a;
--glow: rgba(0,120,255,0.45);
--ok: #00c853;
--warn: #ff9100;
--bad: #ff5252;
}
html[data-theme="dark"] {
--bg: #0f1117;
--panel: #151826;
--ink: #f8fbff;
--muted: #b3b9c6;
--accent: #59f;
--accent-2: #ff6ec7;
--grid: rgba(255,255,255,0.06);
--shadow: #000;
--glow: rgba(136,160,255,0.4);
}


/* ---- Base ---- */
*, *::before, *::after { box-sizing: border-box; }
html, body { height: 100%; }
body {
margin: 0;
font-family: "VT323", monospace;
font-size: 22px;
line-height: 1.4;
color: var(--ink);
background: var(--bg);
overflow-x: hidden;
image-rendering: pixelated;
}


/* Subtle pixel grid background */
body::before {
content: "";
position: fixed; inset: 0; z-index: -2;
background:
linear-gradient(0deg, transparent 31px, var(--grid) 32px),
linear-gradient(90deg, transparent 31px, var(--grid) 32px);
background-size: 32px 32px;
pointer-events: none;
}
/* Scanlines (toggle) */
.scanlines::after {
content: "";
position: fixed; inset: 0; z-index: -1;
background: repeating-linear-gradient(
180deg,
rgba(0,0,0,0.15), rgba(0,0,0,0.15) 1px,
transparent 1px, transparent 3px
);
mix-blend-mode: multiply;
pointer-events: none;
}


/* ---- Helpers ---- */
.container { width: min(1200px, 92vw); margin-inline: auto; }
.grid { display: grid; gap: 1.2rem; }
.two { grid-template-columns: repeat(2, minmax(0, 1fr)); }
.three { grid-template-columns: repeat(3, minmax(0, 1fr)); }
.center { text-align: center; }
.sr-only { position: absolute; width:1px; height:1px; margin:-1px; padding:0; overflow:hidden; clip:rect(0,0,0,0); border:0; }
a { color: var(--accent); text-decoration-thickness: 2px; }


/* ---- Pixel frame + shadow ---- */
.pixel {
position: relative; background: var(--panel);
box-shadow: 0 0 0 4px var(--ink), 0 8px 0 0 var(--shadow);
border: 4px solid var(--ink);
}
.pixel::before, .pixel::after {
</script>
