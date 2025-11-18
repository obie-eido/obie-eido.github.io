<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Jazen Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-light: #f5f3ee;
      --bg-dark: #050505;
      --text-main: #111111;
      --accent: #d0211c;
      --muted: #888888;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Space Grotesk", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: #111111;
      color: var(--text-main);
      line-height: 1.4;
    }

    .page {
      max-width: 1200px;
      margin: 40px auto;
      background: #111111;
    }

    section {
      margin-bottom: 40px;
      box-shadow: 0 18px 40px rgba(0, 0, 0, 0.45);
    }

    /* Hero */

    .hero {
      background: var(--bg-light);
      display: grid;
      grid-template-columns: 3fr 2fr;
      min-height: 420px;
      position: relative;
      overflow: hidden;
    }

    .hero-inner {
      padding: 40px 48px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .hero-top {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 16px;
      margin-bottom: 40px;
    }

    .hero-title {
      font-size: 52px;
      font-weight: 700;
      letter-spacing: 0.12em;
    }

    .hero-title span {
      display: block;
    }

    .hero-meta {
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--muted);
      text-align: right;
      white-space: nowrap;
    }

    .hero-contact {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 24px;
      font-size: 12px;
      margin-bottom: 32px;
    }

    .hero-contact h4 {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      margin-bottom: 6px;
      color: var(--muted);
    }

    .hero-contact p {
      margin-bottom: 4px;
    }

    .hero-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 11px;
    }

    .hero-dot {
      width: 10px;
      height: 10px;
      border-radius: 999px;
      background: var(--accent);
    }

    .hero-image {
      position: relative;
      overflow: hidden;
    }

    .hero-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .hero-side-label {
      position: absolute;
      right: 18px;
      top: 40px;
      writing-mode: vertical-rl;
      text-orientation: mixed;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      font-size: 10px;
      background: #ffffff;
      padding: 6px 4px;
    }

    .hero-accent-bar {
      position: absolute;
      right: 16px;
      bottom: 16px;
      width: 6px;
      height: 40px;
      background: var(--accent);
    }

    /* Dark panel */

    .panel-dark {
      background: var(--bg-dark);
      color: #f5f5f5;
      padding: 32px 40px 18px;
    }

    .panel-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      margin-bottom: 80px;
      color: #d0d0d0;
    }

    .panel-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 40px;
      font-size: 13px;
      margin-bottom: 40px;
    }

    .panel-grid h3 {
      font-size: 13px;
      margin-bottom: 10px;
    }

    .panel-grid p {
      color: #b0b0b0;
      max-width: 260px;
    }

    .panel-thumbs {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 8px;
      font-size: 0;
    }

    .panel-thumbs img {
      width: 100%;
      height: 90px;
      object-fit: cover;
    }

    .panel-side-label {
      position: absolute;
      right: 18px;
      top: 50%;
      transform: translateY(-50%);
      writing-mode: vertical-rl;
      text-orientation: mixed;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      font-size: 10px;
      color: #d0d0d0;
    }

    .panel-wrapper {
      position: relative;
    }

    .panel-accent-bar {
      position: absolute;
      right: 16px;
      bottom: 16px;
      width: 6px;
      height: 40px;
      background: var(--accent);
    }

    /* Overview */

    .overview {
      background: var(--bg-light);
      padding: 32px 40px 28px;
    }

    .overview-topline {
      display: flex;
      justify-content: space-between;
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--muted);
      margin-bottom: 16px;
    }

    .overview-title {
      font-size: 30px;
      font-weight: 700;
      margin-bottom: 22px;
    }

    .overview-grid {
      display: grid;
      grid-template-columns: 2fr 2fr 1.2fr;
      gap: 16px;
      margin-bottom: 20px;
    }

    .overview-grid img {
      width: 100%;
      height: 260px;
      object-fit: cover;
    }

    .overview-copy {
      font-size: 12px;
      max-width: 720px;
      color: #444444;
      margin-bottom: 24px;
    }

    .overview-footer {
      display: flex;
      justify-content: space-between;
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
    }

    .overview-accent-bar {
      position: absolute;
      right: 16px;
      bottom: 16px;
      width: 6px;
      height: 40px;
      background: var(--accent);
    }

    .overview-wrapper {
      position: relative;
    }

    a {
      color: inherit;
      text-decoration: none;
      border-bottom: 1px solid rgba(0, 0, 0, 0.2);
      padding-bottom: 1px;
    }

    /* Responsive */

    @media (max-width: 900px) {
      .hero {
        grid-template-columns: 1fr;
      }

      .hero-image {
        min-height: 260px;
      }

      .panel-grid {
        grid-template-columns: 1fr;
      }

      .panel-thumbs {
        grid-template-columns: repeat(3, 1fr);
      }

      .overview-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 600px) {
      .hero-inner,
      .panel-dark,
      .overview {
        padding: 24px 18px;
      }

      .hero-title {
        font-size: 38px;
      }

      .hero-contact {
        grid-template-columns: 1fr;
      }

      .panel-header {
        flex-direction: column;
        align-items: flex-start;
        gap: 6px;
      }

      .overview-topline {
        flex-direction: column;
        gap: 6px;
      }

      .overview-footer {
        flex-direction: column;
        gap: 6px;
      }
    }
  </style>
</head>
<body>
  <div class="page">

    <!-- Hero section -->
    <section class="hero">
      <div class="hero-inner">
        <div class="hero-top">
          <div class="hero-title">
            <span>JAZEN</span>
            <span>PORTFOLIO</span>
          </div>
          <div class="hero-meta">
            <div>Paris - Global</div>
            <div>Fashion Studio</div>
          </div>
        </div>

        <div class="hero-contact">
          <div>
            <h4>Contact</h4>
            <p>Email: <a href="mailto:hello@jazenstudio.com">hello@jazenstudio.com</a></p>
            <p>Phone: +1 000 000 0000</p>
            <p>Instagram: @yourhandle</p>
            <p>Portfolio: jazenstudio.com</p>
          </div>
          <div>
            <h4>Studio</h4>
            <p>123 Lumiere St</p>
            <p>Paris, France</p>
            <p>Currently: Open to collaborations</p>
            <p>Focus: Fashion, creative direction, visual systems</p>
          </div>
        </div>

        <div class="hero-footer">
          <div class="hero-dot"></div>
          <div>Selected work 2022 - 2025</div>
        </div>
      </div>

      <div class="hero-image">
        <!-- Replace src with your own portrait or hero shot -->
        <img src="https://images.pexels.com/photos/1030895/pexels-photo-1030895.jpeg" alt="Hero image" />
        <div class="hero-side-label">Minimal portfolio by Jazen</div>
        <div class="hero-accent-bar"></div>
      </div>
    </section>

    <!-- Dark panel -->
    <section class="panel-wrapper">
      <div class="panel-dark">
        <div class="panel-header">
          <span>Studio Notes</span>
          <span>Luxury minimalism</span>
          <span>2025</span>
        </div>

        <div class="panel-grid">
          <div>
            <h3>Editorial direction</h3>
            <p>Clean layouts, strict grids, and negative space that lets garments, textures, and bodies speak first.</p>
          </div>
          <div>
            <h3>Visual identity</h3>
            <p>Logotypes, wordmarks, and systems that translate across print, digital, and spatial environments.</p>
          </div>
          <div>
            <h3>Creative atmosphere</h3>
            <p>Work rooted in intimacy and honesty, built around people rather than trends.</p>
          </div>
        </div>

        <div class="panel-thumbs">
          <!-- Replace these with your own small thumbnails -->
          <img src="https://images.pexels.com/photos/37347/office-freelancer-computer-business-37347.jpeg" alt="">
          <img src="https://images.pexels.com/photos/373965/pexels-photo-373965.jpeg" alt="">
          <img src="https://images.pexels.com/photos/1030933/pexels-photo-1030933.jpeg" alt="">
          <img src="https://images.pexels.com/photos/1030896/pexels-photo-1030896.jpeg" alt="">
          <img src="https://images.pexels.com/photos/373911/pexels-photo-373911.jpeg" alt="">
        </div>
      </div>
      <div class="panel-side-label">Curated work across fashion and image making</div>
      <div class="panel-accent-bar"></div>
    </section>

    <!-- Overview -->
    <section class="overview-wrapper">
      <div class="overview">
        <div class="overview-topline">
          <span>Jazen Studio</span>
          <span>Crafting cultural presence</span>
          <span>2025</span>
        </div>

        <div class="overview-title">Portfolio overview 6.0</div>

        <div class="overview-grid">
          <!-- Swap with your project shots -->
          <img src="https://images.pexels.com/photos/1030915/pexels-photo-1030915.jpeg" alt="Project 1">
          <img src="https://images.pexels.com/photos/1030899/pexels-photo-1030899.jpeg" alt="Project 2">
          <img src="https://images.pexels.com/photos/1030898/pexels-photo-1030898.jpeg" alt="Project 3">
        </div>

        <div class="overview-copy">
          Projects as systems, not fragments. Each series lives as a small universe: casting, styling, location, typography, and color working together as one language. This portfolio highlights campaign editorials, lookbooks, and experimental personal work that explores identity, texture, and movement.
        </div>

        <div class="overview-footer">
          <span>www: jazenstudio.com</span>
          <span>Currently based in Paris and Atlanta</span>
          <span>Contact: hello@jazenstudio.com</span>
        </div>
      </div>
      <div class="overview-accent-bar"></div>
    </section>

  </div>
</body>
</html>
