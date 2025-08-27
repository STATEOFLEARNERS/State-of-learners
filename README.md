# State-of-learners
welcome
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>State of Learner - Learn with Skills</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary-dark: #1a237e;
            --primary: #283593;
            --primary-light: #3949ab;
            --accent: #ffd700;
            --accent-dark: #ffc400;
            --light: #f5f5f7;
            --dark: #1a1a1a;
            --gray: #424242;
            --light-gray: #e0e0e0;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
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
            padding: 25px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-content {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .logo-container {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .logo {
            font-size: 3rem;
            margin-right: 15px;
            color: var(--accent);
        }

        .logo-text {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }

        .logo-text h1 {
            font-size: 2.8rem;
            font-weight: 700;
            letter-spacing: 1px;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            line-height: 1;
        }

        .logo-text span {
            color: var(--accent);
            font-size: 1.4rem;
            letter-spacing: 2px;
            margin-top: 5px;
            margin-left: 5px;
        }

        /* Hero Section */
        .hero {
            padding: 100px 0;
            background: linear-gradient(rgba(26, 35, 126, 0.8), rgba(26, 35, 126, 0.8)), url('https://images.unsplash.com/photo-1522881193457-37ae97c905bf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
            flex-grow: 1;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background: var(--accent);
            color: var(--primary-dark);
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            border: none;
            cursor: pointer;
            margin: 10px;
        }

        .btn:hover {
            background: var(--accent-dark);
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
        }

        /* Features Section */
        .features {
            padding: 80px 0;
            background: white;
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

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .feature-card {
            background: var(--light);
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
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

        /* Login Portal */
        .login-portal {
            padding: 80px 0;
            background: linear-gradient(to right, #f5f5f7, #e8eaf6);
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
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
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
            transition: border 0.3s ease;
        }

        .form-group input:focus,
        .form-group select:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 2px rgba(40, 53, 147, 0.2);
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
            transition: background 0.3s ease;
            width: 100%;
        }

        .submit-btn:hover {
            background: var(--primary-dark);
        }

        /* QR Code Section */
        .qr-section {
            background: white;
            padding: 60px 0;
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
            background: #f1f1f1;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 20px 0;
            border: 2px solid var(--primary);
            border-radius: 10px;
            overflow: hidden;
        }

        .qr-code img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Footer */
        footer {
            background: var(--primary-dark);
            color: white;
            padding: 60px 0 30px;
        }

        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-section {
            flex: 1;
            min-width: 250px;
        }

        .footer-section h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--accent);
        }

        .footer-section p, .footer-section li {
            margin-bottom: 10px;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section a {
            color: white;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: var(--accent);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
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
            background-color: rgba(0, 0, 0, 0.5);
        }

        .modal-content {
            background-color: white;
            margin: 10% auto;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 30px rgba(0, 0, 0, 0.3);
            width: 80%;
            max-width: 500px;
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
        }

        .close:hover,
        .close:focus {
            color: var(--primary-dark);
            text-decoration: none;
            cursor: pointer;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }

            .logo-text h1 {
                font-size: 2.2rem;
            }

            .logo-text span {
                font-size: 1.1rem;
            }

            .hero h2 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.2rem;
            }
        }

        @media (max-width: 480px) {
            .logo-text h1 {
                font-size: 1.8rem;
            }

            .logo-text span {
                font-size: 0.9rem;
            }

            .logo {
                font-size: 2.5rem;
            }

            .hero {
                padding: 60px 0;
            }

            .hero h2 {
                font-size: 2rem;
            }
           
            .portal-form {
                padding: 25px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo-container">
                <div class="logo">
                    <i class="fas fa-pencil-alt"></i>
                </div>
                <div class="logo-text">
                    <h1>State of Learner</h1>
                    <span>Learn with Skills</span>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container hero-content">
            <h2>Excel in Mathematics with Expert Guidance</h2>
            <p>Specialized coaching for Class 8-12 and competitive exams</p>
            <button class="btn" id="hero-btn">Student Login Portal</button>
            <button class="btn" id="course-btn">View Our Courses</button>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <h2 class="section-title">Why Choose State of Learner?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <i class="fas fa-chalkboard-teacher"></i>
                    <h3>Expert Faculty</h3>
                    <p>Learn from experienced educators specialized in mathematics</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-book-open"></i>
                    <h3>Comprehensive Curriculum</h3>
                    <p>Structured courses designed for academic excellence</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-chart-line"></i>
                    <h3>Proven Results</h3>
                    <p>Consistent track record of student success</p>
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
            <h2 class="section-title">Scan to Connect With Us</h2>
            <div class="qr-code">
                <!-- Placeholder for QR code - in a real scenario, you would use an actual QR code image -->
                <img src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=https://stateoflearner.com" alt="QR Code">
            </div>
            <p>Scan this QR code to visit our website or save our contact information</p>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>State of Learner</h3>
                    <p>Specialized mathematics coaching for classes 8-12 and competitive exams. Excellence in education since 2015.</p>
                </div>
                <div class="footer-section">
                    <h3>Contact Us</h3>
                    <p><i class="fas fa-map-marker-alt"></i>Amar Maya Balaji Nagar chandpur road (Bulandshahr)</p>
                    <p><i class="fas fa-phone"></i> +91 7830447129</p>
                    <p><i class="fas fa-envelope"></i> 032eevil@gmail.com</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#" id="footer-courses">Our Courses</a></li>
                        <li><a href="#" id="footer-timing">Batch Timings</a></li>
                        <li><a href="#" id="footer-materials">Study Materials</a></li>
                        <li><a href="#" id="footer-results">Results</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Administration</h3>
                    <p>CEO-Founder: <strong>Navil Singh</strong></p>
                    <p>With over 15 years of experience in mathematics education and mentorship.</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2014 State of Learner. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Modal for Course Information -->
    <div id="course-modal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Our Mathematics Courses</h2>
            <div class="modal-body">
                <h3>Class 8-10</h3>
                <p>Comprehensive curriculum covering all board syllabi with focus on concept building</p>
               
                <h3>Class 11-12</h3>
                <p>Advanced mathematics with focus on IIT-JEE, NEET and other competitive exams</p>
               
                <h3>Competitive Exams</h3>
                <p>Dedicated courses for engineering, medical, and other entrance examinations</p>
               
                <button class="btn" id="modal-contact">Contact for Admission</button>
            </div>
        </div>
    </div>

    <script>
        // Functionality for all buttons
        document.addEventListener('DOMContentLoaded', function() {
            // Get modal element
            const modal = document.getElementById('course-modal');
            const closeBtn = document.querySelector('.close');
           
            // Get buttons
            const heroBtn = document.getElementById('hero-btn');
            const courseBtn = document.getElementById('course-btn');
            const loginForm = document.getElementById('login-form');
            const modalContact = document.getElementById('modal-contact');
           
            // Footer links
            const footerCourses = document.getElementById('footer-courses');
            const footerTiming = document.getElementById('footer-timing');
            const footerMaterials = document.getElementById('footer-materials');
            const footerResults = document.getElementById('footer-results');
           
            // Hero button click - scroll to login
            heroBtn.addEventListener('click', function() {
                document.getElementById('login').scrollIntoView({
                    behavior: 'smooth'
                });
            });
           
            // Course button click - show modal
            courseBtn.addEventListener('click', function() {
                modal.style.display = 'block';
            });
           
            // Footer courses link
            footerCourses.addEventListener('click', function(e) {
                e.preventDefault();
                modal.style.display = 'block';
            });
           
            // Other footer links
            const footerLinks = [footerTiming, footerMaterials, footerResults];
            footerLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    alert('This page is coming soon!');
                });
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
            loginForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Login request submitted! We will contact you shortly.');
                loginForm.reset();
            });
           
            // Modal contact button
            modalContact.addEventListener('click', function() {
                modal.style.display = 'none';
                alert('Please call +91 7830447129 for admission inquiries.');
            });
        });
    </script>
</body>
</html>
