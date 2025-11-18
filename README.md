<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Obie Brown Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <!-- Digital looking font -->
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --bg-dark: #020202;
      --bg-light: #f4f4f4;
      --accent: #ff3b3b;
      --text-muted: #b4b4b4;
    }

    * {
      box-sizing: border-box;
    }

    html, body {
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
    }

    body {
      font-family: "Inter", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: var(--bg-dark);
      color: #ffffff;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* Layout utility */
    .page-padding {
      padding: 24px 7vw 32px;
    }

    /* HERO / HOME SECTION */

    .hero {
      min-height: 100vh;
      background: var(--bg-dark);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      position: relative;
      overflow: hidden;
    }

    .hero-header {
      font-family: "Orbitron", system-ui, sans-serif;
      font-size: 15px;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      display: flex;
      gap: 24px;
      align-items: center;
    }

    .hero-header span {
      white-space: nowrap;
    }

    .hero-middle {
      flex: 1;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .hero-middle-inner {
      display: flex;
      flex-wrap: wrap;
      gap: 64px;
      justify-content: center;
      text-align: center;
      font-family: "Orbitron", system-ui, sans-serif;
      font-size: 15px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
    }

    .hero-bottom {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 32px;
      flex-wrap: wrap;
    }

    .hero-description {
      max-width: 320px;
      font-size: 13px;
      line-height: 1.6;
      color: var(--text-muted);
    }

    .hero-description-title {
      font-family: "Orbitron", system-ui, sans-serif;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      font-size: 12px;
      margin-bottom: 12px;
      color: #ffffff;
    }

    /* Work strip */

    .work-strip-wrapper {
      flex: 1;
      min-width: 260px;
    }

    .work-strip {
      display: flex;
      gap: 18px;
      overflow-x: auto;
      padding-bottom: 6px;
      scroll-snap-type: x mandatory;
    }

    .work-strip::-webkit-scrollbar {
      height: 6px;
    }
    .work-strip::-webkit-scrollbar-track {
      background: #111111;
    }
    .work-strip::-webkit-scrollbar-thumb {
      background: #444444;
    }

    .work-item {
      scroll-snap-align: start;
      min-width: 230px;
      background: #111111;
      border-radius: 4px;
      overflow: hidden;
      border: 1px solid #202020;
    }

    .work-item img {
      display: block;
      width: 100%;
      height: auto;
    }

    .work-caption {
      padding: 8px 10px 10px;
      font-size: 11px;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.16em;
      font-family: "Orbitron", system-ui, sans-serif;
    }

    .work-index {
      margin-right: 6px;
      color: #ffffff;
    }

    /* Vertical text on the right */

    .vertical-tag {
      position: absolute;
      top: 50%;
      right: 16px;
      transform: translateY(-50%) rotate(90deg);
      transform-origin: center;
      font-family: "Orbitron", system-ui, sans-serif;
      font-size: 11px;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--text-muted);
      white-space: nowrap;
    }

    /* Scroll hint */

    .scroll-hint {
      position: absolute;
      bottom: 24px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.2em;
      color: var(--text-muted);
      display: flex;
      align-items: center;
      gap: 8px;
      cursor: pointer;
    }

    .scroll-hint svg {
      width: 14px;
      height: 14px;
    }

    /* ABOUT / RESUME SECTION */

    .about {
      background: var(--bg-light);
      color: #111111;
      padding-top: 72px;
      padding-bottom: 80px;
    }

    .about-inner {
      max-width: 1040px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: minmax(0, 3fr) minmax(0, 2fr);
      gap: 48px;
      align-items: start;
    }

    .about-heading {
      font-family: "Orbitron", system-ui, sans-serif;
      font-size: 18px;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      margin-bottom: 16px;
    }

    .about-subtitle {
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 0.24em;
      color: #777777;
      margin-bottom: 18px;
    }

    .about-body {
      font-size: 14px;
      line-height: 1.8;
      color: #333333;
      margin-bottom: 24px;
    }

    .resume-block {
      border-top: 1px solid #dddddd;
      padding-top: 18px;
      margin-top: 4px;
      font-size: 13px;
    }

    .resume-item {
      margin-bottom: 16px;
    }

    .resume-title {
      font-weight: 600;
      font-size: 13px;
    }

    .resume-meta {
      font-size: 12px;
      color: #777777;
      margin-bottom: 6px;
    }

    .resume-text {
      font-size: 13px;
      color: #444444;
    }

    .contact-block {
      margin-top: 24px;
      font-size: 13px;
      line-height: 1.8;
    }

    .contact-block a {
      color: #111111;
      text-decoration: underline;
      text-decoration-thickness: 1px;
      text-underline-offset: 3px;
    }

    .contact-label {
      text-transform: uppercase;
      letter-spacing: 0.16em;
      font-size: 11px;
      color: #777777;
    }

    .social-row {
      margin-top: 10px;
      display: flex;
      gap: 10px;
      align-items: center;
    }

    .social-icon {
      width: 28px;
      height: 28px;
      border-radius: 999px;
      border: 1px solid #cccccc;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-size: 13px;
      font-weight: 500;
      cursor: pointer;
    }

    /* Photo */

    .about-photo {
      width: 100%;
      max-width: 360px;
      margin-left: auto;
      border-radius: 12px;
      aspect-ratio: 3 / 4;
      object-fit: cover;
      border: 1px solid #d6d6d6;
      background: #dddddd;
    }

    .about-photo-caption {
      font-size: 11px;
      color: #888888;
      margin-top: 8px;
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    /* Responsive */

    @media (max-width: 900px) {
      .hero-bottom {
        flex-direction: column;
        align-items: flex-start;
      }

      .vertical-tag {
        display: none;
      }

      .about-inner {
        grid-template-columns: minmax(0, 1fr);
      }

      .about-photo {
        margin: 16px 0 0 0;
      }
    }

    @media (max-width: 600px) {
      .page-padding {
        padding-inline: 18px;
      }

      .hero-middle-inner {
        gap: 28px;
      }

      .hero-header {
        flex-wrap: wrap;
        gap: 12px;
      }
    }
  </style>
</head>
<body>

  <!-- HOME / HERO -->
  <section class="hero page-padding" id="top">
    <header class="hero-header">
      <span>Obie Brown</span>
      <span>Portfolio</span>
      <span>2026</span>
    </header>

    <div class="hero-middle">
      <div class="hero-middle-inner">
        <span>Brand Systems</span>
        <span>Visual Experiments</span>
        <span>Digital Storytelling</span>
      </div>
    </div>

    <div class="hero-bottom">
      <div class="hero-description">
        <div class="hero-description-title">Marketing and Design</div>
        <p>
          Placeholder bio text for Obie Brown. This line explains a focus on
          strategy, visual identity, and concept driven campaigns that live at
          the edge of fashion, culture, and technology. Add a sharper personal
          description here once your portfolio is ready.
        </p>
      </div>

      <div class="work-strip-wrapper">
        <div class="work-strip">
          <!-- Work item 1 -->
          <a class="work-item" href="/404.html">
            <img src="https://via.placeholder.com/480x320?text=Project+01" alt="Project 01 placeholder" />
            <div class="work-caption">
              <span class="work-index">001</span>
              Urban Echo: Campaign Identity
            </div>
          </a>
          <!-- Work item 2 -->
          <a class="work-item" href="/404.html">
            <img src="https://via.placeholder.com/480x320?text=Project+02" alt="Project 02 placeholder" />
            <div class="work-caption">
              <span class="work-index">002</span>
              Lumen Studio: Digital Lookbook
            </div>
          </a>
          <!-- Work item 3 -->
          <a class="work-item" href="/404.html">
            <img src="https://via.placeholder.com/480x320?text=Project+03" alt="Project 03 placeholder" />
            <div class="work-caption">
              <span class="work-index">003</span>
              Signal Type: Visual System
            </div>
          </a>
          <!-- Work item 4 -->
          <a class="work-item" href="/404.html">
            <img src="https://via.placeholder.com/480x320?text=Project+04" alt="Project 04 placeholder" />
            <div class="work-caption">
              <span class="work-index">004</span>
              Transit Moodboard: Experiential Map
            </div>
          </a>
        </div>
      </div>
    </div>

    <div class="vertical-tag">
      Obie Brown: Ongoing Practice in Visual Systems
    </div>

    <a href="#about" class="scroll-hint">
      <span>Scroll to resume</span>
      <svg viewBox="0 0 24 24" aria-hidden="true">
        <path fill="currentColor" d="M12 16.5l-6.3-6.3 1.4-1.4L12 13.7l4.9-4.9 1.4 1.4z"/>
      </svg>
    </a>
  </section>

  <!-- ABOUT / RESUME -->
  <section class="about" id="about">
    <div class="about-inner">
      <div>
        <div class="about-subtitle">Profile</div>
        <h2 class="about-heading">About Obie Brown</h2>
        <p class="about-body">
          Placeholder copy for an extended introduction. Describe your approach
          to marketing and design, how you move between strategy and execution,
          and the kinds of brands or clients you enjoy working with. Touch on
          your interest in fashion, culture, and technology driven storytelling.
        </p>

        <div class="resume-block">
          <div class="resume-item">
            <div class="resume-title">Role Title Here</div>
            <div class="resume-meta">Company Name: 2023 – Present</div>
            <div class="resume-text">
              Short bullet style description of what you do on a daily basis,
              key achievements, and measurable impact. Replace this placeholder
              with real experience items.
            </div>
          </div>
          <div class="resume-item">
            <div class="resume-title">Previous Role Title</div>
            <div class="resume-meta">Studio or Brand: 2020 – 2023</div>
            <div class="resume-text">
              Another block to outline responsibilities in marketing and design,
              such as building campaigns, leading shoots, or developing brand
              systems across digital touchpoints.
            </div>
          </div>
        </div>

        <div class="contact-block">
          <div class="contact-label">Contact</div>
          <div>E-mail: <a href="mailto:jazenbrownjr@gmail.com">jazenbrownjr@gmail.com</a></div>
          <div>Phone: <a href="tel:+16782008121">678-200-8121</a></div>

          <div class="social-row">
            <span class="contact-label">Social</span>
            <!-- Replace with real links or icon fonts later -->
            <div class="social-icon" title="Instagram">IG</div>
            <div class="social-icon" title="Behance">Be</div>
            <div class="social-icon" title="LinkedIn">In</div>
          </div>
        </div>
      </div>

      <div>
        <!-- Replace src with your own portrait later -->
        <img class="about-photo" src="https://via.placeholder.com/600x800?text=Portrait+Placeholder" alt="Portrait placeholder" />
        <div class="about-photo-caption">
          Portrait placeholder: replace with your own image
        </div>
      </div>
    </div>
  </section>

</body>
</html>
