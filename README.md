[RMIEC_Ecosystem_Final.html](https://github.com/user-attachments/files/27729419/RMIEC_Ecosystem_Final.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RMIEC — Integrated Workforce Development Ecosystem</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,300&family=DM+Serif+Display:ital@0;1&display=swap" rel="stylesheet">
<style>
  :root {
    --purple-50:#EEEDFE;--purple-100:#CECBF6;--purple-600:#534AB7;--purple-800:#3C3489;--purple-900:#26215C;
    --teal-50:#E1F5EE;--teal-100:#9FE1CB;--teal-600:#0F6E56;--teal-800:#085041;
    --amber-50:#FAEEDA;--amber-100:#FAC775;--amber-600:#854F0B;--amber-800:#633806;
    --gray-50:#F1EFE8;--gray-100:#D3D1C7;--gray-400:#888780;--gray-800:#444441;
    --bg:#FAFAF8;--surface:#FFFFFF;--border:rgba(0,0,0,0.09);--border-md:rgba(0,0,0,0.15);
    --text-primary:#1a1a18;--text-secondary:#5a5a56;--text-muted:#8a8a84;
    --radius-sm:6px;--radius-md:10px;--radius-lg:14px;--radius-xl:20px;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text-primary);}

  /* HERO */
  .hero{background:var(--purple-900);padding:0;position:relative;overflow:hidden;}
  .hero::before{content:'';position:absolute;top:-60px;right:-60px;width:320px;height:320px;border-radius:50%;background:rgba(255,255,255,0.04);}
  .hero::after{content:'';position:absolute;bottom:-80px;left:30%;width:200px;height:200px;border-radius:50%;background:rgba(255,255,255,0.03);}
  .hero-top{display:flex;align-items:center;justify-content:space-between;gap:1.5rem;padding:1.5rem 2.5rem 0;flex-wrap:wrap;}
  .hero-logo-wrap{background:#fff;border-radius:var(--radius-lg);padding:.6rem 1.1rem;display:inline-flex;align-items:center;}
  .hero-logo-wrap img{height:52px;width:auto;display:block;}
  .hero-contact{display:flex;flex-direction:column;gap:4px;text-align:right;}
  .hero-contact a{font-size:12px;color:rgba(255,255,255,0.6);text-decoration:none;transition:color .12s;}
  .hero-contact a:hover{color:#fff;}
  .hero-body{padding:1.5rem 2.5rem 2.25rem;}
  .hero-eyebrow{font-size:11px;font-weight:500;letter-spacing:.12em;text-transform:uppercase;color:var(--purple-100);margin-bottom:.6rem;}
  .hero-title{font-family:'DM Serif Display',serif;font-size:clamp(1.75rem,4vw,2.5rem);color:#fff;line-height:1.2;margin-bottom:.6rem;max-width:620px;}
  .hero-title em{font-style:italic;color:var(--purple-100);}
  .hero-sub{font-size:13.5px;color:rgba(255,255,255,0.65);line-height:1.6;max-width:560px;font-weight:300;}
  .hero-meta{display:flex;gap:20px;flex-wrap:wrap;margin-top:1.5rem;}
  .hero-stat{display:flex;flex-direction:column;border-left:1px solid rgba(255,255,255,0.15);padding-left:14px;}
  .hero-stat-num{font-size:22px;font-weight:500;color:#fff;}
  .hero-stat-label{font-size:11px;color:rgba(255,255,255,0.5);margin-top:1px;}

  /* NAV */
  .nav-bar{background:var(--surface);border-bottom:1px solid var(--border);padding:0 2rem;display:flex;align-items:center;position:sticky;top:0;z-index:100;overflow-x:auto;gap:0;}
  .nav-tab{font-size:13px;font-weight:400;color:var(--text-muted);padding:.9rem 1rem;border-bottom:2px solid transparent;cursor:pointer;white-space:nowrap;background:none;border-top:none;border-left:none;border-right:none;transition:color .15s,border-color .15s;font-family:'DM Sans',sans-serif;}
  .nav-tab:hover{color:var(--text-secondary);}
  .nav-tab.active{color:var(--purple-800);border-bottom:2px solid var(--purple-600);font-weight:500;}

  /* MAIN */
  .main{padding:2.5rem;max-width:1100px;margin:0 auto;}
  .section{display:none;}
  .section.active{display:block;}
  .section-header{margin-bottom:1.75rem;}
  .section-label{font-size:11px;font-weight:500;letter-spacing:.1em;text-transform:uppercase;color:var(--text-muted);margin-bottom:.4rem;}
  .section-title{font-family:'DM Serif Display',serif;font-size:1.5rem;color:var(--text-primary);}
  .section-desc{font-size:14px;color:var(--text-secondary);line-height:1.6;margin-top:.35rem;max-width:680px;}

  /* PILLARS */
  .pillars{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;margin-bottom:1.5rem;}
  .pillar-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-xl);padding:1.5rem 1.35rem 1.25rem;cursor:pointer;transition:all .18s;position:relative;overflow:hidden;}
  .pillar-card:hover{border-color:var(--border-md);transform:translateY(-1px);box-shadow:0 4px 16px rgba(0,0,0,0.06);}
  .pillar-card.active{border-width:1.5px;}
  .pillar-card .bar{position:absolute;top:0;left:0;right:0;height:4px;border-radius:var(--radius-xl) var(--radius-xl) 0 0;}
  .p1 .bar{background:linear-gradient(90deg,var(--purple-600),var(--purple-100));}
  .p2 .bar{background:linear-gradient(90deg,var(--teal-600),var(--teal-100));}
  .p3 .bar{background:linear-gradient(90deg,var(--amber-600),var(--amber-100));}
  .p1.active{border-color:var(--purple-600);background:#FAFAFF;}
  .p2.active{border-color:var(--teal-600);background:#F7FDFB;}
  .p3.active{border-color:var(--amber-600);background:#FFFCF7;}
  .pillar-icon{font-size:26px;margin-bottom:.65rem;display:block;}
  .pillar-num{font-size:10px;font-weight:600;letter-spacing:.1em;text-transform:uppercase;margin-bottom:.3rem;}
  .p1 .pillar-num{color:var(--purple-600);}
  .p2 .pillar-num{color:var(--teal-600);}
  .p3 .pillar-num{color:var(--amber-600);}
  .pillar-title{font-size:15px;font-weight:500;line-height:1.3;margin-bottom:.4rem;}
  .pillar-sub{font-size:12.5px;color:var(--text-secondary);line-height:1.5;}
  .pillar-outcome{margin-top:.9rem;font-size:12px;font-weight:500;padding:.4rem .7rem;border-radius:20px;display:inline-block;}
  .p1 .pillar-outcome{background:var(--purple-50);color:var(--purple-800);}
  .p2 .pillar-outcome{background:var(--teal-50);color:var(--teal-800);}
  .p3 .pillar-outcome{background:var(--amber-50);color:var(--amber-800);}

  .streams-wrap{display:none;margin-bottom:1rem;}
  .streams-wrap.show{display:block;}
  .streams-intro{font-size:13.5px;color:var(--text-secondary);margin-bottom:1rem;line-height:1.6;}
  .streams-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:12px;}
  .stream-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-lg);padding:1rem 1.1rem;}
  .stream-badge{font-size:10px;font-weight:600;letter-spacing:.08em;text-transform:uppercase;padding:2px 8px;border-radius:20px;display:inline-block;margin-bottom:.5rem;}
  .sb-purple{background:var(--purple-50);color:var(--purple-800);}
  .sb-teal{background:var(--teal-50);color:var(--teal-800);}
  .sb-amber{background:var(--amber-50);color:var(--amber-800);}
  .sb-gray{background:var(--gray-50);color:var(--gray-800);}
  .stream-name{font-size:13px;font-weight:500;margin-bottom:.6rem;}
  .prog-list{list-style:none;}
  .prog-list li{font-size:12px;color:var(--text-secondary);padding:3px 0;display:flex;gap:6px;line-height:1.35;}
  .prog-list li::before{content:"→";font-size:11px;color:var(--text-muted);flex-shrink:0;margin-top:1px;}

  /* SESSION NUMBERED LIST */
  .session-list{list-style:none;margin-top:.5rem;}
  .session-item{display:flex;gap:8px;padding:4px 0;border-bottom:1px solid var(--border);align-items:flex-start;}
  .session-item:last-child{border-bottom:none;}
  .session-num{font-size:10px;font-weight:600;color:var(--text-muted);min-width:18px;margin-top:2px;flex-shrink:0;}
  .session-text{font-size:12px;color:var(--text-secondary);line-height:1.4;}
  .session-meta{display:flex;flex-wrap:wrap;gap:5px;margin-top:.65rem;}
  .meta-tag{font-size:10.5px;font-weight:500;padding:3px 8px;border-radius:20px;display:inline-flex;align-items:center;gap:3px;}
  .mt-purple{background:var(--purple-50);color:var(--purple-800);}
  .mt-teal{background:var(--teal-50);color:var(--teal-800);}
  .mt-amber{background:var(--amber-50);color:var(--amber-800);}
  .mt-gray{background:var(--gray-50);color:var(--gray-800);}

  hr{border:none;border-top:1px solid var(--border);margin:2.5rem 0;}

  /* PIPELINES */
  .pipeline-grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:16px;}
  .pipeline-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-xl);padding:1.25rem;position:relative;overflow:hidden;}
  .pipeline-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;}
  .pl-1::before{background:var(--purple-600);}
  .pl-2::before{background:var(--teal-600);}
  .pl-3::before{background:var(--amber-600);}
  .pipe-title{font-size:13.5px;font-weight:500;margin-bottom:1rem;}
  .pipe-step{display:flex;gap:10px;align-items:flex-start;padding:7px 0;border-bottom:1px solid var(--border);}
  .pipe-step:last-child{border-bottom:none;}
  .step-bubble{width:20px;height:20px;border-radius:50%;font-size:10px;font-weight:600;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px;}
  .pl-1 .step-bubble{background:var(--purple-50);color:var(--purple-800);}
  .pl-2 .step-bubble{background:var(--teal-50);color:var(--teal-800);}
  .pl-3 .step-bubble{background:var(--amber-50);color:var(--amber-800);}
  .step-body strong{font-size:12.5px;font-weight:500;display:block;line-height:1.3;}
  .step-body span{font-size:11px;color:var(--text-muted);}

  /* SECTORS */
  .sector-legend{display:flex;gap:18px;flex-wrap:wrap;margin-bottom:1rem;font-size:12px;color:var(--text-muted);}
  .legend-dot{width:8px;height:8px;border-radius:50%;display:inline-block;margin-right:5px;vertical-align:middle;}
  .tags-wrap{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:2rem;}
  .sector-tag{font-size:12px;font-weight:500;padding:5px 12px;border-radius:20px;border:1px solid;}
  .st-purple{background:var(--purple-50);color:var(--purple-800);border-color:var(--purple-100);}
  .st-teal{background:var(--teal-50);color:var(--teal-800);border-color:var(--teal-100);}
  .st-amber{background:var(--amber-50);color:var(--amber-800);border-color:var(--amber-100);}
  .st-gray{background:var(--gray-50);color:var(--gray-800);border-color:var(--gray-100);}

  /* GAPS */
  .gap-tabs{display:flex;gap:6px;margin-bottom:1rem;flex-wrap:wrap;}
  .gap-tab{font-size:12px;font-weight:500;padding:5px 14px;border-radius:20px;border:1px solid var(--border-md);background:transparent;color:var(--text-secondary);cursor:pointer;transition:all .12s;font-family:'DM Sans',sans-serif;}
  .gap-tab.on{background:var(--text-primary);color:#fff;border-color:var(--text-primary);}
  .gap-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:12px;}
  .gap-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-lg);padding:1rem;}
  .gap-name{font-size:13px;font-weight:500;margin-bottom:.6rem;padding-bottom:.5rem;border-bottom:1px solid var(--border);}
  .gap-item{font-size:12px;color:var(--text-secondary);padding:3px 0;display:flex;gap:6px;line-height:1.4;}
  .gap-item::before{content:"–";color:var(--text-muted);flex-shrink:0;}

  /* SOPs */
  .two-col{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:16px;margin-bottom:2rem;}
  .sop-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-lg);padding:1.1rem;}
  .sop-title{font-size:13px;font-weight:500;margin-bottom:.5rem;display:flex;align-items:center;gap:8px;}
  .sop-num{width:22px;height:22px;border-radius:6px;background:var(--gray-50);color:var(--gray-800);font-size:11px;font-weight:600;display:flex;align-items:center;justify-content:center;}
  .sop-items{list-style:none;}
  .sop-items li{font-size:12px;color:var(--text-secondary);padding:2px 0;display:flex;gap:6px;}
  .sop-items li::before{content:"·";color:var(--text-muted);}

  /* METRICS */
  .metrics-grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:12px;}
  .metric-group{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-lg);padding:1.1rem;}
  .metric-group-title{font-size:12px;font-weight:600;margin-bottom:.7rem;text-transform:uppercase;letter-spacing:.06em;}
  .mg-1 .metric-group-title{color:var(--purple-600);}
  .mg-2 .metric-group-title{color:var(--teal-600);}
  .mg-3 .metric-group-title{color:var(--amber-600);}
  .metric-item{font-size:12px;color:var(--text-secondary);padding:3px 0;display:flex;gap:6px;line-height:1.35;}
  .metric-item::before{content:"↗";font-size:11px;color:var(--text-muted);flex-shrink:0;}

  /* VALUE PROPS */
  .vp-grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px;}
  .vp-card{border-radius:var(--radius-xl);padding:1.5rem;}
  .vp-1{background:var(--purple-900);}
  .vp-2{background:var(--teal-800);}
  .vp-3{background:var(--amber-800);}
  .vp-for{font-size:10px;font-weight:600;letter-spacing:.12em;text-transform:uppercase;margin-bottom:.5rem;opacity:.65;color:#fff;}
  .vp-title{font-family:'DM Serif Display',serif;font-size:1.1rem;color:#fff;margin-bottom:.75rem;line-height:1.3;}
  .vp-quote{font-size:12.5px;color:rgba(255,255,255,0.75);line-height:1.6;margin-bottom:1rem;font-weight:300;}
  .vp-values{display:flex;flex-wrap:wrap;gap:5px;}
  .vp-tag{font-size:11px;font-weight:500;padding:3px 9px;border-radius:20px;background:rgba(255,255,255,0.15);color:rgba(255,255,255,0.9);}
  .strat-box{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-xl);padding:1.75rem 2rem;margin-top:1.5rem;}
  .strat-box p{font-size:13.5px;color:var(--text-secondary);line-height:1.7;}
  .strat-box strong{font-weight:500;color:var(--text-primary);}

  /* PROGRAM DETAIL CARD */
  .prog-detail{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-xl);padding:1.35rem 1.5rem;margin-bottom:1.25rem;}
  .prog-detail-header{display:flex;align-items:flex-start;justify-content:space-between;gap:1rem;margin-bottom:.85rem;flex-wrap:wrap;}
  .prog-detail-title{font-size:15px;font-weight:500;color:var(--text-primary);}
  .prog-detail-sub{font-size:12px;color:var(--text-muted);margin-top:2px;}

  /* FOOTER */
  .page-footer{background:var(--gray-50);border-top:1px solid var(--border);padding:1.25rem 2.5rem;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:12px;margin-top:2rem;}
  .footer-org{font-size:13px;font-weight:500;color:var(--text-secondary);}
  .footer-links{display:flex;gap:16px;}
  .footer-links a{font-size:11px;color:var(--text-muted);text-decoration:none;}
  .footer-links a:hover{color:var(--text-primary);}

  /* PRINT */
  .print-btn{position:fixed;bottom:24px;right:24px;background:var(--purple-800);color:#fff;border:none;border-radius:40px;padding:.65rem 1.2rem;font-size:13px;font-weight:500;cursor:pointer;font-family:'DM Sans',sans-serif;box-shadow:0 4px 16px rgba(60,52,137,0.35);transition:transform .12s,background .12s;display:flex;align-items:center;gap:6px;z-index:200;}
  .print-btn:hover{transform:translateY(-1px);background:var(--purple-900);}

  @media(max-width:680px){
    .pillars,.pipeline-grid,.vp-grid,.metrics-grid,.two-col{grid-template-columns:1fr;}
    .main{padding:1.5rem;}
    .hero-body{padding:1.25rem 1.5rem 1.75rem;}
    .hero-top{padding:1.25rem 1.5rem 0;}
    .nav-bar{padding:0 1rem;}
  }
  @media print{
    .nav-bar,.print-btn{display:none;}
    .section{display:block!important;}
    body{background:white;}
    .hero{background:#26215C;-webkit-print-color-adjust:exact;print-color-adjust:exact;}
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-top">
    <div class="hero-logo-wrap">
      <img src="data:image/jpeg;base64,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AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD/9k=" alt="RMIEC — Rural Manitoba Immigrant Employment Council">
    </div>
    <div class="hero-contact">
      <a href="mailto:info@rmiec.ca">✉ info@rmiec.ca</a>
      <a href="https://rmiec.ca/" target="_blank">🌐 rmiec.ca</a>
    </div>
  </div>
  <div class="hero-body">
    <div class="hero-eyebrow">West Man Immigrant Services</div>
    <h1 class="hero-title">Integrated Workforce<br><em>Development Ecosystem</em></h1>
    <p class="hero-sub">Connecting immigrant talent, employers, and communities through training, networking, and workforce development strategies that strengthen regional economic growth.</p>
    <div class="hero-meta">
      <div class="hero-stat"><span class="hero-stat-num">3</span><span class="hero-stat-label">Strategic Pillars</span></div>
      <div class="hero-stat"><span class="hero-stat-num">15+</span><span class="hero-stat-label">Industry Sectors</span></div>
      <div class="hero-stat"><span class="hero-stat-num">30+</span><span class="hero-stat-label">Programs & Sessions</span></div>
      <div class="hero-stat"><span class="hero-stat-num">3</span><span class="hero-stat-label">Talent Pipelines</span></div>
    </div>
  </div>
</div>

<!-- NAV -->
<nav class="nav-bar">
  <button class="nav-tab active" onclick="showSection('overview',this)">Overview</button>
  <button class="nav-tab" onclick="showSection('programs',this)">Program Menu</button>
  <button class="nav-tab" onclick="showSection('pipelines',this)">Talent Pipelines</button>
  <button class="nav-tab" onclick="showSection('sectors',this)">Sectors</button>
  <button class="nav-tab" onclick="showSection('gaps',this)">Gaps & Priorities</button>
  <button class="nav-tab" onclick="showSection('sops',this)">SOPs & Team</button>
  <button class="nav-tab" onclick="showSection('metrics',this)">Metrics</button>
  <button class="nav-tab" onclick="showSection('values',this)">Value Propositions</button>
</nav>

<div class="main">

<!-- ── OVERVIEW ── -->
<div class="section active" id="s-overview">
  <div class="section-header">
    <div class="section-label">Strategic Framework</div>
    <div class="section-title">Three pillars, one connected system</div>
    <div class="section-desc">Click any pillar to explore its program streams. Each pillar serves a distinct audience but feeds into the same ecosystem.</div>
  </div>
  <div class="pillars">
    <div class="pillar-card p1 active" id="pc-1" onclick="togglePillar(1)">
      <div class="bar"></div><span class="pillar-icon">🎓</span>
      <div class="pillar-num">Pillar 1</div>
      <div class="pillar-title">Job Seeker Development</div>
      <div class="pillar-sub">Prepare immigrant talent to successfully enter, adapt, grow, and stay in the Canadian workforce.</div>
      <div class="pillar-outcome">→ Job-ready, employer-connected talent</div>
    </div>
    <div class="pillar-card p2" id="pc-2" onclick="togglePillar(2)">
      <div class="bar"></div><span class="pillar-icon">🏢</span>
      <div class="pillar-num">Pillar 2</div>
      <div class="pillar-title">Employer Workforce Development</div>
      <div class="pillar-sub">Help employers attract, hire, integrate, retain, and grow immigrant talent successfully.</div>
      <div class="pillar-outcome">→ Newcomer-ready workplaces</div>
    </div>
    <div class="pillar-card p3" id="pc-3" onclick="togglePillar(3)">
      <div class="bar"></div><span class="pillar-icon">🌐</span>
      <div class="pillar-num">Pillar 3</div>
      <div class="pillar-title">Community & Systems Development</div>
      <div class="pillar-sub">Strengthen partnerships between employers, institutions, municipalities, and communities.</div>
      <div class="pillar-outcome">→ Long-term workforce sustainability</div>
    </div>
  </div>
  <div class="streams-wrap show" id="sw-1">
    <div class="streams-intro">Four program streams build a complete journey — from workplace readiness through to long-term career growth.</div>
    <div class="streams-grid">
      <div class="stream-card"><span class="stream-badge sb-purple">Stream 1</span><div class="stream-name">Workplace Readiness</div><ul class="prog-list"><li>Job Seeker Training (weekly, Wed online)</li><li>Canadian hiring expectations</li><li>Interview skills & networking</li><li>Workplace communication</li></ul></div>
      <div class="stream-card"><span class="stream-badge sb-purple">Stream 2</span><div class="stream-name">Sector Pathways</div><ul class="prog-list"><li>Industry Connect (15 sectors, Tue)</li><li>Healthcare, Trades, IT, Childcare</li><li>Manufacturing, Logistics, Agriculture</li><li>AI, Cybersecurity, Cloud Computing</li></ul></div>
      <div class="stream-card"><span class="stream-badge sb-purple">Stream 3</span><div class="stream-name">Career Advancement</div><ul class="prog-list"><li>Credential recognition support</li><li>Professional branding</li><li>Licensing navigation</li><li>Connector Program (mentorship)</li></ul></div>
      <div class="stream-card"><span class="stream-badge sb-purple">Stream 4</span><div class="stream-name">Community Integration</div><ul class="prog-list"><li>Canoo Community Integration</li><li>Volunteer pathways</li><li>Networking supports</li><li>Social & family integration</li></ul></div>
    </div>
  </div>
  <div class="streams-wrap" id="sw-2">
    <div class="streams-intro">Three streams move employers from first awareness through to long-term workforce partnership.</div>
    <div class="streams-grid">
      <div class="stream-card"><span class="stream-badge sb-teal">Stream 1</span><div class="stream-name">Inclusion & Retention</div><ul class="prog-list"><li>Intercultural Exchange (12 sessions, Wed in-person)</li><li>Force Migration Simulation (add-on)</li><li>Diverse team communication</li><li>Emotional intelligence training</li></ul></div>
      <div class="stream-card"><span class="stream-badge sb-teal">Stream 2</span><div class="stream-name">Recruitment & Hiring</div><ul class="prog-list"><li>Talent Match (bi-weekly, Thu 5–7pm)</li><li>Lunch & Learn (Tue & Thu, noon–1pm)</li><li>Interviewing across cultures</li><li>Hiring Without Barriers</li></ul></div>
      <div class="stream-card"><span class="stream-badge sb-teal">Stream 3</span><div class="stream-name">Workforce Sustainability</div><ul class="prog-list"><li>The Rural Playbook</li><li>Career pathways for immigrant talent</li><li>Employer Networking & Partnerships</li><li>Workforce retention planning</li></ul></div>
    </div>
  </div>
  <div class="streams-wrap" id="sw-3">
    <div class="streams-intro">Two streams align systems across sectors and grow regional workforce capacity.</div>
    <div class="streams-grid">
      <div class="stream-card"><span class="stream-badge sb-amber">Stream 1</span><div class="stream-name">Partnership Development</div><ul class="prog-list"><li>Focus Groups & Community Roundtables</li><li>Sector Advisory Discussions</li><li>Employer-community dialogues</li><li>Settlement collaboration</li></ul></div>
      <div class="stream-card"><span class="stream-badge sb-amber">Stream 2</span><div class="stream-name">Rural Workforce Development</div><ul class="prog-list"><li>Industry Connect (rural sessions)</li><li>Rural employer engagement</li><li>Community retention strategy</li><li>Regional workforce planning</li></ul></div>
    </div>
  </div>
</div>

<!-- ── PROGRAMS ── -->
<div class="section" id="s-programs">
  <div class="section-header">
    <div class="section-label">Training Library</div>
    <div class="section-title">Full program menu by audience</div>
    <div class="section-desc">Every program organized by who it serves and what it delivers. Use this as an internal reference, employer package, or onboarding resource.</div>
  </div>

  <div class="section-label" style="margin-bottom:.75rem;">Employer Programs</div>

  <!-- LUNCH & LEARN -->
  <div class="prog-detail">
    <div class="prog-detail-header">
      <div>
        <div class="prog-detail-title">Lunch &amp; Learn</div>
        <div class="prog-detail-sub">12-Session Series · Employer-Focused</div>
      </div>
      <div class="session-meta">
        <span class="meta-tag mt-teal">📅 Tuesdays &amp; Thursdays</span>
        <span class="meta-tag mt-teal">🕛 Noon – 1:00 PM</span>
        <span class="meta-tag mt-teal">💻 Online</span>
        <span class="meta-tag mt-gray">🎙 Facilitated by Ankit</span>
      </div>
    </div>
    <ul class="session-list">
      <li class="session-item"><span class="session-num">01</span><span class="session-text">Unlocking the Immigrant Talent Advantage</span></li>
      <li class="session-item"><span class="session-num">02</span><span class="session-text">Mental Health and Wellbeing in a Diverse Workforce</span></li>
      <li class="session-item"><span class="session-num">03</span><span class="session-text">Hiring Without Barriers: Inclusive Practices That Deliver</span></li>
      <li class="session-item"><span class="session-num">04</span><span class="session-text">Cracking the Code on Credentials &amp; Experience</span></li>
      <li class="session-item"><span class="session-num">05</span><span class="session-text">Interviewing Across Cultures with Confidence</span></li>
      <li class="session-item"><span class="session-num">06</span><span class="session-text">Immigration 101: What Employers Need to Know</span></li>
      <li class="session-item"><span class="session-num">07</span><span class="session-text">Onboarding Newcomers: The First 90 Days That Matter</span></li>
      <li class="session-item"><span class="session-num">08</span><span class="session-text">Language at Work: Support Without Sacrificing Productivity</span></li>
      <li class="session-item"><span class="session-num">09</span><span class="session-text">Retention Through Belonging: How to Make It Stick</span></li>
      <li class="session-item"><span class="session-num">10</span><span class="session-text">Growing From Within: Career Pathways for Immigrant Talent</span></li>
      <li class="session-item"><span class="session-num">11</span><span class="session-text">Strong Communities, Strong Workplaces: Partnerships That Work</span></li>
      <li class="session-item"><span class="session-num">12</span><span class="session-text">The Rural Playbook: Attracting and Keeping Newcomers</span></li>
    </ul>
  </div>

  <!-- INTERCULTURAL EXCHANGE -->
  <div class="prog-detail">
    <div class="prog-detail-header">
      <div>
        <div class="prog-detail-title">Intercultural Exchange</div>
        <div class="prog-detail-sub">12-Session Series · Employer-Focused</div>
      </div>
      <div class="session-meta">
        <span class="meta-tag mt-teal">📅 Wednesdays</span>
        <span class="meta-tag mt-teal">🕑 2:00 PM – 4:00 PM</span>
        <span class="meta-tag mt-teal">🏢 In-Person</span>
        <span class="meta-tag mt-gray">🎙 Enver or Ankit (TBD)</span>
      </div>
    </div>
    <ul class="session-list">
      <li class="session-item"><span class="session-num">01</span><span class="session-text">Understanding Newcomer Journeys</span></li>
      <li class="session-item"><span class="session-num">02</span><span class="session-text">Reducing Bias for Better Hiring</span></li>
      <li class="session-item"><span class="session-num">03</span><span class="session-text">Inclusive Hiring That Attracts Top Talent</span></li>
      <li class="session-item"><span class="session-num">04</span><span class="session-text">Recognizing Transferable Skills &amp; Global Experience</span></li>
      <li class="session-item"><span class="session-num">05</span><span class="session-text">Onboarding That Accelerates Newcomer Success</span></li>
      <li class="session-item"><span class="session-num">06</span><span class="session-text">Cultural Norms for Better Collaboration</span></li>
      <li class="session-item"><span class="session-num">07</span><span class="session-text">Cross-Cultural Communication Essentials</span></li>
      <li class="session-item"><span class="session-num">08</span><span class="session-text">Intercultural Emotional Intelligence</span></li>
      <li class="session-item"><span class="session-num">09</span><span class="session-text">Better Decisions Through Diverse Perspectives</span></li>
      <li class="session-item"><span class="session-num">10</span><span class="session-text">Culturally Aware Customer Service</span></li>
      <li class="session-item"><span class="session-num">11</span><span class="session-text">Giving Feedback in a Multicultural Workplace</span></li>
      <li class="session-item"><span class="session-num">12</span><span class="session-text">Stay &amp; Grow: The Power of Belonging</span></li>
    </ul>
  </div>

  <!-- TALENT MATCH -->
  <div class="prog-detail">
    <div class="prog-detail-header">
      <div>
        <div class="prog-detail-title">Talent Match</div>
        <div class="prog-detail-sub">Bi-Weekly Speed Networking · Employer &amp; Job Seeker</div>
      </div>
      <div class="session-meta">
        <span class="meta-tag mt-teal">📅 Bi-Weekly Thursdays</span>
        <span class="meta-tag mt-teal">🕔 Prep: 3–4 PM | Event: 5–7 PM</span>
        <span class="meta-tag mt-teal">💻 Online</span>
      </div>
    </div>
    <ul class="prog-list" style="margin-top:.5rem;">
      <li>Prep sessions: 1st &amp; 3rd Thursdays, 3:00–4:00 PM</li>
      <li>Main event: 2nd &amp; 4th Thursdays, 5:00–7:00 PM</li>
      <li>Pre-screened immigrant talent meets actively hiring employers</li>
      <li>Sector-specific breakout rooms &amp; speed networking rounds</li>
      <li>Follow-up referral pathways and hiring support</li>
    </ul>
  </div>

  <!-- FORCE MIGRATION -->
  <div class="prog-detail">
    <div class="prog-detail-header">
      <div>
        <div class="prog-detail-title">Force Migration Simulation</div>
        <div class="prog-detail-sub">Experiential Add-On · Employer-Focused</div>
      </div>
      <div class="session-meta">
        <span class="meta-tag mt-amber">Add-On to Intercultural Exchange</span>
      </div>
    </div>
    <ul class="prog-list" style="margin-top:.5rem;">
      <li>Sensitivity-driven experiential learning session</li>
      <li>Transforms perspectives and builds deep empathy</li>
      <li>Improves understanding of refugee and newcomer experiences</li>
      <li>Inspires inclusive leadership and workplace practices</li>
    </ul>
  </div>

  <hr>
  <div class="section-label" style="margin-bottom:.75rem;">Job Seeker Programs</div>
  <div class="streams-grid" style="margin-bottom:2rem;">
    <div class="stream-card"><span class="stream-badge sb-purple">Job Seeker Training</span><div class="stream-name">13-session series · Wed 4–4:30pm · Online</div><ul class="prog-list"><li>Pathways into Healthcare &amp; Trades</li><li>IT, Childcare, Manufacturing, Logistics</li><li>Office, Business, Marketing careers</li><li>Food, Agriculture &amp; Retail</li><li>Careers inside schools</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-purple">Industry Connect</span><div class="stream-name">15-week series · Tue 3–4:30pm · Online</div><ul class="prog-list"><li>Sector-specific employer breakout groups</li><li>AI, Cybersecurity, Cloud, Green Economy</li><li>Healthcare, Trades, Agriculture, Logistics</li><li>Builds labour market intelligence</li><li>Creates sector-specific talent databases</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-purple">Connector Program</span><div class="stream-name">Mentorship &amp; professional networking</div><ul class="prog-list"><li>Connects professionals with industry leaders</li><li>Builds mentorship relationships</li><li>Expands professional networks</li><li>Increases referral opportunities</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-purple">Canoo Integration</span><div class="stream-name">Community belonging support</div><ul class="prog-list"><li>Social integration &amp; cultural engagement</li><li>Reduces isolation, builds belonging</li><li>Partners with museums, parks, festivals</li><li>Supports family integration</li></ul></div>
  </div>

  <div class="section-label" style="margin-bottom:.75rem;">Community Programs</div>
  <div class="streams-grid">
    <div class="stream-card"><span class="stream-badge sb-amber">Focus Groups &amp; Roundtables</span><div class="stream-name">Stakeholder alignment sessions</div><ul class="prog-list"><li>Cross-sector employer-community dialogues</li><li>Sector Advisory Discussions</li><li>Settlement organization collaboration</li><li>Reduces service duplication</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-amber">Rural Workforce Integration</span><div class="stream-name">Regional development</div><ul class="prog-list"><li>Rural employer engagement sessions</li><li>Community retention strategy</li><li>Regional workforce planning</li><li>Labour market intelligence collection</li></ul></div>
  </div>
</div>

<!-- ── PIPELINES ── -->
<div class="section" id="s-pipelines">
  <div class="section-header">
    <div class="section-label">System Flow</div>
    <div class="section-title">How participants move through the system</div>
    <div class="section-desc">Three distinct pipelines — each with a clear start, structured progression, and measurable endpoint. They converge at the Talent Match event.</div>
  </div>
  <div class="pipeline-grid">
    <div class="pipeline-card pl-1">
      <div class="pipe-title" style="color:var(--purple-800);">🎓 Job seeker pipeline</div>
      <div class="pipe-step"><div class="step-bubble">1</div><div class="step-body"><strong>Awareness &amp; registration</strong><span>Outreach, intake, assessment</span></div></div>
      <div class="pipe-step"><div class="step-bubble">2</div><div class="step-body"><strong>Workplace readiness training</strong><span>Job Seeker Training program</span></div></div>
      <div class="pipe-step"><div class="step-bubble">3</div><div class="step-body"><strong>Sector-specific sessions</strong><span>Industry Connect, 15 sectors</span></div></div>
      <div class="pipe-step"><div class="step-bubble">4</div><div class="step-body"><strong>Employer preparation</strong><span>Talent Match prep sessions</span></div></div>
      <div class="pipe-step"><div class="step-bubble">5</div><div class="step-body"><strong>Employer connection</strong><span>Talent Match / Employer Meet-Up</span></div></div>
      <div class="pipe-step"><div class="step-bubble">6</div><div class="step-body"><strong>Retention &amp; career growth</strong><span>Mentorship, credential support</span></div></div>
    </div>
    <div class="pipeline-card pl-2">
      <div class="pipe-title" style="color:var(--teal-800);">🏢 Employer pipeline</div>
      <div class="pipe-step"><div class="step-bubble">1</div><div class="step-body"><strong>Awareness</strong><span>Lunch &amp; Learn, chambers, outreach</span></div></div>
      <div class="pipe-step"><div class="step-bubble">2</div><div class="step-body"><strong>Education</strong><span>Intercultural Exchange series</span></div></div>
      <div class="pipe-step"><div class="step-bubble">3</div><div class="step-body"><strong>Talent access</strong><span>Talent Match participation</span></div></div>
      <div class="pipe-step"><div class="step-bubble">4</div><div class="step-body"><strong>Hiring support</strong><span>Onboarding &amp; retention coaching</span></div></div>
      <div class="pipe-step"><div class="step-bubble">5</div><div class="step-body"><strong>Partnership</strong><span>Repeat hiring, referrals</span></div></div>
      <div class="pipe-step"><div class="step-bubble">6</div><div class="step-body"><strong>Employer champion</strong><span>Advisory council, mentorship</span></div></div>
    </div>
    <div class="pipeline-card pl-3">
      <div class="pipe-title" style="color:var(--amber-800);">🌐 Community pipeline</div>
      <div class="pipe-step"><div class="step-bubble">1</div><div class="step-body"><strong>Outreach</strong><span>Stakeholder &amp; sector mapping</span></div></div>
      <div class="pipe-step"><div class="step-bubble">2</div><div class="step-body"><strong>Engagement</strong><span>Focus groups, roundtables</span></div></div>
      <div class="pipe-step"><div class="step-bubble">3</div><div class="step-body"><strong>Collaborative planning</strong><span>Cross-sector alignment sessions</span></div></div>
      <div class="pipe-step"><div class="step-bubble">4</div><div class="step-body"><strong>Integration support</strong><span>Settlement &amp; cultural supports</span></div></div>
      <div class="pipe-step"><div class="step-bubble">5</div><div class="step-body"><strong>Regional retention</strong><span>Rural strategy &amp; housing referrals</span></div></div>
      <div class="pipe-step"><div class="step-bubble">6</div><div class="step-body"><strong>Workforce sustainability</strong><span>Long-term economic growth</span></div></div>
    </div>
  </div>
</div>

<!-- ── SECTORS ── -->
<div class="section" id="s-sectors">
  <div class="section-header">
    <div class="section-label">Labour Market Alignment</div>
    <div class="section-title">Priority workforce sectors</div>
    <div class="section-desc">Training is aligned to real labour shortages and employer demand — not general programming. Four priority tiers.</div>
  </div>
  <div class="sector-legend">
    <span><span class="legend-dot" style="background:var(--purple-600)"></span>Essential services</span>
    <span><span class="legend-dot" style="background:var(--teal-600)"></span>Skilled workforce</span>
    <span><span class="legend-dot" style="background:var(--amber-600)"></span>Knowledge economy</span>
    <span><span class="legend-dot" style="background:var(--gray-400)"></span>Regional economic drivers</span>
  </div>
  <div class="tags-wrap">
    <span class="sector-tag st-purple">Healthcare &amp; Medical</span>
    <span class="sector-tag st-purple">Childcare</span>
    <span class="sector-tag st-purple">Education &amp; Training</span>
    <span class="sector-tag st-purple">Community Services</span>
    <span class="sector-tag st-teal">Skilled Trades &amp; Construction</span>
    <span class="sector-tag st-teal">Manufacturing &amp; Production</span>
    <span class="sector-tag st-teal">Transportation</span>
    <span class="sector-tag st-teal">Logistics &amp; Warehousing</span>
    <span class="sector-tag st-amber">IT &amp; Software Development</span>
    <span class="sector-tag st-amber">Artificial Intelligence &amp; ML</span>
    <span class="sector-tag st-amber">Cybersecurity</span>
    <span class="sector-tag st-amber">Cloud Computing &amp; Data</span>
    <span class="sector-tag st-amber">Telehealth &amp; Health IT</span>
    <span class="sector-tag st-gray">Agriculture &amp; Agri-Food</span>
    <span class="sector-tag st-gray">Hospitality &amp; Tourism</span>
    <span class="sector-tag st-gray">Retail &amp; E-Commerce</span>
    <span class="sector-tag st-gray">Green Economy &amp; Sustainability</span>
    <span class="sector-tag st-gray">Finance &amp; Professional Services</span>
    <span class="sector-tag st-gray">Public Sector</span>
  </div>
  <div class="section-label" style="margin-bottom:.75rem;">Segmented talent pipeline</div>
  <div class="streams-grid">
    <div class="stream-card"><span class="stream-badge sb-purple">Entry-Level</span><div class="stream-name">Quick workforce entry</div><ul class="prog-list"><li>Customer service, Hospitality, Retail</li><li>Warehousing &amp; general labour</li><li>Focus: foundational workplace skills</li><li>Building Canadian experience</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-teal">Mid-Skilled</span><div class="stream-name">Career pathway development</div><ul class="prog-list"><li>Administrative, Trades support</li><li>Childcare, Healthcare support</li><li>Focus: certification &amp; employer matching</li><li>Logistics &amp; office roles</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-amber">Highly Skilled</span><div class="stream-name">Professional integration</div><ul class="prog-list"><li>Engineers, IT professionals</li><li>Healthcare, Finance, Educators</li><li>Focus: licensing pathways &amp; networking</li><li>Sector-specific employer partnerships</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-gray">Rural Pipeline</span><div class="stream-name">Regional workforce growth</div><ul class="prog-list"><li>Agriculture, Healthcare, Trades</li><li>Focus: community integration</li><li>Employer onboarding &amp; retention</li><li>Settlement organization partnerships</li></ul></div>
  </div>
</div>

<!-- ── GAPS ── -->
<div class="section" id="s-gaps">
  <div class="section-header">
    <div class="section-label">Next Phase Development</div>
    <div class="section-title">Identified gaps — what to build next</div>
    <div class="section-desc">Missing pieces needed to complete a fully operational, data-driven ecosystem. Select a category to explore.</div>
  </div>
  <div class="gap-tabs">
    <button class="gap-tab on" onclick="showGap('emp',this)">Employer side</button>
    <button class="gap-tab" onclick="showGap('js',this)">Job seeker side</button>
    <button class="gap-tab" onclick="showGap('org',this)">Organizational</button>
  </div>
  <div id="gg-emp" class="gap-grid">
    <div class="gap-card"><div class="gap-name">Follow-up system</div><div class="gap-item">Employer retention process &amp; CRM</div><div class="gap-item">Hiring outcome tracking</div><div class="gap-item">Employer satisfaction surveys</div><div class="gap-item">Employer engagement SOP</div></div>
    <div class="gap-card"><div class="gap-name">Onboarding package</div><div class="gap-item">Diversity hiring toolkit</div><div class="gap-item">Rural employer toolkit</div><div class="gap-item">Hiring incentive &amp; resource guide</div><div class="gap-item">Employer success stories</div></div>
    <div class="gap-card"><div class="gap-name">Advisory structure</div><div class="gap-item">Industry advisory council framework</div><div class="gap-item">Employer champion network</div><div class="gap-item">Metrics dashboard for employers</div><div class="gap-item">Repeat hiring pathway system</div></div>
  </div>
  <div id="gg-js" class="gap-grid" style="display:none;">
    <div class="gap-card"><div class="gap-name">Skills training gaps</div><div class="gap-item">Resume workshops</div><div class="gap-item">LinkedIn optimization sessions</div><div class="gap-item">Mock interview system</div><div class="gap-item">Soft skills training module</div></div>
    <div class="gap-card"><div class="gap-name">Support structures</div><div class="gap-item">Mentorship framework &amp; onboarding</div><div class="gap-item">Career coaching structure</div><div class="gap-item">Credential navigation guides</div><div class="gap-item">Digital literacy support</div></div>
    <div class="gap-card"><div class="gap-name">Tracking &amp; progression</div><div class="gap-item">Participant pathway tracking</div><div class="gap-item">Career stage &amp; milestone mapping</div><div class="gap-item">Employment outcome tracking</div><div class="gap-item">Volunteer pathway strategy</div></div>
  </div>
  <div id="gg-org" class="gap-grid" style="display:none;">
    <div class="gap-card"><div class="gap-name">Systems &amp; data</div><div class="gap-item">Centralized training calendar</div><div class="gap-item">CRM &amp; participant database</div><div class="gap-item">Survey &amp; evaluation system</div><div class="gap-item">KPI reporting framework</div></div>
    <div class="gap-card"><div class="gap-name">SOPs needed</div><div class="gap-item">Program planning &amp; delivery SOP</div><div class="gap-item">Employer engagement SOP</div><div class="gap-item">Job seeker intake SOP</div><div class="gap-item">Data &amp; outcome reporting SOP</div></div>
    <div class="gap-card"><div class="gap-name">Team development</div><div class="gap-item">Cross-training plan (all programs)</div><div class="gap-item">Peer presentation practice structure</div><div class="gap-item">Monthly collaborative planning</div><div class="gap-item">Shared training library</div></div>
  </div>
</div>

<!-- ── SOPs ── -->
<div class="section" id="s-sops">
  <div class="section-header">
    <div class="section-label">Operations</div>
    <div class="section-title">SOPs &amp; team development</div>
    <div class="section-desc">A layered set of standard operating procedures ensures consistency across delivery, employer engagement, and reporting — while cross-training keeps the team connected across all programs.</div>
  </div>
  <div class="section-label" style="margin-bottom:.75rem;">Core SOP library</div>
  <div class="two-col">
    <div class="sop-card"><div class="sop-title"><span class="sop-num">1</span> Program Planning SOP</div><ul class="sop-items"><li>Program creation &amp; scheduling</li><li>Facilitator assignment &amp; preparation</li><li>Resource preparation &amp; promotion timelines</li><li>Guest speaker coordination</li></ul></div>
    <div class="sop-card"><div class="sop-title"><span class="sop-num">2</span> Event Delivery SOP</div><ul class="sop-items"><li>Opening scripts &amp; tech setup</li><li>Attendance &amp; breakout room management</li><li>Facilitation flow &amp; engagement management</li><li>Follow-up communication process</li></ul></div>
    <div class="sop-card"><div class="sop-title"><span class="sop-num">3</span> Employer Engagement SOP</div><ul class="sop-items"><li>Employer outreach &amp; onboarding</li><li>Partnership maintenance &amp; follow-up</li><li>Recruitment event coordination</li><li>Employer database updates</li></ul></div>
    <div class="sop-card"><div class="sop-title"><span class="sop-num">4</span> Job Seeker Intake SOP</div><ul class="sop-items"><li>Registration &amp; readiness assessment</li><li>Referral process &amp; sector alignment</li><li>Participation &amp; progression tracking</li><li>Escalation &amp; career support</li></ul></div>
    <div class="sop-card"><div class="sop-title"><span class="sop-num">5</span> Data &amp; Reporting SOP</div><ul class="sop-items"><li>Survey collection &amp; data entry</li><li>KPI monitoring &amp; monthly reporting</li><li>Database management &amp; confidentiality</li><li>Outcome tracking standards</li></ul></div>
  </div>
  <hr>
  <div class="section-label" style="margin-bottom:.75rem;">Team development model</div>
  <div class="streams-grid">
    <div class="stream-card"><span class="stream-badge sb-purple">Cross-Training</span><div class="stream-name">Prevent program silos</div><ul class="prog-list"><li>All staff learn every program's goals</li><li>Referral pathways &amp; employer messaging</li><li>Shadowing, co-facilitation, rotation</li><li>Technology systems familiarity</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-teal">Peer Practice</span><div class="stream-name">Build facilitator confidence</div><ul class="prog-list"><li>Monthly internal practice sessions</li><li>Mock facilitation &amp; peer feedback</li><li>Presentation scoring rubric</li><li>Cultural sensitivity coaching</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-amber">Collaborative Planning</span><div class="stream-name">Keep programs connected</div><ul class="prog-list"><li>Monthly planning meetings (all staff)</li><li>Employer trends &amp; labour shortage review</li><li>Participant feedback &amp; attendance trends</li><li>Upcoming partnerships &amp; referral opportunities</li></ul></div>
  </div>
</div>

<!-- ── METRICS ── -->
<div class="section" id="s-metrics">
  <div class="section-header">
    <div class="section-label">Performance Framework</div>
    <div class="section-title">Success metrics &amp; indicators</div>
    <div class="section-desc">Key performance indicators across all three pillars — the foundation of reporting, funder communications, and program improvement.</div>
  </div>
  <div class="metrics-grid">
    <div class="metric-group mg-1"><div class="metric-group-title">Job seeker metrics</div><div class="metric-item">Number of participants enrolled</div><div class="metric-item">Employment outcomes achieved</div><div class="metric-item">Employer connections made</div><div class="metric-item">Self-reported confidence increase</div><div class="metric-item">Training completion rates</div><div class="metric-item">Networking event participation</div><div class="metric-item">Career advancement over time</div></div>
    <div class="metric-group mg-2"><div class="metric-group-title">Employer metrics</div><div class="metric-item">Number of active employer partners</div><div class="metric-item">Repeat employer participation rate</div><div class="metric-item">Hiring outcomes from Talent Match</div><div class="metric-item">Newcomer retention rates reported</div><div class="metric-item">Employer satisfaction scores</div><div class="metric-item">Employer referrals to program</div><div class="metric-item">Lunch &amp; Learn attendance rate</div></div>
    <div class="metric-group mg-3"><div class="metric-group-title">Community metrics</div><div class="metric-item">Number of active partnerships</div><div class="metric-item">Rural employer engagement rate</div><div class="metric-item">Community events participation</div><div class="metric-item">Cross-sector stakeholder collaboration</div><div class="metric-item">Newcomer community retention rate</div><div class="metric-item">Labour market intelligence reports</div><div class="metric-item">Regional workforce growth indicators</div></div>
  </div>
  <hr>
  <div class="section-label" style="margin-bottom:.75rem;">Recommended next phase — by timeline</div>
  <div class="streams-grid">
    <div class="stream-card"><span class="stream-badge sb-purple">Immediate</span><div class="stream-name">Build the foundation</div><ul class="prog-list"><li>Centralized program calendar</li><li>SOP manuals (all 5 categories)</li><li>Standardized facilitator guides</li><li>Employer &amp; participant database</li><li>Surveys &amp; reporting templates</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-teal">Medium-term</span><div class="stream-name">Grow the ecosystem</div><ul class="prog-list"><li>Mentorship program launch</li><li>Employer advisory council</li><li>Sector councils per industry</li><li>Rural partnership expansion</li><li>Certification &amp; placement pathways</li></ul></div>
    <div class="stream-card"><span class="stream-badge sb-amber">Long-term</span><div class="stream-name">Become the hub</div><ul class="prog-list"><li>Regional employer consortium</li><li>Sector-specific workforce academies</li><li>Provincial employer network</li><li>Data-driven labour market response</li><li>Hybrid workforce development systems</li></ul></div>
  </div>
</div>

<!-- ── VALUES ── -->
<div class="section" id="s-values">
  <div class="section-header">
    <div class="section-label">Strategic Positioning</div>
    <div class="section-title">Value propositions</div>
    <div class="section-desc">What makes this ecosystem unique is that it connects workforce development, economic development, settlement integration, and community retention — not just one of these.</div>
  </div>
  <div class="vp-grid">
    <div class="vp-card vp-1"><div class="vp-for">For job seekers</div><div class="vp-title">Confidence, connections, and a career path.</div><div class="vp-quote">We help immigrant talent build confidence, understand the Canadian labour market, connect with employers, and access meaningful career pathways aligned with their skills and experience.</div><div class="vp-values"><span class="vp-tag">Access</span><span class="vp-tag">Confidence</span><span class="vp-tag">Networks</span><span class="vp-tag">Career growth</span><span class="vp-tag">Belonging</span></div></div>
    <div class="vp-card vp-2"><div class="vp-for">For employers</div><div class="vp-title">Solve your workforce shortage — sustainably.</div><div class="vp-quote">We help employers solve workforce shortages by connecting them with prepared immigrant talent while strengthening inclusive hiring, onboarding, retention, and workforce sustainability.</div><div class="vp-values"><span class="vp-tag">Talent access</span><span class="vp-tag">Retention</span><span class="vp-tag">Diversity</span><span class="vp-tag">Productivity</span><span class="vp-tag">Sustainability</span></div></div>
    <div class="vp-card vp-3"><div class="vp-for">For communities</div><div class="vp-title">Stronger economies through integration.</div><div class="vp-quote">We support stronger communities and regional economies by creating workforce integration systems that connect employers, immigrant talent, and community partners through collaboration.</div><div class="vp-values"><span class="vp-tag">Economic growth</span><span class="vp-tag">Retention</span><span class="vp-tag">Labour force</span><span class="vp-tag">Social inclusion</span></div></div>
  </div>
  <div class="strat-box">
    <div class="section-label" style="margin-bottom:.5rem;">Strategic advantage</div>
    <div style="font-family:'DM Serif Display',serif;font-size:1.2rem;color:var(--text-primary);line-height:1.4;margin-bottom:.75rem;">This is NOT settlement-only. NOT job-search-only. NOT employer-only.</div>
    <p>The RMIEC ecosystem connects <strong>workforce development</strong> + <strong>economic development</strong> + <strong>settlement integration</strong> + <strong>employer engagement</strong> + <strong>community retention</strong> into a single, coordinated system. That integration is the competitive advantage — and what makes long-term labour force sustainability possible for the region.</p>
  </div>
</div>

</div><!-- /main -->

<div class="page-footer">
  <div class="footer-org">RMIEC — Rural Manitoba Immigrant Employment Council</div>
  <div class="footer-links">
    <a href="mailto:info@rmiec.ca">info@rmiec.ca</a>
    <a href="https://rmiec.ca/" target="_blank">rmiec.ca</a>
  </div>
</div>

<button class="print-btn" onclick="window.print()">🖨 Print / Save PDF</button>

<script>
function showSection(id, btn) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
  document.getElementById('s-' + id).classList.add('active');
  btn.classList.add('active');
  window.scrollTo({top: 0, behavior: 'smooth'});
}
function togglePillar(n) {
  [1,2,3].forEach(i => {
    document.getElementById('pc-' + i).classList.toggle('active', i === n);
    document.getElementById('sw-' + i).classList.toggle('show', i === n);
  });
}
function showGap(key, btn) {
  ['emp','js','org'].forEach(k => {
    document.getElementById('gg-' + k).style.display = k === key ? 'grid' : 'none';
  });
  document.querySelectorAll('.gap-tab').forEach(b => b.classList.remove('on'));
  btn.classList.add('on');
}
</script>
</body>
</html>
