<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
  <title>View in AR</title>

  <!-- model-viewer: Google's web component for 3D + AR. Loads as a module. -->
  <script type="module" src="https://ajax.googleapis.com/ajax/libs/model-viewer/3.5.0/model-viewer.min.js"></script>

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&family=Inter:wght@400;500&display=swap" rel="stylesheet" />

  <style>
    :root {
      --void-top: #1a1726;
      --void-bottom: #0c0a14;
      --glow: #6c5ce7;
      --ink: #f4f2fb;
      --muted: #9b96b3;
      --accent: #c8ff4d;
      --accent-ink: #16140f;
      --hairline: rgba(255, 255, 255, 0.08);
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    html, body { height: 100%; }

    body {
      font-family: 'Inter', system-ui, sans-serif;
      color: var(--ink);
      background:
        radial-gradient(120% 80% at 50% 12%, rgba(108, 92, 231, 0.22), transparent 60%),
        linear-gradient(180deg, var(--void-top), var(--void-bottom));
      min-height: 100dvh;
      display: flex;
      flex-direction: column;
      padding: env(safe-area-inset-top) 20px env(safe-area-inset-bottom);
    }

    header {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 22px 4px 10px;
    }
    .dot {
      width: 9px; height: 9px; border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 14px var(--accent);
    }
    .eyebrow {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 12px;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--muted);
    }

    main {
      flex: 1;
      display: flex;
      flex-direction: column;
      max-width: 560px;
      width: 100%;
      margin: 0 auto;
    }

    h1 {
      font-family: 'Space Grotesk', sans-serif;
      font-weight: 700;
      font-size: clamp(2.1rem, 8vw, 3.1rem);
      line-height: 1.02;
      letter-spacing: -0.02em;
      margin: 6px 0 8px;
    }
    h1 em {
      font-style: normal;
      color: var(--glow);
    }
    .lede {
      color: var(--muted);
      font-size: 15px;
      line-height: 1.5;
      max-width: 38ch;
    }

    .stage {
      position: relative;
      flex: 1;
      min-height: 340px;
      margin: 18px 0 8px;
    }

    model-viewer {
      width: 100%;
      height: 100%;
      --poster-color: transparent;
      background: transparent;
    }

    /* The drag-to-rotate hint, shown until the user interacts */
    .hint {
      position: absolute;
      bottom: 10px; left: 50%;
      transform: translateX(-50%);
      font-size: 12px;
      letter-spacing: 0.08em;
      color: var(--muted);
      display: flex;
      align-items: center;
      gap: 7px;
      pointer-events: none;
      transition: opacity 0.4s ease;
    }
    .hint svg { opacity: 0.7; }

    /* AR launch button — the one bold element on the page */
    .ar-button {
      appearance: none;
      border: none;
      width: 100%;
      background: var(--accent);
      color: var(--accent-ink);
      font-family: 'Space Grotesk', sans-serif;
      font-weight: 700;
      font-size: 17px;
      letter-spacing: 0.01em;
      padding: 18px 20px;
      border-radius: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      cursor: pointer;
      transition: transform 0.12s ease, box-shadow 0.2s ease;
      box-shadow: 0 8px 30px rgba(200, 255, 77, 0.18);
    }
    .ar-button:hover { transform: translateY(-1px); }
    .ar-button:active { transform: translateY(0); }
    .ar-button:focus-visible {
      outline: 2px solid var(--ink);
      outline-offset: 3px;
    }

    .footnote {
      text-align: center;
      color: var(--muted);
      font-size: 12.5px;
      line-height: 1.5;
      padding: 14px 0 22px;
    }

    /* Fallback line shown only when AR isn't supported on the device */
    #unsupported {
      display: none;
      text-align: center;
      color: var(--muted);
      font-size: 13px;
      padding: 4px 0 18px;
    }

    @media (prefers-reduced-motion: reduce) {
      .ar-button { transition: none; }
    }
  </style>
</head>
<body>
  <header>
    <span class="dot" aria-hidden="true"></span>
    <span class="eyebrow">Augmented Reality</span>
  </header>

  <main>
    <h1>See it <em>in your space.</em></h1>
    <p class="lede">Drag to spin the model. Tap the button to place it in the room around you, life-size.</p>

    <div class="stage">
      <!--
        ===== SWAP YOUR MODEL HERE =====
        src       -> your .glb / .gltf file (Android + in-page 3D)
        ios-src   -> your .usdz file        (iOS AR Quick Look)
        Both files must be hosted on the same site (or any public URL).
        Replace the two demo URLs below with your own.
      -->
      <model-viewer
        id="viewer"
        src="https://modelviewer.dev/shared-assets/models/Astronaut.glb"
        ios-src="https://modelviewer.dev/shared-assets/models/Astronaut.usdz"
        alt="A 3D model you can view in augmented reality"
        ar
        ar-modes="webxr scene-viewer quick-look"
        ar-scale="auto"
        camera-controls
        auto-rotate
        auto-rotate-delay="0"
        rotation-per-second="18deg"
        shadow-intensity="1"
        exposure="1"
        environment-image="neutral"
        poster-color="transparent">

        <!-- Custom AR button replaces model-viewer's default badge -->
        <button slot="ar-button" class="ar-button">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <path d="M12 2 2 7v10l10 5 10-5V7L12 2Z"/><path d="m2 7 10 5 10-5"/><path d="M12 22V12"/>
          </svg>
          View in your space
        </button>

        <div class="hint" id="hint">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <path d="M14 4.1 12 6"/><path d="m5.1 8-2.9-.8"/><path d="m6 12-1.9 2"/><path d="M7.2 2.2 8 5.1"/><path d="M9.037 9.69a.498.498 0 0 1 .653-.653l11 4.5a.5.5 0 0 1-.074.949l-4.349 1.041a1 1 0 0 0-.74.739l-1.04 4.35a.5.5 0 0 1-.95.074z"/>
          </svg>
          Drag to rotate
        </div>
      </model-viewer>
    </div>

    <button class="ar-button" id="manualAr" style="display:none">View in your space</button>
    <p id="unsupported">Your device or browser doesn't support AR. Try opening this page in Safari (iPhone/iPad) or Chrome (Android).</p>

    <p class="footnote">No app required &middot; Works in Safari on iOS and Chrome on Android</p>
  </main>

  <script>
    const viewer = document.querySelector('#viewer');
    const hint = document.querySelector('#hint');

    // Hide the "drag to rotate" hint once the user actually interacts.
    viewer.addEventListener('camera-change', (e) => {
      if (e.detail.source === 'user-interaction') {
        hint.style.opacity = '0';
      }
    });

    // If the device can't do AR, swap the in-component button context for a clear message.
    viewer.addEventListener('load', () => {
      if (!viewer.canActivateAR) {
        document.querySelector('#unsupported').style.display = 'block';
      }
    });
  </script>
</body>
</html>
