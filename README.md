<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Career Access Pakistan - Daily Job Updates</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-blue: #2563eb;
            --secondary-blue: #3b82f6;
            --primary-green: #10b981;
            --light-green: #34d399;
            --dark: #1f2937;
            --light-bg: #f8fafc;
            --white: #ffffff;
            --shadow: 0 4px 6px -1px rgba(0, 0,0,0.1);
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background: var(--light-bg);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: var(--shadow);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            color: var(--primary-green);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: opacity 0.3s;
        }

        .nav-links a:hover {
            opacity: 0.8;
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            color: white;
            text-align: center;
            padding: 4rem 0;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 12px 24px;
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s;
            cursor: pointer;
        }

        .btn-primary {
            background: var(--primary-green);
            color: white;
        }

        .btn-primary:hover {
            background: var(--light-green);
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }

        .btn-secondary:hover {
            background: white;
            color: var(--primary-blue);
        }

        /* Jobs Grid */
        .jobs-section {
            padding: 4rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 3rem;
            color: var(--dark);
        }

        .filters {
            display: flex;
            gap: 1rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .filter-select {
            padding: 10px 15px;
            border: 2px solid #e5e7eb;
            border-radius: 25px;
            background: white;
            font-size: 1rem;
            min-width: 150px;
        }

        .search-box {
            padding: 12px 20px;
            border: 2px solid #e5e7eb;
            border-radius: 25px;
            font-size: 1rem;
            width: 100%;
            max-width: 300px;
        }

        .jobs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .job-card {
            background: white;
            border-radius: 20px;
            padding: 2rem;
            box-shadow: var(--shadow);
            transition: all 0.3s;
            border-left: 5px solid var(--primary-green);
        }

        .job-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0,0,0.1);
        }

        .job-category {
            display: inline-block;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .category-gov { background: #fef3c7; color: #92400e; }
        .category-private { background: #dbeafe; color: #1e40af; }
        .category-intern { background: #d1fae5; color: #065f46; }
        .category-scholar { background: #f3e8ff; color: #7c3aed; }
        .category-overseas { background: #fef3c7; color: #b45309; }

        .job-title {
            font-size: 1.4rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .job-details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
            margin: 1.5rem 0;
            font-size: 0.95rem;
        }

        .job-detail {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .job-detail i {
            color: var(--primary-green);
            width: 16px;
        }

        .deadline {
            background: #fef2f2;
            color: #dc2626;
            padding: 8px 12px;
            border-radius: 20px;
            font-weight: 600;
            text-align: center;
            margin-top: 1rem;
        }

        .apply-btn {
            width: 100%;
            margin-top: 1.5rem;
        }

        /* Admin Panel */
        .admin-panel {
            background: white;
            border-radius: 20px;
            padding: 2rem;
            margin: 2rem 0;
            box-shadow: var(--shadow);
        }

        .admin-form {
            display: grid;
            gap: 1rem;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .form-group input, .form-group select, .form-group textarea {
            padding: 12px;
            border: 2px solid #e5e7eb;
            border-radius: 10px;
            font-size: 1rem;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        /* Contact Form */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .mobile-menu {
                display: block;
            }

            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .jobs-grid {
                grid-template-columns: 1fr;
            }

            .job-details {
                grid-template-columns: 1fr;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .filters {
                flex-direction: column;
                align-items: center;
            }
        }

        /* Loading */
        .loading {
            text-align: center;
            padding: 2rem;
            font-size: 1.2rem;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 4rem;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav class="container">
            <div class="logo">
                <i class="fas fa-briefcase"></i>
                Career Access Pakistan
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#jobs">Jobs</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#admin" onclick="showAdminPanel()">Admin</a></li>
            </ul>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <h1>Career Access Pakistan</h1>
            <p>Daily job updates in Pakistan with complete details</p>
            <div class="cta-buttons">
                <a href="https://whatsapp.com/channel/0029Va..." class="btn btn-primary" target="_blank">
                    <i class="fab fa-whatsapp"></i> Join WhatsApp Channel
                </a>
                <a href="https://chat.whatsapp.com/..." class="btn btn-secondary" target="_blank">
                    <i class="fab fa-whatsapp"></i> Join WhatsApp Group
                </a>
            </div>
        </div>
    </section>

    <!-- Latest Jobs -->
    <section class="jobs-section">
        <div class="container">
            <h2 class="section-title">Latest Job Opportunities</h2>
            <div id="latest-jobs" class="jobs-grid">
                <!-- Latest 5 jobs will be loaded here -->
            </div>
        </div>
    </section>

    <!-- All Jobs Section -->
    <section id="jobs" class="jobs-section">
        <div class="container">
            <h2 class="section-title">All Job Opportunities</h2>
            
            <!-- Filters -->
            <div class="filters">
                <input type="text" class="search-box" id="searchInput" placeholder="Search by city, company or keyword...">
                <select class="filter-select" id="categoryFilter">
                    <option value="">All Categories</option>
                    <option value="Government">Government Jobs</option>
                    <option value="Private">Private Jobs</option>
                    <option value="Internship">Internships</option>
                    <option value="Scholarship">Scholarships</option>
                    <option value="Overseas">Overseas Jobs</option>
                </select>
                <select class="filter-select" id="cityFilter">
                    <option value="">All Cities</option>
                    <option value="Lahore">Lahore</option>
                    <option value="Karachi">Karachi</option>
                    <option value="Islamabad">Islamabad</option>
                    <option value="Rawalpindi">Rawalpindi</option>
                    <option value="Faisalabad">Faisalabad</option>
                </select>
            </div>

            <div id="all-jobs" class="jobs-grid">
                <!-- All jobs will be loaded here -->
            </div>
        </div>
    </section>

    <!-- Admin Panel -->
    <section id="admin" class="container" style="display: none;">
        <div class="admin-panel">
            <h2 style="text-align: center; margin-bottom: 2rem;"><i class="fas fa-user-shield"></i> Admin Panel</h2>
            <form id="jobForm" class="admin-form">
                <div class="form-row">
                    <div class="form-group">
                        <label>Job Title *</label>
                        <input type="text" id="jobTitle" required>
                    </div>
                    <div class="form-group">
                        <label>Category *</label>
                        <select id="jobCategory" required>
                            <option value="Government">Government Jobs</option>
                            <option value="Private">Private Jobs</option>
                            <option value="Internship">Internships</option>
                            <option value="Scholarship">Scholarships</option>
                            <option value="Overseas">Overseas Jobs</option>
                        </select>
                    </div>
                </div>
                
                <div class="form-row">
                    <div class="form-group">
                        <label>Company/Department *</label>
                        <input type="text" id="company" required>
                    </div>
                    <div class="form-group">
                        <label>Location *</label>
                        <input type="text" id="location" required>
                    </div>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label>Qualification</label>
                        <input type="text" id="qualification" placeholder="e.g., Bachelor's, Master's">
                    </div>
                    <div class="form-group">
                        <label>Experience</label>
                        <input type="text" id="experience" placeholder="e.g., 2-5 years">
                    </div>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label>Salary (Optional)</label>
                        <input type="text" id="salary" placeholder="e.g., 50,000 - 80,000 PKR">
                    </div>
                    <div class="form-group">
                        <label>Deadline *</label>
                        <input type="date" id="deadline" required>
                    </div>
                </div>

                <div class="form-group">
                    <label>Application Method/Link *</label>
                    <textarea id="applyLink" rows="3" placeholder="WhatsApp number, email, or application link" required></textarea>
                </div>

                <button type="submit" class="btn btn-primary" style="width: 100%; padding: 15px;">
                    <i class="fas fa-plus"></i> Add New Job
                </button>
            </form>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="jobs-section" style="background: white;">
        <div class="container">
            <h2 class="section-title">About Career Access Pakistan</h2>
            <div style="max-width: 800px; margin: 0 auto; text-align: center; font-size: 1.1rem;">
                <p>Career Access Pakistan shares daily verified job opportunities to help students and job seekers across Pakistan find their dream careers.</p>
                <br>
                <p>We post authentic Government jobs, Private sector opportunities, Internships, Scholarships, and Overseas jobs with complete details including eligibility criteria, application deadlines, and direct application links.</p>
                <br>
                <p>Join our WhatsApp community for instant notifications and never miss a job opportunity!</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="jobs-section">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <form class="contact-form admin-form">
                <div class="form-row">
                    <div class="form-group">
                        <label>Name</label>
                        <input type="text" required>
                    </div>
                    <div class="form-group">
                        <label>Email</label>
                        <input type="email" required>
                    </div>
                </div>
                <div class="form-group">
                    <label>Message</label>
                    <textarea rows="5" required></textarea>
                </div>
                <button type="submit" class="btn btn-primary" style="width: 100%;">Send Message</button>
            </form>
            <div style="text-align: center; margin-top: 2rem;">
                <p><strong>Admin WhatsApp:</strong> <a href="https://wa.me/923xxxxxxxxx" class="btn btn-primary"><i class="fab fa-whatsapp"></i> Contact Admin</a></p>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2024 Career Access Pakistan. All rights reserved. | Daily Job Updates for Pakistan</p>
        </div>
    </footer>

    <script>
        // Job data storage (localStorage for demo)
        let jobs = JSON.parse(localStorage.getItem('careerJobs')) || [];

        // Sample jobs for demo
        if (jobs.length === 0) {
            jobs = [
                {
                    id: 1,
                    title: "Assistant Manager (BPS-17)",
                    category: "Government",
                    company: "Punjab Police Department",
                    location: "Lahore",
                    qualification: "Master's",
                    experience: "2-5 years",
                    salary: "60,000 - 100,000 PKR",
                    deadline: "2024-12-15",
                    applyLink: "https://wa.me/923001234567"
                },
                {
                    id: 2,
                    title: "Software Engineer",
                    category: "Private",
                    company: "Systems Limited",
                    location: "Karachi",
                    qualification: "BS Computer Science",
                    experience: "1-3 years",
