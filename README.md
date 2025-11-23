 MooncryptoLab-Marketing.github.io
 
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>MoonCrypto_Lab — Crypto Marketing Engine</title>

  <!-- Google font (optional) -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg1: #0f0b1a;
      --bg2: #170923;
      --accent1: #9b5cff; /* purple */
      --accent2: #ff6bb5; /* pink */
      --muted: #bdb8d6;
      --glass: rgba(255,255,255,0.04);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg,var(--bg1),var(--bg2));
      color:#fff;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }

    /* Container */
    .container{max-width:1100px;margin:0 auto;padding:40px 20px;}

    /* Header */
    header{display:flex;align-items:center;justify-content:space-between;gap:20px}
    .brand{display:flex;align-items:center;gap:14px}
    .logo{
      width:56px;height:56px;border-radius:12px;
      background: radial-gradient(circle at 30% 30%, #ffffff22, transparent 20%),
                  linear-gradient(135deg,var(--accent1),var(--accent2));
      display:flex;align-items:center;justify-content:center;font-weight:800;
      box-shadow: 0 6px 20px rgba(0,0,0,0.45), inset 0 -6px 18px rgba(0,0,0,0.15);
      border: 1px solid rgba(255,255,255,0.05);
    }
    .brand h1{font-size:18px;margin:0;letter-spacing:0.2px}
    .brand p{margin:0;font-size:12px;color:var(--muted)}

    nav a{color:var(--muted);text-decoration:none;margin-left:18px;font-weight:600;font-size:14px}
    .cta{display:inline-block;padding:10px 14px;border-radius:10px;background:linear-gradient(90deg,var(--accent2),var(--accent1));text-decoration:none;color:white;font-weight:700;box-shadow:0 8px 30px rgba(155,92,255,0.14)}

    /* Hero */
    .hero{
      margin-top:36px;
      display:grid;
      grid-template-columns: 1fr 420px;
      gap:32px;
      align-items:center;
    }
    .hero-left h2{font-size:34px;margin:0 0 12px 0;line-height:1.05}
    .tag{display:inline-block;background:linear-gradient(90deg,var(--accent1),var(--accent2));padding:6px 10px;border-radius:999px;font-weight:700;color:#fff;font-size:12px;letter-spacing:0.6px}
    .hero-left p{color:var(--muted);margin:14px 0 20px;max-width:62ch}
    .hero-actions{display:flex;gap:12px;flex-wrap:wrap}
    .btn-outline{padding:10px 14px;border-radius:10px;border:1px solid rgba(255,255,255,0.08);background:transparent;color:var(--muted);text-decoration:none;font-weight:700}
    .stat-row{display:flex;gap:18px;margin-top:20px;align-items:center}
    .stat{background:var(--glass);padding:12px 16px;border-radius:12px;border:1px solid rgba(255,255,255,0.04)}
    .stat strong{display:block;font-size:18px}
    .stat span{display:block;color:var(--muted);font-size:13px}

    /* Hero visual */
    .card{
      background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));
      border-radius:18px;padding:22px;border:1px solid rgba(255,255,255,0.04);
      box-shadow: 0 20px 50px rgba(0,0,0,0.6);
      position:relative;overflow:hidden;
    }
    .moon{
      width:100%;height:260px;border-radius:12px;
      background: radial-gradient(circle at 20% 20%, rgba(255,255,255,0.06), transparent 10%),
                  radial-gradient(circle at 80% 80%, rgba(255,255,255,0.02), transparent 10%),
                  linear-gradient(180deg,#160627,#0c0420);
      display:flex;align-items:center;justify-content:center;color:rgba(255,255,255,0.9);font-weight:700;font-size:26px;
      position:relative;
    }
    .moon::after{
      content:"";
      position:absolute;right:-90px;top:-60px;width:240px;height:240px;border-radius:50%;
      background:radial-gradient(circle at 40% 40%, rgba(255,255,255,0.06), transparent 30%), linear-gradient(90deg,#ffffff11,#ffffff00);
      transform:rotate(14deg);
      filter:blur(24px);
    }
    /* subtle floating circles */
    .orb{position:absolute;border-radius:50%;opacity:0.14;filter:blur(6px)}
    .orb.o1{width:110px;height:110px;right:18px;top:14px;background:linear-gradient(90deg,var(--accent2),var(--accent1))}
    .orb.o2{width:70px;height:70px;left:18px;bottom:22px;background:linear-gradient(90deg,var(--accent1),var(--accent2));opacity:0.1}

    /* Services */
    .services{margin-top:48px;display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .service{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:18px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
    .service h3{margin:0 0 10px 0}
    .service p{margin:0;color:var(--muted);font-size:14px}

    /* Projects & logos */
    .projects{margin-top:36px;padding:18px;border-radius:12px;border:1px dashed rgba(255,255,255,0.04);display:flex;flex-direction:column;gap:12px}
    .logos{display:flex;gap:12px;flex-wrap:wrap;align-items:center}
    .logo-placeholder{width:120px;height:48px;background:rgba(255,255,255,0.03);border-radius:8px;display:flex;align-items:center;justify-content:center;color:var(--muted);font-weight:700}

    /* CTA footer */
    .cta-footer{margin-top:36px;display:flex;align-items:center;gap:18px;justify-content:space-between;padding:18px;border-radius:12px;background:linear-gradient(90deg, rgba(155,92,255,0.06), rgba(255,107,181,0.03));border:1px solid rgba(255,255,255,0.03)}
    .links a{color:var(--muted);text-decoration:none;margin-right:12px;font-weight:700}

    /* Footer */
    footer{margin-top:48px;padding:18px 0;color:var(--muted);font-size:13px;text-align:center}

    /* Responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr;gap:22px}
      .services{grid-template-columns:repeat(2,1fr)}
      .container{padding:28px 18px}
    }
    @media (max-width:560px){
      nav{display:none}
      .services{grid-template-columns:1fr}
      .stat-row{flex-direction:column;align-items:flex-start;gap:12px}
      .logo{width:46px;height:46px}
    }

    /* small animation */
    @keyframes floaty {
      0%{ transform: translateY(0px) }
      50%{ transform: translateY(-10px) }
      100%{ transform: translateY(0px) }
    }
    .moon{animation: floaty 6s ease-in-out infinite}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">M</div>
        <div>
          <h1>MoonCrypto_Lab</h1>
          <p class="muted">The Crypto Marketing Engine</p>
        </div>
      </div>

      <nav>
        <a href="#services">Services</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
        <a class="cta" href="#contact">Work with us</a>
      </nav>
    </header>

    <!-- HERO -->
    <section class="hero" aria-labelledby="hero-heading">
      <div class="hero-left">
        <span class="tag">Full-stack Web3 Marketing</span>
        <h2 id="hero-heading">We don’t promote projects — we <strong>make them go viral.</strong></h2>
        <p>MoonCrypto_Lab builds attention, trust, and momentum for DeFi, NFTs, GameFi, and memecoin projects. From presale hype to CEX listing — we create narratives that convert followers into holders.</p>

        <div class="hero-actions">
          <a class="cta" href="#contact">Start a campaign</a>
          <a class="btn-outline" href="#services">Our services</a>
          <a class="btn-outline" href="#projects">See projects</a>
        </div>

        <div class="stat-row" aria-hidden="true">
          <div class="stat"><strong>1000+</strong><span>Community-driven projects</span></div>
          <div class="stat"><strong>Tiered KOLs</strong><span>Crypto influencers network</span></div>
          <div class="stat"><strong>Performance</strong><span>Real engagement, not bots</span></div>
        </div>
      </div>

      <div class="card" aria-hidden="true">
        <div class="moon" role="img" aria-label="Moon themed visual">
          <!-- Replace the inner content with your hero image or animated SVG -->
          <div style="text-align:center">
            <div style="font-size:20px;font-weight:800">MOONCRYPTO_LAB</div>
            <div style="margin-top:6px;color:var(--muted);font-size:13px">Branding • Influencers • Community</div>
          </div>
        </div>
        <div class="orb o1"></div>
        <div class="orb o2"></div>
      </div>
    </section>

    <!-- SERVICES -->
    <section id="services" class="services" aria-labelledby="services-heading">
      <div class="service">
        <h3>Full Campaigns</h3>
        <p>Pre-launch narratives, viral socials, presale buzz, and listing day exposure built end-to-end for launch success.</p>
      </div>

      <div class="service">
        <h3>Influencer & KOL Network</h3>
        <p>Access to tiered crypto influencers, meme pages, and community promoters to deliver authentic reach and conversions.</p>
      </div>

      <div class="service">
        <h3>Community Growth</h3>
        <p>Telegram & Discord growth, moderation, ambassador programs, Zealy & Galxe quest design and gamified onboarding.</p>
      </div>

      <div class="service">
        <h3>Creative Studio</h3>
        <p>Logos, posters, animations, and MOONGOD-themed visuals that build identity and recall across socials.</p>
      </div>

      <div class="service">
        <h3>Listing Support</h3>
        <p>Listing PR, exchange outreach, and listing-day amplification to maximize volume and visibility.</p>
      </div>

      <div class="service">
        <h3>Strategy & Advisory</h3>
        <p>Narrative crafting, holder psychology, growth playbooks, and long-term momentum planning for sustainable success.</p>
      </div>
    </section>

    <!-- PROJECTS / LOGOS -->
    <section id="projects" class="projects" aria-labelledby="projects-heading">
      <h3 id="projects-heading" style="margin:0 0 8px 0">Projects we've worked with</h3>
      <p style="margin:0 0 12px;color:var(--muted);font-size:14px">
      <div class="logos">
        <div class="logo-placeholder">Wojak</div>
        <div class="logo-placeholder">Glamslam</div>
        <div class="logo-placeholder">PepeAI</div>
        <div class="logo-placeholder">Rats</div>
        <div class="logo-placeholder">+1000</div>
        <!-- Add more logo elements or use <img src="/path/to/logo.png" alt="Client name"> -->
      </div>

    <!-- CTA -->
<section id="contact" class="cta-footer" aria-labelledby="contact-heading">
  <div>
    <h3 id="contact-heading" style="margin:0 0 6px 0">Ready to grow your project?</h3>
    <p style="margin:0;color:var(--muted)">Send us a message and we’ll share a tailored growth plan and pricing outline.</p>
  </div>

  <div class="links" style="display:flex;align-items:center;gap:12px;flex-wrap:wrap;">

    <!-- Telegram -->
    <a href="https://t.me/MOONCYRPTO_LAB" 
       target="_blank" 
       rel="noopener noreferrer" 
       class="cta">
      Telegram
    </a>

    <!-- X (Twitter) -->
    <a href="https://x.com/MooncryptoLab" 
       target="_blank" 
       rel="noopener noreferrer" 
       class="btn-outline">
      X (Twitter)
    </a>

    <!-- Linktree -->
    <a href="YOUR_LINKTREE_URL_HERE" 
       target="_blank" 
       rel="noopener noreferrer" 
       class="btn-outline">
      Linktree
    </a>

  </div>
</section>
    <footer>
      ©️ <span id="year"></span> MoonCrypto_Lab — Built for momentum. • <span style="color:var(--muted)">Made with MOONGOD vibes</span>
    </footer>
  </div>

  <script>
    // Set year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Accessibility: enable keyboard focus styles only when user is tabbing
    (function(){
      function handleFirstTab(e){
        if(e.key === 'Tab'){
          document.documentElement.classList.add('user-is-tabbing');
          window.removeEventListener('keydown', handleFirstTab);
        }
      }
      window.addEventListener('keydown', handleFirstTab);
    })();
  </script>
</body>
</html>
