<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Aspersh Upadhyay — Data Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #f9f7f4;
    --surface: #ffffff;
    --text: #1a1a1a;
    --muted: #6b6b6b;
    --border: #e5e2dd;
    --accent: #1a1a1a;
    --tag-bg: #f0ede8;
    --tag-text: #4a4a4a;
    --wip-bg: #fef3e2;
    --wip-text: #92580a;
    --wip-border: #fad89c;
    --done-bg: #e8f5ee;
    --done-text: #1a6b3a;
    --done-border: #a8dcbe;
    --link: #185fa5;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--bg);
    color: var(--text);
    font-size: 15px;
    line-height: 1.7;
  }

  nav {
    position: sticky;
    top: 0;
    background: var(--bg);
    border-bottom: 1px solid var(--border);
    padding: 0 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 56px;
    z-index: 100;
  }

  .nav-logo {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 16px;
    letter-spacing: -0.02em;
    color: var(--text);
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }

  .nav-links a {
    font-size: 13px;
    color: var(--muted);
    text-decoration: none;
    transition: color 0.15s;
  }

  .nav-links a:hover { color: var(--text); }

  .container { max-width: 860px; margin: 0 auto; padding: 0 2rem; }

  section { padding: 5rem 0; }

  .hero { padding: 7rem 0 5rem; }

  .hero-tag {
    display: inline-block;
    font-size: 12px;
    font-weight: 500;
    background: var(--done-bg);
    color: var(--done-text);
    padding: 4px 12px;
    border-radius: 20px;
    margin-bottom: 1.5rem;
    letter-spacing: 0.02em;
  }

  h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(36px, 6vw, 58px);
    font-weight: 700;
    line-height: 1.1;
    letter-spacing: -0.03em;
    margin-bottom: 1.25rem;
  }

  .hero-sub {
    font-size: 17px;
    color: var(--muted);
    max-width: 540px;
    line-height: 1.75;
    margin-bottom: 2rem;
  }

  .hero-links {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }

  .btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 9px 18px;
    border-radius: 8px;
    font-size: 13px;
    font-weight: 500;
    text-decoration: none;
    transition: all 0.15s;
    cursor: pointer;
    border: none;
    font-family: 'Inter', sans-serif;
  }

  .btn-dark {
    background: var(--text);
    color: #ffffff;
  }

  .btn-dark:hover { background: #333; }

  .btn-outline {
    background: transparent;
    color: var(--text);
    border: 1px solid var(--border);
  }

  .btn-outline:hover { background: var(--surface); }

  .divider {
    border: none;
    border-top: 1px solid var(--border);
  }

  h2 {
    font-family: 'Syne', sans-serif;
    font-size: 28px;
    font-weight: 700;
    letter-spacing: -0.02em;
    margin-bottom: 0.5rem;
  }

  .section-label {
    font-size: 12px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--muted);
    margin-bottom: 0.5rem;
  }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    margin-top: 2.5rem;
    align-items: start;
  }

  .about-text p {
    color: var(--muted);
    margin-bottom: 1rem;
    font-size: 15px;
  }

  .about-text p:last-child { margin-bottom: 0; }

  .about-details { display: flex; flex-direction: column; gap: 16px; }

  .detail-row {
    display: flex;
    flex-direction: column;
    gap: 3px;
    padding-bottom: 16px;
    border-bottom: 1px solid var(--border);
  }

  .detail-row:last-child { border-bottom: none; padding-bottom: 0; }

  .detail-label { font-size: 11px; font-weight: 500; text-transform: uppercase; letter-spacing: 0.08em; color: var(--muted); }
  .detail-value { font-size: 14px; color: var(--text); font-weight: 500; }

  .projects-grid {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    margin-top: 2.5rem;
  }

  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 1.75rem 2rem;
    transition: border-color 0.15s;
  }

  .project-card:hover { border-color: #c5c0ba; }

  .project-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 1rem;
    margin-bottom: 0.75rem;
    flex-wrap: wrap;
  }

  .project-title {
    font-family: 'Syne', sans-serif;
    font-size: 18px;
    font-weight: 600;
    letter-spacing: -0.01em;
  }

  .status-badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    font-size: 11px;
    font-weight: 500;
    padding: 3px 10px;
    border-radius: 20px;
    white-space: nowrap;
    flex-shrink: 0;
  }

  .status-done {
    background: var(--done-bg);
    color: var(--done-text);
    border: 1px solid var(--done-border);
  }

  .status-wip {
    background: var(--wip-bg);
    color: var(--wip-text);
    border: 1px solid var(--wip-border);
  }

  .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: currentColor;
    display: inline-block;
  }

  .project-desc {
    color: var(--muted);
    font-size: 14px;
    line-height: 1.7;
    margin-bottom: 1rem;
  }

  .project-finding {
    background: var(--bg);
    border-radius: 8px;
    padding: 10px 14px;
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 1rem;
    border-left: 3px solid var(--border);
    border-radius: 0 8px 8px 0;
  }

  .project-finding strong { color: var(--text); }

  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 1rem;
  }

  .tag {
    background: var(--tag-bg);
    color: var(--tag-text);
    font-size: 11px;
    font-weight: 500;
    padding: 3px 10px;
    border-radius: 20px;
    font-family: 'Inter', sans-serif;
  }

  .project-link {
    font-size: 13px;
    color: var(--link);
    text-decoration: none;
    font-weight: 500;
  }

  .project-link:hover { text-decoration: underline; }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 1rem;
    margin-top: 2.5rem;
  }

  .skill-group {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.25rem;
  }

  .skill-group-title {
    font-size: 11px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--muted);
    margin-bottom: 0.75rem;
  }

  .skill-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 6px;
  }

  .skill-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 13px;
    color: var(--text);
  }

  .skill-level {
    font-size: 11px;
    color: var(--muted);
    font-style: italic;
  }

  .learning-now {
    color: var(--wip-text);
    font-size: 11px;
    font-weight: 500;
    background: var(--wip-bg);
    padding: 1px 7px;
    border-radius: 10px;
  }

  .contact-section {
    border: 1px solid var(--border);
    border-radius: 20px;
    background: var(--surface);
    padding: 3rem;
    text-align: center;
  }

  .contact-section p {
    color: var(--muted);
    max-width: 440px;
    margin: 0.75rem auto 2rem;
    font-size: 15px;
  }

  .contact-links {
    display: flex;
    gap: 12px;
    justify-content: center;
    flex-wrap: wrap;
  }

  footer {
    padding: 2rem;
    text-align: center;
    font-size: 12px;
    color: var(--muted);
    border-top: 1px solid var(--border);
  }

  @media (max-width: 640px) {
    .about-grid { grid-template-columns: 1fr; }
    .container { padding: 0 1.25rem; }
    nav { padding: 0 1.25rem; }
    .nav-links { gap: 1rem; }
    .contact-section { padding: 2rem 1.25rem; }
  }
</style>
</head>
<body>

<nav>
  <a href="#" class="nav-logo">Aspersh Upadhyay</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<div class="container">

  <section class="hero" id="home">
    <div class="hero-tag">Open to work — New Delhi, India</div>
    <h1>Turning data<br/>into decisions.</h1>
    <p class="hero-sub">
      I'm Aspersh, a BCA graduate learning data analytics. I work with SQL, Python, and Power BI to clean, explore, and visualize data. Still building my portfolio but committed to showing real work over polished talk.
    </p>
    <div class="hero-links">
      <a href="https://linkedin.com/in/aspersh-upadhyay" class="btn btn-dark" target="_blank">LinkedIn</a>
      <a href="https://github.com/aspershupadhyay" class="btn btn-outline" target="_blank">GitHub</a>
      <a href="mailto:aspershupadhyay@gmail.com" class="btn btn-outline">Email me</a>
    </div>
  </section>

  <hr class="divider"/>

  <section id="about">
    <div class="section-label">Background</div>
    <h2>A bit about me</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>
          I graduated with a BCA from Swami Vivekananda Subharti University in 2023. Since then I've been working a night shift customer service job while teaching myself data analytics on the side.
        </p>
        <p>
          I got into data because I like the puzzle of it. You take a messy spreadsheet or a broken dataset and you ask questions until it starts making sense. That process genuinely interests me.
        </p>
        <p>
          I know SQL, Python basics (Pandas, NumPy, Seaborn), Excel, and Power BI. I'm not going to pretend I'm an expert. I'm learning, building projects, and trying to get good at the things that actually matter in a real analyst job.
        </p>
      </div>
      <div class="about-details">
        <div class="detail-row">
          <span class="detail-label">Location</span>
          <span class="detail-value">New Delhi, India</span>
        </div>
        <div class="detail-row">
          <span class="detail-label">Education</span>
          <span class="detail-value">BCA, Subharti University (2023)</span>
        </div>
        <div class="detail-row">
          <span class="detail-label">Currently working on</span>
          <span class="detail-value">3 end-to-end analytics projects</span>
        </div>
        <div class="detail-row">
          <span class="detail-label">Looking for</span>
          <span class="detail-value">Entry-level data analyst roles</span>
        </div>
        <div class="detail-row">
          <span class="detail-label">Languages</span>
          <span class="detail-value">Hindi (native), English (working)</span>
        </div>
      </div>
    </div>
  </section>

  <hr class="divider"/>

  <section id="projects">
    <div class="section-label">Portfolio</div>
    <h2>Projects</h2>

    <div class="projects-grid">

      <div class="project-card">
        <div class="project-header">
          <span class="project-title">Seoul Bike Sharing Demand Analysis</span>
          <span class="status-badge status-done"><span class="dot"></span>Completed</span>
        </div>
        <p class="project-desc">
          I worked with a weather and time dataset tracking bike rental counts in Seoul over a full year. The goal was to figure out what conditions drive rental demand so the business can plan better.
        </p>
        <div class="project-finding">
          <strong>What I found:</strong> Temperature has the strongest relationship with rentals (0.73 correlation). Peak demand hits at 5 to 6 PM on weekdays, more than double the daily average. Winter months saw rentals drop by roughly 70%.
        </div>
        <div class="tags">
          <span class="tag">Python</span>
          <span class="tag">Pandas</span>
          <span class="tag">Seaborn</span>
          <span class="tag">Matplotlib</span>
          <span class="tag">NumPy</span>
          <span class="tag">EDA</span>
        </div>
        <a href="https://github.com/aspershupadhyay/Seoul-Bike-Sharing-Demand-Analytics" class="project-link" target="_blank">View on GitHub ↗</a>
      </div>

      <div class="project-card">
        <div class="project-header">
          <span class="project-title">Sales Performance Dashboard</span>
          <span class="status-badge status-done"><span class="dot"></span>Completed</span>
        </div>
        <p class="project-desc">
          Built an interactive dashboard in Power BI to track sales KPIs. Used Power Query to clean and transform the data before loading, then built out visuals for order trends, product performance, and regional breakdowns.
        </p>
        <div class="project-finding">
          <strong>Tools used:</strong> Power BI, Power Query, DAX for calculated measures including MoM growth and category contribution. Published to Power BI Service.
        </div>
        <div class="tags">
          <span class="tag">Power BI</span>
          <span class="tag">DAX</span>
          <span class="tag">Power Query</span>
          <span class="tag">Data Modeling</span>
          <span class="tag">ETL</span>
        </div>
        <a href="https://github.com/aspershupadhyay" class="project-link" target="_blank">View on GitHub ↗</a>
      </div>

      <div class="project-card">
        <div class="project-header">
          <span class="project-title">E-Commerce Sales Analysis</span>
          <span class="status-badge status-wip"><span class="dot"></span>In progress</span>
        </div>
        <p class="project-desc">
          Working on an end-to-end SQL and Excel project using the Superstore dataset. Writing queries to look at revenue trends, top products, regional performance, and customer purchase patterns. Will include an Excel dashboard when done.
        </p>
        <div class="tags">
          <span class="tag">SQL</span>
          <span class="tag">CTEs</span>
          <span class="tag">Window functions</span>
          <span class="tag">Excel</span>
          <span class="tag">Pivot tables</span>
        </div>
        <span style="font-size:12px; color: var(--wip-text);">Link will be added once complete</span>
      </div>

      <div class="project-card">
        <div class="project-header">
          <span class="project-title">Customer Churn Analysis</span>
          <span class="status-badge status-wip"><span class="dot"></span>In progress</span>
        </div>
        <p class="project-desc">
          EDA project on the Telco churn dataset. Exploring which customer segments churn the most and what factors matter. Will produce a full Jupyter notebook with business recommendations at the end.
        </p>
        <div class="tags">
          <span class="tag">Python</span>
          <span class="tag">Pandas</span>
          <span class="tag">Seaborn</span>
          <span class="tag">EDA</span>
        </div>
        <span style="font-size:12px; color: var(--wip-text);">Link will be added once complete</span>
      </div>

      <div class="project-card">
        <div class="project-header">
          <span class="project-title">HR Analytics Dashboard</span>
          <span class="status-badge status-wip"><span class="dot"></span>Upcoming</span>
        </div>
        <p class="project-desc">
          Planning a multi-page Power BI dashboard on the IBM HR dataset. Will include attrition analysis by department, job role, and tenure, with DAX measures and drill-through pages.
        </p>
        <div class="tags">
          <span class="tag">Power BI</span>
          <span class="tag">DAX</span>
          <span class="tag">SQL</span>
          <span class="tag">HR Analytics</span>
        </div>
        <span style="font-size:12px; color: var(--wip-text);">Starting soon</span>
      </div>

    </div>
  </section>

  <hr class="divider"/>

  <section id="skills">
    <div class="section-label">What I work with</div>
    <h2>Skills</h2>

    <div class="skills-grid">

      <div class="skill-group">
        <div class="skill-group-title">Languages</div>
        <ul class="skill-list">
          <li class="skill-item">
            SQL
            <span class="skill-level">intermediate</span>
          </li>
          <li class="skill-item">
            Python
            <span class="skill-level">beginner / learning</span>
          </li>
          <li class="skill-item">
            Java
            <span class="skill-level">basic</span>
          </li>
        </ul>
      </div>

      <div class="skill-group">
        <div class="skill-group-title">Python libraries</div>
        <ul class="skill-list">
          <li class="skill-item">Pandas <span class="skill-level">learning</span></li>
          <li class="skill-item">NumPy <span class="skill-level">learning</span></li>
          <li class="skill-item">Seaborn <span class="skill-level">learning</span></li>
          <li class="skill-item">Matplotlib <span class="skill-level">learning</span></li>
        </ul>
      </div>

      <div class="skill-group">
        <div class="skill-group-title">BI and visualization</div>
        <ul class="skill-list">
          <li class="skill-item">Power BI <span class="skill-level">intermediate</span></li>
          <li class="skill-item">MS Excel <span class="skill-level">intermediate</span></li>
          <li class="skill-item">Tableau <span class="learning-now">learning</span></li>
        </ul>
      </div>

      <div class="skill-group">
        <div class="skill-group-title">Databases</div>
        <ul class="skill-list">
          <li class="skill-item">PostgreSQL <span class="skill-level">learning</span></li>
          <li class="skill-item">MySQL <span class="skill-level">basic</span></li>
        </ul>
      </div>

      <div class="skill-group">
        <div class="skill-group-title">Tools</div>
        <ul class="skill-list">
          <li class="skill-item">Jupyter Notebook <span class="skill-level">regular use</span></li>
          <li class="skill-item">Git / GitHub <span class="skill-level">basic</span></li>
          <li class="skill-item">VS Code <span class="skill-level">regular use</span></li>
        </ul>
      </div>

    </div>
  </section>

  <hr class="divider"/>

  <section id="contact">
    <div class="contact-section">
      <div class="section-label" style="text-align:center;">Get in touch</div>
      <h2>Say hello</h2>
      <p>
        If you're hiring for a data analyst role or just want to connect, feel free to reach out. I'm actively looking for entry-level opportunities in India.
      </p>
      <div class="contact-links">
        <a href="mailto:aspershupadhyay@gmail.com" class="btn btn-dark">aspershupadhyay@gmail.com</a>
        <a href="https://linkedin.com/in/aspersh-upadhyay" class="btn btn-outline" target="_blank">LinkedIn</a>
        <a href="https://github.com/aspershupadhyay" class="btn btn-outline" target="_blank">GitHub</a>
      </div>
    </div>
  </section>

</div>

<footer>
  Aspersh Upadhyay &middot; New Delhi, India &middot; 2026
</footer>

</body>
</html>
