<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Alexio Junior Aaron - Data Engineer</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #44AEFB;
      --bg: #f9fafd;
      --text: #333;
      --soft: #fff;
      --radius: 12px;
      --shadow: rgba(0, 0, 0, 0.1);
    }
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }
    body {
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      padding: 2rem;
      display: flex;
      justify-content: center;
    }
    .container {
      max-width: 800px;
      background: var(--soft);
      padding: 2rem;
      border-radius: var(--radius);
      box-shadow: 0 4px 16px var(--shadow);
    }
    header {
      text-align: center;
      margin-bottom: 1.5rem;
    }
    header h1 {
      font-size: 2.5rem;
      color: var(--primary);
      font-weight: 700;
      display: inline-block;
      position: relative;
    }
    header h1::after {
      content: "";
      position: absolute;
      width: 50px;
      height: 4px;
      background: var(--primary);
      bottom: -8px;
      left: 50%;
      transform: translateX(-50%);
      border-radius: 2px;
    }
    .banner {
      margin: 1.5rem auto;
      width: 100%;
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: 0 4px 12px var(--shadow);
    }
    .banner img {
      display: block;
      width: 100%;
      height: auto;
    }
    .bio {
      margin: 2rem 0;
      text-align: justify;
      font-weight: 300;
      font-size: 1rem;
    }
    .contact {
      text-align: center;
      margin: 1rem 0;
    }
    .contact a {
      background: var(--primary);
      color: #fff;
      padding: 0.75rem 1.5rem;
      text-decoration: none;
      border-radius: var(--radius);
      font-weight: 600;
      transition: background 0.3s;
    }
    .contact a:hover {
      background: darken(var(--primary), 10%);
    }
    .tools {
      margin: 2rem 0;
    }
    .tools h2 {
      color: var(--primary);
      margin-bottom: 1rem;
      font-size: 1.5rem;
    }
    .tools-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
      gap: 1rem;
      justify-items: center;
    }
    .tools-grid img {
      width: 50px;
      opacity: 0.8;
      transition: opacity 0.3s;
    }
    .tools-grid img:hover {
      opacity: 1;
    }
    .stats {
      margin: 2rem 0;
      text-align: center;
    }
    .stats img {
      margin: 0.5rem;
      border-radius: var(--radius);
      box-shadow: 0 4px 12px var(--shadow);
    }
    footer {
      margin-top: 2rem;
      text-align: center;
      font-size: 0.9rem;
      color: #777;
    }
    .footer-icons img {
      margin: 0 0.5rem;
      width: 30px;
      transition: transform 0.3s;
    }
    .footer-icons img:hover {
      transform: translateY(-4px);
    }
    @media (max-width: 600px) {
      .container { padding: 1rem; }
      header h1 { font-size: 2rem; }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>👨🏻‍💻 Alexio Junior Aaron</h1>
    </header>
    <div class="banner">
      <img src="https://user-images.githubusercontent.com/55389276/140866485-8fb1c876-9a8f-4d6a-98dc-08c4981eaf70.gif" alt="GitHub Cover Banner" />
    </div>
    <section class="bio">
      <p>
        Experienced Data Engineer specializing in orchestrating end-to-end data pipelines that ensure seamless data extraction, transformation, deployment, and maintenance while upholding the highest security standards and least privilege principles. I leverage DataOps methodologies and robust orchestration tools such as Airflow to automate workflows and enable scalable data management.
      </p>
      <p>
        Proficient in ETL techniques, data modeling, and tools like dbt, I transform raw data into actionable insights. With a strong foundation in provisioning infrastructure using AWS, Terraform, and CloudFormation, I drive business growth by creating secure, efficient, and innovative data solutions.
      </p>
      <p>
        As a Freelance Data & Analytics Engineer, I am passionate about staying up-to-date with the latest technologies and best practices, collaborating effectively in cross-functional teams to deliver tangible value for every business.
      </p>
    </section>
    <div class="contact">
      <a href="mailto:junioralexioaaron607@gmail.com">Email Me</a>
    </div>
    <section class="tools">
      <h2>⚙️ Languages & Tools</h2>
      <div class="tools-grid">
        <!-- Repeat for each icon -->
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python" title="Python" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-plain-wordmark.svg" alt="PostgreSQL" title="PostgreSQL" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg" alt="MySQL" title="MySQL" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original-wordmark.svg" alt="MongoDB" title="MongoDB" />
        <!-- Add others similarly -->
      </div>
    </section>
    <section class="stats">
      <h2>📊 Statistics</h2>
      <img src="https://github-readme-stats.vercel.app/api?username=Ajay263&hide=stars&count_private=true&show_icons=true&theme=algolia&border_radius=20" alt="GitHub Stats" />
      <img src="https://streak-stats.demolab.com?user=Ajay263&count_private=true&theme=algolia&border_radius=20" alt="GitHub Streak" />
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ajay263&layout=compact&show_icons=true&theme=algolia&border_radius=20" alt="Most Used Languages" />
    </section>
    <footer>
      <div class="footer-icons">
        <a href="#"><img src="https://user-images.githubusercontent.com/78341798/194531650-698ef1b1-9cbd-4b4f-96ef-5a2ec4b5d7e6.svg" alt="YouTube" /></a>
        <a href="https://programming-gym.blogspot.com/"><img src="https://user-images.githubusercontent.com/78341798/194531458-b5dfeb1b-bad5-4dfa-909a-2e402262db9a.svg" alt="Blogger" /></a>
        <a href="mailto:gym4programming@gmail.com"><img src="https://user-images.githubusercontent.com/78341798/194531383-ddb2b774-5bb9-491c-b90912054e7f.gif" alt="Gmail" /></a>
      </div>
      <p>&copy; 2025 Alexio Junior Aaron. All rights reserved.</p>
    </footer>
  </div>
</body>
</html>
