# Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Atif Raza | Operations & Supply Chain Executive</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Playfair+Display:wght@600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #040711;
            --card-bg: rgba(15, 23, 42, 0.85);
            --border-glow: rgba(251, 191, 36, 0.5);
            --accent-gold: #fbbf24;
            --accent-green: #34d399;
            --accent-blue: #38bdf8;
            --text-light: #f8fafc;
            --text-dim: #94a3b8;
            --gradient-mesh: radial-gradient(circle at 50% 0%, #1e293b 0%, #040711 85%);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        
        body { 
            font-family: 'Plus Jakarta Sans', sans-serif; 
            background: var(--bg-dark); 
            color: var(--text-light); 
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation Bar */
        nav {
            position: fixed;
            top: 0; left: 0; right: 0;
            z-index: 100;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 8%;
            background: rgba(4, 7, 17, 0.9);
            backdrop-filter: blur(15px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
        }

        .nav-logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--accent-gold);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
            align-items: center;
        }

        .nav-links a {
            color: var(--text-dim);
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover { color: var(--accent-gold); }

        .btn-contact {
            background: var(--accent-gold);
            color: #040711 !important;
            padding: 0.5rem 1.2rem;
            border-radius: 2rem;
            font-weight: 700 !important;
            box-shadow: 0 4px 15px rgba(251, 191, 36, 0.3);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            background: var(--gradient-mesh);
            padding: 8rem 1.5rem 5rem;
        }

        .hero-content {
            z-index: 10;
            text-align: center;
            max-width: 880px;
            animation: fadeIn 1s ease-out;
        }

        .profile-img-wrapper {
            position: relative;
            width: 190px;
            height: 190px;
            margin: 0 auto 2rem;
        }

        .profile-img-wrapper::before {
            content: "";
            position: absolute;
            inset: -8px;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--accent-gold), transparent, var(--accent-green));
            animation: spinGlow 6s linear infinite;
            filter: blur(10px);
            opacity: 0.85;
        }

        .profile-img-container {
            position: relative;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            border: 3px solid var(--accent-gold);
            overflow: hidden;
            background: #1e293b;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.8);
        }

        .profile-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center;
        }

        .status-badge {
            display: inline-flex;
            align-items: center;
            background: rgba(52, 211, 153, 0.12);
            color: var(--accent-green);
            padding: 0.5rem 1.2rem;
            border-radius: 2rem;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            border: 1px solid rgba(52, 211, 153, 0.3);
            backdrop-filter: blur(8px);
        }

        .status-dot {
            width: 8px;
            height: 8px;
            background: var(--accent-green);
            border-radius: 50%;
            margin-right: 10px;
            box-shadow: 0 0 10px var(--accent-green);
            animation: pulse 2s infinite;
        }

        h1 { 
            font-family: 'Playfair Display', serif; 
            font-size: 4rem; 
            font-weight: 800;
            margin-bottom: 0.8rem; 
            line-height: 1.15;
            background: linear-gradient(to right, #ffffff, #cbd5e1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-subtitle { 
            font-size: 1.2rem; 
            color: var(--text-dim); 
            max-width: 700px; 
            margin: 0 auto 2.5rem; 
        }

        .btn-group { display: flex; gap: 1.2rem; justify-content: center; flex-wrap: wrap; }
        
        .btn { 
            padding: 0.9rem 2.4rem; 
            border-radius: 0.6rem; 
            text-decoration: none; 
            font-weight: 700; 
            font-size: 0.95rem;
            transition: all 0.3s ease; 
        }

        .btn-primary { 
            background: var(--accent-gold); 
            color: #040711; 
            box-shadow: 0 4px 20px rgba(251, 191, 36, 0.35);
        }
        
        .btn-primary:hover { 
            transform: translateY(-3px);
            box-shadow: 0 8px 30px rgba(251, 191, 36, 0.55);
        }

        .btn-secondary { 
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.18); 
            color: var(--text-light); 
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover { 
            background: rgba(255, 255, 255, 0.1);
            border-color: var(--accent-gold);
            transform: translateY(-3px);
        }

        /* KPI Counter Dashboard */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.8rem;
            padding: 4.5rem 10%;
            background: rgba(4, 7, 17, 0.95);
        }

        .stat-card {
            background: var(--card-bg);
            padding: 2.2rem 1.5rem;
            border-radius: 1rem;
            text-align: center;
            border: 1px solid rgba(255,255,255,0.06);
            backdrop-filter: blur(12px);
            transition: transform 0.3s ease, border-color 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            border-color: var(--border-glow);
        }

        .stat-number { 
            font-size: 2.8rem; 
            font-weight: 700; 
            color: var(--accent-gold); 
            display: block; 
            font-family: 'Playfair Display', serif;
        }

        .stat-label { 
            font-size: 0.85rem; 
            color: var(--text-dim); 
            text-transform: uppercase; 
            letter-spacing: 1.2px; 
            margin-top: 0.6rem; 
            font-weight: 600;
        }

        .section-padding { padding: 6.5rem 10%; }
        
        .section-title {
            font-family: 'Playfair Display', serif; 
            font-size: 2.5rem; 
            margin-bottom: 3.5rem;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: "";
            position: absolute;
            left: 0; bottom: -8px;
            width: 50%; height: 3px;
            background: var(--accent-gold);
            border-radius: 2px;
        }

        /* Experience Timeline */
        .timeline-container { 
            position: relative; 
            border-left: 2px solid rgba(255, 255, 255, 0.1); 
            margin-left: 20px; 
            padding-left: 35px; 
        }

        .timeline-item { 
            position: relative; 
            margin-bottom: 3.5rem; 
            background: var(--card-bg);
            padding: 2.2rem;
            border-radius: 1rem;
            border: 1px solid rgba(255,255,255,0.06);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .timeline-item:hover {
            border-color: var(--border-glow);
            transform: translateX(5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .timeline-item::before {
            content: "";
            position: absolute;
            left: -48px;
            top: 32px;
            width: 14px;
            height: 14px;
            background: var(--accent-gold);
            border-radius: 50%;
            box-shadow: 0 0 12px var(--accent-gold);
        }

        .timeline-item h3 { font-size: 1.4rem; color: #fff; font-weight: 600; }
        .company-subtitle { color: var(--accent-gold); font-size: 0.95rem; font-weight: 600; margin-top: 0.3rem; }
        .date-location { color: var(--text-dim); font-size: 0.85rem; margin-bottom: 1.2rem; }

        .exp-list { list-style-type: none; }
        .exp-list li {
            position: relative;
            padding-left: 1.5rem;
            margin-bottom: 0.8rem;
            color: var(--text-dim);
            font-size: 0.95rem;
        }

        .exp-list li::before {
            content: "✦";
            position: absolute;
            left: 0;
            color: var(--accent-gold);
            font-size: 0.75rem;
            top: 2px;
        }

        .tech-tags {
            display: flex;
            gap: 0.6rem;
            flex-wrap: wrap;
            margin-top: 1.2rem;
        }

        .tech-tag {
            background: rgba(251, 191, 36, 0.1);
            color: var(--accent-gold);
            padding: 0.3rem 0.8rem;
            border-radius: 0.4rem;
            font-size: 0.8rem;
            font-weight: 500;
            border: 1px solid rgba(251, 191, 36, 0.2);
        }

        /* Core Skills Section Matrix */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.8rem;
        }

        .skills-card {
            background: var(--card-bg);
            border-radius: 1rem;
            padding: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.06);
            backdrop-filter: blur(10px);
        }

        .skills-card h3 {
            color: var(--accent-gold);
            font-size: 1.25rem;
            margin-bottom: 1.2rem;
            border-bottom: 1px solid rgba(251, 191, 36, 0.2);
            padding-bottom: 0.5rem;
        }

        .skill-list { list-style: none; }
        .skill-list li {
            color: var(--text-dim);
            font-size: 0.95rem;
            margin-bottom: 0.7rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .skill-level {
            font-size: 0.75rem;
            color: var(--accent-green);
            background: rgba(52, 211, 153, 0.1);
            padding: 0.2rem 0.6rem;
            border-radius: 1rem;
        }

        /* 4K Visual Projects Showcase Gallery Grid */
        .showcase-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .showcase-card {
            background: var(--card-bg);
            border-radius: 1.2rem;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.08);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            cursor: pointer;
        }

        .showcase-card:hover {
            transform: translateY(-10px);
            border-color: var(--accent-gold);
            box-shadow: 0 15px 35px rgba(251, 191, 36, 0.25);
        }

        .showcase-img-box {
            width: 100%;
            height: 220px;
            overflow: hidden;
            position: relative;
        }

        .showcase-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s ease;
        }

        .showcase-card:hover .showcase-img { transform: scale(1.1); }

        .click-hint {
            position: absolute;
            bottom: 12px;
            right: 12px;
            background: rgba(4, 7, 17, 0.85);
            color: var(--accent-gold);
            padding: 0.4rem 0.9rem;
            border-radius: 2rem;
            font-size: 0.75rem;
            font-weight: 700;
            border: 1px solid var(--accent-gold);
            backdrop-filter: blur(5px);
        }

        .showcase-info { padding: 1.6rem; }
        .showcase-info h3 { font-size: 1.3rem; color: #fff; margin-bottom: 0.5rem; }
        .showcase-info p { font-size: 0.9rem; color: var(--text-dim); }

        /* Modal Component */
        .modal {
            display: none;
            position: fixed;
            inset: 0;
            z-index: 200;
            background: rgba(4, 7, 17, 0.92);
            backdrop-filter: blur(15px);
            align-items: center;
            justify-content: center;
            padding: 1.5rem;
        }

        .modal-content {
            background: #0f172a;
            border: 1px solid var(--accent-gold);
            border-radius: 1.2rem;
            max-width: 680px;
            width: 100%;
            padding: 2.5rem;
            position: relative;
            box-shadow: 0 25px 60px rgba(0,0,0,0.85);
            animation: fadeIn 0.3s ease-out;
        }

        .modal-close {
            position: absolute;
            top: 1.2rem; right: 1.6rem;
            color: var(--text-dim);
            font-size: 2.2rem;
            cursor: pointer;
            transition: color 0.3s;
        }

        .modal-close:hover { color: var(--accent-gold); }
        .modal-title { color: var(--accent-gold); font-size: 1.75rem; margin-bottom: 1rem; font-family: 'Playfair Display', serif; }
        .modal-body { color: var(--text-dim); font-size: 0.95rem; }
        .modal-body ul { list-style: none; margin-top: 1.2rem; }
        .modal-body ul li { margin-bottom: 0.7rem; padding-left: 1.4rem; position: relative; }
        .modal-body ul li::before { content: "✔"; position: absolute; left: 0; color: var(--accent-green); font-weight: bold; }

        /* Education & Certification Section */
        .edu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
            gap: 1.8rem;
            margin-top: 2rem;
        }

        .edu-card {
            background: var(--card-bg);
            border-radius: 1rem;
            padding: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.06);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .edu-card:hover {
            border-color: var(--accent-blue);
            transform: translateY(-5px);
        }

        .edu-card h3 { color: var(--accent-blue); font-size: 1.3rem; margin-bottom: 0.4rem; }
        .edu-card .institution { color: #fff; font-size: 0.95rem; font-weight: 600; }
        .edu-card .duration { color: var(--accent-gold); font-size: 0.85rem; margin-top: 0.2rem; font-weight: 500; }
        
        .edu-desc {
            margin-top: 1rem;
            list-style: none;
        }

        .edu-desc li {
            color: var(--text-dim);
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
            padding-left: 1.2rem;
            position: relative;
        }

        .edu-desc li::before {
            content: "▹";
            position: absolute;
            left: 0;
            color: var(--accent-blue);
        }

        footer { 
            text-align: center; 
            padding: 3.5rem 1rem; 
            background: #02040a; 
            color: var(--text-dim); 
            border-top: 1px solid rgba(255,255,255,0.05);
        }
        
        footer a { color: var(--accent-gold); text-decoration: none; font-weight: 600; }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.4; } }
        @keyframes spinGlow { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }

    </style>
</head>
<body>

    <!-- Top Navigation -->
    <nav>
        <a href="#" class="nav-logo">Atif Raza</a>
        <ul class="nav-links">
            <li><a href="#experience">Experience</a></li>
            <li><a href="#skills">Skills Matrix</a></li>
            <li><a href="#showcase">Portfolio</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="https://wa.me/923095156042" target="_blank" class="btn-contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="status-badge">
                <span class="status-dot"></span> Available for Supply Chain & Operations Roles
            </div>
            
            <div class="profile-img-wrapper">
                <div class="profile-img-container">
                    <img src="https://images.unsplash.com/photo-1586528116311-ad8dd3c8310d?q=80&w=1000&auto=format&fit=crop" 
                         alt="Logistics Operations Control Room" class="profile-img">
                </div>
            </div>

            <h1>Atif Raza</h1>
            <p class="hero-subtitle">Executive MBA Candidate & Operations Specialist bridging complex logistics infrastructure with data-driven operational efficiency.</p>
            
            <div class="btn-group">
                <a href="#experience" class="btn btn-primary">Explore Experience</a>
                <a href="https://wa.me/923095156042" target="_blank" class="btn btn-secondary">WhatsApp: +92 309 5156042</a>
            </div>
        </div>
    </section>

    <!-- Metrics KPI Counter -->
    <div class="stats-grid" id="stats-section">
        <div class="stat-card">
            <span class="stat-number" data-target="50" data-suffix="+">0</span>
            <span class="stat-label">Fleet Managed Daily</span>
        </div>
        <div class="stat-card">
            <span class="stat-number" data-target="3" data-suffix="+ Yrs">0</span>
            <span class="stat-label">Operations Exp</span>
        </div>
        <div class="stat-card">
            <span class="stat-number" data-target="99.2" data-suffix="%">0</span>
            <span class="stat-label">Dispatch TAT Rate</span>
        </div>
        <div class="stat-card">
            <span class="stat-number" data-target="200" data-suffix="+">0</span>
            <span class="stat-label">KDP Publications</span>
        </div>
    </div>

    <!-- Experience Timeline Section -->
    <section class="section-padding" id="experience">
        <h2 class="section-title">Professional Detailed Experience</h2>
        
        <div class="timeline-container">
            
            <div class="timeline-item">
                <h3>Operations Executive / Team Lead</h3>
                <div class="company-subtitle">OpenPort (Private) Limited — On-site at Bulleh Shah Packaging</div>
                <div class="date-location">August 2023 – Present | Kasur, Pakistan</div>
                
                <ul class="exp-list">
                    <li>Managing complete end-to-end logistics dispatches, shipment tracking, and transporter coordination.</li>
                    <li>Monitoring vehicle movement from initial dispatch to final destination delivery (timings, delays, and status updates).</li>
                    <li>Managing OpenShipper system for streamlined order creation, dispatch tracking, and live operations monitoring.</li>
                    <li>Developing and monitoring dynamic Power BI dashboards (tracking shipment status, transporter performance, and live vehicle location).</li>
                    <li>Verifying transporter billing records and handling halting/demurrage charges claims based on GPS tracking data.</li>
                    <li>Acting as primary single point of contact (SPOC) between transporters, external tracking teams, and internal plant management.</li>
                </ul>

                <div class="tech-tags">
                    <span class="tech-tag">Power BI</span>
                    <span class="tech-tag">GPS Fleet Tracking</span>
                    <span class="tech-tag">OpenShipper</span>
                    <span class="tech-tag">Halting Analytics</span>
                    <span class="tech-tag">Advanced Excel</span>
                </div>
            </div>

            <div class="timeline-item">
                <h3>Freelance Book Formatting & Design Specialist</h3>
                <div class="company-subtitle">Upwork & Fiverr Marketplaces</div>
                <div class="date-location">September 2020 – July 2025 | Remote</div>

                <ul class="exp-list">
                    <li>Formatted and produced 200+ books for Amazon KDP and IngramSpark, covering print-ready interiors and eBook conversions.</li>
                    <li>Utilized Adobe InDesign, Illustrator, and Photoshop to design high-quality layouts adhering to international publishing standards.</li>
                    <li>Maintained excellent client ratings and repeat business through clear project communication and timely delivery.</li>
                </ul>

                <div class="tech-tags">
                    <span class="tech-tag">Adobe InDesign</span>
                    <span class="tech-tag">Amazon KDP</span>
                    <span class="tech-tag">Print Formatting</span>
                    <span class="tech-tag">Photoshop</span>
                </div>
            </div>

            <div class="timeline-item">
                <h3>Sales & Data Entry Specialist</h3>
                <div class="company-subtitle">Doce Bakers & Sweets</div>
                <div class="date-location">February 2021 – July 2023 | Lahore, Pakistan</div>

                <ul class="exp-list">
                    <li>Managed daily sales records, stock/inventory levels, and accurate point-of-sale entries.</li>
                    <li>Handled customer queries and order reconciliation to ensure a smooth buying experience.</li>
                    <li>Maintained meticulous data entry logs for store inventory vs sales matching.</li>
                </ul>

                <div class="tech-tags">
                    <span class="tech-tag">Inventory Records</span>
                    <span class="tech-tag">Data Entry</span>
                    <span class="tech-tag">POS Systems</span>
                </div>
            </div>

        </div>
    </section>

    <!-- Skills Matrix Section -->
    <section class="section-padding" id="skills" style="background: rgba(4, 7, 17, 0.6);">
        <h2 class="section-title">Core Competencies & Technical Skills</h2>
        
        <div class="skills-grid">
            <div class="skills-card">
                <h3>Logistics & Supply Chain</h3>
                <ul class="skill-list">
                    <li>End-to-End Fleet Ops <span class="skill-level">Expert</span></li>
                    <li>GPS Vehicle Tracking <span class="skill-level">Advanced</span></li>
                    <li>OpenShipper ERP <span class="skill-level">Expert</span></li>
                    <li>Transporter Coordination <span class="skill-level">Advanced</span></li>
                    <li>Halting Claim Management <span class="skill-level">Expert</span></li>
                </ul>
            </div>

            <div class="skills-card">
                <h3>Data & Analytics</h3>
                <ul class="skill-list">
                    <li>Power BI Dashboards <span class="skill-level">Advanced</span></li>
                    <li>Advanced MS Excel (KPIs) <span class="skill-level">Expert</span></li>
                    <li>Python Automation <span class="skill-level">Certified</span></li>
                    <li>Data Science Fundamentals <span class="skill-level">Intermediate</span></li>
                    <li>Performance Analytics <span class="skill-level">Advanced</span></li>
                </ul>
            </div>

            <div class="skills-card">
                <h3>Publishing & Tools</h3>
                <ul class="skill-list">
                    <li>Adobe InDesign Layouts <span class="skill-level">Expert</span></li>
                    <li>Amazon KDP Formatting <span class="skill-level">Expert</span></li>
                    <li>Photoshop & Illustrator <span class="skill-level">Advanced</span></li>
                    <li>HTML / CSS / JavaScript <span class="skill-level">Intermediate</span></li>
                    <li>Project Documentation <span class="skill-level">Advanced</span></li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Visual Project Showcase Gallery Grid -->
    <section class="section-padding" id="showcase">
        <h2 class="section-title" style="display: block; text-align: center;">Featured Portfolio Projects</h2>
        
        <div class="showcase-grid">
            
            <div class="showcase-card" onclick="openModal('powerbi')">
                <div class="showcase-img-box">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?q=80&w=1000&auto=format&fit=crop" 
                         alt="Power BI Dashboard" class="showcase-img">
                    <span class="click-hint">Click for Details ➔</span>
                </div>
                <div class="showcase-info">
                    <h3>Power BI Logistics Dashboard</h3>
                    <p>Dynamic KPI reporting, turnaround time (TAT) tracking, and vehicle stay-time analytics.</p>
                </div>
            </div>

            <div class="showcase-card" onclick="openModal('gps')">
                <div class="showcase-img-box">
                    <img src="https://images.unsplash.com/photo-1519003722824-194d4455a60c?q=80&w=1000&auto=format&fit=crop" 
                         alt="GPS Fleet Tracking" class="showcase-img">
                    <span class="click-hint">Click for Details ➔</span>
                </div>
                <div class="showcase-info">
                    <h3>GPS Fleet Tracking & Halting</h3>
                    <p>Real-time vehicle monitoring, geo-fenced destination pings, and demurrage verification.</p>
                </div>
            </div>

            <div class="showcase-card" onclick="openModal('openshipper')">
                <div class="showcase-img-box">
                    <img src="https://images.unsplash.com/photo-1586528116311-ad8dd3c8310d?q=80&w=1000&auto=format&fit=crop" 
                         alt="Supply Chain Control Room" class="showcase-img">
                    <span class="click-hint">Click for Details ➔</span>
                </div>
                <div class="showcase-info">
                    <h3>OpenShipper System Integration</h3>
                    <p>End-to-end plant dispatch management and electronic Proof of Delivery (ePOD) control.</p>
                </div>
            </div>

            <div class="showcase-card" onclick="openModal('excel')">
                <div class="showcase-img-box">
                    <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?q=80&w=1000&auto=format&fit=crop" 
                         alt="Excel KPI Tracker" class="showcase-img">
                    <span class="click-hint">Click for Details ➔</span>
                </div>
                <div class="showcase-info">
                    <h3>Excel Stay-Time KPI Tracker</h3>
                    <p>Dynamic Slicers, Pivot tables, and conditional alerts for transporter stay-time delay reduction.</p>
                </div>
            </div>

            <div class="showcase-card" onclick="openModal('billing')">
                <div class="showcase-img-box">
                    <img src="https://images.unsplash.com/photo-1554224155-8d04cb21cd6c?q=80&w=1000&auto=format&fit=crop" 
                         alt="Billing Audit System" class="showcase-img">
                    <span class="click-hint">Click for Details ➔</span>
                </div>
                <div class="showcase-info">
                    <h3>Transporter Billing & Halting Audit</h3>
                    <p>Verification system for freight charges, halting claims, and invoice reconciliation against GPS data.</p>
                </div>
            </div>

            <div class="showcase-card" onclick="openModal('kdp')">
                <div class="showcase-img-box">
                    <img src="https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?q=80&w=1000&auto=format&fit=crop" 
                         alt="Amazon KDP Publishing" class="showcase-img">
                    <span class="click-hint">Click for Details ➔</span>
                </div>
                <div class="showcase-info">
                    <h3>Amazon KDP Publishing & Layouts</h3>
                    <p>200+ print-ready book interiors, typography, and eBook conversions in Adobe InDesign.</p>
                </div>
            </div>

        </div>
    </section>

    <!-- Education & Certifications Hub -->
    <section class="section-padding" id="education" style="background: rgba(4, 7, 17, 0.6);">
        <h2 class="section-title">Education & Academic Background</h2>
        
        <div class="edu-grid">
            <div class="edu-card">
                <h3>Executive MBA</h3>
                <div class="institution">University of the Punjab, Lahore</div>
                <div class="duration">Currently Pursuing (2026 - 2028)</div>
                <ul class="edu-desc">
                    <li>Focus on Supply Chain Management, Business Administration, and Marketing Strategy.</li>
                    <li>Applying business leadership concepts to optimize real-time logistics operations.</li>
                </ul>
            </div>

            <div class="edu-card">
                <h3>BS Information Technology</h3>
                <div class="institution">University of Education, Lahore</div>
                <div class="duration">Graduated 2019 - 2023</div>
                <ul class="edu-desc">
                    <li>Grade: B | Strong focus on Software Engineering, Data Analysis, and Systems Integration.</li>
                    <li>Built web applications and automation scripts for process optimization.</li>
                </ul>
            </div>

            <div class="edu-card">
                <h3>Python Programming Certification</h3>
                <div class="institution">Certiport — Pearson VUE</div>
                <div class="duration">Issued Apr 2026</div>
                <ul class="edu-desc">
                    <li>Automation scripting, data structures, and problem-solving fundamentals.</li>
                </ul>
            </div>

            <div class="edu-card">
                <h3>Data Science & Analytics Master</h3>
                <div class="institution">Udemy Certified</div>
                <div class="duration">Issued Aug 2024</div>
                <ul class="edu-desc">
                    <li>Data cleaning, visualization, predictive modeling, and statistical analysis.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Modal Pop-up Component -->
    <div class="modal" id="projectModal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal()">&times;</span>
            <h3 class="modal-title" id="modalTitle">Project Details</h3>
            <div class="modal-body" id="modalBody">Project information details go here...</div>
        </div>
    </div>

    <footer>
        <p>Direct Call / WhatsApp: <a href="tel:+923095156042">+92 309 5156042</a> | Email: <a href="mailto:atifraza4070@gmail.com">atifraza4070@gmail.com</a></p>
        <p style="margin-top: 0.6rem; font-size: 0.85rem;"><a href="https://www.linkedin.com/in/atifraza4050" target="_blank">LinkedIn Profile</a> | Kasur / Lahore, Punjab, Pakistan</p>
    </footer>

    <script>
        // Counter Animation
        let hasAnimated = false;
        function runCounters() {
            if (hasAnimated) return;
            hasAnimated = true;
            
            const counters = document.querySelectorAll('.stat-number');
            counters.forEach(counter => {
                const target = parseFloat(counter.getAttribute('data-target'));
                const suffix = counter.getAttribute('data-suffix') || '';
                let current = 0;
                const increment = target / 50;
                
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        counter.innerText = (target % 1 === 0 ? target : target.toFixed(1)) + suffix;
                        clearInterval(timer);
                    } else {
                        counter.innerText = (current % 1 === 0 ? Math.floor(current) : current.toFixed(1)) + suffix;
                    }
                }, 30);
            });
        }

        window.addEventListener('DOMContentLoaded', runCounters);
        window.addEventListener('scroll', runCounters);

        // Extended Project Modals Dictionary
        const projectData = {
            powerbi: {
                title: "Power BI & Logistics Analytics Dashboard",
                body: "Developed dynamic interactive dashboards to analyze vehicle turnaround time (TAT), daily dispatch volumes, and transporter performance metrics.<br><ul><li>Reduced stay-time by 18% using live KPI tracking.</li><li>Automated Excel-to-PowerBI reporting workflows.</li><li>Implemented conditional formatting for delayed dispatch alerts.</li></ul>"
            },
            gps: {
                title: "Real-Time GPS Fleet Tracking System",
                body: "Monitored 50+ fleet vehicles daily from dispatch to customer destination.<br><ul><li>Utilized geo-fenced location pings for exact arrival updates.</li><li>Handled halting and demurrage claims based on GPS location data logs.</li><li>Improved transporter accountability and route optimization.</li></ul>"
            },
            openshipper: {
                title: "Supply Chain & OpenShipper Operations",
                body: "Executed complete plant dispatches on-site at Bulleh Shah Packaging (BSP) Kasur.<br><ul><li>Single Point of Contact (SPOC) between plant teams and transporters.</li><li>Managed order creation, electronic Proof of Delivery (ePOD), and billing verification.</li><li>Resolved daily operational delays and vehicle tracking discrepancies.</li></ul>"
            },
            excel: {
                title: "Automated Excel Stay-Time Tracker",
                body: "Built dynamic Excel models featuring KPI summary cards, interactive slicers, and conditional logic.<br><ul><li>Tracked vehicle stay-time across multiple unloading points.</li><li>Enabled management visibility into transporter bottleneck trends.</li><li>Reduced manual data entry time by over 40%.</li></ul>"
            },
            billing: {
                title: "Transporter Billing & Halting Audit System",
                body: "Engineered a verification framework for transporter invoices and halting claims.<br><ul><li>Cross-referenced claimed halting hours with GPS location log timestamps.</li><li>Prevented invalid charge approvals, saving operational budget.</li><li>Maintained 100% accurate billing reconciliation logs.</li></ul>"
            },
            kdp: {
                title: "Amazon KDP & Digital Publishing",
                body: "Delivered 200+ book formatting and cover design projects for international authors on Upwork & Fiverr.<br><ul><li>Expertise in Adobe InDesign, Photoshop, and Kindle Create.</li><li>Print-ready PDF formatting (hardcover, paperback, and eBook).</li><li>100% 5-star client feedback and repeat orders.</li></ul>"
            }
        };

        function openModal(key) {
            const modal = document.getElementById('projectModal');
            document.getElementById('modalTitle').innerHTML = projectData[key].title;
            document.getElementById('modalBody').innerHTML = projectData[key].body;
            modal.style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('projectModal').style.display = 'none';
        }
    </script>

</body>
</html>
