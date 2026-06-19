<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mahadev Kishan Gurram — Aspiring Data Analyst</title>
<meta name="description" content="Mahadev Kishan Gurram — Aspiring Data Analyst / IT Fresher. Data analysis, visualization, and cloud computing.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,300;9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  /* ============ DESIGN TOKENS ============ */
  :root{
    --bg:#fbfcfe;
    --bg-elevated:#ffffff;
    --bg-soft:#f1f4f9;
    --text:#0c1320;
    --text-muted:#52607a;
    --text-faint:#8b97ad;
    --border:#e4e9f1;
    --accent:#1d4ed8;
    --accent-deep:#10246b;
    --accent-soft:#e8eefc;
    --accent-glow:rgba(29,78,216,0.18);
    --mono:'JetBrains Mono', monospace;
    --display:'Fraunces', serif;
    --body:'Inter', sans-serif;
    --radius-sm:10px;
    --radius-md:16px;
    --radius-lg:28px;
    --shadow-sm:0 1px 2px rgba(12,19,32,0.04), 0 1px 1px rgba(12,19,32,0.03);
    --shadow-md:0 8px 24px rgba(12,19,32,0.06), 0 2px 8px rgba(12,19,32,0.04);
    --shadow-lg:0 24px 64px rgba(12,19,32,0.10), 0 8px 24px rgba(12,19,32,0.06);
    --ease:cubic-bezier(.16,.8,.24,1);
  }

  [data-theme="dark"]{
    --bg:#07090d;
    --bg-elevated:#0e121a;
    --bg-soft:#12161f;
    --text:#eef1f7;
    --text-muted:#9aa5bb;
    --text-faint:#5d6679;
    --border:#1d2330;
    --accent:#5b8def;
    --accent-deep:#a9c6ff;
    --accent-soft:#121d34;
    --accent-glow:rgba(91,141,239,0.22);
    --shadow-sm:0 1px 2px rgba(0,0,0,0.3);
    --shadow-md:0 8px 24px rgba(0,0,0,0.45), 0 2px 8px rgba(0,0,0,0.3);
    --shadow-lg:0 24px 64px rgba(0,0,0,0.55), 0 8px 24px rgba(0,0,0,0.35);
  }

  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--bg);
    color:var(--text);
    font-family:var(--body);
    font-size:16px;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    transition:background .4s var(--ease), color .4s var(--ease);
    overflow-x:hidden;
  }
  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    *,*::before,*::after{animation-duration:.001ms !important; animation-iteration-count:1 !important; transition-duration:.001ms !important; scroll-behavior:auto !important;}
  }

  img{max-width:100%;display:block;}
  a{color:inherit;text-decoration:none;}
  ul{list-style:none;}
  :focus-visible{outline:2px solid var(--accent);outline-offset:3px;border-radius:4px;}

  .wrap{max-width:1120px;margin:0 auto;padding:0 32px;}
  @media (max-width:640px){.wrap{padding:0 20px;}}

  .eyebrow{
    font-family:var(--mono);
    font-size:12.5px;
    letter-spacing:.14em;
    text-transform:uppercase;
    color:var(--accent);
    display:flex;align-items:center;gap:10px;
    margin-bottom:18px;
  }
  .eyebrow::before{content:'';width:7px;height:7px;border-radius:50%;background:var(--accent);box-shadow:0 0 0 4px var(--accent-glow);}

  h1,h2,h3{font-family:var(--display);font-weight:600;letter-spacing:-0.01em;color:var(--text);}

  /* ============ NAVBAR ============ */
  .navbar{
    position:fixed;top:0;left:0;right:0;z-index:1000;
    display:flex;align-items:center;justify-content:center;
    padding:18px 0;
    transition:padding .35s var(--ease), background .35s var(--ease), box-shadow .35s var(--ease), border-color .35s var(--ease);
  }
  .navbar.scrolled{
    padding:11px 0;
    background:color-mix(in srgb, var(--bg) 82%, transparent);
    backdrop-filter:blur(16px) saturate(160%);
    -webkit-backdrop-filter:blur(16px) saturate(160%);
    border-bottom:1px solid var(--border);
    box-shadow:var(--shadow-sm);
  }
  .nav-inner{
    width:100%;max-width:1120px;padding:0 32px;
    display:flex;align-items:center;justify-content:space-between;
  }
  .nav-logo{
    font-family:var(--display);font-weight:600;font-size:18.5px;
    display:flex;align-items:center;gap:10px;
    letter-spacing:-0.01em;
  }
  .nav-logo .mark{
    width:30px;height:30px;border-radius:9px;
    background:linear-gradient(135deg,var(--accent),var(--accent-deep));
    display:flex;align-items:center;justify-content:center;
    color:#fff;font-family:var(--mono);font-weight:500;font-size:13px;
    flex-shrink:0;
  }
  .nav-links{display:flex;align-items:center;gap:34px;}
  .nav-links a{
    font-size:14.5px;font-weight:500;color:var(--text-muted);
    position:relative;padding:4px 0;
    transition:color .25s var(--ease);
  }
  .nav-links a::after{
    content:'';position:absolute;bottom:0;left:0;right:0;height:1px;
    background:var(--accent);transform:scaleX(0);transform-origin:left;
    transition:transform .3s var(--ease);
  }
  .nav-links a:hover{color:var(--text);}
  .nav-links a:hover::after{transform:scaleX(1);}
  .nav-right{display:flex;align-items:center;gap:18px;}

  .theme-toggle{
    width:38px;height:38px;border-radius:50%;
    border:1px solid var(--border);background:var(--bg-elevated);
    display:flex;align-items:center;justify-content:center;cursor:pointer;
    transition:transform .3s var(--ease), border-color .3s var(--ease), background .3s var(--ease);
    flex-shrink:0;
  }
  .theme-toggle:hover{transform:translateY(-2px);border-color:var(--accent);}
  .theme-toggle svg{width:17px;height:17px;stroke:var(--text);}
  .theme-toggle .sun{display:none;}
  [data-theme="dark"] .theme-toggle .sun{display:block;}
  [data-theme="dark"] .theme-toggle .moon{display:none;}

  .nav-cta{
    font-size:13.5px;font-weight:600;color:#fff;
    background:var(--text);
    padding:9px 18px;border-radius:100px;
    transition:transform .25s var(--ease), box-shadow .25s var(--ease), background .25s var(--ease);
    white-space:nowrap;
  }
  [data-theme="dark"] .nav-cta{background:var(--accent);}
  .nav-cta:hover{transform:translateY(-2px);box-shadow:var(--shadow-md);}

  .nav-burger{display:none;width:38px;height:38px;border-radius:50%;border:1px solid var(--border);background:var(--bg-elevated);align-items:center;justify-content:center;cursor:pointer;flex-direction:column;gap:4px;}
  .nav-burger span{width:16px;height:1.5px;background:var(--text);display:block;transition:transform .3s var(--ease), opacity .3s var(--ease);}
  .nav-burger.open span:nth-child(1){transform:translateY(5.5px) rotate(45deg);}
  .nav-burger.open span:nth-child(2){opacity:0;}
  .nav-burger.open span:nth-child(3){transform:translateY(-5.5px) rotate(-45deg);}

  .mobile-menu{
    position:fixed;top:0;left:0;right:0;bottom:0;z-index:999;
    background:var(--bg);
    display:flex;flex-direction:column;align-items:center;justify-content:center;gap:34px;
    opacity:0;visibility:hidden;transform:translateY(-12px);
    transition:opacity .35s var(--ease), transform .35s var(--ease), visibility .35s;
  }
  .mobile-menu.open{opacity:1;visibility:visible;transform:translateY(0);}
  .mobile-menu a{font-family:var(--display);font-size:30px;font-weight:600;color:var(--text);}

  @media (max-width:860px){
    .nav-links{display:none;}
    .nav-burger{display:flex;}
  }

  /* ============ HERO ============ */
  .hero{
    position:relative;
    min-height:100vh;
    display:flex;align-items:center;
    padding:160px 0 100px;
    overflow:hidden;
  }
  .hero-bg{
    position:absolute;inset:0;z-index:0;pointer-events:none;
    background:
      radial-gradient(ellipse 700px 500px at 82% 8%, var(--accent-glow), transparent 60%),
      radial-gradient(ellipse 500px 400px at 8% 90%, var(--accent-glow), transparent 60%);
    opacity:.9;
  }
  .hero-grid-overlay{
    position:absolute;inset:0;z-index:0;pointer-events:none;
    background-image:
      linear-gradient(var(--border) 1px, transparent 1px),
      linear-gradient(90deg, var(--border) 1px, transparent 1px);
    background-size:64px 64px;
    mask-image:radial-gradient(ellipse 900px 600px at 50% 0%, black, transparent 70%);
    -webkit-mask-image:radial-gradient(ellipse 900px 600px at 50% 0%, black, transparent 70%);
    opacity:.5;
  }
  .hero-inner{
    position:relative;z-index:1;
    display:grid;grid-template-columns:1.25fr .75fr;gap:64px;align-items:center;width:100%;
  }
  .hero-headline{
    font-size:clamp(40px, 5.6vw, 72px);
    line-height:1.04;
    font-weight:600;
    letter-spacing:-0.02em;
    margin-bottom:24px;
  }
  .hero-headline .line{display:block;overflow:hidden;}
  .hero-headline .line span{display:inline-block;}
  .hero-headline em{
    font-style:italic;font-weight:500;color:var(--accent);
    background:linear-gradient(90deg, var(--accent), var(--accent-deep));
    -webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent;
  }
  .hero-sub{
    font-size:18px;color:var(--text-muted);max-width:480px;margin-bottom:36px;
    line-height:1.65;
  }
  .hero-actions{display:flex;gap:14px;flex-wrap:wrap;margin-bottom:48px;}
  .btn{
    display:inline-flex;align-items:center;gap:8px;
    font-size:14.5px;font-weight:600;
    padding:13px 24px;border-radius:100px;
    transition:transform .3s var(--ease), box-shadow .3s var(--ease), background .3s var(--ease), border-color .3s var(--ease);
    border:1px solid transparent;cursor:pointer;
  }
  .btn-primary{background:var(--accent);color:#fff;box-shadow:0 1px 0 rgba(255,255,255,.15) inset, var(--shadow-sm);}
  .btn-primary:hover{transform:translateY(-3px);box-shadow:var(--shadow-lg);}
  .btn-secondary{background:transparent;color:var(--text);border-color:var(--border);}
  .btn-secondary:hover{transform:translateY(-3px);border-color:var(--accent);box-shadow:var(--shadow-md);}
  .btn svg{width:15px;height:15px;}

  .hero-stats{display:flex;gap:36px;flex-wrap:wrap;}
  .hero-stat .num{
    font-family:var(--display);font-size:30px;font-weight:600;color:var(--text);
    display:block;
  }
  .hero-stat .label{font-size:12.5px;color:var(--text-faint);font-family:var(--mono);letter-spacing:.04em;}

  .hero-card{
    position:relative;
    background:var(--bg-elevated);
    border:1px solid var(--border);
    border-radius:var(--radius-lg);
    padding:40px 32px;
    box-shadow:var(--shadow-lg);
    text-align:center;
  }
  .hero-avatar{
    width:128px;height:128px;border-radius:50%;
    margin:0 auto 22px;object-fit:cover;
    border:3px solid var(--bg-elevated);
    box-shadow:0 0 0 1px var(--border), var(--shadow-md);
  }
  .hero-card h3{font-size:20px;margin-bottom:4px;}
  .hero-card .role{font-size:13.5px;color:var(--accent);font-family:var(--mono);margin-bottom:18px;}
  .hero-card .loc{font-size:13px;color:var(--text-faint);display:flex;align-items:center;justify-content:center;gap:6px;margin-bottom:20px;}
  .hero-card .loc svg{width:13px;height:13px;flex-shrink:0;}
  .pulse-strip{
    display:flex;align-items:flex-end;gap:4px;height:36px;justify-content:center;margin-bottom:18px;
  }
  .pulse-strip .bar{
    width:5px;border-radius:3px;background:linear-gradient(180deg, var(--accent), var(--accent-deep));
    animation:pulse 1.8s ease-in-out infinite;
  }
  .pulse-strip .bar:nth-child(1){height:40%;animation-delay:0s;}
  .pulse-strip .bar:nth-child(2){height:75%;animation-delay:.15s;}
  .pulse-strip .bar:nth-child(3){height:50%;animation-delay:.3s;}
  .pulse-strip .bar:nth-child(4){height:95%;animation-delay:.45s;}
  .pulse-strip .bar:nth-child(5){height:60%;animation-delay:.6s;}
  .pulse-strip .bar:nth-child(6){height:80%;animation-delay:.75s;}
  .pulse-strip .bar:nth-child(7){height:35%;animation-delay:.9s;}
  @keyframes pulse{0%,100%{opacity:.55;transform:scaleY(.85);}50%{opacity:1;transform:scaleY(1);}}
  .hero-card-links{display:flex;gap:10px;justify-content:center;}
  .icon-link{
    width:36px;height:36px;border-radius:50%;border:1px solid var(--border);
    display:flex;align-items:center;justify-content:center;
    transition:transform .25s var(--ease), border-color .25s var(--ease), background .25s var(--ease);
  }
  .icon-link svg{width:16px;height:16px;stroke:var(--text-muted);}
  .icon-link:hover{transform:translateY(-3px);border-color:var(--accent);background:var(--accent-soft);}
  .icon-link:hover svg{stroke:var(--accent);}

  @media (max-width:900px){
    .hero-inner{grid-template-columns:1fr;gap:48px;}
    .hero-card{max-width:360px;margin:0 auto;}
  }

  /* ============ SECTION SCAFFOLDING ============ */
  section{padding:120px 0;position:relative;}
  @media (max-width:640px){section{padding:80px 0;}}
  .section-head{margin-bottom:56px;max-width:620px;}
  .section-head h2{font-size:clamp(30px,4vw,42px);line-height:1.1;}
  .section-head p{color:var(--text-muted);font-size:16.5px;margin-top:14px;}

  .reveal{opacity:0;transform:translateY(28px);transition:opacity .8s var(--ease), transform .8s var(--ease);}
  .reveal.in{opacity:1;transform:translateY(0);}
  .stagger > *{transition-delay:calc(var(--i,0) * 90ms);}

  /* ============ ABOUT ============ */
  .about{background:var(--bg-soft);border-top:1px solid var(--border);border-bottom:1px solid var(--border);}
  .about-grid{display:grid;grid-template-columns:auto 1fr;gap:56px;align-items:start;}
  .about-num{
    font-family:var(--display);font-size:120px;font-weight:300;color:var(--accent);
    line-height:1;opacity:.16;
  }
  .about-text p{font-size:19px;line-height:1.75;color:var(--text);margin-bottom:18px;}
  .about-tags{display:flex;gap:10px;flex-wrap:wrap;margin-top:28px;}
  .about-tag{
    font-family:var(--mono);font-size:12.5px;color:var(--accent);
    background:var(--accent-soft);border:1px solid var(--border);
    padding:7px 14px;border-radius:100px;
  }
  @media (max-width:700px){.about-grid{grid-template-columns:1fr;}.about-num{font-size:64px;}}

  /* ============ EXPERIENCE / TIMELINE ============ */
  .timeline{position:relative;padding-left:32px;}
  .timeline::before{
    content:'';position:absolute;left:0;top:8px;bottom:8px;width:1px;
    background:linear-gradient(180deg, var(--accent), var(--border) 90%);
  }
  .tl-item{position:relative;padding-bottom:56px;}
  .tl-item:last-child{padding-bottom:0;}
  .tl-dot{
    position:absolute;left:-37px;top:4px;width:13px;height:13px;border-radius:50%;
    background:var(--bg);border:2px solid var(--accent);
    box-shadow:0 0 0 5px var(--bg-soft, var(--bg));
  }
  .tl-card{
    background:var(--bg-elevated);border:1px solid var(--border);border-radius:var(--radius-md);
    padding:30px 32px;transition:transform .35s var(--ease), box-shadow .35s var(--ease), border-color .35s var(--ease);
  }
  .tl-card:hover{transform:translateY(-4px);box-shadow:var(--shadow-md);border-color:var(--accent);}
  .tl-top{display:flex;justify-content:space-between;align-items:flex-start;gap:16px;flex-wrap:wrap;margin-bottom:6px;}
  .tl-role{font-size:19px;font-weight:700;font-family:var(--body);}
  .tl-company{color:var(--accent);font-weight:600;}
  .tl-dates{font-family:var(--mono);font-size:12.5px;color:var(--text-faint);white-space:nowrap;padding-top:4px;}
  .tl-achv{margin-top:16px;display:flex;flex-direction:column;gap:10px;}
  .tl-achv li{display:flex;gap:10px;font-size:15px;color:var(--text-muted);line-height:1.6;}
  .tl-achv li::before{content:'';width:5px;height:5px;border-radius:50%;background:var(--accent);margin-top:8px;flex-shrink:0;}

  /* ============ PROJECTS ============ */
  .projects-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:24px;}
  .proj-card{
    background:var(--bg-elevated);border:1px solid var(--border);border-radius:var(--radius-md);
    padding:32px;display:flex;flex-direction:column;gap:18px;
    transition:transform .35s var(--ease), box-shadow .35s var(--ease), border-color .35s var(--ease);
    position:relative;overflow:hidden;
  }
  .proj-card::before{
    content:'';position:absolute;top:0;left:0;right:0;height:3px;
    background:linear-gradient(90deg,var(--accent),var(--accent-deep));
    transform:scaleX(0);transform-origin:left;transition:transform .4s var(--ease);
  }
  .proj-card:hover{transform:translateY(-6px);box-shadow:var(--shadow-lg);border-color:var(--accent);}
  .proj-card:hover::before{transform:scaleX(1);}
  .proj-icon{
    width:46px;height:46px;border-radius:12px;background:var(--accent-soft);
    display:flex;align-items:center;justify-content:center;
  }
  .proj-icon svg{width:22px;height:22px;stroke:var(--accent);}
  .proj-card h3{font-size:19px;}
  .proj-card p{color:var(--text-muted);font-size:14.5px;line-height:1.65;flex-grow:1;}
  .proj-tags{display:flex;gap:8px;flex-wrap:wrap;}
  .proj-tag{font-family:var(--mono);font-size:11.5px;color:var(--text-muted);background:var(--bg-soft);border:1px solid var(--border);padding:5px 10px;border-radius:6px;}
  .proj-link{display:flex;align-items:center;gap:7px;font-size:14px;font-weight:600;color:var(--accent);margin-top:6px;}
  .proj-link svg{width:14px;height:14px;transition:transform .25s var(--ease);}
  .proj-card:hover .proj-link svg{transform:translate(3px,-3px);}
  .proj-stats{display:flex;gap:18px;font-family:var(--mono);font-size:12px;color:var(--text-faint);border-top:1px solid var(--border);padding-top:14px;}
  .proj-stats strong{color:var(--text);font-weight:600;}

  /* ============ SKILLS ============ */
  .skills-wrap{display:flex;flex-direction:column;gap:14px;}
  .skill-row{display:grid;grid-template-columns:160px 1fr;gap:24px;align-items:center;}
  .skill-cat{font-family:var(--mono);font-size:12.5px;color:var(--text-faint);letter-spacing:.05em;text-transform:uppercase;}
  .skill-pills{display:flex;gap:10px;flex-wrap:wrap;}
  .skill-pill{
    font-size:14px;font-weight:500;padding:9px 18px;border-radius:100px;
    background:var(--bg-elevated);border:1px solid var(--border);
    transition:transform .25s var(--ease), border-color .25s var(--ease), color .25s var(--ease), background .25s var(--ease);
  }
  .skill-pill:hover{transform:translateY(-3px);border-color:var(--accent);color:var(--accent);background:var(--accent-soft);}
  @media (max-width:700px){.skill-row{grid-template-columns:1fr;gap:10px;}}

  /* ============ EDUCATION ============ */
  .edu-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:20px;}
  .edu-card{
    background:var(--bg-elevated);border:1px solid var(--border);border-radius:var(--radius-md);
    padding:26px 28px;transition:transform .3s var(--ease),box-shadow .3s var(--ease),border-color .3s var(--ease);
  }
  .edu-card:hover{transform:translateY(-4px);box-shadow:var(--shadow-md);border-color:var(--accent);}
  .edu-top{display:flex;justify-content:space-between;gap:12px;align-items:flex-start;}
  .edu-degree{font-size:16.5px;font-weight:700;line-height:1.4;}
  .edu-score{font-family:var(--mono);font-size:13px;color:var(--accent);background:var(--accent-soft);padding:4px 10px;border-radius:8px;white-space:nowrap;}
  .edu-school{color:var(--text-muted);font-size:14.5px;margin-top:6px;}
  .edu-year{font-family:var(--mono);font-size:12px;color:var(--text-faint);margin-top:10px;}
  @media (max-width:700px){.edu-grid{grid-template-columns:1fr;}}

  /* ============ CONTACT ============ */
  .contact-section{
    background:linear-gradient(160deg, var(--accent-deep), var(--accent));
    border-radius:var(--radius-lg);
    padding:80px 60px;
    text-align:center;
    position:relative;overflow:hidden;
    color:#fff;
  }
  .contact-section::before{
    content:'';position:absolute;inset:0;
    background-image:radial-gradient(circle, rgba(255,255,255,.12) 1px, transparent 1px);
    background-size:22px 22px;opacity:.5;
  }
  .contact-inner{position:relative;z-index:1;max-width:560px;margin:0 auto;}
  .contact-section h2{color:#fff;font-size:clamp(28px,4vw,40px);margin-bottom:16px;}
  .contact-section p{color:rgba(255,255,255,.82);font-size:16.5px;margin-bottom:34px;}
  .contact-section .btn-primary{background:#fff;color:var(--accent-deep);}
  .contact-section .btn-secondary{border-color:rgba(255,255,255,.35);color:#fff;}
  .contact-section .btn-secondary:hover{border-color:#fff;box-shadow:none;background:rgba(255,255,255,.1);}
  .contact-actions{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;margin-bottom:36px;}
  .contact-socials{display:flex;gap:14px;justify-content:center;}
  .contact-socials .icon-link{border-color:rgba(255,255,255,.3);}
  .contact-socials .icon-link svg{stroke:#fff;}
  .contact-socials .icon-link:hover{background:rgba(255,255,255,.15);border-color:#fff;}
  @media (max-width:640px){.contact-section{padding:56px 28px;}}

  /* ============ FOOTER ============ */
  footer{padding:44px 0;border-top:1px solid var(--border);}
  .footer-inner{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:16px;}
  .footer-inner p{font-size:13.5px;color:var(--text-faint);}
  .footer-inner .footer-links{display:flex;gap:22px;}
  .footer-inner .footer-links a{font-size:13.5px;color:var(--text-muted);transition:color .25s var(--ease);}
  .footer-inner .footer-links a:hover{color:var(--accent);}

  /* ============ BACK TO TOP ============ */
  .to-top{
    position:fixed;bottom:28px;right:28px;z-index:500;
    width:46px;height:46px;border-radius:50%;
    background:var(--accent);color:#fff;border:none;
    display:flex;align-items:center;justify-content:center;cursor:pointer;
    box-shadow:var(--shadow-md);
    opacity:0;visibility:hidden;transform:translateY(10px);
    transition:opacity .3s var(--ease), transform .3s var(--ease), visibility .3s;
  }
  .to-top.show{opacity:1;visibility:visible;transform:translateY(0);}
  .to-top svg{width:18px;height:18px;}
  .to-top:hover{transform:translateY(-3px);}
</style>
</head>
<body data-theme="light">

<!-- ============ NAVBAR ============ -->
<nav class="navbar" id="navbar">
  <div class="nav-inner">
    <a href="#top" class="nav-logo"><span class="mark">MG</span>Mahadev</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#education">Education</a></li>
    </ul>
    <div class="nav-right">
      <button class="theme-toggle" id="themeToggle" aria-label="Toggle dark mode">
        <svg class="moon" viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/></svg>
        <svg class="sun" viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="4"/><path d="M12 2v2M12 20v2M4.93 4.93l1.41 1.41M17.66 17.66l1.41 1.41M2 12h2M20 12h2M6.34 17.66l-1.41 1.41M19.07 4.93l-1.41 1.41"/></svg>
      </button>
      <a href="#contact" class="nav-cta">Let's talk</a>
      <button class="nav-burger" id="navBurger" aria-label="Open menu"><span></span><span></span><span></span></button>
    </div>
  </div>
</nav>

<div class="mobile-menu" id="mobileMenu">
  <a href="#about">About</a>
  <a href="#experience">Experience</a>
  <a href="#projects">Projects</a>
  <a href="#skills">Skills</a>
  <a href="#education">Education</a>
  <a href="#contact">Contact</a>
</div>

<!-- ============ HERO ============ -->
<header class="hero" id="top">
  <div class="hero-bg"></div>
  <div class="hero-grid-overlay"></div>
  <div class="wrap hero-inner">
    <div>
      <div class="eyebrow">Available for opportunities</div>
      <h1 class="hero-headline">
        <span class="line"><span>Mahadev Kishan</span></span>
        <span class="line"><span>Gurram —</span></span>
        <span class="line"><span><em>turning raw data</em></span></span>
        <span class="line"><span>into real decisions.</span></span>
      </h1>
      <p class="hero-sub">Aspiring Data Analyst &amp; IT Fresher specializing in Python, SQL, AWS, and BI visualization — bringing a cross-disciplinary edge from hospitality management to data-driven problem solving.</p>
      <div class="hero-actions">
        <a href="#projects" class="btn btn-primary">View my work
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
        </a>
        <a href="#contact" class="btn btn-secondary">Get in touch</a>
      </div>
      <div class="hero-stats">
        <div class="hero-stat"><span class="num">82%</span><span class="label">MCA — Data Analytics</span></div>
        <div class="hero-stat"><span class="num">5</span><span class="label">Languages Spoken</span></div>
        <div class="hero-stat"><span class="num">10+</span><span class="label">SQL KPIs Built</span></div>
      </div>
    </div>

    <div class="hero-card">
      <img class="hero-avatar" src="https://github.com/chefmaahi.png" alt="Mahadev Kishan Gurram" loading="lazy" onerror="this.onerror=null;this.src='data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22128%22 height=%22128%22><rect width=%22100%25%22 height=%22100%25%22 fill=%22%231d4ed8%22/><text x=%2250%25%22 y=%2255%25%22 font-size=%2244%22 fill=%22white%22 text-anchor=%22middle%22 font-family=%22sans-serif%22>MG</text></svg>'">
      <h3>Mahadev Kishan Gurram</h3>
      <div class="role">Aspiring Data Analyst / IT Fresher</div>
      <div class="loc">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 1 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
        Curchorem, South Goa, India
      </div>
      <div class="pulse-strip" aria-hidden="true">
        <div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div><div class="bar"></div>
      </div>
      <div class="hero-card-links">
        <a class="icon-link" href="mailto:thechefmaahi@gmail.com" aria-label="Email" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16v16H4z"/><path d="m22 6-10 7L2 6"/></svg>
        </a>
        <a class="icon-link" href="https://www.linkedin.com/in/gurram-mahadev-kishan/" aria-label="LinkedIn" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-4 0v7h-4V8h4v1.5A5 5 0 0 1 16 8z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
        </a>
        <a class="icon-link" href="https://github.com/chefmaahi" aria-label="GitHub" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
        </a>
      </div>
    </div>
  </div>
</header>

<!-- ============ ABOUT ============ -->
<section class="about" id="about">
  <div class="wrap">
    <div class="about-grid reveal">
      <div class="about-num">01</div>
      <div>
        <div class="eyebrow">About</div>
        <div class="about-text">
          <p>I'm a motivated MCA graduate specializing in Data Analytics, with a working foundation in Python, SQL, AWS, and BI tools like Power BI and Tableau. My path here wasn't conventional — I bring a unique cross-disciplinary background that combines technology with hospitality management.</p>
          <p>That mix gives me an edge most analysts don't have: strong communication, fast adaptability, and a genuinely client-centric way of thinking about data. I'm eager to contribute to data-driven decision-making in a real IT environment.</p>
        </div>
        <div class="about-tags">
          <span class="about-tag">Python</span>
          <span class="about-tag">SQL</span>
          <span class="about-tag">AWS</span>
          <span class="about-tag">Power BI</span>
          <span class="about-tag">Tableau</span>
          <span class="about-tag">Data Visualization</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ============ EXPERIENCE ============ -->
<section id="experience">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">Experience &amp; Background</div>
      <h2>From hospitality floors to data dashboards.</h2>
      <p>A cross-disciplinary path that built real-world skills in adaptability, client focus, and now — analytical thinking.</p>
    </div>

    <div class="timeline">
      <div class="tl-item reveal">
        <div class="tl-dot"></div>
        <div class="tl-card">
          <div class="tl-top">
            <div class="tl-role">Data Analytics Trainee <span style="color:var(--text-faint);font-weight:400;">@</span> <span class="tl-company">Self-Directed Project Work</span></div>
            <div class="tl-dates">2024 — Present</div>
          </div>
          <ul class="tl-achv">
            <li>Designed and deployed a real-time sales performance analytics platform processing 1,000+ retail transactions using Python, SQLite (star schema), and Tableau.</li>
            <li>Built an automated ETL pipeline with 10 SQL-driven KPIs and a 4-model ensemble forecasting system to support revenue and profitability decisions.</li>
            <li>Maintained a clean, modular codebase backed by 19 unit tests to ensure data quality and pipeline reliability.</li>
          </ul>
        </div>
      </div>

      <div class="tl-item reveal">
        <div class="tl-dot"></div>
        <div class="tl-card">
          <div class="tl-top">
            <div class="tl-role">Hospitality Operations <span style="color:var(--text-faint);font-weight:400;">@</span> <span class="tl-company">Hotel Management Practicum</span></div>
            <div class="tl-dates">2018 — 2023</div>
          </div>
          <ul class="tl-achv">
            <li>Developed strong interpersonal, team coordination, and cross-functional communication skills across guest-facing operations.</li>
            <li>Practiced consistent time management and problem-solving in fast-paced, deadline-driven environments.</li>
            <li>Built a client-centric mindset that now directly informs how I approach stakeholder needs in data projects.</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ============ PROJECTS ============ -->
<section class="about" id="projects">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">Selected Work</div>
      <h2>Projects that put data to work.</h2>
      <p>Real pipelines, real KPIs, real forecasting — built end-to-end from raw data to actionable insight.</p>
    </div>

    <div class="projects-grid">
      <div class="proj-card reveal">
        <div class="proj-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 3v18h18"/><path d="M18.7 8 13 13.7l-4-4L3 16"/></svg>
        </div>
        <h3>Real-Time Sales Performance Analytics Dashboard</h3>
        <p>A real-time sales analytics platform for retail businesses, processing 1,000+ transactions through an automated ETL pipeline. Includes 10 SQL-driven KPIs and a 4-model ensemble forecasting system covering revenue, profitability, and customer demographics — all backed by 19 unit tests for data quality.</p>
        <div class="proj-tags">
          <span class="proj-tag">Python</span>
          <span class="proj-tag">SQLite</span>
          <span class="proj-tag">Tableau</span>
          <span class="proj-tag">ETL</span>
        </div>
        <div class="proj-stats">
          <span><strong>1,000+</strong> transactions</span>
          <span><strong>10</strong> KPIs</span>
          <span><strong>19</strong> unit tests</span>
        </div>
        <a class="proj-link" href="https://github.com/chefmaahi/retail_sales_project" target="_blank" rel="noopener">
          View on GitHub
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M7 17 17 7M7 7h10v10"/></svg>
        </a>
      </div>

      <div class="proj-card reveal">
        <div class="proj-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
        </div>
        <h3>BI Foundations: Power BI &amp; Tableau</h3>
        <p>Coursework-driven dashboard builds covering data modeling, DAX fundamentals, and interactive visualization design — forming the foundation behind every dashboard in this portfolio.</p>
        <div class="proj-tags">
          <span class="proj-tag">Power BI</span>
          <span class="proj-tag">Tableau</span>
          <span class="proj-tag">Data Viz</span>
        </div>
        <div class="proj-stats">
          <span><strong>Microsoft</strong> certified</span>
          <span><strong>Nxtwave</strong> certified</span>
        </div>
        <a class="proj-link" href="https://github.com/chefmaahi" target="_blank" rel="noopener">
          Explore GitHub profile
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M7 17 17 7M7 7h10v10"/></svg>
        </a>
      </div>

      <div class="proj-card reveal">
        <div class="proj-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2 2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
        </div>
        <h3>Cloud &amp; Database Fundamentals</h3>
        <p>Applied learning in AWS cloud services and Linux systems alongside MySQL database design — the infrastructure layer supporting scalable, production-style data pipelines.</p>
        <div class="proj-tags">
          <span class="proj-tag">AWS</span>
          <span class="proj-tag">Linux</span>
          <span class="proj-tag">MySQL</span>
        </div>
        <div class="proj-stats">
          <span><strong>Chandigarh University</strong> coursework</span>
        </div>
        <a class="proj-link" href="https://github.com/chefmaahi" target="_blank" rel="noopener">
          See more repos
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M7 17 17 7M7 7h10v10"/></svg>
        </a>
      </div>
    </div>
  </div>
</section>

<!-- ============ SKILLS ============ -->
<section id="skills">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">Toolbox</div>
      <h2>Skills, extracted from real work.</h2>
      <p>Pulled directly from coursework, certifications, and hands-on project experience.</p>
    </div>

    <div class="skills-wrap">
      <div class="skill-row reveal">
        <div class="skill-cat">Languages</div>
        <div class="skill-pills">
          <span class="skill-pill">Python</span>
          <span class="skill-pill">SQL / MySQL</span>
          <span class="skill-pill">HTML</span>
          <span class="skill-pill">CSS</span>
        </div>
      </div>
      <div class="skill-row reveal">
        <div class="skill-cat">Data &amp; BI</div>
        <div class="skill-pills">
          <span class="skill-pill">Power BI</span>
          <span class="skill-pill">Tableau</span>
          <span class="skill-pill">Data Visualization</span>
          <span class="skill-pill">ETL Pipelines</span>
          <span class="skill-pill">Forecasting Models</span>
        </div>
      </div>
      <div class="skill-row reveal">
        <div class="skill-cat">Cloud &amp; OS</div>
        <div class="skill-pills">
          <span class="skill-pill">AWS</span>
          <span class="skill-pill">Linux</span>
        </div>
      </div>
      <div class="skill-row reveal">
        <div class="skill-cat">Frameworks</div>
        <div class="skill-pills">
          <span class="skill-pill">Bootstrap</span>
          <span class="skill-pill">Flexbox</span>
          <span class="skill-pill">SQLite</span>
        </div>
      </div>
      <div class="skill-row reveal">
        <div class="skill-cat">Productivity</div>
        <div class="skill-pills">
          <span class="skill-pill">MS Excel</span>
          <span class="skill-pill">MS Word</span>
          <span class="skill-pill">PowerPoint</span>
        </div>
      </div>
      <div class="skill-row reveal">
        <div class="skill-cat">Core Strengths</div>
        <div class="skill-pills">
          <span class="skill-pill">Analytical Thinking</span>
          <span class="skill-pill">Cross-Team Collaboration</span>
          <span class="skill-pill">Multilingual Communication</span>
          <span class="skill-pill">Adaptability</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ============ EDUCATION ============ -->
<section class="about" id="education">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">Education</div>
      <h2>Academic foundation.</h2>
      <p>A path through hospitality and computer applications, culminating in a specialization in data analytics.</p>
    </div>

    <div class="edu-grid">
      <div class="edu-card reveal">
        <div class="edu-top">
          <div class="edu-degree">Master of Computer Applications (MCA) — Data Analytics</div>
          <div class="edu-score">82%</div>
        </div>
        <div class="edu-school">Chandigarh University, Punjab</div>
        <div class="edu-year">Jul 2024 — May 2026 (Expected)</div>
      </div>

      <div class="edu-card reveal">
        <div class="edu-top">
          <div class="edu-degree">B.Sc. in Hotel Management</div>
          <div class="edu-score">80.8%</div>
        </div>
        <div class="edu-school">Chennai's Amrita International Institute of Hotel Management, Bangalore</div>
        <div class="edu-year">Jul 2021 — May 2023</div>
      </div>

      <div class="edu-card reveal">
        <div class="edu-top">
          <div class="edu-degree">3-Year Diploma in Hotel Management</div>
          <div class="edu-score">77.52%</div>
        </div>
        <div class="edu-school">Guardian Angel Institute of Hotel Management &amp; Catering Technology, Goa</div>
        <div class="edu-year">Jul 2018 — May 2021</div>
      </div>

      <div class="edu-card reveal">
        <div class="edu-top">
          <div class="edu-degree">Intermediate — Science (PCM)</div>
          <div class="edu-score">58.9%</div>
        </div>
        <div class="edu-school">Sri Gayatri Junior College, Kadapa, Andhra Pradesh</div>
        <div class="edu-year">Jun 2016 — Apr 2018</div>
      </div>
    </div>
  </div>
</section>

<!-- ============ CONTACT ============ -->
<section id="contact">
  <div class="wrap">
    <div class="contact-section reveal">
      <div class="contact-inner">
        <div class="eyebrow" style="color:rgba(255,255,255,.85);"><span style="display:inline-block;width:7px;height:7px;border-radius:50%;background:#fff;box-shadow:0 0 0 4px rgba(255,255,255,.25);"></span>Open to opportunities</div>
        <h2>Let's build something data-driven.</h2>
        <p>I'm actively looking for opportunities in data analysis and BI. Reach out — I'd love to talk about how I can help your team make sense of its data.</p>
        <div class="contact-actions">
          <a href="mailto:thechefmaahi@gmail.com" class="btn btn-primary">Email me</a>
          <a href="tel:+919182871498" class="btn btn-secondary">Call / WhatsApp</a>
        </div>
        <div class="contact-socials">
          <a class="icon-link" href="https://www.linkedin.com/in/gurram-mahadev-kishan/" target="_blank" rel="noopener" aria-label="LinkedIn">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-4 0v7h-4V8h4v1.5A5 5 0 0 1 16 8z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          </a>
          <a class="icon-link" href="https://github.com/chefmaahi" target="_blank" rel="noopener" aria-label="GitHub">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
          </a>
          <a class="icon-link" href="mailto:thechefmaahi@gmail.com" target="_blank" rel="noopener" aria-label="Email">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16v16H4z"/><path d="m22 6-10 7L2 6"/></svg>
          </a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ============ FOOTER ============ -->
<footer>
  <div class="wrap footer-inner">
    <p>© 2026 Mahadev Kishan Gurram. Built with intent.</p>
    <div class="footer-links">
      <a href="mailto:thechefmaahi@gmail.com">Email</a>
      <a href="https://www.linkedin.com/in/gurram-mahadev-kishan/" target="_blank" rel="noopener">LinkedIn</a>
      <a href="https://github.com/chefmaahi" target="_blank" rel="noopener">GitHub</a>
    </div>
  </div>
</footer>

<button class="to-top" id="toTop" aria-label="Back to top">
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 19V5M5 12l7-7 7 7"/></svg>
</button>

<script>
(function(){
  "use strict";

  /* ---- Theme toggle ---- */
  var root = document.body;
  var toggle = document.getElementById('themeToggle');
  var stored = null;
  try{ stored = window.localStorage ? null : null; }catch(e){}
  // Use in-memory state only (no localStorage per artifact constraints);
  // default to system preference on load.
  var prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
  if(prefersDark){ root.setAttribute('data-theme','dark'); }

  toggle.addEventListener('click', function(){
    var current = root.getAttribute('data-theme');
    root.setAttribute('data-theme', current === 'dark' ? 'light' : 'dark');
  });

  /* ---- Sticky navbar state ---- */
  var nav = document.getElementById('navbar');
  function onScroll(){
    if(window.scrollY > 40){ nav.classList.add('scrolled'); } else { nav.classList.remove('scrolled'); }
    var toTopBtn = document.getElementById('toTop');
    if(window.scrollY > 600){ toTopBtn.classList.add('show'); } else { toTopBtn.classList.remove('show'); }
  }
  window.addEventListener('scroll', onScroll, {passive:true});
  onScroll();

  /* ---- Back to top ---- */
  document.getElementById('toTop').addEventListener('click', function(){
    window.scrollTo({top:0, behavior:'smooth'});
  });

  /* ---- Mobile menu ---- */
  var burger = document.getElementById('navBurger');
  var mobileMenu = document.getElementById('mobileMenu');
  burger.addEventListener('click', function(){
    burger.classList.toggle('open');
    mobileMenu.classList.toggle('open');
  });
  mobileMenu.querySelectorAll('a').forEach(function(a){
    a.addEventListener('click', function(){
      burger.classList.remove('open');
      mobileMenu.classList.remove('open');
    });
  });

  /* ---- Scroll reveal animations ---- */
  var revealEls = document.querySelectorAll('.reveal');
  if('IntersectionObserver' in window){
    var io = new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if(entry.isIntersecting){
          entry.target.classList.add('in');
          io.unobserve(entry.target);
        }
      });
    }, {threshold:0.12, rootMargin:'0px 0px -40px 0px'});
    revealEls.forEach(function(el){ io.observe(el); });
  } else {
    revealEls.forEach(function(el){ el.classList.add('in'); });
  }

  /* ---- Smooth scroll for in-page anchors (with navbar offset) ---- */
  document.querySelectorAll('a[href^="#"]').forEach(function(link){
    link.addEventListener('click', function(e){
      var id = this.getAttribute('href');
      if(id.length < 2) return;
      var target = document.querySelector(id);
      if(target){
        e.preventDefault();
        var offset = 70;
        var top = target.getBoundingClientRect().top + window.pageYOffset - offset;
        window.scrollTo({top:top, behavior:'smooth'});
      }
    });
  });
})();
</script>
</body>
</html>
