<!--
  KirkiLan — single-file HTML mockup (desktop-first)
  Notes:
  - Minimalist black/white/grunge style
  - Replace placeholder images with your product photos
  - Save this file as KirkiLan_homepage.html and open in a browser
--><!doctype html>

<html lang="ru">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>KirkiLan — Home</title>
  <style>
    /* Basic reset */
    *{box-sizing:border-box;margin:0;padding:0}
    html,body{height:100%}
    body{
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: #f2f2f2;
      color:#0a0a0a;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.2;
    }/* subtle grunge paper texture (SVG data) */
body::before{
  content:"";
  position:fixed;inset:0;z-index:0;pointer-events:none;
  background-image:linear-gradient(rgba(0,0,0,0.02), rgba(0,0,0,0.02)),
    repeating-linear-gradient(45deg, rgba(0,0,0,0.01) 0 1px, transparent 1px 6px);
  opacity:0.6;
}

.container{max-width:1100px;margin:40px auto;padding:24px;position:relative;z-index:1}

/* Header */
header{display:flex;align-items:center;justify-content:space-between;margin-bottom:28px}
.brand{font-size:48px;letter-spacing:1px;font-weight:700}
nav{display:flex;gap:28px;align-items:center}
nav a{color:#111;text-decoration:none;font-weight:600}

.icons{display:flex;gap:12px;align-items:center}
.icon{width:26px;height:26px;border:2px solid #111;border-radius:4px;display:inline-flex;align-items:center;justify-content:center;font-size:12px}

/* Hero */
.hero{position:relative;margin-bottom:28px}
.hero .photo{
  width:100%;height:540px;background-size:cover;background-position:center;display:block;position:relative;filter:grayscale(100%);
  border:6px solid rgba(0,0,0,0.04);
}
/* SURVIVE style overlay */
.hero .overlay{
  position:absolute;left:0;right:0;top:50%;transform:translateY(-50%);
  text-align:center;pointer-events:none
}
.hero .overlay h1{
  font-size:124px;margin:0;line-height:0.9;color:rgba(255,255,255,0.98);font-weight:900;
  letter-spacing:2px;text-transform:uppercase;text-shadow:0 2px 0 rgba(0,0,0,0.35);
  mix-blend-mode:screen;padding:0 14px
}
.hero .overlay .sub{display:block;margin-top:12px;font-size:14px;color:rgba(255,255,255,0.9);font-weight:700}

/* Collections grid */
.collections{display:grid;grid-template-columns:1fr 1fr;gap:26px}
.tile{position:relative;overflow:hidden}
.tile .img{height:420px;background-size:cover;background-position:center;filter:grayscale(100%);display:block}
.tile .label{
  position:absolute;left:18px;top:18px;background:rgba(0,0,0,0.6);color:#fff;padding:10px 18px;font-weight:800;text-transform:uppercase;font-size:40px;letter-spacing:1px;
  box-shadow:0 6px 18px rgba(0,0,0,0.2);
}

/* Make other headings look like SURVIVE but smaller */
.section-title{
  font-size:48px;font-weight:800;text-transform:uppercase;color:#111;margin:28px 0 12px;padding-left:4px
}

footer{margin-top:36px;border-top:1px solid rgba(0,0,0,0.06);padding-top:18px;display:flex;justify-content:space-between;align-items:center}
footer .meta{color:#666;font-size:13px}

/* Desktop-first, but some responsiveness */
@media (max-width:1000px){
  .container{padding:16px}
  .hero .overlay h1{font-size:84px}
  .section-title{font-size:36px}
  .tile .img{height:320px}
}
@media (max-width:700px){
  .brand{font-size:32px}
  header{flex-direction:column;align-items:flex-start;gap:10px}
  .collections{grid-template-columns:1fr}
  .hero .photo{height:360px}
  .hero .overlay h1{font-size:54px}
  .tile .img{height:260px}
}

/* tiny interaction */
.tile:hover .img{transform:scale(1.03);transition:transform 500ms ease}
.tile .img{transition:transform 500ms ease}

  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">KirkiLan</div>
      <nav>
        <a href="#survive">Survive</a>
        <a href="#think">Think About It</a>
        <a href="#togdale">Togdale</a>
        <a href="#collections">Коллекции</a>
      </nav>
      <div class="icons">
        <div class="icon">🔍</div>
        <div class="icon">🛒</div>
      </div>
    </header><!-- HERO: replace background-image URL with your own photo -->
<section class="hero" id="survive">
  <div class="photo" style="background-image:url('https://images.unsplash.com/photo-1520975919318-1c0073d53f62?q=80&w=1600&auto=format&fit=crop&sat=-100');"></div>
  <div class="overlay">
    <h1>SURVIVE</h1>
    <span class="sub">COLLECTION 2025</span>
  </div>
</section>

<!-- Collections grid -->
<div class="collections" id="collections">
  <div class="tile" id="think">
    <div class="img" style="background-image:url('https://images.unsplash.com/photo-1541099649105-f69ad21f3246?q=80&w=1200&auto=format&fit=crop&sat=-100');"></div>
    <div class="label">THINK ABOUT IT</div>
  </div>

  <div class="tile" id="togdale">
    <div class="img" style="background-image:url('https://images.unsplash.com/photo-1524504388940-b1c1722653e1?q=80&w=1200&auto=format&fit=crop&sat=-100');"></div>
    <div class="label">TOGDALE</div>
  </div>
</div>

<footer>
  <div class="meta">© 2025 KirkiLan. Minimal streetwear crafted to survive.</div>
  <div class="meta">Instagram · TikTok</div>
</footer>

  </div>  <!-- Optional: small script to make section links smooth -->  <script>
    document.querySelectorAll('nav a').forEach(a=>{
      a.addEventListener('click', e=>{
        e.preventDefault();
        const id = a.getAttribute('href').slice(1);
        const el = document.getElementById(id);
        if(el) el.scrollIntoView({behavior:'smooth',block:'start'});
      })
    })
  </script></body>
</html>
