<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Obie Brown Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <!-- Coding style font -->
  <link href="https://fonts.googleapis.com/css2?family=Source+Code+Pro:wght@400;500;600&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />

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

    .page-padding {
      padding: 24px 0 32px;
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
      font-family: "Source Code Pro", "SFMono-Regular", Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.22em;
      display: flex;
      align-items: center;
      padding-inline: 24px;
    }

    .hero-name {
      margin-right: 12px;
      white-space: nowrap;
    }

    .hero-tag {
      margin-left: auto;
      margin-right: 80px;
      white-space: nowrap;
    }

    .hero-year {
      margin-right: 24px;
      white-space: nowrap;
    }

    .hero-middle {
      flex: 1;
      display: flex;
      align-items: center;
      padding-inline: 24px;
    }

    .hero-middle-inner {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      flex-wrap: nowrap;
      justify-content: flex-start;
      align-items: center;
      gap: 260px; /* large spacing between phrases */
      font-family: "Source Code Pro", "SFMono-Regular", Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.24em;
      text-align: left;
      white-space: nowrap;
    }

    .hero-bottom {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 32px;
      flex-wrap: nowrap;
      padding-inline: 24px;
    }

    .hero-description {
      flex: 0 0 20%;
      max-width: 260px;
      font-size: 12px;
      line-height: 1.7;
      color: var(--text-muted);
    }

    .hero-description-title {
      font-family: "Source Code Pro", "SFMono-Regular", Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      text-transform: uppercase;
      letter-spacing: 0.2em;
      font-size: 11px;
      margin-bottom: 12px;
      color: #ffffff;
    }

    /* Work strip */

    .work-strip-wrapper {
      position: relative;
      flex: 0 0 80%;
      min-width: 260px;
    }

    .work-strip {
      display: flex;
      gap: 18px;
      overflow-x: auto;
      padding-bottom: 6px;
      scroll-snap-type: x mandatory;
      scrollbar-width: none; /* Firefox hide scrollbar */
    }

    .work-strip::-webkit-scrollbar {
      display: none; /* WebKit hide */
    }

    .work-item {
      scroll-snap-align: start;
      min-width: 260px;
      background: #111111;
      border-radius: 0;
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
      letter-spacing: 0.18em;
      font-family: "Source Code Pro", "SFMono-Regular", Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
    }

    .work-index {
      margin-right: 6px;
      color: #ffffff;
    }

    .work-next-arrow {
      position: absolute;
      right: 24px;
      top: 50%;
      transform: translateY(-50%);
      width: 40px;
      height: 40px;
      border-radius: 999px;
      border: 1px solid #444444;
      background: rgba(5, 5, 5, 0.9);
      color: #ffffff;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.25s ease-in-out;
      font-size: 18px;
    }

    .work-strip-wrapper:hover .work-next-arrow {
      opacity: 1;
      pointer-events: auto;
    }

    /* ABOUT / RESUME SECTION */

    .about {
      background: var(--bg-light);
      color: #111111;
      padding: 72px 24px 80px;
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
      font-family: "Source Code Pro", "SFMono-Regular", Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      font-size: 18px;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      margin-bottom: 16px;
    }

    .about-subtitle {
      font-size: 13px;
      text-transform: uppercase;
      letter-spacing: 0.26em;
      color: #777777;
      margin-bottom: 18px;
    }

    .about-body {
      font-size: 13px;
      line-height: 1.85;
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

    .social-logo {
      width: 32px;
      height: 32px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
    }

    .social-logo img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      display: block;
    }

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

    @media (max-width: 900px) {
      .hero-bottom {
        flex-direction: column;
        align-items: flex-start;
      }

      .hero-description {
        flex: 0 0 100%;
        max-width: 100%;
      }

      .work-strip-wrapper {
        flex: 0 0 100%;
      }

      .about-inner {
        grid-template-columns: minmax(0, 1fr);
      }

      .about-photo {
        margin: 16px 0 0 0;
      }
    }

    @media (max-width: 600px) {
      .hero-middle-inner {
        gap: 120px;
        font-size: 11px;
      }

      .hero-header {
        padding-inline: 16px;
      }

      .hero-year {
        margin-right: 16px;
      }

      .hero-bottom {
        padding-inline: 16px;
      }

      .about {
        padding-inline: 16px;
      }

      .work-next-arrow {
        right: 16px;
      }
    }
  </style>
</head>
<body>

  <!-- HOME / HERO -->
  <section class="hero page-padding" id="top">
    <header class="hero-header">
      <span class="hero-name">Obie Brown</span>
      <span class="hero-tag">Portfolio</span>
      <span class="hero-year">2026</span>
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
          <!-- Use your own AI generated artwork here later -->
          <a class="work-item" href="/404.html">
            <img src="https://picsum.photos/seed/ai-project-01/480/320" alt="AI generated project 01" />
            <div class="work-caption">
              <span class="work-index">001</span>
              Urban Echo: Campaign Identity
            </div>
          </a>

          <a class="work-item" href="/404.html">
            <img src="https://picsum.photos/seed/ai-project-02/480/320" alt="AI generated project 02" />
            <div class="work-caption">
              <span class="work-index">002</span>
              Lumen Studio: Digital Lookbook
            </div>
          </a>

          <a class="work-item" href="/404.html">
            <img src="https://picsum.photos/seed/ai-project-03/480/320" alt="AI generated project 03" />
            <div class="work-caption">
              <span class="work-index">003</span>
              Signal Type: Visual System
            </div>
          </a>

          <a class="work-item" href="/404.html">
            <img src="https://picsum.photos/seed/ai-project-04/480/320" alt="AI generated project 04" />
            <div class="work-caption">
              <span class="work-index">004</span>
              Transit Moodboard: Experiential Map
            </div>
          </a>
        </div>

        <button class="work-next-arrow" type="button" aria-label="Next project">
          →
        </button>
      </div>
    </div>
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
            <!-- Replace src values with your own logo files -->
            <a class="social-logo" href="#">
              <img src="instagram-logo.svg" alt="Instagram logo" />
            </a>
            <a class="social-logo" href="#">
              <img src="behance-logo.svg" alt="Behance logo" />
            </a>
            <a class="social-logo" href="#">
              <img src="linkedin-logo.svg" alt="LinkedIn logo" />
            </a>
          </div>
        </div>
      </div>

      <div>
        <!-- Replace src with your own portrait later -->
        <img class="about-photo" src="https://picsum.photos/seed/portrait-ai/600/800" alt="Portrait placeholder" />
        <div class="about-photo-caption">
          Portrait placeholder: replace with your own image
        </div>
      </div>
    </div>
  </section>

  <script>
    // Scroll to next work item when arrow is clicked
    document.addEventListener("DOMContentLoaded", function () {
      const strip = document.querySelector(".work-strip");
      const arrow = document.querySelector(".work-next-arrow");

      if (!strip || !arrow) return;

      arrow.addEventListener("click", function () {
        const item = strip.querySelector(".work-item");
        if (!item) return;

        const style = window.getComputedStyle(strip);
        const gap = parseFloat(style.columnGap || style.gap || "18") || 18;

        const width = item.getBoundingClientRect().width;
        const scrollAmount = width + gap;

        strip.scrollBy({
          left: scrollAmount,
          behavior: "smooth"
        });
      });
    });
  </script>
</body>
</html>
