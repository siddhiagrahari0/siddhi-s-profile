<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Siddhi Agrahari - UI/UX Designer, Web Developer & Digital Marketing Executive. 18-year-old creative professional specializing in modern design, development, and digital marketing.">
    <meta name="author" content="Siddhi Agrahari">
    <meta name="keywords" content="UI/UX Designer, Web Developer, Digital Marketing, Portfolio, Siddhi Agrahari">
    <title>Siddhi Agrahari | UI/UX Designer & Digital Marketer</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #0a0a0f;
            color: #e2e8f0;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        .container {
            max-width: 1300px;
            margin: 0 auto;
            padding: 0 32px;
        }

        /* Glassmorphism Card */
        .glass-card {
            background: rgba(18, 18, 28, 0.85);
            backdrop-filter: blur(12px);
            border-radius: 28px;
            border: 1px solid rgba(99, 102, 241, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            padding: 28px;
            transition: all 0.4s cubic-bezier(0.2, 0.9, 0.4, 1.1);
        }

        .glass-card:hover {
            transform: translateY(-6px);
            border-color: rgba(99, 102, 241, 0.4);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }

        /* Buttons */
        .btn-primary {
            background: linear-gradient(135deg, #6366f1, #a855f7);
            color: white;
            padding: 14px 32px;
            border-radius: 48px;
            text-decoration: none;
            font-weight: 600;
            display: inline-block;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(99, 102, 241, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(139, 92, 246, 0.4);
            background: linear-gradient(135deg, #7c3aed, #c026d3);
        }

        .btn-outline {
            background: transparent;
            border: 1.5px solid #8b5cf6;
            color: #c4b5fd;
            padding: 12px 30px;
            border-radius: 48px;
            text-decoration: none;
            font-weight: 600;
            display: inline-block;
            transition: all 0.3s;
        }

        .btn-outline:hover {
            background: rgba(139, 92, 246, 0.15);
            border-color: #a855f7;
            color: white;
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            padding: 100px 0 60px;
            text-align: center;
            position: relative;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(99, 102, 241, 0.15);
            backdrop-filter: blur(8px);
            padding: 8px 20px;
            border-radius: 60px;
            font-size: 0.85rem;
            font-weight: 500;
            margin-bottom: 24px;
            border: 1px solid rgba(139, 92, 246, 0.3);
            color: #a78bfa;
        }

        .hero h1 {
            font-size: 4.2rem;
            font-weight: 800;
            background: linear-gradient(135deg, #ffffff, #a78bfa, #6366f1);
            background-size: 200% auto;
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: shimmer 3s linear infinite;
        }

        @keyframes shimmer {
            0% { background-position: 0% 50%; }
            100% { background-position: 200% 50%; }
        }

        .tagline {
            font-size: 1.6rem;
            font-weight: 600;
            background: linear-gradient(135deg, #c4b5fd, #818cf8);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin: 16px 0;
        }

        /* Graphic Stacks - Skill Icons */
        .stack-icons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 40px 0 20px;
        }

        .stack-icon {
            background: rgba(25, 25, 40, 0.8);
            backdrop-filter: blur(8px);
            border-radius: 20px;
            padding: 12px 20px;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            font-weight: 600;
            border: 1px solid rgba(99, 102, 241, 0.25);
            transition: all 0.3s;
        }

        .stack-icon i {
            font-size: 1.8rem;
            color: #8b5cf6;
        }

        .stack-icon:hover {
            transform: translateY(-4px);
            border-color: #a855f7;
            background: rgba(99, 102, 241, 0.2);
        }

        /* Skills with progress */
        .skill-item {
            margin-bottom: 24px;
        }
        .skill-name {
            font-weight: 600;
            margin-bottom: 8px;
            display: flex;
            justify-content: space-between;
        }
        .progress-bar {
            background: rgba(255,255,255,0.06);
            border-radius: 20px;
            height: 10px;
            overflow: hidden;
        }
        .progress-fill {
            background: linear-gradient(90deg, #6366f1, #c084fc);
            width: 0%;
            height: 100%;
            border-radius: 20px;
            transition: width 1.2s ease-out;
            position: relative;
            overflow: hidden;
        }
        .progress-fill::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            animation: shine 2s infinite;
        }

        /* Portfolio Image Cards - Realistic Photos */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 28px;
            margin-top: 40px;
        }

        .portfolio-card {
            background: rgba(18, 18, 28, 0.8);
            backdrop-filter: blur(8px);
            border-radius: 24px;
            overflow: hidden;
            border: 1px solid rgba(99, 102, 241, 0.2);
            transition: all 0.3s;
        }

        .portfolio-card:hover {
            transform: translateY(-8px);
            border-color: rgba(139, 92, 246, 0.5);
            box-shadow: 0 20px 35px rgba(0, 0, 0, 0.4);
        }

        .portfolio-img {
            width: 100%;
            height: 240px;
            object-fit: cover;
            display: block;
        }

        .portfolio-info {
            padding: 20px;
        }

        .portfolio-info h3 {
            margin-bottom: 8px;
            font-size: 1.2rem;
            color: #e2e8f0;
        }

        .portfolio-info p {
            color: #a0aec0;
            font-size: 0.9rem;
        }

        .portfolio-tag {
            display: inline-block;
            background: rgba(99, 102, 241, 0.2);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.7rem;
            margin-top: 12px;
            color: #a78bfa;
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 28px;
            margin-top: 40px;
        }

        .service-card {
            background: rgba(18, 18, 28, 0.8);
            backdrop-filter: blur(8px);
            border-radius: 24px;
            padding: 28px;
            border: 1px solid rgba(99, 102, 241, 0.2);
            transition: all 0.3s;
            text-align: center;
        }

        .service-card:hover {
            transform: translateY(-5px);
            border-color: rgba(139, 92, 246, 0.4);
            background: rgba(25, 25, 45, 0.9);
        }

        .service-card i {
            font-size: 2.5rem;
            color: #8b5cf6;
            margin-bottom: 16px;
        }

        .service-card h3 {
            margin-bottom: 12px;
            font-size: 1.3rem;
        }

        /* Testimonials with Images */
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 28px;
            margin-top: 40px;
        }

        .testimonial-card {
            background: rgba(18, 18, 28, 0.8);
            backdrop-filter: blur(8px);
            border-radius: 24px;
            padding: 24px;
            border: 1px solid rgba(99, 102, 241, 0.2);
            transition: all 0.3s;
            display: flex;
            flex-direction: column;
        }

        .testimonial-card:hover {
            transform: translateY(-5px);
            border-color: rgba(139, 92, 246, 0.4);
        }

        .client-row {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 16px;
        }

        .client-avatar {
            width: 55px;
            height: 55px;
            border-radius: 50%;
            object-fit: cover;
            border: 2px solid #8b5cf6;
        }

        .client-info h4 {
            font-size: 1rem;
            margin-bottom: 4px;
        }

        .client-info p {
            font-size: 0.8rem;
            color: #a78bfa;
        }

        .stars {
            color: #fbbf24;
            margin: 12px 0;
            font-size: 1rem;
        }

        .testimonial-text {
            font-size: 0.95rem;
            line-height: 1.5;
            color: #cbd5e1;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 28px;
            margin-top: 40px;
        }

        /* Contact & Social */
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin: 40px 0;
        }
        .contact-item {
            display: flex;
            align-items: center;
            gap: 16px;
            font-size: 1.1rem;
            flex-wrap: wrap;
        }
        .contact-item i {
            width: 40px;
            height: 40px;
            background: rgba(99, 102, 241, 0.12);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 60px;
            color: #a78bfa;
        }
        .social-links {
            margin-top: 20px;
        }
        .social-links a {
            color: #c4b5fd;
            font-size: 1.8rem;
            margin-right: 24px;
            transition: all 0.3s;
            display: inline-block;
        }
        .social-links a:hover {
            color: #a855f7;
            transform: translateY(-4px);
        }

        /* Copy button */
        .copy-btn {
            background: rgba(99, 102, 241, 0.15);
            border: 1px solid rgba(139, 92, 246, 0.3);
            border-radius: 8px;
            padding: 6px 14px;
            font-size: 0.75rem;
            cursor: pointer;
            transition: all 0.2s;
            color: #c4b5fd;
            font-weight: 500;
        }
        .copy-btn:hover {
            background: rgba(139, 92, 246, 0.4);
            color: white;
        }

        /* Toast Notification */
        .toast-msg {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(135deg, #6366f1, #a855f7);
            color: white;
            padding: 12px 28px;
            border-radius: 48px;
            font-size: 0.9rem;
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s;
            pointer-events: none;
        }

        footer {
            text-align: center;
            padding: 40px 0;
            color: #6b7280;
            border-top: 1px solid rgba(99, 102, 241, 0.15);
            margin-top: 60px;
        }

        .nav-links {
            display: flex;
            justify-content: center;
            gap: 32px;
            padding: 20px 0;
            flex-wrap: wrap;
        }
        .nav-links a {
            color: #c4b5fd;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: #a855f7;
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.2rem; }
            .tagline { font-size: 1.1rem; }
            .container { padding: 0 20px; }
            .stack-icon { padding: 8px 14px; font-size: 0.85rem; }
            .portfolio-img { height: 180px; }
        }
    </style>
</head>
<body>

<div class="container">
    <!-- Navigation -->
    <div class="nav-links">
        <a href="#">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#services">Services</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#contact">Contact</a>
    </div>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-badge">
            <i class="fas fa-star-of-life"></i> Creative Professional · Open for Work
        </div>
        <h1>Siddhi Agrahari</h1>
        <div class="tagline">UI/UX Designer | Web Developer | Digital Marketing Executive</div>
        <p style="max-width: 650px; margin: 20px auto; color: #a0aec0;">Passionate about creating user-friendly designs, high-converting websites, and result-driven digital marketing strategies.</p>
        
        <div class="stack-icons">
            <div class="stack-icon"><i class="fab fa-figma"></i> Figma</div>
            <div class="stack-icon"><i class="fab fa-html5"></i> HTML/CSS</div>
            <div class="stack-icon"><i class="fab fa-google"></i> Google Ads</div>
            <div class="stack-icon"><i class="fab fa-canva"></i> Canva</div>
            <div class="stack-icon"><i class="fas fa-chart-line"></i> SEO</div>
            <div class="stack-icon"><i class="fas fa-envelope"></i> Email Marketing</div>
        </div>

        <div style="margin-top: 32px;">
            <a href="#portfolio" class="btn-primary">✨ View Portfolio</a>
            <a href="#" class="btn-outline" style="margin-left: 16px;">📄 Download Resume</a>
            <a href="#contact" class="btn-outline" style="margin-left: 16px;">💬 Contact Me</a>
        </div>
    </section>

    <!-- About Me -->
    <section class="glass-card" id="about" style="margin: 20px 0 40px;">
        <h2 style="margin-bottom: 16px; display: flex; align-items: center; gap: 12px;"><i class="fas fa-user-astronaut" style="color:#8b5cf6;"></i> About Me</h2>
        <p style="font-size: 1.05rem; line-height: 1.7;">Siddhi Agrahari is a <strong style="color:#a78bfa;">12th pass young professional</strong> with expertise in UI/UX Design, Web Development, Graphic Design, Digital Marketing, Google Ads, Email Marketing, and Telecalling. At just <strong style="color:#a78bfa;">18 years old</strong>, Siddhi combines creativity, technical skills, and marketing knowledge to help businesses grow online. 🚀</p>
    </section>

    <!-- Skills -->
    <section id="skills">
        <h2 style="margin: 40px 0 10px;"><i class="fas fa-code-branch"></i> Technical Stacks & Skills</h2>
        <div class="skills-grid">
            <div class="glass-card">
                <div class="skill-item"><div class="skill-name">UI/UX Design <span>95%</span></div><div class="progress-bar"><div class="progress-fill" style="width: 95%;"></div></div></div>
                <div class="skill-item"><div class="skill-name">Web Development <span>90%</span></div><div class="progress-bar"><div class="progress-fill" style="width: 90%;"></div></div></div>
                <div class="skill-item"><div class="skill-name">Digital Marketing <span>92%</span></div><div class="progress-bar"><div class="progress-fill" style="width: 92%;"></div></div></div>
                <div class="skill-item"><div class="skill-name">SEO <span>85%</span></div><div class="progress-bar"><div class="progress-fill" style="width: 85%;"></div></div></div>
            </div>
            <div class="glass-card">
                <div class="skill-item"><div class="skill-name">Google Ads <span>88%</span></div><div class="progress-bar"><div class="progress-fill" style="width: 88%;"></div></div></div>
                <div class="skill-item"><div class="skill-name">Email Marketing <span>87%</span></div><div class="progress-bar"><div class="progress-fill" style="width: 87%;"></div></div></div>
                <div class="skill-item"><div class="skill-name">Canva Design <span>96%</span></div><div class="progress-bar"><div class="progress-fill" style="width: 96%;"></div></div></div>
                <div class="skill-item"><div class="skill-name">Telecalling <span>90%</span></div><div class="progress-bar"><div class="progress-fill" style="width: 90%;"></div></div></div>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section id="services">
        <h2 style="margin: 60px 0 20px;"><i class="fas fa-cogs"></i> Services I Offer</h2>
        <div class="services-grid">
            <div class="service-card"><i class="fas fa-laptop-code"></i><h3>Website Design & Development</h3><p>Responsive, fast, and modern websites tailored to your brand.</p></div>
            <div class="service-card"><i class="fas fa-paint-brush"></i><h3>UI/UX Prototyping</h3><p>User flows, wireframes, interactive prototypes in Figma.</p></div>
            <div class="service-card"><i class="fas fa-chart-simple"></i><h3>Google Ads Management</h3><p>High-ROI campaigns, keyword research, and optimization.</p></div>
            <div class="service-card"><i class="fas fa-envelope-open-text"></i><h3>Email Marketing</h3><p>Automations, newsletters, and drip campaigns.</p></div>
            <div class="service-card"><i class="fas fa-search"></i><h3>SEO Optimization</h3><p>On-page, off-page, and technical SEO strategies.</p></div>
            <div class="service-card"><i class="fas fa-phone-alt"></i><h3>Telecalling Support</h3><p>Lead generation, client follow-ups, and sales support.</p></div>
        </div>
    </section>

    <!-- Portfolio with Realistic Photos -->
    <section id="portfolio">
        <h2 style="margin: 60px 0 20px;"><i class="fas fa-th-large"></i> Latest Portfolio</h2>
        <div class="portfolio-grid">
            <div class="portfolio-card">
                <img src="https://images.unsplash.com/photo-1586717791821-3f44a563fa4c?w=600&h=400&fit=crop" alt="Mobile App UI Design" class="portfolio-img">
                <div class="portfolio-info">
                    <h3>📱 Mobile App UI Design</h3>
                    <p>Fintech app with smooth animations and modern UI.</p>
                    <span class="portfolio-tag">UI/UX</span>
                </div>
            </div>
            <div class="portfolio-card">
                <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?w=600&h=400&fit=crop" alt="Business Website Development" class="portfolio-img">
                <div class="portfolio-info">
                    <h3>🌐 Business Website Dev</h3>
                    <p>Full-stack corporate site with CMS integration.</p>
                    <span class="portfolio-tag">Web Dev</span>
                </div>
            </div>
            <div class="portfolio-card">
                <img src="https://images.unsplash.com/photo-1611162617213-7d7a39e9b1d7?w=600&h=400&fit=crop" alt="Instagram Post Designs" class="portfolio-img">
                <div class="portfolio-info">
                    <h3>📸 Instagram Post Designs</h3>
                    <p>20+ viral graphics for brand campaigns.</p>
                    <span class="portfolio-tag">Graphic Design</span>
                </div>
            </div>
            <div class="portfolio-card">
                <img src="https://images.unsplash.com/photo-1563986768609-322da13575f3?w=600&h=400&fit=crop" alt="Google Ads Campaign" class="portfolio-img">
                <div class="portfolio-info">
                    <h3>📊 Google Ads Campaign</h3>
                    <p>30% lower CPA achieved for e-commerce client.</p>
                    <span class="portfolio-tag">Marketing</span>
                </div>
            </div>
            <div class="portfolio-card">
                <img src="https://images.unsplash.com/photo-1526948128573-703ee1aeb6fa?w=600&h=400&fit=crop" alt="Email Marketing Template" class="portfolio-img">
                <div class="portfolio-info">
                    <h3>✉️ Email Marketing Template</h3>
                    <p>45% open rate design for newsletter.</p>
                    <span class="portfolio-tag">Email Marketing</span>
                </div>
            </div>
            <div class="portfolio-card">
                <img src="https://images.unsplash.com/photo-1581291518633-83b4ebd1d83e?w=600&h=400&fit=crop" alt="Landing Page Design" class="portfolio-img">
                <div class="portfolio-info">
                    <h3>🚀 Landing Page Design</h3>
                    <p>High-converting SaaS landing page.</p>
                    <span class="portfolio-tag">Web Design</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Me -->
    <section class="glass-card" style="margin: 40px 0;">
        <h2 style="margin-bottom: 24px;"><i class="fas fa-medal"></i> Why Choose Me?</h2>
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px,1fr)); gap: 20px;">
            <div>🎨 Creative & Innovative Designs</div>
            <div>📈 Marketing-Focused Strategies</div>
            <div>👥 User-Friendly Interfaces</div>
            <div>💬 Professional Communication</div>
            <div>💰 Affordable & Reliable Services</div>
            <div>⚡ Fast Turnaround Time</div>
        </div>
    </section>

    <!-- Testimonials with Client Photos -->
    <section>
        <h2><i class="fas fa-star"></i> Client Love</h2>
        <div class="testimonials-grid">
            <div class="testimonial-card">
                <div class="client-row">
                    <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Ankit Sharma" class="client-avatar">
                    <div class="client-info">
                        <h4>Ankit Sharma</h4>
                        <p>Founder, TechStart</p>
                    </div>
                </div>
                <div class="stars">★★★★★</div>
                <p class="testimonial-text">“Siddhi redesigned our entire brand identity — traffic increased 60%! Her UI/UX skills are outstanding for an 18-year-old.”</p>
            </div>
            <div class="testimonial-card">
                <div class="client-row">
                    <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Priya Verma" class="client-avatar">
                    <div class="client-info">
                        <h4>Priya Verma</h4>
                        <p>Marketing Head, GrowMore</p>
                    </div>
                </div>
                <div class="stars">★★★★★</div>
                <p class="testimonial-text">“Very professional Google Ads expert. ROI doubled in 2 months. Highly recommend Siddhi for digital marketing.”</p>
            </div>
            <div class="testimonial-card">
                <div class="client-row">
                    <img src="https://randomuser.me/api/portraits/men/45.jpg" alt="Rajat Mishra" class="client-avatar">
                    <div class="client-info">
                        <h4>Rajat Mishra</h4>
                        <p>CEO, CreativeHub</p>
                    </div>
                </div>
                <div class="stars">★★★★★</div>
                <p class="testimonial-text">“Incredible work ethic and design sense. Siddhi delivered our website ahead of schedule with perfect execution.”</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="glass-card" id="contact" style="margin: 50px 0;">
        <h2><i class="fas fa-paper-plane"></i> Let's Connect</h2>
        <div class="contact-info">
            <div class="contact-item">
                <i class="fas fa-envelope"></i>
                <span><strong>Email:</strong> siddhiagrahari773@gmail.com</span>
                <button class="copy-btn" data-copy="siddhiagrahari773@gmail.com">📋 Copy</button>
            </div>
            <div class="contact-item">
                <i class="fas fa-phone-alt"></i>
                <span><strong>Phone:</strong> +91 8400755424</span>
                <button class="copy-btn" data-copy="8400755424">📋 Copy</button>
            </div>
            <div class="contact-item">
                <i class="fas fa-map-marker-alt"></i>
                <span><strong>Location:</strong> Lucknow, Uttar Pradesh, India</span>
            </div>
        </div>
        <div class="social-links">
            <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
            <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
            <a href="#" aria-label="Behance"><i class="fab fa-behance"></i></a>
            <a href="#" aria-label="GitHub"><i class="fab fa-github"></i></a>
            <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
        </div>
    </section>
</div>

<footer>
    <p>© 2026 Siddhi Agrahari. All Rights Reserved. | Built with <i class="fas fa-heart" style="color:#f472b6;"></i> & Gradient Magic</p>
</footer>

<div id="toast" class="toast-msg">✅ Copied to clipboard!</div>

<script>
    // Animate progress bars
    const progressBars = document.querySelectorAll('.progress-fill');
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if(entry.isIntersecting) {
                const bar = entry.target;
                const width = bar.style.width;
                bar.style.width = '0%';
                setTimeout(() => { bar.style.width = width; }, 100);
                observer.unobserve(bar);
            }
        });
    }, { threshold: 0.5 });
    progressBars.forEach(bar => observer.observe(bar));

    // Copy to clipboard
    const toast = document.getElementById('toast');
    const copyButtons = document.querySelectorAll('.copy-btn');
    
    copyButtons.forEach(btn => {
        btn.addEventListener('click', async () => {
            const textToCopy = btn.getAttribute('data-copy');
            try {
                await navigator.clipboard.writeText(textToCopy);
                toast.style.opacity = '1';
                setTimeout(() => { toast.style.opacity = '0'; }, 2000);
            } catch (err) {
                const textarea = document.createElement('textarea');
                textarea.value = textToCopy;
                document.body.appendChild(textarea);
                textarea.select();
                document.execCommand('copy');
                document.body.removeChild(textarea);
                toast.style.opacity = '1';
                setTimeout(() => { toast.style.opacity = '0'; }, 2000);
            }
        });
    });

    // Smooth scroll
    document.querySelectorAll('.nav-links a').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            const href = this.getAttribute('href');
            if (href && href !== '#' && href.startsWith('#')) {
                e.preventDefault();
                const target = document.querySelector(href);
                if (target) target.scrollIntoView({ behavior: 'smooth' });
            }
        });
    });
</script>
</body>
</html># siddhi-s-profile
