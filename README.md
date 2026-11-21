<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jai Prakash Narayan Sarvodaya Vidyalaya | Udaipur, Varanasi</title>
<style>
  :root {
    --navy: #0a1a3a;
    --navy2: #112a5c;
    --gold: #f5b82e;
    --gold2: #ffd978;
    --saffron: #ff7a1a;
    --white: #ffffff;
    --soft: #f4f7fc;
    --text: #1d2740;
    --muted: #6b7690;
    --shadow: 0 18px 45px rgba(10,26,58,.15);
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; scroll-padding-top: 110px; }
  body { font-family: "Segoe UI", system-ui, -apple-system, sans-serif; color: var(--text); background: var(--white); overflow-x: hidden; line-height: 1.65; }
  a { color: inherit; }
  img { max-width: 100%; }

  /* ---------- STATUS BAR ---------- */
  .status-bar {
    background: linear-gradient(90deg, var(--navy), var(--navy2));
    color: #cfd8ee; font-size: .82rem; padding: 8px 6%;
    display: flex; justify-content: space-between; align-items: center; gap: 14px; flex-wrap: wrap;
    position: relative; z-index: 110;
  }
  .status-bar .left, .status-bar .right { display: flex; gap: 18px; align-items: center; flex-wrap: wrap; }
  .status-bar span.item { display: inline-flex; align-items: center; gap: 6px; }
  .live-dot { width: 8px; height: 8px; border-radius: 50%; background: #3ddc84; box-shadow: 0 0 0 0 rgba(61,220,132,.7); animation: ping 1.8s infinite; }
  @keyframes ping { 0% { box-shadow: 0 0 0 0 rgba(61,220,132,.7);} 70% { box-shadow: 0 0 0 10px rgba(61,220,132,0);} 100% { box-shadow: 0 0 0 0 rgba(61,220,132,0);} }
  .ticker-wrap { overflow: hidden; flex: 1; min-width: 200px; max-width: 520px; }
  .ticker { display: inline-block; white-space: nowrap; color: var(--gold2); animation: ticker 22s linear infinite; }
  @keyframes ticker { from { transform: translateX(100%);} to { transform: translateX(-100%);} }
  .status-bar a { color: var(--gold); text-decoration: none; }

  /* ---------- NAVBAR ---------- */
  nav {
    position: sticky; top: 0; z-index: 100;
    background: rgba(255,255,255,.92); backdrop-filter: blur(14px);
    box-shadow: 0 2px 20px rgba(10,26,58,.08);
    padding: 12px 6%; display: flex; justify-content: space-between; align-items: center;
    transition: padding .3s, box-shadow .3s;
  }
  nav.scrolled { padding: 8px 6%; box-shadow: 0 6px 30px rgba(10,26,58,.15); }
  .brand { display: flex; align-items: center; gap: 12px; text-decoration: none; }
  .crest {
    width: 48px; height: 48px; border-radius: 50%;
    background: conic-gradient(from 0deg, var(--gold), var(--saffron), var(--gold2), var(--gold));
    display: flex; align-items: center; justify-content: center; font-size: 1.4rem;
    animation: spin 10s linear infinite; box-shadow: 0 6px 18px rgba(245,184,46,.4);
  }
  .crest-inner { width: 40px; height: 40px; border-radius: 50%; background: var(--navy); display: flex; align-items: center; justify-content: center; animation: spinRev 10s linear infinite; }
  @keyframes spin { to { transform: rotate(360deg);} }
  @keyframes spinRev { to { transform: rotate(-360deg);} }
  .brand-text { line-height: 1.2; }
  .brand-text strong { display: block; color: var(--navy); font-size: .98rem; }
  .brand-text small { color: var(--muted); font-size: .72rem; letter-spacing: .5px; }

  .menu { display: flex; gap: 4px; list-style: none; }
  .menu a {
    position: relative; text-decoration: none; color: var(--navy); font-weight: 600; font-size: .9rem;
    padding: 9px 13px; border-radius: 8px; transition: color .3s, background .3s; display: block;
  }
  .menu a::after {
    content: ""; position: absolute; left: 50%; bottom: 3px; width: 0; height: 2px;
    background: var(--gold); transform: translateX(-50%); transition: width .3s;
  }
  .menu a:hover, .menu a.active { color: var(--saffron); background: #fff6e6; }
  .menu a:hover::after, .menu a.active::after { width: 60%; }
  .menu-toggle { display: none; background: none; border: none; font-size: 1.8rem; cursor: pointer; color: var(--navy); }

  /* ---------- HERO ---------- */
  .hero {
    position: relative; min-height: 88vh; overflow: hidden;
    background: linear-gradient(135deg, var(--navy) 0%, #183a7a 55%, #0d2350 100%);
    color: var(--white); display: flex; align-items: center; justify-content: center; text-align: center;
    padding: 80px 6%;
  }
  .hero::before {
    content: ""; position: absolute; inset: 0;
    background-image: radial-gradient(rgba(255,255,255,.12) 1px, transparent 1px);
    background-size: 28px 28px; animation: drift 30s linear infinite;
  }
  @keyframes drift { to { background-position: 280px 280px; } }
  .blob { position: absolute; border-radius: 50%; filter: blur(70px); opacity: .45; animation: float 12s ease-in-out infinite; }
  .blob.b1 { width: 380px; height: 380px; background: var(--saffron); top: -120px; left: -100px; }
  .blob.b2 { width: 320px; height: 320px; background: var(--gold); bottom: -120px; right: -80px; animation-delay: -6s; }
  @keyframes float { 50% { transform: translate(30px,-25px) scale(1.08);} }
  .hero-inner { position: relative; z-index: 2; max-width: 900px; }
  .hero .eyebrow {
    display: inline-block; padding: 7px 18px; border-radius: 999px; font-size: .85rem; letter-spacing: 1px;
    background: rgba(245,184,46,.15); border: 1px solid rgba(245,184,46,.5); color: var(--gold2);
    animation: fadeUp .8s ease both;
  }
  .hero h1 {
    font-size: clamp(2rem, 5.2vw, 3.8rem); line-height: 1.15; margin: 22px 0 16px; font-weight: 800;
    animation: fadeUp .9s ease .2s both;
  }
  .hero h1 .gold {
    background: linear-gradient(90deg, var(--gold), var(--gold2), var(--saffron), var(--gold));
    background-size: 300% auto; -webkit-background-clip: text; color: transparent; animation: shine 5s linear infinite;
  }
  @keyframes shine { to { background-position: 300% center; } }
  .hero p.sub { font-size: 1.1rem; color: #d6def2; max-width: 640px; margin: 0 auto 32px; animation: fadeUp .9s ease .4s both; }
  .hero .btns { display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; animation: fadeUp .9s ease .6s both; }
  .btn {
    padding: 14px 30px; border-radius: 40px; text-decoration: none; font-weight: 700; font-size: .95rem;
    transition: transform .3s, box-shadow .3s; display: inline-block;
  }
  .btn.gold { background: linear-gradient(90deg, var(--gold), var(--saffron)); color: var(--navy); box-shadow: 0 10px 25px rgba(245,184,46,.35); }
  .btn.outline { border: 2px solid rgba(255,255,255,.5); color: var(--white); }
  .btn:hover { transform: translateY(-3px); }
  .scroll-hint { position: absolute; bottom: 24px; left: 50%; transform: translateX(-50%); color: var(--gold2); font-size: .8rem; animation: bounce 2s infinite; z-index: 2; }
  @keyframes bounce { 50% { transform: translate(-50%, 8px);} }

  /* ---------- STATS ---------- */
  .stats {
    margin-top: -60px; position: relative; z-index: 5;
    max-width: 1000px; margin-left: auto; margin-right: auto; padding: 0 6%;
    display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 20px;
  }
  .stat {
    background: var(--white); border-radius: 18px; padding: 26px 18px; text-align: center; box-shadow: var(--shadow);
    border-bottom: 4px solid var(--gold); transition: transform .4s;
  }
  .stat:hover { transform: translateY(-6px); }
  .stat .num { font-size: 2.2rem; font-weight: 800; color: var(--navy); }
  .stat .lbl { color: var(--muted); font-size: .9rem; }

  /* ---------- SECTIONS ---------- */
  section { padding: 90px 6%; }
  .alt { background: var(--soft); }
  .title { text-align: center; margin-bottom: 52px; }
  .title small { color: var(--saffron); font-weight: 700; letter-spacing: 3px; text-transform: uppercase; font-size: .8rem; }
  .title h2 { color: var(--navy); font-size: clamp(1.8rem, 3.5vw, 2.5rem); margin-top: 8px; }
  .title .line { width: 70px; height: 4px; margin: 14px auto 0; border-radius: 4px; background: linear-gradient(90deg, var(--gold), var(--saffron)); }

  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 50px; align-items: center; max-width: 1100px; margin: auto; }
  .about-card {
    background: linear-gradient(135deg, var(--navy), var(--navy2)); color: #dbe3f5; border-radius: 26px; padding: 44px;
    box-shadow: var(--shadow); position: relative; overflow: hidden;
  }
  .about-card::after { content: "🏫"; position: absolute; right: -10px; bottom: -20px; font-size: 9rem; opacity: .08; }
  .about-card h3 { color: var(--gold); font-size: 1.4rem; margin-bottom: 14px; }
  .about-text h3 { color: var(--navy); font-size: 1.5rem; margin-bottom: 12px; }
  .about-text p { color: var(--muted); margin-bottom: 14px; }
  .check { list-style: none; margin-top: 16px; }
  .check li { padding: 6px 0 6px 28px; position: relative; color: var(--text); }
  .check li::before { content: "✔"; position: absolute; left: 0; color: var(--saffron); font-weight: 700; }

  .cards { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 24px; max-width: 1200px; margin: auto; }
  .card {
    background: var(--white); border-radius: 20px; padding: 34px 26px; text-align: center;
    box-shadow: 0 8px 26px rgba(10,26,58,.07); border: 1px solid #e6ebf5;
    transition: transform .45s, box-shadow .45s; position: relative; overflow: hidden;
  }
  .card::before {
    content: ""; position: absolute; top: 0; left: 0; right: 0; height: 4px;
    background: linear-gradient(90deg, var(--gold), var(--saffron)); transform: scaleX(0); transform-origin: left; transition: transform .5s;
  }
  .card:hover { transform: translateY(-10px); box-shadow: var(--shadow); }
  .card:hover::before { transform: scaleX(1); }
  .card .ic {
    width: 74px; height: 74px; margin: 0 auto 18px; border-radius: 22px; font-size: 2rem;
    background: linear-gradient(135deg, #fff3d6, #ffe0b0); display: flex; align-items: center; justify-content: center;
    transition: transform .5s;
  }
  .card:hover .ic { transform: rotate(-8deg) scale(1.1); }
  .card h3 { color: var(--navy); margin-bottom: 8px; font-size: 1.15rem; }
  .card p { color: var(--muted); font-size: .93rem; }

  .notice-board { max-width: 900px; margin: auto; display: grid; gap: 16px; }
  .notice {
    display: flex; gap: 18px; align-items: flex-start; background: var(--white); border-radius: 16px; padding: 20px 22px;
    box-shadow: 0 6px 20px rgba(10,26,58,.06); border-left: 5px solid var(--saffron); transition: transform .3s;
  }
  .notice:hover { transform: translateX(8px); }
  .notice .date { min-width: 64px; background: var(--navy); color: var(--gold); border-radius: 12px; text-align: center; padding: 8px 6px; font-weight: 700; }
  .notice .date b { display: block; font-size: 1.4rem; color: var(--white); }
  .notice .date span { font-size: .75rem; text-transform: uppercase; }
  .notice h4 { color: var(--navy); margin-bottom: 4px; }
  .notice p { color: var(--muted); font-size: .92rem; }

  .admission {
    background: linear-gradient(120deg, var(--saffron), var(--gold)); color: var(--navy); text-align: center;
    border-radius: 28px; padding: 60px 30px; max-width: 1100px; margin: auto; position: relative; overflow: hidden;
  }
  .admission::after { content: ""; position: absolute; width: 260px; height: 260px; border-radius: 50%; background: rgba(255,255,255,.25); top: -90px; right: -60px; animation: float 9s ease-in-out infinite; }
  .admission h2 { font-size: clamp(1.7rem, 3.5vw, 2.4rem); margin-bottom: 12px; position: relative; z-index: 1; }
  .admission p { max-width: 620px; margin: 0 auto 26px; position: relative; z-index: 1; font-weight: 500; }
  .admission .btn.dark { background: var(--navy); color: var(--gold); position: relative; z-index: 1; }

  .contact-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 22px; max-width: 1100px; margin: auto; }
  .contact-item {
    background: var(--white); border-radius: 18px; padding: 28px 24px; box-shadow: 0 8px 24px rgba(10,26,58,.07);
    display: flex; gap: 16px; align-items: flex-start; transition: transform .3s;
  }
  .contact-item:hover { transform: translateY(-5px); }
  .contact-item .ci { font-size: 1.6rem; background: #fff3d6; width: 52px; height: 52px; border-radius: 14px; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
  .contact-item h4 { color: var(--navy); margin-bottom: 4px; }
  .contact-item p, .contact-item a { color: var(--muted); font-size: .95rem; text-decoration: none; }
  .contact-item a:hover { color: var(--saffron); }

  .map-box { max-width: 1100px; margin: 40px auto 0; border-radius: 22px; overflow: hidden; box-shadow: var(--shadow); }
  .map-box iframe { width: 100%; height: 340px; border: 0; display: block; }

  .school-photo { border-radius: 22px; overflow: hidden; box-shadow: var(--shadow); margin: 18px 0 6px; border: 4px solid #fff; }
  .school-photo img { width: 100%; display: block; transition: transform .8s ease; }
  .school-photo:hover img { transform: scale(1.06); }

  .tour-card { display: grid; grid-template-columns: 1.2fr 1fr; gap: 40px; align-items: center; max-width: 1100px; margin: auto; background: #fff; border-radius: 26px; padding: 26px; box-shadow: var(--shadow); }
  .tour-photo { position: relative; border-radius: 20px; overflow: hidden; min-height: 300px; background: linear-gradient(135deg, var(--navy2), var(--navy)); }
  .tour-photo img { width: 100%; height: 100%; object-fit: cover; display: block; transition: transform .8s ease; }
  .tour-photo:hover img { transform: scale(1.06); }
  .tour-photo.empty { display: flex; align-items: center; justify-content: center; }
  .tour-empty { display: none; flex-direction: column; align-items: center; gap: 10px; color: var(--gold2); font-size: 2.5rem; text-align: center; padding: 20px; }
  .tour-photo.empty .tour-empty { display: flex; }
  .tour-empty span { font-size: .95rem; color: #d6def2; }
  .tour-text h3 { color: var(--navy); font-size: 1.5rem; margin-bottom: 12px; }
  .tour-text p { color: var(--muted); margin-bottom: 22px; }
  .tour-btn { color: var(--navy); }
  @media (max-width: 860px) { .tour-card { grid-template-columns: 1fr; } }

  /* ---------- AIR SHOW GALLERY ---------- */
  .tour-intro { text-align: center; max-width: 720px; margin: -20px auto 36px; color: var(--muted); }
  .gallery { display: grid; grid-template-columns: repeat(auto-fill, minmax(230px, 1fr)); gap: 18px; max-width: 1200px; margin: auto; }
  .gallery .g-item { position: relative; border-radius: 18px; overflow: hidden; aspect-ratio: 4/3; cursor: pointer; box-shadow: 0 8px 24px rgba(10,26,58,.12); background: var(--navy2); opacity: 0; transform: translateY(30px); transition: opacity .6s ease, transform .6s ease; }
  .gallery .g-item.show { opacity: 1; transform: none; }
  .gallery .g-item img { width: 100%; height: 100%; object-fit: cover; display: block; transition: transform .6s ease; }
  .gallery .g-item:hover img { transform: scale(1.1); }
  .gallery .g-item::after { content: "🔍"; position: absolute; inset: 0; display: flex; align-items: center; justify-content: center; font-size: 2rem; background: rgba(10,26,58,.45); opacity: 0; transition: opacity .3s; }
  .gallery .g-item:hover::after { opacity: 1; }
  .lightbox { position: fixed; inset: 0; z-index: 300; background: rgba(5,10,25,.94); display: none; align-items: center; justify-content: center; flex-direction: column; padding: 20px; }
  .lightbox.open { display: flex; animation: fadeIn .3s ease; }
  .lightbox img { max-width: 92vw; max-height: 80vh; border-radius: 14px; box-shadow: 0 20px 60px rgba(0,0,0,.6); animation: zoomIn .4s ease; }
  .lb-btn { position: absolute; background: rgba(255,255,255,.12); border: 1px solid rgba(255,255,255,.3); color: #fff; width: 48px; height: 48px; border-radius: 50%; font-size: 1.6rem; cursor: pointer; transition: background .3s; }
  .lb-btn:hover { background: var(--gold); color: var(--navy); }
  .lb-close { top: 18px; right: 18px; }
  .lb-prev { left: 18px; top: 50%; transform: translateY(-50%); }
  .lb-next { right: 18px; top: 50%; transform: translateY(-50%); }
  .lb-cap { color: var(--gold2); margin-top: 16px; font-weight: 600; }
  @keyframes zoomIn { from { transform: scale(.85); opacity: 0; } to { transform: none; opacity: 1; } }

  /* ---------- FOOTER ---------- */
  footer { background: var(--navy); color: #b9c4de; padding: 60px 6% 24px; }
  .foot-grid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 40px; max-width: 1100px; margin: auto; }
  footer h4 { color: var(--gold); margin-bottom: 14px; }
  footer ul { list-style: none; }
  footer ul li { margin-bottom: 8px; }
  footer ul a { color: #b9c4de; text-decoration: none; transition: color .3s; }
  footer ul a:hover { color: var(--gold); }
  .copy { text-align: center; margin-top: 40px; padding-top: 20px; border-top: 1px solid rgba(255,255,255,.1); font-size: .85rem; }

  /* ---------- FLOATING ---------- */
  .to-top {
    position: fixed; right: 22px; bottom: 22px; width: 50px; height: 50px; border-radius: 50%; border: none;
    background: linear-gradient(135deg, var(--gold), var(--saffron)); color: var(--navy); font-size: 1.3rem; font-weight: 700;
    cursor: pointer; box-shadow: 0 10px 25px rgba(0,0,0,.25); opacity: 0; transform: translateY(20px); transition: all .4s; z-index: 150;
  }
  .to-top.show { opacity: 1; transform: none; }

  /* ---------- REVEAL ---------- */
  .reveal { opacity: 0; transform: translateY(40px); transition: opacity .9s ease, transform .9s ease; }
  .reveal.show { opacity: 1; transform: none; }
  .reveal-left { opacity: 0; transform: translateX(-50px); transition: all .9s ease; }
  .reveal-left.show { opacity: 1; transform: none; }
  @keyframes fadeUp { from { opacity: 0; transform: translateY(30px);} to { opacity: 1; transform: none;} }

  /* ---------- RESPONSIVE ---------- */
  @media (max-width: 960px) {
    .menu-toggle { display: block; }
    .menu {
      position: fixed; top: 0; right: -100%; width: 270px; height: 100vh; background: var(--white);
      flex-direction: column; padding: 90px 24px; box-shadow: -10px 0 30px rgba(0,0,0,.15); transition: right .45s ease;
    }
    .menu.open { right: 0; }
    .menu a { font-size: 1rem; }
    .about-grid, .foot-grid { grid-template-columns: 1fr; }
  }
  @media (max-width: 560px) {
    .brand-text small { display: none; }
    .status-bar .right { display: none; }
    .hero { min-height: 80vh; }
  }
  @media (prefers-reduced-motion: reduce) { *, *::before, *::after { animation: none !important; transition: none !important; } .reveal, .reveal-left { opacity: 1; transform: none; } }
</style>
</head>
<body>

<!-- STATUS BAR -->
<div class="status-bar">
  <div class="left">
    <span class="item"><span class="live-dot"></span> <span id="clock"></span></span>
    <span class="item">📍 Udaipur, Varanasi</span>
  </div>
  <div class="ticker-wrap"><div class="ticker">📢 Admission 2027-28 ke liye abhi apply karein &nbsp;•&nbsp; Vidyalaya ka samay: subah 10:00 se shaam 4:00 tak &nbsp;•&nbsp; Sabhi ko swagat hai!</div></div>
  <div class="right">
    <span class="item">📞 <a href="tel:+916388681913">Call Karein</a></span>
  </div>
</div>

<!-- NAVBAR -->
<nav id="navbar">
  <a href="#home" class="brand">
    <div class="crest"><div class="crest-inner">🎓</div></div>
    <div class="brand-text">
      <strong>Jai Prakash Narayan</strong>
      <small>SARVODAYA VIDYALAYA, UDAIPUR</small>
    </div>
  </a>
  <button class="menu-toggle" id="menuToggle" aria-label="Menu">☰</button>
  <ul class="menu" id="menu">
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#academics">Academics</a></li>
    <li><a href="#facilities">Facilities</a></li>
    <li><a href="#library">Library</a></li>
    <li><a href="#computerlab">Computer Lab</a></li>
    <li><a href="#tour">Student Tour</a></li>
    <li><a href="#notices">Notices</a></li>
    <li><a href="#admission">Admission</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<header class="hero" id="home">
  <div class="blob b1"></div>
  <div class="blob b2"></div>
  <div class="hero-inner">
    <span class="eyebrow">✨ Gyan • Sanskar • Seva</span>
    <h1>Swagat hai <span class="gold">Jai Prakash Narayan Sarvodaya Vidyalaya</span></h1>
    <p class="sub">Udaipur, Varanasi me ek aisi shiksha jo bachchon ke gyan ke saath unke charitra aur sanskar bhi nikhaare. Aapka bachcha yahan ek ujjwal bhavishya ki taraf badhta hai.</p>
    <div class="btns">
      <a href="#admission" class="btn gold">Admission Lein</a>
      <a href="#about" class="btn outline">Vidyalaya Dekhein</a>
    </div>
  </div>
  <div class="scroll-hint">↓ Neeche scroll karein</div>
</header>

<!-- STATS -->
<div class="stats">
  <div class="stat reveal"><div class="num" data-count="300">0</div><div class="lbl">Students</div></div>
  <div class="stat reveal"><div class="num" data-count="17">0</div><div class="lbl">Teachers</div></div>
  <div class="stat reveal"><div class="num" data-count="25">0</div><div class="lbl">Saal ka Anubhav</div></div>
  <div class="stat reveal"><div class="num" data-count="98">0</div><div class="lbl">% Pariksha Parinaam</div></div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-card reveal-left">
      <h3>Hamara Lakshya</h3>
      <p>"Sarvodaya" ka arth hai sabka uday. Hum har bachche ko padhai, anushasan aur sewa bhav ke saath aage badhne ke liye taiyaar karte hain.</p>
      <p style="margin-top:14px">Hamare shikshak har bachche par vyaktigat dhyan dete hain, taaki koi bhi peeche na rahe.</p>
    </div>
    <div class="about-text reveal">
      <div class="title" style="text-align:left;margin-bottom:20px"><small>About Us</small><h2>Vidyalaya ke bare me</h2><div class="line" style="margin-left:0"></div></div>
      <p>Jai Prakash Narayan Sarvodaya Vidyalaya Udaipur, Varanasi ka ek bharosemand vidyalaya hai jahan shiksha ke saath sanskaar par bhi bharpoor zor diya jaata hai.</p>
      <div class="school-photo"><img src="students.jpg" alt="Vidyalaya ke chhatra"></div>
      <ul class="check">
        <li>Anubhavi aur samarpit shikshak</li>
        <li>Smart classes aur digital padhai</li>
        <li>Surakshit aur anushasit vaataavaran</li>
        <li>Khel, sangeet aur kala ki gatividhiyan</li>
      </ul>
    </div>
  </div>
</section>

<!-- ACADEMICS -->
<section id="academics" class="alt">
  <div class="title reveal"><small>Academics</small><h2>Padhai ke Star</h2><div class="line"></div></div>
  <div class="cards">
    <div class="card reveal"><div class="ic">📘</div><h3>Primary (1 - 5)</h3><p>Buniyaadi shiksha, khel-khel me seekhna aur nayi cheezon ke prati jigyasa jagana.</p></div>
    <div class="card reveal"><div class="ic">📗</div><h3>Middle (6 - 8)</h3><p>Vishay ki gehri samajh, project based padhai aur vyaktitva ka vikas.</p></div>
    <div class="card reveal"><div class="ic">📕</div><h3>Secondary (9 - 10)</h3><p>Board pariksha ki taiyari, regular tests aur lagatar mentorship.</p></div>
  </div>
</section>

<!-- FACILITIES -->
<section id="facilities">
  <div class="title reveal"><small>Facilities</small><h2>Hamari Suvidhayein</h2><div class="line"></div></div>
  <div class="cards">
    <div class="card reveal"><div class="ic">🧪</div><h3>Science Lab</h3><p>Prayogshala me hath se prayog karke vigyan ko samjhna.</p></div>
    <div class="card reveal"><div class="ic">🏀</div><h3>Khel Maidan</h3><p>Cricket, kho-kho, kabaddi aur anya khelon ki suvidha.</p></div>
    <div class="card reveal"><div class="ic">🎨</div><h3>Kala aur Sangeet</h3><p>Chitrakala, sangeet aur natak ke liye alag manch.</p></div>
    <div class="card reveal"><div class="ic">🚌</div><h3>Transport</h3><p>Surakshit bus seva jo aapke bachche ko ghar ke paas tak laaye.</p></div>
  </div>
</section>

<!-- LIBRARY -->
<section id="library" class="alt">
  <div class="title reveal"><small>Library</small><h2>Pustakalaya</h2><div class="line"></div></div>
  <div class="cards">
    <div class="card reveal"><div class="ic">📚</div><h3>Vishal Sangrah</h3><p>Paathyakram ki kitaabon ke saath kahani, vigyan aur itihaas ki kitaabein.</p></div>
    <div class="card reveal"><div class="ic">🔍</div><h3>Shaant Padhai Kaksha</h3><p>Shaant vaataavaran me padhne aur research karne ki vyavastha.</p></div>
    <div class="card reveal"><div class="ic">📰</div><h3>Patrika aur Samachar</h3><p>Roz ke akhbaar aur patrikaon se duniya se judne ka mauka.</p></div>
  </div>
</section>

<!-- COMPUTER LAB -->
<section id="computerlab">
  <div class="title reveal"><small>Computer Lab</small><h2>Computer Prayogshala</h2><div class="line"></div></div>
  <div class="cards">
    <div class="card reveal"><div class="ic">💻</div><h3>Modern Computers</h3><p>Har chhatra ke liye computer, digital padhai ke liye poori taiyari.</p></div>
    <div class="card reveal"><div class="ic">🌐</div><h3>Internet Suvidha</h3><p>Tej internet ke saath research, projects aur online classes.</p></div>
    <div class="card reveal"><div class="ic">🤖</div><h3>Coding aur Basic AI</h3><p>Bachchon ko coding aur technology ki buniyaadi samajh.</p></div>
  </div>
</section>

<!-- NOTICES -->
<section id="notices" class="alt">
  <div class="title reveal"><small>Notices</small><h2>Taaza Soochna</h2><div class="line"></div></div>
  <div class="notice-board">
    <div class="notice reveal"><div class="date"><b>01</b><span>Dec</span></div><div><h4>Vaarshik Utsav</h4><p>Vidyalaya ka vaarshik utsav aur khel pratiyogita ka aayojan.</p></div></div>
    <div class="notice reveal"><div class="date"><b>15</b><span>Dec</span></div><div><h4>Parent-Teacher Meeting</h4><p>Abhibhavakon ke saath bachchon ki pragati par charcha.</p></div></div>
    <div class="notice reveal"><div class="date"><b>05</b><span>Jan</span></div><div><h4>Admission Open</h4><p>Naye satra ke liye admission prakriya shuru. Jaldi apply karein.</p></div></div>
  </div>
</section>

<!-- ADMISSION -->
<section id="admission">
  <div class="admission reveal">
    <h2>Apne bachche ka bhavishya aaj hi shuru karein</h2>
    <p>Admission ke liye vidyalaya office me sampark karein ya call karke jaankari lein.</p>
    <a href="#contact" class="btn dark">Ab Sampark Karein</a>
  </div>
</section>

<!-- STUDENT TOUR -->
<section id="tour" class="alt">
  <div class="title reveal"><small>Student Tour</small><h2>Air Show in Varanasi</h2><div class="line"></div></div>
  <div class="tour-intro reveal">
    <p>Vidyalaya ke chhatron ne Air Show in Varanasi me bhaag liya. Kisi bhi photo par click karke bade size me dekhein.</p>
  </div>
  <div class="gallery" id="gallery"></div>
  <div class="lightbox" id="lightbox">
    <button class="lb-btn lb-close" id="lbClose" aria-label="Band karein">✕</button>
    <button class="lb-btn lb-prev" id="lbPrev" aria-label="Pichli photo">‹</button>
    <img id="lbImg" alt="Air Show in Varanasi">
    <button class="lb-btn lb-next" id="lbNext" aria-label="Agli photo">›</button>
    <div class="lb-cap">Air Show in Varanasi</div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="alt">
  <div class="title reveal"><small>Contact</small><h2>Sampark Karein</h2><div class="line"></div></div>
  <div class="contact-grid">
    <div class="contact-item reveal"><div class="ci">📍</div><div><h4>Pata</h4><p>Vanarsi, Udaipur<br>Varanasi, Uttar Pradesh<br>Pin: 221101</p></div></div>
    <div class="contact-item reveal"><div class="ci">📞</div><div><h4>Phone</h4><a href="tel:+916388681913">+91 6388681913</a></div></div>
    <div class="contact-item reveal"><div class="ci">✉️</div><div><h4>Email</h4><a href="mailto:Atschandapur@gmail.com">Atschandapur@gmail.com</a></div></div>
    <div class="contact-item reveal"><div class="ci">🕘</div><div><h4>Samay</h4><p>Somvar - Shanivar<br>10:00 AM - 4:00 PM</p></div></div>
  </div>
  <div class="map-box reveal">
    <iframe loading="lazy" title="Vidyalaya ki location" src="https://www.google.com/maps?q=Vanarsi+Udaipur+Varanasi+221101&output=embed"></iframe>
  </div>
</section>

<footer>
  <div class="foot-grid">
    <div>
      <h4>Jai Prakash Narayan Sarvodaya Vidyalaya</h4>
      <p>Udaipur, Varanasi. Gyan, sanskar aur seva ke saath bachchon ke ujjwal bhavishya ka nirmaan.</p>
    </div>
    <div>
      <h4>Quick Links</h4>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#academics">Academics</a></li>
        <li><a href="#library">Library</a></li>
        <li><a href="#computerlab">Computer Lab</a></li>
      </ul>
    </div>
    <div>
      <h4>Madad</h4>
      <ul>
        <li><a href="#admission">Admission</a></li>
        <li><a href="#notices">Notices</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
  </div>
  <div class="copy">© <span id="year"></span> Jai Prakash Narayan Sarvodaya Vidyalaya. Sab adhikar surakshit.</div>
</footer>

<button class="to-top" id="toTop" aria-label="Upar jayein">↑</button>

<script>
  // Live clock in status bar
  function tick() {
    const d = new Date();
    document.getElementById("clock").textContent = d.toLocaleString("hi-IN", { weekday: "short", day: "2-digit", month: "short", hour: "2-digit", minute: "2-digit" });
  }
  tick(); setInterval(tick, 30000);

  // Sticky navbar shrink + back to top + active link
  const nav = document.getElementById("navbar");
  const toTop = document.getElementById("toTop");
  const links = document.querySelectorAll(".menu a");
  window.addEventListener("scroll", () => {
    nav.classList.toggle("scrolled", window.scrollY > 60);
    toTop.classList.toggle("show", window.scrollY > 400);
    let current = "home";
    document.querySelectorAll("section[id], header[id]").forEach(s => {
      if (window.scrollY >= s.offsetTop - 150) current = s.id;
    });
    links.forEach(a => a.classList.toggle("active", a.getAttribute("href") === "#" + current));
  });
  toTop.addEventListener("click", () => window.scrollTo({ top: 0, behavior: "smooth" }));

  // Mobile menu
  const menu = document.getElementById("menu");
  document.getElementById("menuToggle").addEventListener("click", () => menu.classList.toggle("open"));
  links.forEach(a => a.addEventListener("click", () => menu.classList.remove("open")));

  // Scroll reveal + counters
  function countUp(el) {
    const target = +el.dataset.count;
    const duration = 1600;
    const start = performance.now();
    function step(now) {
      const p = Math.min((now - start) / duration, 1);
      el.textContent = Math.floor(target * (1 - Math.pow(1 - p, 3))) + (el.dataset.count == 98 ? "%" : "+");
      if (p < 1) requestAnimationFrame(step);
    }
    requestAnimationFrame(step);
  }
  const io = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add("show");
        e.target.querySelectorAll("[data-count]").forEach(countUp);
        io.unobserve(e.target);
      }
    });
  }, { threshold: 0.2 });
  document.querySelectorAll(".reveal, .reveal-left").forEach(el => io.observe(el));

  // Air Show gallery: photos add karne ke liye yahan file names bhi badal sakte hain
  const tourPhotos = ["tour1.jpg", "tour2.jpg", "tour3.jpg", "tour4.jpg", "tour5.jpg", "tour6.jpg", "tour7.jpg", "tour8.jpg", "tour9.jpg", "tour10.jpg", "tour11.jpg", "tour12.jpg", "tour13.webp", "tour14.jpg"];
  const gallery = document.getElementById("gallery");
  const lightbox = document.getElementById("lightbox");
  const lbImg = document.getElementById("lbImg");
  let lbIndex = 0;
  const loaded = [];
  tourPhotos.forEach(src => {
    const img = new Image();
    img.onload = () => {
      loaded.push(src);
      const item = document.createElement("div");
      item.className = "g-item";
      const im = document.createElement("img");
      im.src = src; im.alt = "Air Show in Varanasi";
      item.appendChild(im);
      item.addEventListener("click", () => openLight(loaded.indexOf(src)));
      gallery.appendChild(item);
      requestAnimationFrame(() => item.classList.add("show"));
    };
    img.src = src;
  });
  function openLight(i) {
    lbIndex = i;
    lbImg.src = loaded[lbIndex];
    lightbox.classList.add("open");
    document.body.style.overflow = "hidden";
  }
  function closeLight() { lightbox.classList.remove("open"); document.body.style.overflow = ""; }
  function shiftLight(d) {
    lbIndex = (lbIndex + d + loaded.length) % loaded.length;
    lbImg.src = loaded[lbIndex];
  }
  document.getElementById("lbClose").addEventListener("click", closeLight);
  document.getElementById("lbPrev").addEventListener("click", () => shiftLight(-1));
  document.getElementById("lbNext").addEventListener("click", () => shiftLight(1));
  lightbox.addEventListener("click", e => { if (e.target === lightbox) closeLight(); });
  document.addEventListener("keydown", e => {
    if (!lightbox.classList.contains("open")) return;
    if (e.key === "Escape") closeLight();
    if (e.key === "ArrowLeft") shiftLight(-1);
    if (e.key === "ArrowRight") shiftLight(1);
  });

  document.getElementById("year").textContent = new Date().getFullYear();
</script>
</body>
</html>
