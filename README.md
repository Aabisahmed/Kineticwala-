# Kineticwala-
Kinetic Wala Official Website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Kinetic Wala – Learn Smart. Build Strong Foundations.</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;0,600;1,400&display=swap" rel="stylesheet" />
<style>
  /* ─── CSS Variables ─────────────────────────────── */
  :root {
    --blue-primary: #1E3A8A;
    --blue-cta:     #2563EB;
    --blue-hover:   #DBEAFE;
    --blue-mid:     #3B82F6;
    --blue-deep:    #1e40af;
    --white:        #FFFFFF;
    --gray-dark:    #1F2937;
    --gray-mid:     #4B5563;
    --gray-light:   #9CA3AF;
    --bg-light:     #F3F4F6;
    --bg-section:   #EFF6FF;
    --shadow-sm:    0 2px 8px rgba(30,58,138,.08);
    --shadow-md:    0 8px 32px rgba(30,58,138,.13);
    --shadow-lg:    0 20px 60px rgba(30,58,138,.18);
    --radius:       16px;
    --radius-sm:    10px;
    --transition:   0.28s cubic-bezier(.4,0,.2,1);
  }

  /* ─── Reset & Base ──────────────────────────────── */
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'DM Sans', sans-serif;
    color: var(--gray-dark);
    background: var(--white);
    line-height: 1.65;
    overflow-x: hidden;
  }
  img { max-width: 100%; display: block; }
  a { text-decoration: none; color: inherit; }
  ul { list-style: none; }

  /* ─── Typography ────────────────────────────────── */
  .display { font-family: 'Sora', sans-serif; font-weight: 800; }
  h1,h2,h3,h4 { font-family: 'Sora', sans-serif; }

  /* ─── Utility ───────────────────────────────────── */
  .container { max-width: 1200px; margin: 0 auto; padding: 0 24px; }
  .section { padding: 96px 0; }
  .section-alt { background: var(--bg-light); }
  .section-blue { background: var(--bg-section); }
  .tag {
    display: inline-block;
    background: var(--blue-hover);
    color: var(--blue-primary);
    font-size: .78rem;
    font-weight: 700;
    letter-spacing: .08em;
    text-transform: uppercase;
    padding: 6px 14px;
    border-radius: 50px;
    margin-bottom: 18px;
  }
  .section-title {
    font-size: clamp(2rem, 4vw, 2.8rem);
    color: var(--blue-primary);
    line-height: 1.2;
    margin-bottom: 16px;
  }
  .section-sub {
    font-size: 1.1rem;
    color: var(--gray-mid);
    max-width: 600px;
    margin-bottom: 56px;
  }

  /* ─── Buttons ───────────────────────────────────── */
  .btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 14px 30px;
    border-radius: 50px;
    font-family: 'Sora', sans-serif;
    font-weight: 600;
    font-size: .95rem;
    cursor: pointer;
    border: none;
    transition: var(--transition);
  }
  .btn-primary {
    background: var(--blue-cta);
    color: #fff;
    box-shadow: 0 4px 20px rgba(37,99,235,.35);
  }
  .btn-primary:hover {
    background: var(--blue-deep);
    transform: translateY(-2px);
    box-shadow: 0 8px 30px rgba(37,99,235,.45);
  }
  .btn-outline {
    background: transparent;
    color: var(--blue-primary);
    border: 2px solid var(--blue-primary);
  }
  .btn-outline:hover {
    background: var(--blue-hover);
    transform: translateY(-2px);
  }

  /* ─── Navigation ────────────────────────────────── */
  #navbar {
    position: sticky;
    top: 0;
    z-index: 1000;
    background: rgba(255,255,255,.92);
    backdrop-filter: blur(18px);
    border-bottom: 1px solid rgba(30,58,138,.08);
    transition: box-shadow var(--transition);
  }
  #navbar.scrolled { box-shadow: var(--shadow-md); }
  .nav-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 68px;
  }
  .nav-logo {
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .nav-logo-img {
    height: 44px;
    width: auto;
    object-fit: contain;
  }
  .nav-links {
    display: flex;
    align-items: center;
    gap: 4px;
  }
  .nav-links a {
    padding: 8px 16px;
    border-radius: 8px;
    font-weight: 500;
    font-size: .92rem;
    color: var(--gray-mid);
    transition: var(--transition);
    position: relative;
  }
  .nav-links a:hover, .nav-links a.active {
    color: var(--blue-primary);
    background: var(--blue-hover);
  }
  .nav-cta {
    background: var(--blue-cta) !important;
    color: #fff !important;
    font-family: 'Sora', sans-serif;
    font-weight: 600 !important;
    padding: 9px 20px !important;
  }
  .nav-cta:hover { background: var(--blue-deep) !important; }
  .nav-hamburger {
    display: none;
    flex-direction: column;
    gap: 5px;
    cursor: pointer;
    padding: 6px;
  }
  .nav-hamburger span {
    display: block;
    width: 24px;
    height: 2px;
    background: var(--blue-primary);
    border-radius: 2px;
    transition: var(--transition);
  }

  /* ─── Mobile Nav ────────────────────────────────── */
  .mobile-nav {
    display: none;
    flex-direction: column;
    background: #fff;
    border-top: 1px solid var(--blue-hover);
    padding: 16px 24px 24px;
    gap: 4px;
  }
  .mobile-nav a {
    padding: 12px 16px;
    border-radius: 10px;
    font-weight: 500;
    color: var(--gray-dark);
    transition: var(--transition);
  }
  .mobile-nav a:hover { background: var(--blue-hover); color: var(--blue-primary); }
  .mobile-nav.open { display: flex; }

  /* ─── Hero ──────────────────────────────────────── */
  #hero {
    min-height: 92vh;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
    background: linear-gradient(135deg, #EFF6FF 0%, #DBEAFE 40%, #EFF6FF 100%);
  }
  .hero-bg-shapes {
    position: absolute;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
  }
  .hero-shape {
    position: absolute;
    border-radius: 50%;
    opacity: .12;
    background: var(--blue-primary);
  }
  .hero-shape-1 { width: 600px; height: 600px; right: -180px; top: -180px; }
  .hero-shape-2 { width: 300px; height: 300px; left: -80px; bottom: -80px; opacity: .07; }
  .hero-shape-3 { width: 180px; height: 180px; right: 30%; top: 60%; opacity: .06; }
  /* Grid pattern overlay */
  .hero-grid {
    position: absolute;
    inset: 0;
    background-image: radial-gradient(circle, rgba(30,58,138,.12) 1px, transparent 1px);
    background-size: 40px 40px;
  }
  .hero-content {
    position: relative;
    z-index: 2;
    max-width: 680px;
  }
  .hero-slogan {
    display: inline-flex;
    align-items: center;
    gap: 4px;
    font-family: 'Sora', sans-serif;
    font-size: 1.05rem;
    font-weight: 700;
    color: var(--blue-primary);
    background: #fff;
    border: 1px solid rgba(30,58,138,.15);
    border-radius: 50px;
    padding: 10px 22px;
    margin-bottom: 24px;
    box-shadow: var(--shadow-sm);
    animation: fadeDown .75s .05s ease both;
    letter-spacing: .01em;
  }
  .slogan-quote {
    font-size: 1.4rem;
    color: #ea580c;
    line-height: 1;
    font-style: italic;
  }
    align-items: center;
    gap: 8px;
    background: rgba(37,99,235,.1);
    border: 1px solid rgba(37,99,235,.2);
    color: var(--blue-cta);
    padding: 8px 18px;
    border-radius: 50px;
    font-size: .82rem;
    font-weight: 600;
    letter-spacing: .04em;
    margin-bottom: 28px;
    animation: fadeDown .7s ease both;
  }
  .hero-badge .dot {
    width: 7px; height: 7px;
    background: #22c55e;
    border-radius: 50%;
    animation: pulse 1.8s infinite;
  }
  .hero-title {
    font-size: clamp(2.6rem, 6vw, 4.2rem);
    color: var(--blue-primary);
    line-height: 1.12;
    margin-bottom: 24px;
    animation: fadeUp .8s .1s ease both;
  }
  .hero-title .accent { color: var(--blue-cta); }
  .hero-sub {
    font-size: 1.12rem;
    color: var(--gray-mid);
    line-height: 1.7;
    margin-bottom: 40px;
    animation: fadeUp .8s .2s ease both;
  }
  .hero-btns {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    animation: fadeUp .8s .3s ease both;
  }
  .hero-stats {
    display: flex;
    gap: 40px;
    margin-top: 60px;
    animation: fadeUp .8s .4s ease both;
    flex-wrap: wrap;
  }
  .hero-stat {}
  .hero-stat-num {
    font-family: 'Sora', sans-serif;
    font-size: 1.9rem;
    font-weight: 800;
    color: var(--blue-primary);
  }
  .hero-stat-label { font-size: .85rem; color: var(--gray-mid); font-weight: 500; }
  .hero-visual {
    position: absolute;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
    width: 44%;
    max-width: 520px;
    pointer-events: none;
    animation: floatUp .9s .2s ease both;
  }
  .hero-card-float {
    background: #fff;
    border-radius: var(--radius);
    box-shadow: var(--shadow-lg);
    padding: 28px;
    position: relative;
    overflow: hidden;
  }
  .hero-card-float::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--blue-cta), #60a5fa);
  }
  .hcf-subjects {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 20px;
  }
  .hcf-subject {
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--bg-light);
    border-radius: var(--radius-sm);
    padding: 12px 14px;
  }
  .hcf-subject .icon { font-size: 1.4rem; }
  .hcf-subject .name { font-size: .85rem; font-weight: 600; color: var(--gray-dark); }
  .hcf-classes {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }
  .hcf-class {
    background: var(--blue-hover);
    color: var(--blue-primary);
    font-size: .8rem;
    font-weight: 700;
    padding: 6px 14px;
    border-radius: 50px;
  }

  /* ─── Why KW Feature Cards ──────────────────────── */
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 24px;
  }
  .feature-card {
    background: #fff;
    border-radius: var(--radius);
    padding: 32px 28px;
    box-shadow: var(--shadow-sm);
    border: 1px solid rgba(30,58,138,.07);
    transition: var(--transition);
    position: relative;
    overflow: hidden;
  }
  .feature-card::after {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: var(--radius);
    border: 2px solid var(--blue-cta);
    opacity: 0;
    transition: var(--transition);
  }
  .feature-card:hover { transform: translateY(-6px); box-shadow: var(--shadow-md); }
  .feature-card:hover::after { opacity: 1; }
  .feature-icon {
    width: 56px;
    height: 56px;
    background: var(--blue-hover);
    border-radius: 14px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.6rem;
    margin-bottom: 20px;
  }
  .feature-card h3 {
    font-size: 1.1rem;
    color: var(--blue-primary);
    margin-bottom: 10px;
  }
  .feature-card p { font-size: .92rem; color: var(--gray-mid); line-height: 1.65; }

  /* ─── About Founder ─────────────────────────────── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1.5fr;
    gap: 64px;
    align-items: center;
  }
  .about-img-wrap {
    position: relative;
  }
  .about-img-placeholder {
    width: 100%;
    aspect-ratio: 4/5;
    border-radius: 24px;
    overflow: hidden;
    box-shadow: var(--shadow-lg);
    position: relative;
  }
  .about-img-placeholder img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top center;
    display: block;
    border-radius: 24px;
    transition: transform .5s ease;
  }
  .about-img-placeholder:hover img { transform: scale(1.04); }
  .about-img-placeholder::after {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 24px;
    background: linear-gradient(to top, rgba(30,58,138,.35) 0%, transparent 50%);
    pointer-events: none;
  }
  .about-img-placeholder .founder-name {
    font-family: 'Sora', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    color: #fff;
    position: absolute;
    bottom: 20px;
    left: 20px;
    z-index: 2;
    text-shadow: 0 1px 4px rgba(0,0,0,.4);
  }
  .about-badge {
    position: absolute;
    bottom: -16px;
    right: -16px;
    background: var(--blue-cta);
    color: #fff;
    border-radius: 14px;
    padding: 14px 20px;
    box-shadow: var(--shadow-md);
    text-align: center;
  }
  .about-badge .num { font-family: 'Sora', sans-serif; font-size: 1.4rem; font-weight: 800; }
  .about-badge .lbl { font-size: .72rem; font-weight: 500; opacity: .9; }
  .about-content h2 { margin-bottom: 20px; }
  .about-content p { color: var(--gray-mid); margin-bottom: 18px; font-size: 1rem; line-height: 1.75; }
  .about-points { margin-top: 28px; display: flex; flex-direction: column; gap: 14px; }
  .about-point {
    display: flex;
    align-items: flex-start;
    gap: 14px;
    padding: 16px 20px;
    background: var(--bg-section);
    border-radius: var(--radius-sm);
    border-left: 3px solid var(--blue-cta);
  }
  .about-point-icon { font-size: 1.2rem; flex-shrink: 0; margin-top: 1px; }
  .about-point-text { font-size: .9rem; color: var(--gray-dark); font-weight: 500; }

  /* ─── Classes ───────────────────────────────────── */
  .classes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 24px;
  }
  .class-card {
    background: #fff;
    border-radius: var(--radius);
    box-shadow: var(--shadow-sm);
    overflow: hidden;
    cursor: pointer;
    transition: var(--transition);
    border: 1px solid rgba(30,58,138,.08);
  }
  .class-card:hover { transform: translateY(-8px); box-shadow: var(--shadow-lg); }
  .class-card-header {
    background: var(--blue-primary);
    padding: 32px 28px 24px;
    position: relative;
    overflow: hidden;
  }
  .class-card-header::before {
    content: '';
    position: absolute;
    width: 120px; height: 120px;
    border-radius: 50%;
    background: rgba(255,255,255,.08);
    top: -40px; right: -30px;
  }
  .class-card-header::after {
    content: '';
    position: absolute;
    width: 70px; height: 70px;
    border-radius: 50%;
    background: rgba(255,255,255,.06);
    bottom: -20px; left: 60px;
  }
  .class-num {
    font-family: 'Sora', sans-serif;
    font-size: 3rem;
    font-weight: 800;
    color: rgba(255,255,255,.15);
    position: absolute;
    top: 8px; right: 20px;
    line-height: 1;
  }
  .class-label {
    color: rgba(255,255,255,.7);
    font-size: .8rem;
    font-weight: 600;
    letter-spacing: .08em;
    text-transform: uppercase;
    margin-bottom: 6px;
  }
  .class-title {
    color: #fff;
    font-size: 1.5rem;
    font-weight: 800;
    font-family: 'Sora', sans-serif;
    position: relative;
    z-index: 1;
  }
  .class-card-body { padding: 24px 28px; }
  .class-subjects { display: flex; flex-direction: column; gap: 10px; margin-bottom: 22px; }
  .class-subject {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: .88rem;
    color: var(--gray-mid);
  }
  .class-subject .dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--blue-cta);
    flex-shrink: 0;
  }
  .class-cta {
    width: 100%;
    justify-content: center;
    border-radius: var(--radius-sm);
  }

  /* ─── Free Demo ─────────────────────────────────── */
  .demo-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
  }
  .demo-card {
    background: #fff;
    border-radius: var(--radius);
    padding: 32px 24px;
    box-shadow: var(--shadow-sm);
    border: 1px solid rgba(30,58,138,.07);
    cursor: pointer;
    transition: var(--transition);
    text-align: center;
  }
  .demo-card:hover {
    transform: translateY(-6px);
    box-shadow: var(--shadow-md);
    border-color: var(--blue-cta);
    background: var(--bg-section);
  }
  .demo-icon {
    font-size: 2.4rem;
    margin-bottom: 16px;
    display: block;
  }
  .demo-card h3 { font-size: 1rem; color: var(--blue-primary); margin-bottom: 10px; }
  .demo-card p { font-size: .85rem; color: var(--gray-mid); line-height: 1.6; }
  .demo-badge {
    display: inline-block;
    background: #dcfce7;
    color: #16a34a;
    font-size: .72rem;
    font-weight: 700;
    padding: 3px 10px;
    border-radius: 50px;
    margin-top: 12px;
  }

  /* ─── Robotics ──────────────────────────────────── */
  .robotics-wrap {
    display: grid;
    grid-template-columns: 1.2fr 1fr;
    gap: 60px;
    align-items: center;
  }
  .robotics-content h2 { margin-bottom: 18px; }
  .robotics-content p { color: var(--gray-mid); margin-bottom: 30px; font-size: 1rem; }
  .robotics-list { display: flex; flex-direction: column; gap: 16px; margin-bottom: 36px; }
  .robotics-item {
    display: flex;
    align-items: flex-start;
    gap: 16px;
    padding: 16px 20px;
    background: #fff;
    border-radius: var(--radius-sm);
    box-shadow: var(--shadow-sm);
    transition: var(--transition);
  }
  .robotics-item:hover { transform: translateX(6px); box-shadow: var(--shadow-md); }
  .robotics-item-icon {
    font-size: 1.4rem;
    width: 44px; height: 44px;
    background: var(--blue-hover);
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .robotics-item-text h4 { font-size: .95rem; color: var(--blue-primary); margin-bottom: 4px; }
  .robotics-item-text p { font-size: .83rem; color: var(--gray-mid); line-height: 1.5; }
  .robotics-visual {
    background: linear-gradient(145deg, var(--blue-primary), #1e40af);
    border-radius: 24px;
    padding: 48px 36px;
    text-align: center;
    position: relative;
    overflow: hidden;
    cursor: pointer;
    transition: var(--transition);
    box-shadow: var(--shadow-lg);
  }
  .robotics-visual:hover { transform: translateY(-6px) scale(1.01); }
  .robotics-visual::before {
    content: '';
    position: absolute;
    width: 300px; height: 300px;
    border-radius: 50%;
    background: rgba(255,255,255,.05);
    top: -80px; right: -80px;
  }
  .robotics-emoji { font-size: 5rem; display: block; margin-bottom: 20px; }
  .robotics-visual h3 {
    color: #fff;
    font-size: 1.5rem;
    margin-bottom: 12px;
    position: relative;
    z-index: 1;
  }
  .robotics-visual p {
    color: rgba(255,255,255,.75);
    font-size: .9rem;
    position: relative;
    z-index: 1;
  }
  .robotics-visual .coming-tag {
    display: inline-block;
    background: rgba(255,255,255,.15);
    color: #fff;
    border: 1px solid rgba(255,255,255,.25);
    padding: 7px 20px;
    border-radius: 50px;
    font-size: .82rem;
    font-weight: 600;
    margin-top: 20px;
    position: relative;
    z-index: 1;
  }

  /* ─── Community ─────────────────────────────────── */
  .community-section {
    text-align: center;
    padding: 96px 0;
    background: linear-gradient(135deg, var(--blue-primary) 0%, #1e40af 100%);
    position: relative;
    overflow: hidden;
  }
  .community-section::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at 80% 20%, rgba(255,255,255,.07), transparent 50%),
                radial-gradient(circle at 20% 80%, rgba(255,255,255,.05), transparent 50%);
  }
  .community-section .tag { background: rgba(255,255,255,.15); color: #fff; }
  .community-section h2 { color: #fff; }
  .community-section .section-sub { color: rgba(255,255,255,.75); margin: 0 auto 48px; }
  .social-cards {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .social-card {
    display: flex;
    align-items: center;
    gap: 14px;
    background: rgba(255,255,255,.1);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255,255,255,.2);
    border-radius: var(--radius);
    padding: 20px 28px;
    color: #fff;
    cursor: pointer;
    transition: var(--transition);
    min-width: 200px;
    justify-content: center;
  }
  .social-card:hover {
    background: rgba(255,255,255,.18);
    transform: translateY(-4px);
    border-color: rgba(255,255,255,.4);
  }
  .social-card-icon { f
