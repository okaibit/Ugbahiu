<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Built in Nigeria — the directory</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton&family=IBM+Plex+Mono:wght@400;500;600;700&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --yellow:#FFC629;
    --yellow-dim:#E8B21C;
    --ink:#14151A;
    --ink-soft:#2B2D34;
    --paper:#FAF9F5;
    --card:#FFFFFF;
    --line:#E7E4DA;
    --green:#0B6E4F;
    --rust:#D64526;
    --indigo:#24487A;
    --muted:#6B6A63;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:'IBM Plex Sans', sans-serif;
    -webkit-font-smoothing:antialiased;
  }

  .display{font-family:'Anton', sans-serif; letter-spacing:0.01em; text-transform:uppercase;}
  .mono{font-family:'IBM Plex Mono', monospace;}

  a{color:inherit;}

  /* ---------- stripe divider (signature element) ---------- */
  .stripe{
    height:14px;
    background:repeating-linear-gradient(
      -45deg,
      var(--ink) 0px, var(--ink) 16px,
      var(--yellow) 16px, var(--yellow) 32px
    );
  }
  .stripe.thin{height:8px;}

  /* ---------- nav ---------- */
  nav{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:22px 6vw;
    max-width:1280px;
    margin:0 auto;
  }
  .wordmark{
    display:flex;
    align-items:baseline;
    gap:8px;
    font-family:'Anton', sans-serif;
    font-size:20px;
    letter-spacing:0.02em;
  }
  .wordmark .tag{
    background:var(--ink);
    color:var(--yellow);
    font-family:'IBM Plex Mono', monospace;
    font-size:10px;
    font-weight:600;
    padding:2px 6px;
    border-radius:3px;
    letter-spacing:0.06em;
  }
  .nav-links{
    display:flex;
    align-items:center;
    gap:32px;
    font-size:14px;
    font-weight:500;
  }
  .nav-links a{
    text-decoration:none;
    color:var(--ink-soft);
    padding-bottom:3px;
    border-bottom:2px solid transparent;
    transition:border-color .15s ease;
  }
  .nav-links a:hover{border-color:var(--yellow);}
  .nav-cta{
    background:var(--ink);
    color:var(--paper) !important;
    padding:9px 18px;
    border-radius:6px;
    border-bottom:none !important;
    font-weight:600;
  }
  .nav-cta:hover{background:var(--ink-soft);}
  @media (max-width:760px){ .nav-links{display:none;} }

  /* ---------- hero ---------- */
  .hero{
    max-width:1280px;
    margin:0 auto;
    padding:64px 6vw 56px;
  }
  .eyebrow{
    display:inline-flex;
    align-items:center;
    gap:8px;
    font-family:'IBM Plex Mono', monospace;
    font-size:12px;
    font-weight:600;
    letter-spacing:0.08em;
    text-transform:uppercase;
    color:var(--muted);
    margin-bottom:18px;
  }
  .eyebrow .dot{
    width:7px;height:7px;border-radius:50%;
    background:var(--green);
    box-shadow:0 0 0 3px rgba(11,110,79,0.15);
    animation:pulse 2s infinite;
  }
  @keyframes pulse{
    0%,100%{opacity:1;}
    50%{opacity:0.35;}
  }
  @media (prefers-reduced-motion:reduce){ .eyebrow .dot{animation:none;} }

  h1.headline{
    font-size:clamp(52px, 9vw, 112px);
    line-height:0.92;
    margin:0 0 26px;
  }
  h1.headline .highlight{
    background:var(--yellow);
    padding:0 10px;
    box-decoration-break:clone;
    -webkit-box-decoration-break:clone;
  }

  .subhead{
    max-width:560px;
    font-size:18px;
    line-height:1.55;
    color:var(--ink-soft);
    margin:0 0 34px;
  }
  .subhead strong{color:var(--ink);}

  .hero-actions{
    display:flex;
    gap:14px;
    flex-wrap:wrap;
    margin-bottom:56px;
  }
  .btn{
    font-family:'IBM Plex Sans', sans-serif;
    font-size:15px;
    font-weight:600;
    padding:14px 24px;
    border-radius:7px;
    border:2px solid var(--ink);
    cursor:pointer;
    text-decoration:none;
    display:inline-flex;
    align-items:center;
    gap:8px;
    transition:transform .12s ease, box-shadow .12s ease;
  }
  .btn:hover{ transform:translateY(-2px); }
  .btn-primary{ background:var(--ink); color:var(--yellow); }
  .btn-primary:hover{ box-shadow:4px 4px 0 var(--yellow); }
  .btn-secondary{ background:transparent; color:var(--ink); }
  .btn-secondary:hover{ box-shadow:4px 4px 0 var(--ink); }

  /* ---------- ticker ---------- */
  .ticker{
    background:var(--ink);
    color:var(--paper);
    padding:26px 6vw;
  }
  .ticker-inner{
    max-width:1280px;
    margin:0 auto;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:24px;
  }
  .ticker-stat{ text-align:left; }
  .ticker-stat .num{
    font-family:'IBM Plex Mono', monospace;
    font-size:clamp(26px,4vw,38px);
    font-weight:700;
    color:var(--yellow);
    line-height:1;
  }
  .ticker-stat .lbl{
    font-family:'IBM Plex Mono', monospace;
    font-size:11px;
    letter-spacing:0.08em;
    text-transform:uppercase;
    color:#B9B8B2;
    margin-top:8px;
  }
  @media (max-width:640px){
    .ticker-inner{grid-template-columns:1fr; gap:18px;}
  }

  /* ---------- filters ---------- */
  .filters{
    max-width:1280px;
    margin:0 auto;
    padding:44px 6vw 20px;
    display:flex;
    gap:10px;
    flex-wrap:wrap;
  }
  .pill{
    font-family:'IBM Plex Mono', monospace;
    font-size:13px;
    font-weight:500;
    padding:9px 16px;
    border-radius:20px;
    border:1.5px solid var(--line);
    background:var(--card);
    cursor:pointer;
    transition:all .15s ease;
    color:var(--ink-soft);
  }
  .pill:hover{ border-color:var(--ink); }
  .pill.active{
    background:var(--yellow);
    border-color:var(--ink);
    color:var(--ink);
  }

  /* ---------- grid ---------- */
  .grid-section{
    max-width:1280px;
    margin:0 auto;
    padding:20px 6vw 100px;
  }
  .grid{
    display:grid;
    grid-template-columns:repeat(auto-fill, minmax(280px, 1fr));
    gap:20px;
  }
  .card{
    background:var(--card);
    border:1.5px solid var(--line);
    border-radius:12px;
    padding:22px;
    display:flex;
    flex-direction:column;
    gap:14px;
    transition:transform .15s ease, box-shadow .15s ease, border-color .15s ease;
  }
  .card:hover{
    transform:translateY(-3px);
    box-shadow:0 10px 24px rgba(20,21,26,0.08);
    border-color:var(--ink);
  }
  .card-top{
    display:flex;
    align-items:flex-start;
    justify-content:space-between;
    gap:10px;
  }
  .badge{
    width:42px;height:42px;
    border-radius:9px;
    background:var(--ink);
    color:var(--yellow);
    display:flex;align-items:center;justify-content:center;
    font-family:'Anton', sans-serif;
    font-size:18px;
    flex-shrink:0;
  }
  .card h3{
    margin:0;
    font-size:17px;
    font-weight:700;
  }
  .cat-tag{
    font-family:'IBM Plex Mono', monospace;
    font-size:10.5px;
    letter-spacing:0.05em;
    text-transform:uppercase;
    color:var(--indigo);
    background:rgba(36,72,122,0.08);
    padding:4px 8px;
    border-radius:5px;
    white-space:nowrap;
  }
  .card p.desc{
    margin:0;
    font-size:14px;
    line-height:1.5;
    color:var(--muted);
    flex-grow:1;
  }
  .card-foot{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding-top:12px;
    border-top:1px solid var(--line);
  }
  .builder{
    font-size:12px;
    color:var(--muted);
  }
  .vote-btn{
    display:flex;
    align-items:center;
    gap:7px;
    background:var(--yellow);
    border:2px solid var(--ink);
    border-radius:6px;
    padding:7px 11px;
    cursor:pointer;
    font-family:'IBM Plex Mono', monospace;
    font-weight:700;
    font-size:13px;
    color:var(--ink);
    transition:transform .1s ease;
  }
  .vote-btn:hover{ transform:scale(1.05); }
  .vote-btn:active{ transform:scale(0.96); }
  .vote-btn .arrow{ font-size:12px; }
  .vote-btn.voted{
    background:var(--green);
    border-color:var(--green);
    color:var(--paper);
  }

  .card.hidden{display:none;}

  /* ---------- footer cta ---------- */
  .footer-cta{
    background:var(--ink);
    color:var(--paper);
    padding:80px 6vw;
    text-align:center;
  }
  .footer-cta h2{
    font-family:'Anton', sans-serif;
    font-size:clamp(32px,5vw,52px);
    margin:0 0 16px;
    text-transform:uppercase;
  }
  .footer-cta h2 span{ color:var(--yellow); }
  .footer-cta p{
    color:#B9B8B2;
    max-width:480px;
    margin:0 auto 32px;
    font-size:15px;
    line-height:1.6;
  }

  footer{
    padding:28px 6vw;
    display:flex;
    justify-content:space-between;
    align-items:center;
    font-size:13px;
    color:var(--muted);
    max-width:1280px;
    margin:0 auto;
    flex-wrap:wrap;
    gap:12px;
  }
</style>
</head>
<body>

<nav>
  <div class="wordmark">
    BUILT<span style="color:var(--yellow); -webkit-text-stroke:1px var(--ink);">IN</span>NAIJA
    <span class="tag">DIRECTORY</span>
  </div>
  <div class="nav-links">
    <a href="#discover">Discover</a>
    <a href="#directory">Directory</a>
    <a href="#stats">Stats</a>
    <a href="#" class="nav-cta">Submit a product</a>
  </div>
</nav>

<div class="hero" id="discover">
  <div class="eyebrow"><span class="dot"></span> Live &nbsp;·&nbsp; verdicts added daily</div>
  <h1 class="headline">
    Built<br>
    <span class="highlight">in Nigeria</span>
  </h1>
  <p class="subhead">
    A directory of products, apps, and tools made by Nigerian builders.
    <strong>Vote for the ones you actually use</strong> — no submission gets ranked by hype alone.
  </p>
  <div class="hero-actions">
    <a href="#directory" class="btn btn-primary">Browse the directory →</a>
    <a href="#" class="btn btn-secondary">Submit your product</a>
  </div>
</div>

<div class="stripe"></div>

<div class="ticker" id="stats">
  <div class="ticker-inner">
    <div class="ticker-stat">
      <div class="num" data-target="312">0</div>
      <div class="lbl">Products listed</div>
    </div>
    <div class="ticker-stat">
      <div class="num" data-target="189">0</div>
      <div class="lbl">Builders behind them</div>
    </div>
    <div class="ticker-stat">
      <div class="num" data-target="4281">0</div>
      <div class="lbl">Votes cast this month</div>
    </div>
  </div>
</div>

<div class="filters" id="directory">
  <div class="pill active" data-filter="all">All</div>
  <div class="pill" data-filter="fintech">Fintech</div>
  <div class="pill" data-filter="logistics">Logistics</div>
  <div class="pill" data-filter="agritech">AgriTech</div>
  <div class="pill" data-filter="commerce">Commerce</div>
  <div class="pill" data-filter="edtech">EdTech</div>
  <div class="pill" data-filter="healthtech">HealthTech</div>
  <div class="pill" data-filter="devtools">Dev tools</div>
  <div class="pill" data-filter="creator">Creator tools</div>
</div>

<div class="grid-section">
  <div class="grid" id="grid"></div>
</div>

<div class="stripe thin"></div>

<div class="footer-cta">
  <h2>Made something? <span>List it.</span></h2>
  <p>Takes two minutes. Every submission goes live after a quick review — no gatekeeping, just a sanity check.</p>
  <a href="#" class="btn btn-primary" style="border-color:var(--yellow);">Submit your product →</a>
</div>

<footer>
  <span>Built in Nigeria — a directory, not a marketplace.</span>
  <span>Concept mockup</span>
</footer>

<script>
  const products = [
    { name:"PayCove", cat:"fintech", catLabel:"Fintech", desc:"Send and request money across Nigerian banks in one tap.", votes:312, builder:"@tundeb" },
    { name:"Kanla", cat:"logistics", catLabel:"Logistics", desc:"Real-time delivery tracking built for Lagos dispatch riders.", votes:218, builder:"@kanla_hq" },
    { name:"Sokoto Pay", cat:"commerce", catLabel:"Commerce", desc:"Point-of-sale and inventory for market traders.", votes:154, builder:"@aisha_dev" },
    { name:"Vitals NG", cat:"healthtech", catLabel:"HealthTech", desc:"Book verified clinic appointments in under a minute.", votes:143, builder:"@drchike" },
    { name:"FarmLedger", cat:"agritech", catLabel:"AgriTech", desc:"Digital record-keeping for smallholder farmers and cooperatives.", votes:96, builder:"@ogaifarm" },
    { name:"ClassNaija", cat:"edtech", catLabel:"EdTech", desc:"Offline-first learning app for secondary school students.", votes:88, builder:"@bisiteach" },
    { name:"CreatorDesk", cat:"creator", catLabel:"Creator tools", desc:"Invoicing and contracts built for Nigerian freelancers.", votes:77, builder:"@workwithokai" },
    { name:"StackBuilders", cat:"devtools", catLabel:"Dev tools", desc:"Deploy Nigerian-hosted infrastructure with a single command.", votes:61, builder:"@femideploys" },
  ];

  const grid = document.getElementById('grid');
  const voted = new Set();

  function render(){
    grid.innerHTML = '';
    products.forEach((p, i) => {
      const card = document.createElement('div');
      card.className = 'card';
      card.dataset.cat = p.cat;
      const initial = p.name.charAt(0);
      const isVoted = voted.has(i);
      card.innerHTML = `
        <div class="card-top">
          <div class="badge">${initial}</div>
          <div class="cat-tag">${p.catLabel}</div>
        </div>
        <h3>${p.name}</h3>
        <p class="desc">${p.desc}</p>
        <div class="card-foot">
          <span class="builder">by ${p.builder}</span>
          <button class="vote-btn ${isVoted ? 'voted' : ''}" data-idx="${i}">
            <span class="arrow">▲</span> ${p.votes + (isVoted ? 1 : 0)}
          </button>
        </div>
      `;
      grid.appendChild(card);
    });

    document.querySelectorAll('.vote-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        const idx = parseInt(btn.dataset.idx);
        if (voted.has(idx)) {
          voted.delete(idx);
        } else {
          voted.add(idx);
        }
        render();
      });
    });
  }
  render();

  // filter pills
  document.querySelectorAll('.pill').forEach(pill => {
    pill.addEventListener('click', () => {
      document.querySelectorAll('.pill').forEach(p => p.classList.remove('active'));
      pill.classList.add('active');
      const filter = pill.dataset.filter;
      document.querySelectorAll('.card').forEach(card => {
        card.classList.toggle('hidden', filter !== 'all' && card.dataset.cat !== filter);
      });
    });
  });

  // count-up ticker
  const nums = document.querySelectorAll('.ticker-stat .num');
  const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  nums.forEach(el => {
    const target = parseInt(el.dataset.target);
    if (prefersReducedMotion) { el.textContent = target.toLocaleString(); return; }
    let current = 0;
    const step = Math.ceil(target / 60);
    const interval = setInterval(() => {
      current += step;
      if (current >= target) { current = target; clearInterval(interval); }
      el.textContent = current.toLocaleString();
    }, 20);
  });
</script>

</body>
</html>