<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alexio Junior Aaron | Data Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #0ea5e9;
            --dark: #0f172a;
            --light: #f8fafc;
            --gray: #64748b;
            --gray-light: #cbd5e1;
            --success: #10b981;
            --danger: #ef4444;
            --warning: #f59e0b;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.7;
            color: var(--dark);
            background-color: var(--light);
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            position: relative;
            background: linear-gradient(135deg, var(--primary-dark), var(--secondary));
            color: white;
            padding: 100px 0 160px;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
            text-align: center;
        }

        .header-content {
            max-width: 900px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }

        .header-title {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 20px;
            background: linear-gradient(90deg, #ffffff, #e0e7ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: shimmer 2s infinite linear;
            background-size: 200% 100%;
        }

        @keyframes shimmer {
            0% {
                background-position: -200% 0;
            }
            100% {
                background-position: 200% 0;
            }
        }

        .header-subtitle {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid rgba(255, 255, 255, 0.3);
            margin-bottom: 20px;
        }

        .cta-btn {
            display: inline-block;
            background-color: white;
            color: var(--primary);
            padding: 12px 28px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .cta-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }

        .animated-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .animated-bg .shape {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }

        .shape:nth-child(1) {
            width: 300px;
            height: 300px;
            top: -100px;
            left: -50px;
        }

        .shape:nth-child(2) {
            width: 200px;
            height: 200px;
            bottom: -50px;
            right: 100px;
        }

        .shape:nth-child(3) {
            width: 150px;
            height: 150px;
            top: 50%;
            right: -50px;
        }

        /* About Section */
        .about-section {
            margin-top: -60px;
            position: relative;
            z-index: 2;
        }

        .about-card {
            background-color: white;
            padding: 50px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            margin-bottom: 60px;
        }

        .about-text {
            text-align: justify;
            font-size: 1.05rem;
            color: var(--gray);
            margin-bottom: 30px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .social-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            background-color: var(--primary);
            color: white;
            height: 40px;
            padding: 0 20px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .social-btn i {
            margin-right: 8px;
        }

        .social-btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }

        /* Skills Section */
        .section-title {
            text-align: center;
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 50px;
            position: relative;
            color: var(--dark);
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 2px;
        }

        .skills-container {
            margin-bottom: 80px;
        }

        .skills-category {
            margin-bottom: 40px;
        }

        .category-title {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-left: 15px;
        }

        .category-title::before {
            content: '';
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 6px;
            height: 20px;
            background-color: var(--primary);
            border-radius: 3px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            gap: 30px;
            justify-items: center;
            margin: 0 auto;
            max-width: 1000px;
        }

        .skill-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            transition: transform 0.3s ease;
        }

        .skill-item:hover {
            transform: translateY(-8px);
        }

        .skill-item img {
            height: 50px;
            margin-bottom: 8px;
        }

        .skill-name {
            font-size: 0.75rem;
            text-align: center;
            color: var(--gray);
        }

        /* Stats Section */
        .stats-section {
            padding: 80px 0;
            background-color: var(--dark);
            color: white;
            position: relative;
        }

        .stats-bg {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            opacity: 0.2;
            background-image: url('https://user-images.githubusercontent.com/78341798/194534778-d662496c-ae00-4e8d-ae9b-b90912054e7f.gif');
            background-size: cover;
            background-position: center;
        }

        .stats-section .section-title {
            color: white;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            position: relative;
            z-index: 1;
        }

        .stat-card {
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 40px 0;
            text-align: center;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }

        .footer-icon {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }

        .footer-icon:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            font-size: 0.9rem;
            color: var(--gray-light);
        }

        /* Animation */
        @keyframes floatUp {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-15px);
            }
            100% {
                transform: translateY(0);
            }
        }

        .animate-float {
            animation: floatUp 3s ease-in-out infinite;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-title {
                font-size: 2.5rem;
            }
            
            .about-card {
                padding: 30px;
            }
            
            .skills-grid {
                grid-template-columns: repeat(auto-fill, minmax(70px, 1fr));
                gap: 20px;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="animated-bg">
            <div class="shape"></div>
            <div class="shape"></div>
            <div class="shape"></div>
        </div>
        <div class="container">
            <div class="header-content">
                <img src="https://user-images.githubusercontent.com/55389276/140866485-8fb1c876-9a8f-4d6a-98dc-08c4981eaf70.gif" alt="Profile Banner" style="width: 100%; margin-bottom: 30px; border-radius: 15px;">
                <h1 class="header-title">Alexio Junior Aaron</h1>
                <p class="header-subtitle">Data & Analytics Engineer | AWS | ETL | Data Pipelines | Data Modeling</p>
                <a href="mailto:junioralexioaaron607@gmail.com" class="cta-btn">
                    <i class="fas fa-envelope"></i> Get In Touch
                </a>
            </div>
        </div>
    </header>

    <!-- About Section -->
    <section class="about-section">
        <div class="container">
            <div class="about-card">
                <p class="about-text">
                    Experienced Data Engineer specializing in orchestrating end-to-end data pipelines that ensure seamless data extraction, transformation, deployment, and maintenance while upholding the highest security standards and least privilege principles. I leverage DataOps methodologies and robust orchestration tools such as Airflow to automate workflows and enable scalable data management. Proficient in ETL techniques, data modeling, and tools like dbt, I transform raw data into actionable insights. With a strong foundation in provisioning infrastructure using AWS, Terraform, and CloudFormation, I drive business growth by creating secure, efficient, and innovative data solutions. As a Freelance Data & Analytics Engineer, I am passionate about staying up-to-date with the latest technologies and best practices, collaborating effectively in cross-functional teams to deliver tangible value for every business.
                </p>
                <div class="social-links">
                    <a href="mailto:junioralexioaaron607@gmail.com" class="social-btn">
                        <i class="fas fa-envelope"></i> Email Me
                    </a>
                    <a href="https://github.com/Ajay263" class="social-btn">
                        <i class="fab fa-github"></i> GitHub
                    </a>
                    <a href="https://www.linkedin.com/" class="social-btn">
                        <i class="fab fa-linkedin"></i> LinkedIn
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="skills-container container">
        <h2 class="section-title">Skills & Technologies</h2>

        <!-- Programming Languages -->
        <div class="skills-category">
            <h3 class="category-title">Programming Languages</h3>
            <div class="skills-grid">
                <div class="skill-item">
                    <img alt="Python" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/>
                    <span class="skill-name">Python</span>
                </div>
                <div class="skill-item">
                    <img alt="JavaScript" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-plain.svg"/>
                    <span class="skill-name">JavaScript</span>
                </div>
            </div>
        </div>

        <!-- Databases -->
        <div class="skills-category">
            <h3 class="category-title">Databases</h3>
            <div class="skills-grid">
                <div class="skill-item">
                    <img alt="PostgreSQL" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-plain-wordmark.svg"/>
                    <span class="skill-name">PostgreSQL</span>
                </div>
                <div class="skill-item">
                    <img alt="MySQL" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg"/>
                    <span class="skill-name">MySQL</span>
                </div>
                <div class="skill-item">
                    <img alt="MongoDB" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original-wordmark.svg"/>
                    <span class="skill-name">MongoDB</span>
                </div>
                <div class="skill-item">
                    <img alt="SQLite" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sqlite/sqlite-original.svg"/>
                    <span class="skill-name">SQLite</span>
                </div>
                <div class="skill-item">
                    <img alt="Redshift" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/aws-redshift.svg"/>
                    <span class="skill-name">Redshift</span>
                </div>
            </div>
        </div>

        <!-- AWS Services -->
        <div class="skills-category">
            <h3 class="category-title">AWS Services</h3>
            <div class="skills-grid">
                <div class="skill-item">
                    <img alt="AWS" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original-wordmark.svg"/>
                    <span class="skill-name">AWS</span>
                </div>
                <div class="skill-item">
                    <img alt="S3" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/aws-s3.svg"/>
                    <span class="skill-name">S3</span>
                </div>
                <div class="skill-item">
                    <img alt="AWS Glue" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/aws-glue.svg"/>
                    <span class="skill-name">AWS Glue</span>
                </div>
                <div class="skill-item">
                    <img alt="AWS Lambda" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/aws-lambda.svg"/>
                    <span class="skill-name">Lambda</span>
                </div>
                <div class="skill-item">
                    <img alt="AWS EC2" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/aws-ec2.svg"/>
                    <span class="skill-name">EC2</span>
                </div>
                <div class="skill-item">
                    <img alt="AWS SNS" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/aws-sns.svg"/>
                    <span class="skill-name">SNS</span>
                </div>
                <div class="skill-item">
                    <img alt="CloudTrail" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/aws-cloudtrail.svg"/>
                    <span class="skill-name">CloudTrail</span>
                </div>
                <div class="skill-item">
                    <img alt="CloudFormation" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/aws-cloudformation.svg"/>
                    <span class="skill-name">CloudFormation</span>
                </div>
            </div>
        </div>

        <!-- Big Data Tools -->
        <div class="skills-category">
            <h3 class="category-title">Big Data & ETL Tools</h3>
            <div class="skills-grid">
                <div class="skill-item">
                    <img alt="Apache Spark" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/apache/apache-original-wordmark.svg"/>
                    <span class="skill-name">Spark</span>
                </div>
                <div class="skill-item">
                    <img alt="Apache Kafka" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/apachekafka/apachekafka-original-wordmark.svg"/>
                    <span class="skill-name">Kafka</span>
                </div>
                <div class="skill-item">
                    <img alt="Apache Airflow" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/airflow.svg"/>
                    <span class="skill-name">Airflow</span>
                </div>
                <div class="skill-item">
                    <img alt="DBT" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/dbt.svg"/>
                    <span class="skill-name">dbt</span>
                </div>
            </div>
        </div>

        <!-- DevOps Tools -->
        <div class="skills-category">
            <h3 class="category-title">DevOps Tools</h3>
            <div class="skills-grid">
                <div class="skill-item">
                    <img alt="Docker" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-plain-wordmark.svg"/>
                    <span class="skill-name">Docker</span>
                </div>
                <div class="skill-item">
                    <img alt="Terraform" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/terraform/terraform-original-wordmark.svg"/>
                    <span class="skill-name">Terraform</span>
                </div>
                <div class="skill-item">
                    <img alt="GitHub" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original-wordmark.svg"/>
                    <span class="skill-name">GitHub</span>
                </div>
                <div class="skill-item">
                    <img alt="GitHub Actions" src="https://raw.githubusercontent.com/gilbarbara/logos/master/logos/github-actions.svg"/>
                    <span class="skill-name">GitHub Actions</span>
                </div>
            </div>
        </div>

        <!-- Monitoring -->
        <div class="skills-category">
            <h3 class="category-title">Monitoring</h3>
            <div class="skills-grid">
                <div class="skill-item">
                    <img alt="Grafana" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/grafana/grafana-original-wordmark.svg"/>
                    <span class="skill-name">Grafana</span>
                </div>
                <div class="skill-item">
                    <img alt="Prometheus" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/prometheus/prometheus-original-wordmark.svg"/>
                    <span class="skill-name">Prometheus</span>
                </div>
            </div>
        </div>

        <!-- Collaboration -->
        <div class="skills-category">
            <h3 class="category-title">Collaboration</h3>
            <div class="skills-grid">
                <div class="skill-item">
                    <img alt="Slack" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/slack/slack-original.svg"/>
                    <span class="skill-name">Slack</span>
                </div>
                <div class="skill-item">
                    <img alt="VSCode" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg"/>
                    <span class="skill-name">VSCode</span>
                </div>
                <div class="skill-item">
                    <img alt="Jupyter" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original-wordmark.svg"/>
                    <span class="skill-name">Jupyter</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats-section">
        <div class="stats-bg"></div>
        <div class="container">
            <h2 class="section-title">GitHub Statistics</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=Ajay263&hide=stars&count_private=true&show_icons=true&theme=algolia&border_radius=20" alt="GitHub Stats" style="width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://streak-stats.demolab.com?user=Ajay263&count_private=true&theme=algolia&border_radius=20" alt="GitHub Streak" style="width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ajay263&layout=compact&show_icons=true&theme=algolia&border_radius=20" alt="Most Used Languages" style="width: 100%; border-radius: 10px;">
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-links">
                <a href="#" class="footer-icon"><i class="fab fa-youtube"></i></a>
                <a href="https://programming-gym.blogspot.com/" class="footer-icon"><i class="fab fa-blogger"></i></a>
                <a href="mailto:junioralexioaaron607@gmail.com" class="footer-icon"><i class="fas fa-envelope"></i></a>
                <a href="https://github.com/Ajay263" class="footer-icon"><i class="fab fa-github"></i></a>
                <a href="#" class="footer-icon"><i class="fab fa-linkedin"></i></a>
            </div>
            <p class="copyright">© 2025 Alexio Junior Aaron. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Simple animation for elements
        document.addEventListener('DOMContentLoaded', function() {
            // Add floating animation to skill items with delay
            const skillItems = document.querySelectorAll('.skill-item');
            skillItems.forEach((item, index) => {
                setTimeout(() => {
                    item.style.animation = `floatUp 3s ease-in-out infinite`;
                    item.style.animationDelay = `${index * 0.1}s`;
                }, 300);
            });
        });
    </script>
</body>
</html>
