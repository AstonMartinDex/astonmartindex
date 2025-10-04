
<html>
<head>
  <title>Aston Martin Dex</title>
  <meta name="description" content="Your AI‑Powered Design Assistant. Generate, customize, and perfect designs with cutting‑edge AI." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: black;             
      --panel: #34ebb7;          
      --card: #151827;           
      --muted: #a8b0c2;          
      --text: #f5f7ff;           
      --accent: #34ebb7;         
      --accent-2: #34ebb7;      
    }
    .blog { grid-template-columns:repeat(auto-fit,minmax(300px,1fr)); }
    .post {
      background:var(--card); border-radius:var(--radius); overflow:hidden;
      border:1px solid var(--border); transition:transform var(--transition);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      color:var(--text);
      background: radial-gradient(1200px 800px at 10% -10%, rgba(139,92,246,.07), transparent 50%),
                  radial-gradient(800px 600px at 110% 10%, rgba(79,70,229,.08), transparent 40%),
                  var(--bg);
      line-height:1.6;
    }

    a{color:inherit;text-decoration:none}
    .container{width:min(1200px, 92vw); margin-inline:auto}
    .section{padding:72px 0}
    .grid{display:grid; gap:24px}

    /* Header */
    header{
      position:sticky; top:0; z-index:50;
      backdrop-filter:saturate(160%) blur(12px);
      background:linear-gradient(to bottom, rgba(16,18,24,.65), rgba(16,18,24,.65));
      border-bottom:var(--border);
    }
    .nav{display:flex; align-items:center; justify-content:space-between; padding:16px 0}
    .brand{display:flex; align-items:center; gap:12px; font-weight:800; letter-spacing:.2px}
    nav a{opacity:.9; font-weight:500; padding:10px 12px; border-radius:10px}
    nav a:hover{background:rgba(255,255,255,.04)}

    .btn{display:inline-flex; align-items:center; justify-content:center; gap:10px; font-weight:700; letter-spacing:.2px;
      padding:12px 18px; border-radius:14px; border:var(--border); position:relative; overflow:hidden}
    .btn-primary{
      background:#34ebb7;
      border-color: transparent;
    }
    .btn-ghost{background:rgba(255,255,255,.02)}

    /* Hero */
    .hero{display:grid; grid-template-columns: 1.15fr .85fr; gap:40px; align-items:center; padding:56px 0}
    .badge{display:inline-flex; align-items:center; gap:8px; padding:8px 12px; border-radius:999px; font-size:.85rem; background:#34ebb7; border:1px solid rgba(139,92,246,.25)}
    h1{font-size: clamp(36px, 4.2vw, 56px); line-height:1.05; margin:16px 0 18px; letter-spacing:-.5px}
    h1 .accent{background:#34ebb7; -webkit-background-clip:text; background-clip:text; -webkit-text-fill-color:transparent}
    .lead{font-size: clamp(16px, 1.2vw, 18px); color:var(--muted); max-width:60ch}
    .cta{display:flex; gap:12px; flex-wrap:wrap; margin-top:24px}

    .hero-art{
      position:relative; isolation:isolate; aspect-ratio:1/1; border-radius:var(--radius-2xl);
      background: radial-gradient(120% 120% at 80% 20%, rgba(139,92,246,.18), transparent 60%), var(--panel);
      border:var(--border); box-shadow:var(--shadow-2);
      overflow:hidden;
    }
    .hero-swoosh{position:absolute; inset:10% 8% 8% 10%; background:url('https://images.unsplash.com/photo-1607644941052-d9f3bde2d9a9?q=80&w=1200&auto=format&fit=crop') center/cover no-repeat; filter:saturate(130%) hue-rotate(-10deg)}
    .hero-glow{position:absolute; inset:-20% -30% -30% -20%; background:radial-gradient(50% 50% at 60% 40%, rgba(139,92,246,.65), transparent 55%), radial-gradient(50% 50% at 40% 60%, rgba(6,182,212,.45), transparent 55%); filter: blur(60px); opacity:.55; z-index:-1}

    /* Logos */
    .logos{display:grid; grid-template-columns:repeat(6,1fr); gap:22px; opacity:.85}
    .logos div{height:40px; border-radius:12px; display:grid; place-items:center; background:rgba(255,255,255,.02); border:var(--border)}

    /* Section titles */
    .eyebrow{letter-spacing:.18em; text-transform:uppercase; font-weight:700; font-size:.85rem; color:#c4c9d7}
    .title{font-size: clamp(28px, 3.2vw, 42px); margin:10px 0 18px}
    .title .accent{color:var(--accent-2)}
    .subtitle{color:var(--muted); max-width:70ch}

    /* Feature steps */
    .steps{grid-template-columns: repeat(3, 1fr)}
    .card{background:linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02)); border:var(--border); border-radius:var(--radius-xl); padding:24px; }
    .icon{
      width:44px; height:44px; border-radius:12px; display:grid; place-items:center; background:#34ebb7; 
    }
    .card h3{margin:16px 0 8px}
    .card p{color:var(--muted)}

    /* Pricing */
    .pricing{grid-template-columns: repeat(3, 1fr)}
    .price-card{position:relative; padding:26px; border-radius:22px; background:linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02)); border:var(--border); box-shadow:var(--shadow-2)}
    .price-card.highlight{background:linear-gradient(180deg, rgba(139,92,246,.18), rgba(255,255,255,.03)); outline: 1px solid rgba(139,92,246,.5)}
    .price{display:flex; align-items:flex-end; gap:10px; margin:10px 0}
    .price strong{font-size:38px}
    .billing{display:flex; align-items:center; gap:12px; margin:14px 0 26px}
    .switch{position:relative; width:56px; height:32px; background:rgba(255,255,255,.12); border-radius:999px; cursor:pointer}
    .switch::after{content:""; position:absolute; top:3px; left:3px; width:26px; height:26px; border-radius:50%; background:#fff; transition: transform .25s ease}
    .switch.active{background:linear-gradient(90deg, var(--accent), #4f46e5)}
    .switch.active::after{transform: translateX(24px)}
    .badge-save{font-size:.75rem; padding:6px 10px; border-radius:999px; background:rgba(16,185,129,.16); border:1px solid rgba(16,185,129,.35); color:#a7f3d0}
    .features{display:grid; gap:10px; margin:14px 0 20px; color:var(--muted)}
    .features li{display:flex; gap:10px}

    /* Blog */
    .blog{grid-template-columns: repeat(4, 1fr)}
    .post{overflow:hidden; border-radius:18px; background:var(--panel); border:var(--border)}
    .post .thumb{aspect-ratio: 16/10; background:#111; background-size:cover; background-position:center}
    .post .meta{padding:14px 20px}
    .post small{opacity:.75}

    /* CTA banner */
    .cta-banner{position:relative; overflow:hidden; border-radius:26px; border:var(--border); background:linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02)); min-height:220px; display:grid; grid-template-columns: 1.1fr .9fr; align-items:center; box-shadow:var(--shadow-2)}
    .cta-banner .art{position:relative; height:100%;}
    .cta-banner .blob{position:absolute; inset:10% 8% 10% 10%; background:url('https://images.unsplash.com/photo-1614851099131-31bd732ff9b6?q=80&w=1200&auto=format&fit=crop') center/cover no-repeat; filter:saturate(140%)}

    /* Footer */
    footer{border-top:var(--border); padding:36px 0 60px; color:#c5cad6}
    .foot{display:grid; grid-template-columns: 1.1fr .9fr; gap:24px}
    .links{display:grid; grid-template-columns: repeat(3, 1fr); gap:16px}
    .links a{display:block; padding:6px 0; opacity:.85}
    .links a:hover{opacity:1}

    /* Responsive */
    @media (max-width: 1024px){
      .hero{grid-template-columns: 1fr; gap:28px}
      .cta-banner{grid-template-columns: 1fr}
      .foot{grid-template-columns: 1fr}
    }
    @media (max-width: 900px){
      .logos{grid-template-columns: repeat(3,1fr)}
      .steps{grid-template-columns: 1fr}
      .pricing{grid-template-columns: 1fr}
      .blog{grid-template-columns: 1fr 1fr}
    }
.grid.blog {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* equal width cards */
  gap: 20px;
}

.post {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background: #34ebb7;
  border-radius: 9px;
  overflow: hidden;
  min-height: 300px; /* make them taller */
}

.thumb {
  flex: 1; 
  background-size: cover;
  background-position: center;
}

.meta {
  padding: 10px;
  color: black;
}

  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <span>Aston Martin Dex</span>
      </div>
      <nav aria-label="Primary">
        <a href="#features">Features</a>
        <a href="#pricing">Updates</a>
        <a href="#insights">Insights</a>
      </nav>
      <div style="display:flex; gap:10px">
        <a class="btn btn-primary" href="https://discord.com/oauth2/authorize?client_id=1365316232777171056" target="_blank" rel="noopener noreferrer">
          Add Now
        </a>
      </div>
    </div>
  </header>

  <main>
<section class="container hero" style="display:flex; align-items:center; justify-content:space-between; gap:40px;">
  
  <div style="flex:1;">
    <h1><span class="accent">Aston Martin</span><br/> Dex Bot</h1>
    <p class="lead">
      The all new dex bot based on Aston Martin with all the new cars, 
      just perfect for your interest be a part of us now!
    </p>
<div class="cta">
  <a class="btn btn-primary" href="https://discord.gg/fb9sRDgT" target="_blank" rel="noopener noreferrer">
    Get Started
  </a>
  <a class="btn btn-ghost" href="https://www.astonmartin.com/en" target="_blank" rel="noopener noreferrer">
    Learn More
  </a>
</div>

  </div>

  <div style="flex:1; text-align:right;">
    <img src="https://i.pinimg.com/736x/72/27/f7/7227f70958a8c37c47fa16237cf5d795.jpg" style="max-width:100%; height:auto;">
  </div>

</section>


    <!-- Features / Steps -->
    <section id="features" class="container section">
      <div>
        <div class="eyebrow">Aston Martin Dex</div>
        <h2 class="title">Automobile <span class="accent">Dex Bot</span></h2>
        <p class="subtitle">Discover how our Dex bot checks your car knowledge through our hourly spawns. Following is a little discription.</p>
      </div>
      <div class="grid steps" style="margin-top:24px">
        <article class="card">
          <div class="icon" aria-hidden="true">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M4 7a3 3 0 0 1 3-3h10a3 3 0 0 1 3 3v10a3 3 0 0 1-3 3H7a3 3 0 0 1-3-3V7Z" stroke="white" opacity=".9" stroke-width="1.5"/>
              <path d="M8 15l3-3 3 3 3-4 2 3" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
            </svg>
          </div>
          <h3>All the Cars</h3>
          <p>We add all the cars through out Aston's history from latest to antique.</p>
        </article>
        <article class="card">
          <div class="icon" aria-hidden="true">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle cx="12" cy="12" r="8" stroke="white" stroke-width="1.5"/>
              <path d="M9.5 9.5l5 5m0-5l-5 5" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
            </svg>
          </div>
          <h3>Error Free</h3>
          <p>Aston Martin Dex provides a user friendly interface with minimum errors to avoid frustration.</p>
        </article>
        <article class="card">
          <div class="icon" aria-hidden="true">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M7 17l10-10" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
              <path d="M14 6l4 4" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
              <rect x="3" y="15" width="6" height="6" rx="2" stroke="white" stroke-width="1.5"/>
            </svg>
          </div>
          <h3>Refined to Perfection</h3>
          <p>Perfect for all the Aston Martin lovers out there.</p>
        </article>
      </div>
    </section>

    <!-- Updates -->
    <section id="insights" class="container section">
      <div>
        <div class="eyebrow">Updates</div>
        <h2 class="title">Catch all the new <span class="accent">Updates</span></h2>
        <p>Get all the lastest news regarding FC Mobile</p>    
      </div>

<div class="grid blog">
  <article class="post">
    <div class="thumb" style="background-image:url('https://images.pistonheads.com/nimg/44188/aston_martin_lead.jpg')"></div>
    <div class="meta">
      <small>Oct 2025 • Update</small>
      <h3>Added more dexes</h3>
    </div>
  </article>

  <article class="post">
    <div class="thumb" style="background-image:url('https://miro.medium.com/1*untpfVILgd0Xu09yZqlSbg.jpeg')"></div>
    <div class="meta">
      <small>Sept 2025 • Update</small>
      <h3>Fixed some bugs</h3>
    </div>
  </article>
</div>

    <!-- Insights / Blog -->
    <section id="insights" class="container section">
      <div>
        <div class="eyebrow">What do we offer?</div>
        <h2 class="title">Get all the information <span class="accent">about us</span></h2>
        <p class="subtitle">Dive into the world of Aston Martins through a new portal.</p>
      </div>

      <div class="grid blog" style="margin-top:24px">
        <article class="post">
          <div class="thumb" style="background-image:url('https://media.gq-magazine.co.uk/photos/6405fb643e977a7efb8a7764/master/pass/Aston-Martin-Valkyrie-HED.jpg')"></div>
          <div class="meta">
            <small>Aston Martin</small>
            <h3 style="margin:8px 0 6px">Learn and collect about all the Aston Martins</h3>
          </div>
        </article>
        <article class="post">
          <div class="thumb" style="background-image:url('https://hips.hearstapps.com/hmg-prod/images/2026-aston-martin-vantage-roadster-112-681b61e83bfee.jpg?crop=0.719xw:0.539xh;0.0976xw,0.224xh&resize=1200:*')"></div>
          <div class="meta">
            <small>Car Knowledge</small>
            <h3 style="margin:8px 0 6px">Put your car knowledge to the test and get a chance to improve it espeacially about Aston Martins</h3>
          </div>
        </article>
        <article class="post">
          <div class="thumb" style="background-image:url('https://media.astonmartin.com/wp-content/uploads/2024/10/ce859c89496adc2e56207f62e0616485-m.jpg.webp')"></div>
          <div class="meta">
            <small>Timeline</small>
            <h3 style="margin:8px 0 6px">Find about the evolution of Aston Martin.</h3>
          </div>
        </article>
        <article class="post">
          <div class="thumb" style="background-image:url('https://www.astonmartin.com/-/media/models---amr25/heros/amr25_hero_desktop.jpg?mw=1920&rev=-1&hash=252FBA9A3B1DE9CEDFE9C415C87C9970')"></div>
          <div class="meta">
            <small>Aston Martin F1</small>
            <h3 style="margin:8px 0 6px">Show your loyalty for Aston by getting updates regarding the Formula 1 team</h3>
          </div>
        </article>
      </div>

      <div style="display:flex; justify-content:center; margin-top:18px">
        <a class="btn btn-ghost" href="#">Read More</a>
      </div>
    </section>

<!-- CTA Banner -->
<section class="container section">
  <div class="cta-banner">
    <div style="padding:26px 26px 32px">
      <h2 class="title" style="margin-top:6px">
        Start Your <span class="accent">Journey</span> Today
      </h2>
      <p class="subtitle">Join our discord server for further details</p>
      <div class="cta" style="margin-top:18px">
        <a class="btn btn-primary" href="https://discord.gg/fb9sRDgT" target="_blank" rel="noopener noreferrer">
          Get Started
        </a>
      </div>
    </div>
    <div class="art">
      <div class="blob" role="img" aria-label="Purple 3D fluid art"></div>
    </div>
  </div>
</section>

  </main>

<!-- Footer -->
<footer>
  <div class="container foot">
    
    <!-- Brand / About -->
    <div>
      <div class="brand" style="margin-bottom:8px">
        <div class="logo" aria-hidden="true"></div>
        <strong>Aston Martin Dex Bot</strong>
      </div>
      <p style="color:var(--muted); max-width:50ch">
        The ultimate Discord bot for Aston Martin enthusiasts. Collect, trade, and explore legendary cars while competing with friends in your server.
      </p>
    </div>

    <!-- Links -->
    <div class="links">

      <!-- Bot Features -->
      <div>
        <strong>Bot Features</strong>
        <a href="#spawn">Car Spawns</a>
        <a href="#dex">Dex Collection</a>
        <a href="#rarity">Rarity System</a>
      </div>

      <!-- Community -->
      <div>
        <strong>Community</strong>
        <a href="#">Support Server</a>
        <a href="#">Invite Bot</a>
        <a href="#">Report a Bug</a>
      </div>

      <!-- Resources -->
      <div>
        <strong>Resources</strong>
        <a href="#commands">Commands</a>
        <a href="#">Docs</a>
        <a href="#">FAQ</a>
      </div>

    </div>
  </div>
</footer>


  <script>
    // Smooth in‑page links
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const id = a.getAttribute('href');
        if(id.length>1){
          const el = document.querySelector(id);
          if(el){ e.preventDefault(); el.scrollIntoView({behavior:'smooth'}); }
        }
      });
    });

    // Pricing toggle (Monthly / Yearly with 20% off applied to yearly)
    const switchEl = document.getElementById('billingSwitch');
    const prices = {
      monthly: { basic: 14.99, pro: 29.99 },
      yearly:  { basic: 14.99*12*0.8, pro: 29.99*12*0.8 } // 20% savings
    };
    const fmt = v => '$' + v.toFixed(2).replace(/\.00$/,'');
    const updatePrices = yearly => {
      const tier = yearly ? 'yearly' : 'monthly';
      document.getElementById('p-basic').textContent = fmt(prices[tier].basic) + (yearly ? '' : '');
      document.getElementById('p-pro').textContent   = fmt(prices[tier].pro) + (yearly ? '' : '');
      document.getElementById('saveBadge').style.opacity = yearly ? 1 : .6;
    };
    const toggle = () => {
      switchEl.classList.toggle('active');
      const yearly = switchEl.classList.contains('active');
      switchEl.setAttribute('aria-checked', yearly ? 'true' : 'false');
      updatePrices(yearly);
    };
    switchEl.addEventListener('click', toggle);
    switchEl.addEventListener('keydown', e=>{ if(e.key==='Enter' || e.key===' ') { e.preventDefault(); toggle(); }});
    updatePrices(false);
  </script>
</body>
</html>

