/* Skin "Tarantula" (verte) pour GamePad Viewer
   Usage : ?p=1&css=<URL brute de ce fichier> */

:root {
  --tara-deep: #06201a;
  --tara-emerald: #0b3d2e;
  --tara-neon: #2be38a;
  --tara-glow: #3cff9a;
  --tara-bronze: #c9a35a;
}

html, body {
  background: radial-gradient(ellipse at 30% 20%, rgba(43, 227, 138, 0.35), transparent 60%),
              linear-gradient(160deg, var(--tara-emerald), var(--tara-deep)) !important;
  background-size: cover !important;
}

button, .button, .stick, .trigger, [class*="button"], [class*="stick"], [class*="trigger"] {
  filter: drop-shadow(0 0 6px var(--tara-glow));
}

[class*="active"], .pressed {
  fill: var(--tara-neon) !important;
  color: var(--tara-neon) !important;
  box-shadow: 0 0 12px var(--tara-glow);
}

[class*="dpad"] {
  fill: var(--tara-bronze) !important;
}
