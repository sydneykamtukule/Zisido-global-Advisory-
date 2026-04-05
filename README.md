# Zisido-global-Advisory-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zisido Global Advisory | Your Partner in Academic & Professional Excellence</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        /* --- CSS VARIABLES & RESET --- */
        :root {
            --primary: #0A1628; /* Deep Navy Blue */
            --accent: #D4AF37;  /* Gold */
            --text-light: #FFFFFF;
            --text-dark: #333333;
            --bg-light: #F8F9FA;
            --bg-gray: #f0f2f5;
            --transition: all 0.3s ease-in-out;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--text-light);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* --- REUSABLE COMPONENTS --- */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            cursor: pointer;
            text-align: center;
            border: 2px solid transparent;
        }

        .btn-gold {
            background-color: var(--accent);
            color: var(--primary);
        }

        .btn-gold:hover {
            background-color: transparent;
            border-color: var(--accent);
            color: var(--accent);
            transform: translateY(-3px);
        }

        .btn-outline {
            background-color: transparent;
            border-color: var(--text-light);
            color: var(--text-light);
        }

        .btn-outline:hover {
            background-color: var(--text-light);
            color: var(--primary);
            transform: translateY(-3px);
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--accent);
        }

        /* --- NAVIGATION --- */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 0;
            z-index: 1000;
            transition: var(--transition);
        }

        nav.scrolled {
            background-color: var(--primary);
            padding: 15px 0;
            box-shadow: 0 5px 20px rgba(0,0,0,0.2);
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            text-decoration: none;
            line-height: 1;
        }

        .logo .brand-main {
            font-weight: 800;
            font-size: 1.8rem;
            color: var(--accent);
            letter-spacing: 1px;
        }

        .logo .brand-sub {
            display: block;
            font-size: 0.75rem;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 30px;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-light);
            font-weight: 500;
            font-size: 0.95rem;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .nav-links .active {
            color: var(--accent);
        }

        .hamburger {
            display: none;
            cursor: pointer;
            color: var(--text-light);
            font-size: 1.8rem;
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #0A1628 0%, #162a47 100%);
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            color: var(--text-light);
        }

        /* Animated Particle Background Simulation */
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: radial-gradient(var(--accent) 0.5px, transparent 0.5px);
            background-size: 30px 30px;
            opacity: 0.1;
            animation: move-bg 60s linear infinite;
        }

        @keyframes move-bg {
            from { background-position: 0 0; }
            to { background-position: 1000px 1000px; }
        }

        .hero-content {
            max-width: 800px;
            z-index: 2;
            position: relative;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(212, 175, 55, 0.15);
            color: var(--accent);
            padding: 8px 16px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 20px;
            border: 1px solid var(--accent);
            animation: fadeInUp 0.8s ease-out;
        }

        .hero h1 {
            font-size: 3.8rem;
            line-height: 1.2;
            margin-bottom: 20px;
            animation: fadeInUp 1s ease-out;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 40px;
            opacity: 0.9;
            animation: fadeInUp 1.2s ease-out;
        }

        .hero-btns {
            display: flex;
            gap: 20px;
            animation: fadeInUp 1.4s ease-out;
        }

        /* --- SERVICES SECTION --- */
        .services {
            padding: 100px 0;
        }

        .service-category {
            margin-bottom: 60px;
        }

        .category-title {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 30px;
            border-left: 5px solid var(--accent);
            padding-left: 15px;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
        }

        .service-card {
            background: white;
            padding: 40px 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            transition: var(--transition);
            border: 1px solid #eee;
            text-align: center;
        }

        .service-card:hover {
            transform: translateY(-10px);
            border-color: var(--accent);
            box-shadow: 0 15px 35px rgba(212, 175, 55, 0.2);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            display: block;
        }

        .service-card h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: var(--primary);
        }

        .service-card p {
            font-size: 0.95rem;
            color: #666;
        }

        /* --- WHY CHOOSE US --- */
        .why-us {
            padding: 100px 0;
            background-color: var(--bg-light);
        }

        .trust-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .trust-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            background: white;
            padding: 25px;
            border-radius: 10px;
        }

        .trust-icon {
            color: var(--accent);
            font-size: 1.5rem;
            flex-shrink: 0;
        }

        .trust-text h4 {
            font-size: 1.1rem;
            color: var(--primary);
            margin-bottom: 5px;
        }

        .trust-text p {
            font-size: 0.9rem;
            color: #666;
        }

        /* --- HOW IT WORKS --- */
        .how-it-works {
            padding: 100px 0;
        }

        .steps-container {
            display: flex;
            justify-content: space-between;
            gap: 30px;
            margin-top: 50px;
        }

        .step {
            flex: 1;
            text-align: center;
            position: relative;
        }

        .step-number {
            width: 60px;
            height: 60px;
            background-color: var(--accent);
            color: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 700;
            margin: 0 auto 20px;
            position: relative;
            z-index: 2;
        }

        .step:not(:last-child)::after {
            content: '';
            position: absolute;
            top: 30px;
            left: calc(50% + 40px);
            width: calc(100% - 80px);
            height: 2px;
            border-top: 2px dashed #ddd;
            z-index: 1;
        }

        .step h3 {
            margin-bottom: 10px;
            color: var(--primary);
        }

        /* --- TESTIMONIALS --- */
        .testimonials {
            padding: 100px 0;
            background-color: var(--primary);
            color: var(--text-light);
        }

        .testimonials .section-title h2 {
            color: var(--text-light);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial-card {
            background: rgba(255,255,255,0.05);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.1);
            position: relative;
        }

        .stars {
            color: var(--accent);
            margin-bottom: 20px;
            font-size: 1.2rem;
        }

        .quote {
            font-style: italic;
            margin-bottom: 25px;
            font-size: 1.05rem;
        }

        .client-info {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .client-meta h4 {
            font-size: 1rem;
            color: var(--accent);
        }

        .client-meta span {
            font-size: 0.85rem;
            opacity: 0.7;
        }

        /* --- CTA BANNER --- */
        .cta-banner {
            padding: 80px 0;
            background-color: var(--accent);
            color: var(--primary);
            text-align: center;
        }

        .cta-banner h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            font-weight: 800;
        }

        .cta-banner p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            font-weight: 500;
        }

        .btn-navy {
            background-color: var(--primary);
            color: var(--text-light);
            font-size: 1.2rem;
            padding: 15px 40px;
        }

        .btn-navy:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        /* --- FOOTER --- */
        footer {
            background-color: #050b14;
            color: var(--text-light);
            padding: 80px 0 30px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr;
            gap: 60px;
            margin-bottom: 50px;
        }

        .footer-about .logo {
            margin-bottom: 20px;
            display: inline-block;
        }

        .footer-about p {
            opacity: 0.7;
            font-size: 0.95rem;
            max-width: 400px;
        }

        .footer-links h4, .footer-contact h4 {
            font-size: 1.2rem;
            margin-bottom: 25px;
            color: var(--accent);
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links ul li {
            margin-bottom: 12px;
        }

        .footer-links ul li a {
            color: var(--text-light);
            text-decoration: none;
            opacity: 0.7;
            transition: var(--transition);
        }

        .footer-links ul li a:hover {
            opacity: 1;
            color: var(--accent);
            padding-left: 5px;
        }

        .contact-info-item {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
            opacity: 0.8;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            opacity: 0.6;
        }

        /* --- FLOATING WHATSAPP --- */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 30px;
            box-shadow: 2px 2px 10px rgba(0,0,0,0.2);
            z-index: 1000;
            text-decoration: none;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(37, 211, 102, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
        }

        /* --- ANIMATIONS --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* --- MOBILE RESPONSIVENESS --- */
        @media (max-width: 992px) {
            .hero h1 { font-size: 2.8rem; }
            .footer-grid { grid-template-columns: 1fr 1fr; }
            .footer-about { grid-column: span 2; }
            .steps-container { flex-direction: column; }
            .step:not(:last-child)::after { display: none; }
            .step { margin-bottom: 40px; }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: var(--primary);
                flex-direction: column;
                padding: 20px;
                text-align: center;
            }

            .nav-links.show {
                display: flex;
            }

            .hamburger {
                display: block;
            }

            .hero h1 { font-size: 2.3rem; }
            .hero-btns { flex-direction: column; }
            .section-title h2 { font-size: 2rem; }
            .footer-grid { grid-template-columns: 1fr; }
            .footer-about { grid-column: span 1; }
        }
    </style>
</head>
<body>

    <!-- NAVIGATION -->
    <nav id="navbar">
        <div class="container">
            <a href="#" class="logo">
                <span class="brand-main">ZISIDO</span>
                <span class="brand-sub">Global Advisory</span>
            </a>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home" class="active">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#why-us">Why Us</a></li>
                <li><a href="#testimonials">Testimonials</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="https://wa.me/265995061815" class="btn btn-gold">Get Help Now</a></li>
            </ul>
            <div class="hamburger" id="hamburger">☰</div>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-badge">✅ Trusted by Students & Professionals</div>
                <h1>Excel Academically & Professionally — We've Got You Covered</h1>
                <p>Expert consulting, writing, recruitment support, and advertising services tailored for students and professionals in Malawi and beyond.</p>
                <div class="hero-btns">
                    <a href="https://wa.me/265995061815" class="btn btn-gold">Start Your Project →</a>
                    <a href="#services" class="btn btn-outline">View Our Services ↓</a>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-title reveal">
                <h2>Our Specialized Services</h2>
            </div>

            <!-- Category A -->
            <div class="service-category reveal">
                <h3 class="category-title">Academic & Professional Writing</h3>
                <div class="services-grid">
                    <div class="service-card">
                        <span class="service-icon">📝</span>
                        <h3>Assignments</h3>
                        <p>High-quality guidance and writing support for all academic levels.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">🔬</span>
                        <h3>Research Proposals</h3>
                        <p>Compelling proposals that meet rigorous academic standards.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">📊</span>
                        <h3>Data Collection & Analysis</h3>
                        <p>Expert assistance with quantitative and qualitative data processing.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">📄</span>
                        <h3>Concept Notes</h3>
                        <p>Developing clear and concise outlines for your research ideas.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">✏️</span>
                        <h3>Proofreading & Editing</h3>
                        <p>Polishing your work to ensure perfect grammar and flow.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">🔎</span>
                        <h3>Plagiarism Check</h3>
                        <p>Official Turnitin reports to guarantee 100% originality.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">🎓</span>
                        <h3>Dissertations & Projects</h3>
                        <p>Comprehensive support from initial draft to final submission.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">📋</span>
                        <h3>CVs & Application Letters</h3>
                        <p>Professional profiles that get you noticed by top employers.</p>
                    </div>
                </div>
            </div>

            <!-- Category B -->
            <div class="service-category reveal">
                <h3 class="category-title">Business & Corporate Services</h3>
                <div class="services-grid">
                    <div class="service-card">
                        <span class="service-icon">📢</span>
                        <h3>Advertising</h3>
                        <p>Effective promotion for Job Vacancies, Businesses, and Study Opportunities.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">🤝</span>
                        <h3>Recruitment Support</h3>
                        <p>Expert CV screening and candidate shortlisting for your organization.</p>
                    </div>
                    <div class="service-card">
                        <span class="service-icon">💼</span>
                        <h3>Corporate Writing</h3>
                        <p>Writing professional business plans and corporate communications.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- WHY CHOOSE US -->
    <section class="why-us" id="why-us">
        <div class="container">
            <div class="section-title reveal">
                <h2>Why Students & Professionals Choose Zisido</h2>
            </div>
            <div class="trust-grid reveal">
                <div class="trust-item">
                    <div class="trust-icon">✅</div>
                    <div class="trust-text">
                        <h4>Expert Consultants & Writers</h4>
                        <p>Our team consists of seasoned academics and industry professionals.</p>
                    </div>
                </div>
                <div class="trust-item">
                    <div class="trust-icon">✅</div>
                    <div class="trust-text">
                        <h4>Confidential & Plagiarism-Free</h4>
                        <p>Your privacy is our priority. We deliver 100% unique, custom work.</p>
                    </div>
                </div>
                <div class="trust-item">
                    <div class="trust-icon">✅</div>
                    <div class="trust-text">
                        <h4>Fast Turnaround Times</h4>
                        <p>Tight deadlines? No problem. We deliver quality work on time.</p>
                    </div>
                </div>
                <div class="trust-item">
                    <div class="trust-icon">✅</div>
                    <div class="trust-text">
                        <h4>Affordable Pricing</h4>
                        <p>Premium advisory services at rates designed for students.</p>
                    </div>
                </div>
                <div class="trust-item">
                    <div class="trust-icon">✅</div>
                    <div class="trust-text">
                        <h4>Turnitin Reports Provided</h4>
                        <p>We provide proof of originality with every academic project.</p>
                    </div>
                </div>
                <div class="trust-item">
                    <div class="trust-icon">✅</div>
                    <div class="trust-text">
                        <h4>Serving Clients Across Malawi</h4>
                        <p>A trusted name from Lilongwe to Blantyre and beyond.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- HOW IT WORKS -->
    <section class="how-it-works">
        <div class="container">
            <div class="section-title reveal">
                <h2>How It Works — Simple & Fast</h2>
            </div>
            <div class="steps-container reveal">
                <div class="step">
                    <div class="step-number">1</div>
                    <span class="service-icon">📱</span>
                    <h3>Contact Us</h3>
                    <p>Send a message on WhatsApp with your request.</p>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <span class="service-icon">📋</span>
                    <h3>Share Requirements</h3>
                    <p>Send your task details, instructions, and deadline.</p>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <span class="service-icon">✨</span>
                    <h3>Quality Delivery</h3>
                    <p>Receive your completed, professionally vetted work.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title reveal">
                <h2>What Our Clients Say</h2>
            </div>
            <div class="testimonial-grid reveal">
                <div class="testimonial-card">
                    <div class="stars">⭐⭐⭐⭐⭐</div>
                    <p class="quote">"Zisido helped me with my final year dissertation. The data analysis was top-notch, and the plagiarism report gave me total peace of mind. Highly recommended!"</p>
                    <div class="client-info">
                        <div class="client-meta">
                            <h4>Chisomo M.</h4>
                            <span>University Student, Malawi</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">⭐⭐⭐⭐⭐</div>
                    <p class="quote">"I was struggling to get interviews until I used their CV writing service. Within two weeks, I had three interview calls. Their professionalism is unmatched."</p>
                    <div class="client-info">
                        <div class="client-meta">
                            <h4>Kondwani K.</h4>
                            <span>HR Professional, Blantyre</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">⭐⭐⭐⭐⭐</div>
                    <p class="quote">"Fast, reliable, and very affordable. They handled my urgent research proposal in just 3 days and it was accepted without any corrections!"</p>
                    <div class="client-info">
                        <div class="client-meta">
                            <h4>Faith T.</h4>
                            <span>Post-Graduate Student</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA BANNER -->
    <section class="cta-banner reveal">
        <div class="container">
            <h2>Ready to Take Your Work to the Next Level?</h2>
            <p>Contact us today on WhatsApp — fast response guaranteed.</p>
            <a href="https://wa.me/265995061815" class="btn btn-navy">Chat With Us on WhatsApp 🚀</a>
        </div>
    </section>

    <!-- FOOTER -->
    <footer id="contact">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-about">
                    <a href="#" class="logo">
                        <span class="brand-main">ZISIDO</span>
                        <span class="brand-sub">Global Advisory</span>
                    </a>
                    <p>Your premier partner for academic excellence and professional career growth. We provide high-impact advisory services for students and professionals across Malawi and the globe.</p>
                </div>
                <div class="footer-links">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#why-us">Why Choose Us</a></li>
                        <li><a href="#testimonials">Testimonials</a></li>
                    </ul>
                </div>
                <div class="footer-contact">
                    <h4>Contact Details</h4>
                    <div class="contact-info-item">
                        <span>📞</span>
                        <p>+265 995 061 815</p>
                    </div>
                    <div class="contact-info-item">
                        <span>💬</span>
                        <p>WhatsApp: +265 995 061 815</p>
                    </div>
                    <div class="contact-info-item">
                        <span>📍</span>
                        <p>Serving Malawi & Beyond</p>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 Zisido Global Advisory. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <!-- WHATSAPP FLOATING BUTTON -->
    <a href="https://wa.me/265995061815" class="whatsapp-float" target="_blank">
        <svg viewBox="0 0 32 32" width="35" height="35" fill="white">
            <path d="M16 0c-8.837 0-16 7.163-16 16 0 2.825 0.737 5.607 2.137 8.046l-2.137 7.954 8.143-2.135c2.378 1.332 5.064 2.035 7.857 2.035 8.837 0 16-7.163 16-16s-7.163-16-16-16zM16 29.333c-2.453 0-4.839-0.641-6.932-1.854l-0.497-0.291-5.132 1.346 1.371-5.105-0.317-0.505c-1.328-2.115-2.025-4.577-2.025-7.124 0-7.352 5.981-13.333 13.333-13.333 7.352 0 13.333 5.981 13.333 13.333s-5.981 13.333-13.333 13.333zM22.846 19.167c-0.375-0.188-2.219-1.094-2.563-1.219s-0.594-0.188-0.844 0.188c-0.25 0.375-0.969 1.219-1.188 1.469s-0.438 0.281-0.813 0.094c-0.375-0.188-1.583-0.583-3.016-1.865-1.115-0.995-1.865-2.224-2.083-2.604s-0.021-0.583 0.167-0.771c0.167-0.167 0.375-0.438 0.563-0.656 0.188-0.219 0.25-0.375 0.375-0.625s0.063-0.469-0.031-0.656c-0.094-0.188-0.844-2.031-1.156-2.781s-0.615-0.646-0.844-0.656c-0.219-0.010-0.469-0.010-0.719-0.010s-0.656 0.094-1 0.469c-0.344 0.375-1.313 1.281-1.313 3.125s1.344 3.625 1.531 3.875c0.188 0.25 2.646 4.042 6.406 5.667 0.896 0.385 1.594 0.615 2.141 0.792 0.896 0.281 1.714 0.24 2.354 0.146 0.714-0.104 2.219-0.906 2.531-1.781s0.313-1.625 0.219-1.781c-0.094-0.156-0.344-0.25-0.719-0.438z"></path>
        </svg>
    </a>

    <!-- JAVASCRIPT -->
    <script>
        // 1. STICKY NAVBAR COLOR CHANGE
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 50) {
                nav.classList.add('scrolled');
            } else {
                nav.classList.remove('scrolled');
            }
        });

        // 2. MOBILE MENU TOGGLE
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('show');
            hamburger.textContent = navLinks.classList.contains('show') ? '✕' : '☰';
        });

        // Close mobile menu when link is clicked
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('show');
                hamburger.textContent = '☰';
            });
        });

        // 3. SCROLL REVEAL ANIMATION (Intersection Observer)
        const revealElements = document.querySelectorAll('.reveal');
        
        const revealObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, { threshold: 0.1 });

        revealElements.forEach(el => revealObserver.observe(el));

        // 4. ACTIVE LINK HIGHLIGHTING
        const sections = document.querySelectorAll('section');
        const navItems = document.querySelectorAll('.nav-links a');

        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 100) {
                    current = section.getAttribute('id');
                }
            });

            navItems.forEach(item => {
                item.classList.remove('active');
                if (item.getAttribute('href').includes(current)) {
                    item.classList.add('active');
                }
            });
        });

        // 5. TESTIMONIALS SLIDER (Simple Mobile Rotation)
        let touchStartX = 0;
        let touchEndX = 0;
        const slider = document.querySelector('.testimonial-grid');

        slider.addEventListener('touchstart', e => {
            touchStartX = e.changedTouches[0].screenX;
        });

        slider.addEventListener('touchend', e => {
            touchEndX = e.changedTouches[0].screenX;
            handleSwipe();
        });

        function handleSwipe() {
            if (touchStartX - touchEndX > 50) {
                // Swiped left
                slider.scrollBy({ left: 300, behavior: 'smooth' });
            }
            if (touchEndX - touchStartX > 50) {
                // Swiped right
                slider.scrollBy({ left: -300, behavior: 'smooth' });
            }
        }
    </script>
</body>
</html>
