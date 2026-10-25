# healthweb
racing mind
<!doctype html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#f4f0e8">
  <meta name="description" content="Confidential mental health support and useful numbers for people working in racing yards.">
  <title>Yardline | Support for racing-yard staff</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      color-scheme: light;
      --ink: #202923;
      --muted: #626a62;
      --paper: #f4f0e8;
      --white: #fffdf9;
      --line: #d8d7ca;
      --green: #234d3b;
      --green-dark: #193a2d;
      --lime: #dceba7;
      --coral: #c64b34;
      --coral-pale: #f8e6df;
      --blue: #dce9eb;
      --sans: "DM Sans", sans-serif;
      --display: "Manrope", sans-serif;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      background: var(--paper);
      color: var(--ink);
      font-family: var(--sans);
      font-size: 16px;
      line-height: 1.5;
    }
    a { color: inherit; }
    button, a { -webkit-tap-highlight-color: transparent; }
    .wrap { width: min(1180px, calc(100% - 48px)); margin-inline: auto; }
    .skip-link {
      position: absolute; top: 8px; left: 8px; z-index: 10;
      padding: 10px 14px; background: var(--white); transform: translateY(-150%);
    }
    .skip-link:focus { transform: translateY(0); }
    header {
      min-height: 78px;
      display: flex; align-items: center;
      border-bottom: 1px solid rgba(32,41,35,.13);
    }
    .header-inner { display: flex; align-items: center; justify-content: space-between; gap: 24px; }
    .brand { display: inline-flex; align-items: center; gap: 11px; text-decoration: none; }
    .brand-mark {
      width: 34px; height: 34px; display: grid; place-items: center;
      color: var(--lime); background: var(--green); border-radius: 50% 50% 4px 50%;
      font: 800 16px var(--display); transform: rotate(-8deg);
    }
    .brand-name { font: 800 19px var(--display); letter-spacing: 0; }
    .brand-note { margin-left: 3px; color: var(--muted); font-size: 12px; }
    nav { display: flex; align-items: center; gap: 30px; }
    nav a { text-decoration: none; color: #38433b; font-size: 14px; font-weight: 600; }
    nav a:hover { text-decoration: underline; text-underline-offset: 4px; }
    .header-call {
      display: inline-flex; align-items: center; gap: 9px; min-height: 42px;
      padding: 0 14px; border-radius: 3px; background: var(--green); color: white;
      font-size: 13px; font-weight: 700; text-decoration: none;
    }
    .header-call:hover, .primary-link:hover { background: var(--green-dark); }
    .phone-icon { width: 17px; height: 17px; flex: 0 0 auto; }

    main { padding: 31px 0 72px; }
    .eyebrow {
      display: flex; align-items: center; gap: 10px; margin: 0 0 16px;
      color: var(--green); font-size: 11px; font-weight: 700; letter-spacing: 1.2px; text-transform: uppercase;
    }
    .eyebrow::before { content: ""; width: 23px; height: 2px; background: var(--coral); }
    .intro { display: grid; grid-template-columns: 1.1fr .9fr; gap: 38px; align-items: end; margin-bottom: 25px; }
    h1, h2, h3, p { margin-top: 0; }
    h1 { max-width: 660px; margin-bottom: 0; font: 700 clamp(38px, 5vw, 64px)/1.03 var(--display); letter-spacing: 0; }
    .intro-copy { max-width: 410px; margin: 0 0 4px; color: #555f56; font-size: 16px; }
    .hero-grid { display: grid; grid-template-columns: 1.04fr .96fr; min-height: 412px; }
    .image-panel {
      position: relative; overflow: hidden; min-height: 412px;
      background: #4d5c49 url("https://images.unsplash.com/photo-1553284965-83fd3e82fa5a?auto=format&fit=crop&w=1400&q=85") center 49% / cover no-repeat;
      color: white;
    }
    .image-panel::before {
      content: ""; position: absolute; inset: 0;
      background: linear-gradient(180deg, rgba(13,31,23,.05) 24%, rgba(13,31,23,.82) 100%);
    }
    .image-caption { position: absolute; right: 26px; bottom: 24px; left: 28px; z-index: 1; }
    .image-caption .tag { margin: 0 0 10px; color: var(--lime); font-size: 11px; font-weight: 700; letter-spacing: 1.3px; text-transform: uppercase; }
    .image-caption h2 { max-width: 430px; margin: 0 0 8px; font: 700 29px/1.18 var(--display); }
    .image-caption p { max-width: 430px; margin: 0; color: rgba(255,255,255,.86); font-size: 14px; }
    .help-panel { display: flex; flex-direction: column; background: var(--white); padding: 28px 30px 25px; }
    .help-panel-heading { display: flex; align-items: flex-start; justify-content: space-between; gap: 12px; margin-bottom: 10px; }
    .help-panel h2 { margin: 0; font: 700 24px var(--display); }
    .uk-label { color: var(--muted); font-size: 11px; white-space: nowrap; }
    .urgent-note { margin: 0 0 12px; color: var(--muted); font-size: 13px; }
    .number-list { margin: 0; padding: 0; list-style: none; }
    .number-item { display: grid; grid-template-columns: 1fr auto; gap: 12px; align-items: center; padding: 15px 0; border-top: 1px solid #e7e4db; }
    .number-item.emergency { margin: 0 -12px; padding: 14px 12px; background: var(--coral-pale); border-top: 0; }
    .number-name { display: block; margin-bottom: 2px; font-weight: 700; font-size: 14px; }
    .number-detail { display: block; max-width: 300px; color: var(--muted); font-size: 12px; line-height: 1.45; }
    .number-actions { display: flex; flex-direction: column; align-items: flex-end; gap: 4px; }
    .number-link { color: var(--green); font: 800 18px var(--display); text-decoration-thickness: 1px; text-underline-offset: 3px; white-space: nowrap; }
    .emergency .number-link { color: #9f3827; }
    .text-link { color: var(--muted); font-size: 11px; text-decoration: none; }
    .text-link:hover { text-decoration: underline; }
    .availability { display: inline-flex; align-items: center; gap: 5px; color: var(--muted); font-size: 10px; }
    .availability::before { content: ""; width: 6px; height: 6px; background: #64915a; border-radius: 50%; }
    .primary-link {
      display: flex; justify-content: space-between; align-items: center; gap: 10px;
      width: 100%; margin-top: auto; padding: 13px 15px; background: var(--green); color: white;
      font-size: 13px; font-weight: 700; text-decoration: none; transition: background .18s ease;
    }
    .arrow { font-size: 18px; line-height: 1; }

    .support-section { padding-top: 59px; }
    .section-top { display: flex; align-items: end; justify-content: space-between; gap: 24px; margin-bottom: 20px; }
    .section-top .eyebrow { margin-bottom: 9px; }
    .section-top h2 { margin: 0; font: 700 30px/1.15 var(--display); }
    .section-aside { max-width: 360px; margin: 0; color: var(--muted); font-size: 13px; }
    .support-grid { display: grid; grid-template-columns: repeat(3, 1fr); border-top: 1px solid var(--line); border-bottom: 1px solid var(--line); }
    .support-item { min-height: 190px; padding: 22px 24px 24px 0; }
    .support-item + .support-item { padding-left: 24px; border-left: 1px solid var(--line); }
    .item-number { display: block; margin-bottom: 22px; color: var(--coral); font: 700 12px var(--display); }
    .support-item h3 { margin-bottom: 8px; font: 700 18px var(--display); }
    .support-item p { max-width: 305px; margin: 0 0 13px; color: var(--muted); font-size: 13px; }
    .plain-link { color: var(--green); font-size: 12px; font-weight: 700; text-underline-offset: 3px; }

    .yard-strip { display: grid; grid-template-columns: 1fr auto; gap: 24px; align-items: center; margin-top: 48px; padding: 24px 28px; background: var(--blue); }
    .yard-strip h2 { margin: 0 0 5px; font: 700 20px var(--display); }
    .yard-strip p { max-width: 590px; margin: 0; color: #515f61; font-size: 13px; }
    .yard-strip a { display: inline-flex; align-items: center; gap: 14px; color: #234b50; font-size: 13px; font-weight: 700; text-decoration: none; white-space: nowrap; }
    .yard-strip a:hover { text-decoration: underline; text-underline-offset: 4px; }
    footer { padding: 22px 0 30px; border-top: 1px solid var(--line); color: #687067; font-size: 11px; }
    .footer-inner { display: flex; justify-content: space-between; gap: 20px; }
    footer p { margin: 0; }
    footer a { color: inherit; text-underline-offset: 2px; }

    @media (max-width: 760px) {
      .wrap { width: min(100% - 32px, 560px); }
      header { min-height: 66px; }
      .brand-note, nav { display: none; }
      .header-call { min-height: 40px; padding-inline: 11px; font-size: 12px; }
      main { padding-top: 25px; }
      .intro { grid-template-columns: 1fr; gap: 12px; margin-bottom: 18px; }
      h1 { max-width: 520px; font-size: clamp(40px, 12vw, 58px); }
      .intro-copy { max-width: 500px; font-size: 14px; }
      .hero-grid { grid-template-columns: 1fr; }
      .image-panel { min-height: 310px; }
      .help-panel { padding: 23px 20px 20px; }
      .support-section { padding-top: 43px; }
      .section-top { display: block; }
      .section-top h2 { font-size: 27px; }
      .section-aside { margin-top: 9px; }
      .support-grid { grid-template-columns: 1fr; }
      .support-item { min-height: unset; padding: 17px 0 19px; }
      .support-item + .support-item { padding-left: 0; border-left: 0; border-top: 1px solid var(--line); }
      .item-number { margin-bottom: 8px; }
      .support-item h3 { margin-bottom: 5px; }
      .support-item p { margin-bottom: 8px; }
      .yard-strip { grid-template-columns: 1fr; gap: 15px; margin-top: 34px; padding: 20px; }
      .footer-inner { flex-direction: column; gap: 8px; }
    }
    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
      *, *::before, *::after { transition-duration: .01ms !important; }
    }
  </style>
</head>
<body>
  <a class="skip-link" href="#main">Skip to support</a>
  <header>
    <div class="wrap header-inner">
      <a class="brand" href="#top" aria-label="Yardline home">
        <span class="brand-mark" aria-hidden="true">Y</span>
        <span class="brand-name">yardline</span>
        <span class="brand-note">support for racing people</span>
      </a>
      <nav aria-label="Main navigation">
        <a href="#support">Find support</a>
        <a href="#everyday">Everyday wellbeing</a>
        <a href="#yards">For yards</a>
      </nav>
      <a class="header-call" href="tel:08006300443">
        <svg class="phone-icon" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M7.2 3.8h2.2l1.1 4.4-1.8 1.8a15.1 15.1 0 0 0 5.3 5.3l1.8-1.8 4.4 1.1v2.2a2 2 0 0 1-2.2 2A15.9 15.9 0 0 1 5.2 6a2 2 0 0 1 2-2.2Z" stroke="currentColor" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round"/></svg>
        Call Racing Welfare
      </a>
    </div>
  </header>

  <main id="main" class="wrap">
    <section id="top" aria-labelledby="page-title">
      <div class="intro">
        <div>
          <p class="eyebrow">A bit of support goes a long way</p>
          <h1 id="page-title">You look after them.<br>We’re here for you.</h1>
        </div>
        <p class="intro-copy">Racing yards can ask a lot of you. Whether it’s a tough shift, a difficult stretch, or just a need to talk, support is here without judgement.</p>
      </div>

      <div class="hero-grid" id="support">
        <div class="image-panel" role="img" aria-label="Racehorse being cared for outdoors">
          <div class="image-caption">
            <p class="tag">You don’t have to figure it out alone</p>
            <h2>Start with one conversation.</h2>
            <p>Talk to someone who understands the racing community and what working in a yard can be like.</p>
          </div>
        </div>
        <section class="help-panel" aria-labelledby="help-title">
          <div class="help-panel-heading">
            <h2 id="help-title">Useful numbers</h2>
            <span class="uk-label">UK support</span>
          </div>
          <p class="urgent-note">You can call now. You don’t need to have the right words.</p>
          <ul class="number-list">
            <li class="number-item">
              <div><span class="number-name">Racing Welfare</span><span class="number-detail">Confidential support for anyone working in, or retired from, horseracing.</span></div>
              <div class="number-actions"><a class="number-link" href="tel:08006300443">0800 630 0443</a><span class="availability">24-hour helpline</span></div>
            </li>
            <li class="number-item">
              <div><span class="number-name">Samaritans</span><span class="number-detail">For anyone who needs someone to listen, day or night.</span></div>
              <div class="number-actions"><a class="number-link" href="tel:116123">116 123</a><span class="availability">Free, 24/7</span></div>
            </li>
            <li class="number-item">
              <div><span class="number-name">Shout</span><span class="number-detail">Free, confidential text support if talking feels difficult.</span></div>
              <div class="number-actions"><a class="number-link" href="sms:85258?body=SHOUT">Text SHOUT</a><span class="text-link">to 85258 · 24/7</span></div>
            </li>
            <li class="number-item emergency">
              <div><span class="number-name">Immediate danger</span><span class="number-detail">If you or someone else is in immediate danger, call emergency services.</span></div>
              <div class="number-actions"><a class="number-link" href="tel:999">999 / 112</a><span class="text-link">Emergency services</span></div>
            </li>
          </ul>
          <a class="primary-link" href="https://racingwelfare.co.uk/" target="_blank" rel="noreferrer">Visit Racing Welfare <span class="arrow" aria-hidden="true">↗</span></a>
        </section>
      </div>
    </section>

    <section class="support-section" id="everyday" aria-labelledby="everyday-title">
      <div class="section-top">
        <div><p class="eyebrow">For the everyday stuff, too</p><h2 id="everyday-title">Small steps count.</h2></div>
        <p class="section-aside">You don’t have to wait until things feel unbearable before reaching out.</p>
      </div>
      <div class="support-grid">
        <article class="support-item">
          <span class="item-number">01 / CHECK IN</span>
          <h3>How are you, really?</h3>
          <p>Take a minute to notice what’s going on for you. Tired, wound up, flat, okay: it all counts.</p>
          <a class="plain-link" href="https://racingwelfare.co.uk/mental-health/" target="_blank" rel="noreferrer">Explore mental wellbeing resources <span aria-hidden="true">↗</span></a>
        </article>
        <article class="support-item">
          <span class="item-number">02 / TALK</span>
          <h3>Say it to someone</h3>
          <p>A trusted person, a colleague, or a support line. You can start with “I’m not sure what I need.”</p>
          <a class="plain-link" href="tel:08006300443">Call Racing Welfare <span aria-hidden="true">→</span></a>
        </article>
        <article class="support-item">
          <span class="item-number">03 / LOOK OUT</span>
          <h3>Check on your people</h3>
          <p>A quiet “How are you doing?” can open a door. Listen, give them time, and help them find support.</p>
          <a class="plain-link" href="https://racingwelfare.co.uk/mental-health/" target="_blank" rel="noreferrer">Support and guidance <span aria-hidden="true">↗</span></a>
        </article>
      </div>
    </section>

    <aside class="yard-strip" id="yards">
      <div><h2>For trainers and yard managers</h2><p>Make support part of the day-to-day. Find guidance and practical resources for looking after the people in your yard.</p></div>
      <a href="https://racingwelfare.co.uk/" target="_blank" rel="noreferrer">Resources for racing yards <span class="arrow" aria-hidden="true">↗</span></a>
    </aside>
  </main>

  <footer>
    <div class="wrap footer-inner">
      <p>Yardline is a signposting page, not a counselling or emergency service. UK numbers and services; availability may change.</p>
      <p>In an emergency, call <a href="tel:999">999</a> or <a href="tel:112">112</a>.</p>
    </div>
  </footer>
</body>
</html>
