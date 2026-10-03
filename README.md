<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CareerHub - Job Application Portal</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f5f7ff;
            color: #1e293b;
            line-height: 1.6;
        }

        header {
            background: #172554;
            color: white;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        header h2 {
            font-size: 26px;
        }

        header h2 span {
            color: #a5b4fc;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-size: 14px;
        }

        nav a:hover {
            color: #a5b4fc;
        }

        .hero {
            background: linear-gradient(135deg, #172554, #4f46e5);
            color: white;
            text-align: center;
            padding: 85px 20px;
        }

        .hero h1 {
            font-size: 43px;
            margin-bottom: 15px;
        }

        .hero p {
            max-width: 600px;
            margin: 0 auto 25px;
            color: #e0e7ff;
        }

        .button {
            display: inline-block;
            background: #ffffff;
            color: #3730a3;
            padding: 12px 25px;
            text-decoration: none;
            border-radius: 6px;
            font-weight: bold;
            border: none;
            cursor: pointer;
        }

        .button:hover {
            background: #e0e7ff;
        }

        section {
            padding: 60px 8%;
        }

        .section-title {
            text-align: center;
            color: #172554;
            font-size: 30px;
            margin-bottom: 12px;
        }

        .section-description {
            text-align: center;
            color: #64748b;
            margin-bottom: 35px;
        }

        .jobs {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 22px;
        }

        .job-card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            border: 1px solid #e2e8f0;
            box-shadow: 0 5px 15px #1725540a;
            transition: 0.3s;
        }

        .job-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px #17255415;
        }

        .job-card .icon {
            font-size: 32px;
            margin-bottom: 12px;
        }

        .job-card h3 {
            color: #172554;
            margin-bottom: 5px;
        }

        .company {
            color: #64748b;
            font-size: 14px;
        }

        .tag {
            display: inline-block;
            background: #e0e7ff;
            color: #3730a3;
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 12px;
            margin: 15px 5px 12px 0;
        }

        .job-card p.description {
            color: #64748b;
            font-size: 14px;
            margin-bottom: 18px;
        }

        .apply-link {
            color: #4f46e5;
            text-decoration: none;
            font-weight: bold;
            font-size: 14px;
        }

        .apply-link:hover {
            text-decoration: underline;
        }

        .about {
            background: #e9edff;
            text-align: center;
        }

        .about p {
            max-width: 700px;
            margin: 15px auto 0;
            color: #475569;
        }

        .application {
            max-width: 850px;
            margin: auto;
        }

        form {
            background: white;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 5px 25px #1725540d;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            font-weight: bold;
            font-size: 14px;
            margin-bottom: 8px;
        }

        input, select, textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #cbd5e1;
            border-radius: 6px;
            font-family: Arial, sans-serif;
            font-size: 14px;
        }

        input:focus, select:focus, textarea:focus {
            outline: 2px solid #c7d2fe;
            border-color: #4f46e5;
        }

        textarea {
            resize: vertical;
        }

        .submit-button {
            width: 100%;
            padding: 14px;
            background: #4f46e5;
            color: white;
            border: none;
            border-radius: 6px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        .submit-button:hover {
            background: #3730a3;
        }

        .note {
            text-align: center;
            color: #64748b;
            font-size: 12px;
            margin-top: 15px;
        }

        footer {
            background: #172554;
            color: white;
            text-align: center;
            padding: 25px 15px;
        }

        footer p {
            font-size: 13px;
            color: #cbd5e1;
        }

        @media (max-width: 800px) {
            .jobs {
                grid-template-columns: 1fr 1fr;
            }

            .hero h1 {
                font-size: 34px;
            }
        }

        @media (max-width: 550px) {
            header {
                justify-content: center;
                text-align: center;
            }

            nav a {
                margin: 0 7px;
            }

            .jobs {
                grid-template-columns: 1fr;
            }

            .form-row {
                grid-template-columns: 1fr;
                gap: 0;
            }

            form {
                padding: 22px;
            }

            section {
                padding: 45px 6%;
            }
        }
    </style>
</head>

<body>

    <header>
        <h2>Career<span>Hub.</span></h2>
        <nav>
            <a href="#home">Home</a>
            <a href="#jobs">Jobs</a>
            <a href="#about">About</a>
            <a href="#apply">Apply</a>
        </nav>
    </header>

    <div class="hero" id="home">
        <h1>Build Your Future With Us</h1>
        <p>
            Discover exciting career opportunities, showcase your skills,
            and take the next step towards your dream job.
        </p>
        <a href="#jobs" class="button">Explore Jobs &rarr;</a>
    </div>

    <section id="jobs">
        <h2 class="section-title">Explore Open Positions</h2>
        <p class="section-description">
            Find your perfect role and start your professional journey.
        </p>

        <div class="jobs">

            <div class="job-card">
                <div class="icon">💻</div>
                <h3>Web Developer</h3>
                <p class="company">Technology Department</p>
                <span class="tag">Full-time</span>
                <span class="tag">Entry-level</span>
                <p class="description">
                    Create responsive websites and help develop
                    engaging online experiences.
                </p>
                <a href="#apply" class="apply-link"
                   onclick="document.getElementById('position').value='Web Developer'">
                    Apply for this job &rarr;
                </a>
            </div>

            <div class="job-card">
                <div class="icon">📊</div>
                <h3>Data Analyst</h3>
                <p class="company">Analytics Department</p>
                <span class="tag">Full-time</span>
                <span class="tag">Entry-level</span>
                <p class="description">
                    Analyze information, identify patterns,
                    and help businesses make informed decisions.
                </p>
                <a href="#apply" class="apply-link"
                   onclick="document.getElementById('position').value='Data Analyst'">
                    Apply for this job &rarr;
                </a>
            </div>

            <div class="job-card">
                <div class="icon">🎨</div>
                <h3>UI/UX Designer</h3>
                <p class="company">Design Department</p>
                <span class="tag">Full-time</span>
                <span class="tag">Entry-level</span>
                <p class="description">
                    Design attractive, accessible, and user-friendly
                    digital products.
                </p>
                <a href="#apply" class="apply-link"
                   onclick="document.getElementById('position').value='UI/UX Designer'">
                    Apply for this job &rarr;
                </a>
            </div>

        </div>
    </section>

    <section class="about" id="about">
        <h2 class="section-title">About CareerHub</h2>
        <p>
            CareerHub is a job application portal concept designed to
            connect job seekers with employment opportunities.
            Our goal is to make exploring jobs and applying for positions
            simple and accessible.
        </p>
    </section>

    <section id="apply">
        <div class="application">
            <h2 class="section-title">Apply for Your Dream Job</h2>
            <p class="section-description">
                Complete the form below to express your interest.
            </p>

            <form action="#" method="get">

                <div class="form-row">
                    <div class="form-group">
                        <label for="name">Full Name</label>
                        <input type="text" id="name" name="name"
                               placeholder="Enter your full name" required>
                    </div>

                    <div class="form-group">
                        <label for="email">Email Address</label>
                        <input type="email" id="email" name="email"
                               placeholder="Enter your email" required>
                    </div>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label for="phone">Phone Number</label>
                        <input type="tel" id="phone" name="phone"
                               placeholder="Enter your phone number" required>
                    </div>

                    <div class="form-group">
                        <label for="position">Position Applying For</label>
                        <select id="position" name="position" required>
                            <option value="">Select a position</option>
                            <option>Web Developer</option>
                            <option>Data Analyst</option>
                            <option>UI/UX Designer</option>
                        </select>
                    </div>
                </div>

                <div class="form-group">
                    <label for="education">Educational Qualification</label>
                    <input type="text" id="education" name="education"
                           placeholder="e.g. B.E. in Computer Science" required>
                </div>

                <div class="form-group">
                    <label for="resume">Resume URL (optional)</label>
                    <input type="url" id="resume" name="resume"
                           placeholder="Paste your resume link">
                </div>

                <div class="form-group">
                    <label for="message">Skills and Experience</label>
                    <textarea id="message" name="message" rows="4"
                              placeholder="Tell us about your skills..."
                              required></textarea>
                </div>

                <button type="submit" class="submit-button">
                    Submit Application
                </button>

                <p class="note">
                    Student project demo. This form does not store or
                    send applications to an employer.
                </p>

            </form>
        </div>
    </section>

    <footer>
        <h3>CareerHub.</h3>
        <p>Connecting talent with opportunity.</p>
        <p>&copy; 2026 CareerHub. Student Project.</p>
    </footer>

</body>
</html>
