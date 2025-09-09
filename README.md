# State-of-learners
welcome
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>State of Learner - Mathematics Excellence</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        :root {
            --primary-dark: #1a4b5f;
            --primary: #2a7a94;
            --primary-light: #48a0b9;
            --accent: #ff7e5f;
            --accent-dark: #e86a4c;
            --light: #f8f9fa;
            --dark: #2d3436;
            --gray: #636e72;
            --light-gray: #dfe6e9;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.08);
            --card-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: var(--light);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(to right, var(--primary-dark), var(--primary));
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }
       
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
       
        .logo-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }
       
        .logo {
            font-size: 2.5rem;
            color: var(--accent);
        }
       
        .logo-text {
            display: flex;
            flex-direction: column;
        }
       
        .logo-text h1 {
            font-size: 28px;
            font-weight: 700;
            letter-spacing: 1px;
            color: white;
            line-height: 1;
        }
       
        .logo-text span {
            color: var(--accent);
            font-size: 14px;
            letter-spacing: 1.5px;
            margin-top: 3px;
        }
       
        .nav-toggle {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 24px;
            cursor: pointer;
        }
       
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }
       
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
            padding: 5px 0;
            font-size: 16px;
        }
       
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: var(--transition);
        }
       
        nav ul li a:hover::after {
            width: 100%;
        }

        /* Hero Section with Lazy Loading */
        .hero {
            padding: 120px 0;
            background: linear-gradient(rgba(26, 75, 95, 0.85), rgba(26, 75, 95, 0.85));
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
       
        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0;
            transition: opacity 1s ease;
            background: url('https://images.unsplash.com/photo-1522881193457-37ae97c905bf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80') no-repeat center center/cover;
        }
       
        .hero-bg.loaded {
            opacity: 1;
        }
       
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }
       
        .hero h2 {
            font-size: 3.2rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
        }
       
        .hero p {
            font-size: 1.4rem;
            margin-bottom: 30px;
            opacity: 0.95;
        }
       
        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 14px 32px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: var(--transition);
            box-shadow: var(--shadow);
            border: none;
            cursor: pointer;
            margin: 10px;
        }
       
        .btn:hover {
            background: var(--accent-dark);
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
        }
       
        .btn-outline {
            background: transparent;
            border: 2px solid white;
            color: white;
        }
       
        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }

        /* Sections */
        section {
            padding: 100px 0;
        }
       
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            color: var(--primary-dark);
            position: relative;
        }
       
        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--accent);
            margin: 15px auto;
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }
       
        .about-text {
            flex: 1;
        }
       
        .about-text h3 {
            font-size: 28px;
            color: var(--primary-dark);
            margin-bottom: 20px;
        }
       
        .about-text p {
            margin-bottom: 20px;
            line-height: 1.8;
        }
       
        .stats-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-top: 40px;
        }
       
        .stat-item {
            text-align: center;
            padding: 25px;
            background: white;
            border-radius: 8px;
            box-shadow: var(--card-shadow);
        }
       
        .stat-number {
            font-size: 36px;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 10px;
        }
       
        .stat-label {
            font-size: 16px;
            color: var(--gray);
        }

        /* Features Section */
        .features {
            padding: 80px 0;
            background: white;
        }
       
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
       
        .feature-card {
            background: var(--light);
            padding: 35px 30px;
            border-radius: 12px;
            text-align: center;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border-top: 4px solid var(--primary);
        }
       
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
       
        .feature-card i {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
       
        .feature-card h3 {
            margin-bottom: 15px;
            color: var(--primary-dark);
        }
       
        .feature-card p {
            color: var(--gray);
            line-height: 1.7;
        }

        /* Courses Section */
        .courses {
            background: var(--light);
        }
       
        .course-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }
       
        .course-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border-top: 4px solid var(--primary);
            height: 100%;
            display: flex;
            flex-direction: column;
        }
       
        .course-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
       
        .course-image {
            height: 200px;
            overflow: hidden;
        }
       
        .course-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
       
        .course-card:hover .course-image img {
            transform: scale(1.1);
        }
       
        .course-content {
            padding: 25px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
       
        .course-content h3 {
            font-size: 22px;
            color: var(--primary);
            margin-bottom: 15px;
        }
       
        .course-content p {
            margin-bottom: 25px;
            color: var(--gray);
            flex-grow: 1;
        }
       
        .course-features {
            margin-bottom: 20px;
        }
       
        .course-features li {
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
       
        .course-features i {
            color: var(--accent);
            font-size: 16px;
        }

        /* Testimonials Section */
        .testimonials {
            background: linear-gradient(to right, #f5f5f7, #e8eaf6);
        }
       
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
       
        .testimonial-card {
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: var(--card-shadow);
            position: relative;
        }
       
        .testimonial-card::before {
            content: '"';
            font-size: 60px;
            color: var(--primary);
            opacity: 0.2;
            position: absolute;
            top: 20px;
            left: 20px;
            line-height: 1;
        }
       
        .testimonial-text {
            margin-bottom: 20px;
            font-style: italic;
            color: #555;
            line-height: 1.7;
        }
       
        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }
       
        .author-image {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
        }
       
        .author-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
       
        .author-details h4 {
            font-size: 18px;
            color: var(--primary-dark);
            margin-bottom: 5px;
        }
       
        .author-details p {
            font-size: 14px;
            color: var(--gray);
        }

        /* Login Portal */
        .login-portal {
            padding: 80px 0;
            background: white;
        }
       
        .portal-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 40px;
        }
       
        .portal-info {
            flex: 1;
            min-width: 300px;
        }
       
        .portal-form {
            flex: 1;
            background: var(--light);
            padding: 40px;
            border-radius: 15px;
            box-shadow: var(--card-shadow);
            min-width: 300px;
        }
       
        .form-group {
            margin-bottom: 20px;
        }
       
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--primary-dark);
        }
       
        .form-group input,
        .form-group select {
            width: 100%;
            padding: 15px;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            font-size: 1rem;
            transition: var(--transition);
        }
       
        .form-group input:focus,
        .form-group select:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 2px rgba(42, 122, 148, 0.2);
        }
       
        .submit-btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 15px;
            border-radius: 8px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            width: 100%;
        }
       
        .submit-btn:hover {
            background: var(--primary-dark);
        }

        /* QR Code Section */
        .qr-section {
            background: linear-gradient(to right, var(--primary-dark), var(--primary));
            color: white;
            padding: 80px 0;
            text-align: center;
        }
       
        .qr-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
       
        .qr-code {
            width: 180px;
            height: 180px;
            background: white;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 20px 0;
            border: 2px solid var(--accent);
            border-radius: 10px;
            overflow: hidden;
            padding: 10px;
        }
       
        .qr-code img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
       
        .payment-options {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
       
        .payment-option {
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 14px;
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        /* Contact Section - Updated with Map and Larger Message Box */
        .contact {
            background: white;
        }
       
        .contact-content {
            display: flex;
            gap: 40px;
        }
       
        .contact-info {
            flex: 1;
        }
       
        .contact-form {
            flex: 1;
        }
       
        .contact-info h3, .contact-form h3 {
            font-size: 28px;
            color: var(--primary-dark);
            margin-bottom: 25px;
        }
       
        .info-item {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }
       
        .info-icon {
            width: 50px;
            height: 50px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            margin-right: 15px;
            flex-shrink: 0;
        }
       
        .info-content h4 {
            font-size: 18px;
            margin-bottom: 5px;
        }
       
        .info-content p {
            color: var(--gray);
        }
       
        /* Map Container */
        .map-container {
            margin-top: 30px;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            height: 400px;
        }
       
        .map-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
       
        /* Larger Message Box */
        .form-group textarea {
            min-height: 200px; /* Increased from the previous value */
            resize: vertical;
        }

        /* Footer */
        footer {
            background: var(--primary-dark);
            color: white;
            padding: 80px 0 30px;
        }
       
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
       
        .footer-section h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--accent);
        }
       
        .footer-section p, .footer-section li {
            margin-bottom: 10px;
            opacity: 0.9;
        }
       
        .footer-section ul {
            list-style: none;
        }
       
        .footer-section a {
            color: white;
            text-decoration: none;
            transition: var(--transition);
        }
       
        .footer-section a:hover {
            color: var(--accent);
        }
       
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
       
        .social-icons a {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            transition: var(--transition);
            font-size: 18px;
        }
       
        .social-icons a:hover {
            background: var(--accent);
            color: var(--primary-dark);
            transform: translateY(-3px);
        }
       
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 15px;
            opacity: 0.8;
        }

        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            box-shadow: var(--shadow);
            transition: var(--transition);
            z-index: 999;
            opacity: 0;
            visibility: hidden;
        }
       
        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }
       
        .back-to-top:hover {
            background: var(--primary-dark);
            transform: translateY(-5px);
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.7);
        }
       
        .modal-content {
            background-color: white;
            margin: 10% auto;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 30px rgba(0, 0, 0, 0.3);
            width: 80%;
            max-width: 600px;
            position: relative;
            animation: modalopen 0.5s;
        }
       
        @keyframes modalopen {
            from {opacity: 0; transform: translateY(-60px);}
            to {opacity: 1; transform: translateY(0);}
        }
       
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            position: absolute;
            top: 15px;
            right: 25px;
            cursor: pointer;
        }
       
        .close:hover {
            color: var(--primary-dark);
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content, .contact-content {
                flex-direction: column;
            }
           
            .hero h2 {
                font-size: 2.8rem;
            }
           
            .header-container {
                flex-direction: column;
                text-align: center;
                gap: 15px;
            }
           
            nav ul {
                justify-content: center;
                flex-wrap: wrap;
            }
           
            .stats-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
       
        @media (max-width: 768px) {
            .logo-text h1 {
                font-size: 24px;
            }
           
            .logo-text span {
                font-size: 12px;
            }
           
            .hero {
                padding: 80px 0;
            }
           
            .hero h2 {
                font-size: 2.2rem;
            }
           
            .hero p {
                font-size: 1.2rem;
            }
           
            .section-title {
                font-size: 28px;
            }
           
            .header-container {
                flex-direction: row;
                justify-content: space-between;
            }
           
            .nav-toggle {
                display: block;
            }
           
            nav {
                display: none;
                width: 100%;
            }
           
            nav.active {
                display: block;
            }
           
            nav ul {
                flex-direction: column;
                gap: 10px;
                margin-top: 20px;
            }
           
            .portal-container {
                flex-direction: column;
            }
           
            .stats-container {
                grid-template-columns: 1fr;
            }
           
            .map-container {
                height: 300px;
            }
        }
       
        @media (max-width: 576px) {
            .container {
                padding: 0 15px;
            }
           
            section {
                padding: 80px 0;
            }
           
            .hero h2 {
                font-size: 1.8rem;
            }
           
            .course-grid, .features-grid, .testimonial-grid {
                grid-template-columns: 1fr;
            }
           
            .modal-content {
                padding: 25px;
            }
           
            .back-to-top {
                bottom: 20px;
                right: 20px;
                width: 40px;
                height: 40px;
            }
           
            .section-title {
                font-size: 24px;
            }
           
            .payment-options {
                flex-direction: column;
                align-items: center;
            }
           
            .btn {
                padding: 12px 25px;
                font-size: 1rem;
            }
           
            .map-container {
                height: 250px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo-container">
                <div class="logo">
                    <i class="fas fa-pencil-alt"></i>
                </div>
                <div class="logo-text">
                    <h1>State of Learner</h1>
                    <span>Learn with Skills</span>
                </div>
            </div>
            <button class="nav-toggle" aria-label="Toggle navigation">
                <i class="fas fa-bars"></i>
            </button>
            <nav id="main-nav">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#courses">Courses</a></li>
                    <li><a href#features">Features</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#login">Login</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section with Lazy Loading -->
    <section id="home" class="hero">
        <div class="hero-bg" id="hero-bg"></div>
        <div class="container hero-content">
            <h2>Excel in Mathematics with Expert Guidance</h2>
            <p>Specialized coaching for Class 8-12 and competitive exams with proven results</p>
            <div class="hero-buttons">
                <a href="#login" class="btn">Student Login Portal</a>
                <a href="#courses" class="btn btn-outline">View Our Courses</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About Us</h2>
                <p>Learn more about our mission, values, and what makes us different</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Transforming Mathematics Education Since 2014</h3>
                    <p>State of Learner is a premier mathematics coaching institute dedicated to providing exceptional education for students preparing for Class 8-12 board exams and various competitive examinations.</p>
                    <p>Founded by Navil Singh, our institute has a proven track record of producing top performers in mathematics. We believe in nurturing mathematical thinking through personalized attention and innovative teaching methodologies.</p>
                    <p>Our experienced faculty, comprehensive study materials, and regular assessment system ensure that our students are well-prepared to excel in their academic pursuits and achieve their career goals.</p>
                    <a href="#contact" class="btn">Get In Touch</a>

                    <div class="stats-container">
                        <div class="stat-item">
                            <div class="stat-number">1000+</div>
                            <div class="stat-label">Students Trained</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">94%</div>
                            <div class="stat-label">Success Rate</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">10+</div>
                            <div class="stat-label">Years of Excellence</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Courses Section -->
    <section id="courses" class="courses">
        <div class="container">
            <div class="section-title">
                <h2>Our Courses</h2>
                <p>Comprehensive mathematics programs designed for academic excellence</p>
            </div>
            <div class="course-grid">
                <div class="course-card">
                    <div class="course-image">
                        <img src="https://images.unsplash.com/photo-1635070041078-e363dbe005cb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Class 8-10">
                    </div>
                    <div class="course-content">
                        <h3>Class 8-10 Mathematics</h3>
                        <p>Comprehensive coaching for CBSE and ICSE boards with focus on concept clarity and application.</p>
                        <ul class="course-features">
                            <li><i class="fas fa-check-circle"></i> Foundation building</li>
                            <li><i class="fas fa-check-circle"></i> Regular tests and assessments</li>
                            <li><i class="fas fa-check-circle"></i> Doubt clearing sessions</li>
                        </ul>
                        <a href="#" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="course-card">
                    <div class="course-image">
                        <img src="https://images.unsplash.com/photo-1532094349884-543bc11b234d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Class 11-12">
                    </div>
                    <div class="course-content">
                        <h3>Class 11-12 Mathematics</h3>
                        <p>Advanced mathematics with focus on board exams and competitive entrance examinations.</p>
                        <ul class="course-features">
                            <li><i class="fas fa-check-circle"></i> Advanced problem solving</li>
                            <li><i class="fas fa-check-circle"></i> Board exam preparation</li>
                            <li><i class="fas fa-check-circle"></i> Mock test series</li>
                        </ul>
                        <a href="#" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="course-card">
                    <div class="course-image">
                        <img src="https://images.unsplash.com/photo-1571260899304-425eee4c7efc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Competitive Exams">
                    </div>
                    <div class="course-content">
                        <h3>Competitive Exams Preparation</h3>
                        <p>Rigorous training program for engineering, medical, and other entrance examinations.</p>
                        <ul class="course-features">
                            <li><i class="fas fa-check-circle"></i> Exam-specific strategies</li>
                            <li><i class="fas fa-check-circle"></i> Previous year paper analysis</li>
                            <li><i class="fas fa-check-circle"></i> Time management techniques</li>
                        </ul>
                        <a href="#" class="btn">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <div class="container">
            <div class="section-title">
                <h2>Why Choose Us</h2>
                <p>Discover what makes State of Learner the preferred choice for mathematics students</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <i class="fas fa-chalkboard-teacher"></i>
                    <h3>Expert Faculty</h3>
                    <p>Our faculty comprises experienced mathematics educators with years of teaching experience.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-book-open"></i>
                    <h3>Study Material</h3>
                    <p>Comprehensive and updated study material designed to cover all aspects of the syllabus.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-clipboard-list"></i>
                    <h3>Regular Tests</h3>
                    <p>Weekly tests and practice sessions to track progress and identify areas for improvement.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-chart-line"></i>
                    <h3>Performance Analysis</h3>
                    <p>Detailed performance reports with insights to help students focus on weak areas.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Student Testimonials</h2>
                <p>Hear from our successful students about their experience at State of Learner</p>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "The faculty at State of Learner helped me understand complex mathematical concepts easily. Their personalized approach made all the difference in my board exam preparation."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Student">
                        </div>
                        <div class="author-details">
                            <h4>Rahul Verma</h4>
                            <p>Class 12, 96% in Mathematics</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "The study material and test series at State of Learner are exceptional. They helped me secure a top rank in the regional mathematics olympiad."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/women/65.jpg" alt="Student">
                        </div>
                        <div class="author-details">
                            <h4>Priya Sharma</h4>
                            <p>Mathematics Olympiad Winner</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "I improved my mathematics score by 30% after joining State of Learner. Their focus on concept clarity really helped me excel in competitive exams."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/men/45.jpg" alt="Student">
                        </div>
                        <div class="author-details">
                            <h4>Amit Patel</h4>
                            <p>JEE Mathematics Top Performer</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Login Portal -->
    <section id="login" class="login-portal">
        <div class="container portal-container">
            <div class="portal-info">
                <h2 class="section-title">Student Login Portal</h2>
                <p>Access your personalized learning dashboard to track your progress, access study materials, and communicate with your instructors.</p>
                <p>New students can register by filling out the form with their details.</p>
            </div>
            <div class="portal-form">
                <h3>Login / Register</h3>
                <form id="login-form">
                    <div class="form-group">
                        <label for="name">Student Name</label>
                        <input type="text" id="name" placeholder="Enter your full name" required>
                    </div>
                    <div class="form-group">
                        <label for="father">Father's Name</label>
                        <input type="text" id="father" placeholder="Enter your father's name" required>
                    </div>
                    <div class="form-group">
                        <label for="contact">Contact Number</label>
                        <input type="tel" id="contact" placeholder="Enter your mobile number" required>
                    </div>
                    <div class="form-group">
                        <label for="class">Class</label>
                        <select id="class" required>
                            <option value="">Select your class</option>
                            <option value="8">Class 8</option>
                            <option value="9">Class 9</option>
                            <option value="10">Class 10</option>
                            <option value="11">Class 11</option>
                            <option value="12">Class 12</option>
                            <option value="competitive">Competitive Exams</option>
                        </select>
                    </div>
                    <button type="submit" class="submit-btn">Access Learning Portal</button>
                </form>
            </div>
        </div>
    </section>

    <!-- QR Code Section -->
    <section class="qr-section">
        <div class="container qr-container">
            <h2 class="section-title">Connect With Us</h2>
            <div class="qr-code">
                <img src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=https://stateoflearner.com" alt="QR Code">
            </div>
            <p>Scan this QR code to visit our website or save our contact information</p>
            <div class="payment-options">
                <span class="payment-option">Google Pay</span>
                <span class="payment-option">PhonePe</span>
                <span class="payment-option">Paytm</span>
            </div>
        </div>
    </section>

    <!-- Contact Section - Updated with Map and Larger Message Box -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
                <p>Get in touch with us for any queries or information</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Get In Touch</h3>
                    <div class="info-item">
                        <div class="info-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="info-content">
                            <h4>Address</h4>
                            <p>Amar Maya Balaji Nagar chandpur road (Bulandshahr)</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="info-content">
                            <h4>Email</h4>
                            <p>032eevil@gmail.com</p>
                        </div>
                    </div>
                   
                    <!-- Embedded Map -->
                    <div class="map-container">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d468.9869115231523!2d77.83801381648011!3d28.398426197971258!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390ca7d4806fd5e5%3A0x13507ea6646186bf!2sSTATE%20OF%20LEARNERS!5e1!3m2!1sen!2sin!4v1757349175318!5m2!1sen!2sin" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Send Message</h3>
                    <form id="messageForm">
                        <div class="form-group">
                            <label for="contact-name">Full Name</label>
                            <input type="text" id="contact-name" class="form-control" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <label for="contact-email">Email Address</label>
                            <input type="email" id="contact-email" class="form-control" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <label for="contact-message">Your Message</label>
                            <textarea id="contact-message" class="form-control" placeholder="Type your message here..." required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>State of Learner</h3>
                    <p>Specialized mathematics coaching for classes 8-12 and competitive exams. Excellence in education since 2014.</p>
                    <p>Founded by: <strong>Navil Singh</strong></p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#courses">Courses</a></li>
                        <li><a href="#login">Login</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Courses</h3>
                    <ul>
                        <li><a href="#">Class 8-10 Mathematics</a></li>
                        <li><a href="#">Class 11-12 Mathematics</a></li>
                        <li><a href="#">Competitive Exams</a></li>
                        <li><a href="#">Crash Courses</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Contact Information</h3>
                    <p><i class="fas fa-map-marker-alt"></i> Amar Maya Balaji Nagar chandpur road (Bulandshahr)</p>
                    <p><i class="fas fa-envelope"></i> 032eevil@gmail.com</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2014 State of Learner. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <a href="#" class="back-to-top" id="backToTop">
        <i class="fas fa-arrow-up"></i>
    </a>

    <!-- Modal for Course Information -->
    <div id="course-modal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Our Mathematics Courses</h2>
            <div class="modal-body">
                <h3>Class 8-10</h3>
                <p>Comprehensive curriculum covering all board syllabi with focus on concept building</p>
               
                <h3>Class 11-12</h3>
                <p>Advanced mathematics with focus on board exams and competitive entrance tests</p>
               
                <h3>Competitive Exams</h3>
                <p>Dedicated courses for engineering, medical, and other entrance examinations</p>
               
                <button class="btn" id="modal-contact">Contact for Admission</button>
            </div>
        </div>
    </div>

    <script>
        // Navigation Toggle
        const navToggle = document.querySelector('.nav-toggle');
        const mainNav = document.getElementById('main-nav');
       
        navToggle.addEventListener('click', function() {
            mainNav.classList.toggle('active');
        });
       
        // Close navigation when clicking on a link
        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', () => {
                mainNav.classList.remove('active');
            });
        });
       
        // Back to Top Button
        const backToTopButton = document.getElementById('backToTop');
       
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                backToTopButton.classList.add('visible');
            } else {
                backToTopButton.classList.remove('visible');
            }
        });
       
        backToTopButton.addEventListener('click', (e) => {
            e.preventDefault();
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
       
        // Lazy load hero background
        document.addEventListener('DOMContentLoaded', function() {
            const heroBg = document.getElementById('hero-bg');
            const imageUrl = heroBg.style.backgroundImage.replace('url("', '').replace('")', '');
           
            // Create an image object to load the background
            const img = new Image();
            img.src = imageUrl;
            img.onload = function() {
                heroBg.classList.add('loaded');
            };
        });

        // Modal functionality
        document.addEventListener('DOMContentLoaded', function() {
            // Get modal element
            const modal = document.getElementById('course-modal');
            const closeBtn = document.querySelector('.close');
           
            // Get buttons
            const courseBtn = document.querySelector('a[href="#courses"]');
            const modalContact = document.getElementById('modal-contact');
           
            // Course button click - show modal
            courseBtn.addEventListener('click', function(e) {
                e.preventDefault();
                modal.style.display = 'block';
            });
           
            // Close modal
            closeBtn.addEventListener('click', function() {
                modal.style.display = 'none';
            });
           
            // Close modal if clicked outside
            window.addEventListener('click', function(e) {
                if (e.target == modal) {
                    modal.style.display = 'none';
                }
            });
           
            // Form submission
            document.getElementById('login-form').addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Login request submitted! We will contact you shortly.');
                this.reset();
            });
           
            // Contact form submission
            document.getElementById('messageForm').addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Thank you for your message. We will get back to you soon.');
                this.reset();
            });
           
            // Modal contact button
            modalContact.addEventListener('click', function() {
                modal.style.display = 'none';
                alert('Please email us at 032eevil@gmail.com for admission inquiries.');
            });
           
            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                   
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                   
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        targetElement.scrollIntoView({
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>
</body>
</html>
