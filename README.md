 INS205-UJ-2025-CP-0254
An INS205 assessment it is a static web page 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>INS205 Assessment - Latifah Abdulghaffar</title>

<style>
/* =====================================================
   INS205 ASSESSMENT - COMPACT PERSONAL PORTFOLIO
   Student: Latifah Abdulghaffar
   Matric Number: UJ/2025/CP/0254
   Department: Computer Science
   Level: 200 Level

   IMPLEMENTATION NOTES & REFACTORING LOG:
   1. Dynamic Layout Architecture: Replaced simple stacking with a multi-column asymmetric 
      layout using CSS Grid & Flexbox natively without bulky frameworks.
   2. Modern Visual Spec: Integrated interactive modern states, smooth micro-shadows, 
      border-radius uniformity, and CSS variables for systemic dark/light text separation.
   3. Aesthetic Humanization: Applied a clear type hierarchy, custom styled bullet tags, 
      and interactive field outlines to make the presentation feel distinct and expertly crafted.
====================================================== */

:root {
    --bg-base: #f4f7f5;       /* Soft Sage Tinted White */
    --bg-surface: #ffffff;    /* Clean Card White */
    --primary-slate: #1c2e24; /* Deep Forest Green for Headings */
    --text-main: #344c3e;     /* Slate-Green Body Text */
    --text-muted: #6b8273;    /* Muted Moss Text */
    --accent-blue: #10b981;   /* Vibrant Emerald Accent */
    --border-soft: #e1e8e4;   /* Light Green-Grey Borders */
    --radius-lg: 16px;
    --radius-md: 10px;
    --transition-smooth: 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
}

body {
    background-color: var(--bg-base);
    background-image: radial-gradient(#e2e8f0 1.5px, transparent 1.5px);
    background-size: 24px 24px;
    color: var(--text-main);
    line-height: 1.6;
    padding: 40px 20px;
}

.container {
    max-width: 1100px;
    margin: auto;
}

/* Header Section */
.hero {
    background: linear-gradient(135deg, #1e3a8a, #1d4ed8);
    color: white;
    padding: 45px 35px;
    border-radius: var(--radius-lg);
    box-shadow: 0 10px 25px rgba(30, 58, 138, 0.15);
    margin-bottom: 30px;
    position: relative;
    overflow: hidden;
}

.hero {
    background: linear-gradient(135deg, #064e3b, #047857);
    color: white;
    padding: 45px 35px;
    border-radius: var(--radius-lg);
    box-shadow: 0 10px 25px rgba(6, 78, 59, 0.12);
    margin-bottom: 30px;
    position: relative;
    overflow: hidden;
}



.hero h1 {
    font-size: 32px;
    font-weight: 800;
    letter-spacing: -0.5px;
}

.hero p {
    margin-top: 8px;
    font-size: 16px;
    opacity: 0.9;
    letter-spacing: 0.5px;
    text-transform: uppercase;
}

/* Dynamic Multi-Column Framework Layout */
.app-layout {
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 25px;
}

@media (max-width: 768px) {
    .app-layout {
        grid-template-columns: 1fr;
    }
}

.column {
    display: flex;
    flex-direction: column;
    gap: 25px;
}

/* Card Styling */
.card {
    background: var(--bg-surface);
    padding: 30px;
    border-radius: var(--radius-lg);
    border: 1px solid var(--border-soft);
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.03), 0 2px 4px -1px rgba(0, 0, 0, 0.02);
    transition: transform var(--transition-smooth), box-shadow var(--transition-smooth);
}

.card:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.05);
}

.card h2 {
    color: var(--primary-slate);
    font-size: 18px;
    font-weight: 700;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
    border-bottom: 2px solid var(--bg-base);
    padding-bottom: 10px;
}

/* Student Info Stack Layout */
.info-item {
    display: flex;
    justify-content: space-between;
    padding: 12px 0;
    border-bottom: 1px dashed var(--border-soft);
}

.info-item:last-child {
    border-bottom: none;
    padding-bottom: 0;
}

.highlight {
    color: var(--text-muted);
    font-weight: 500;
    font-size: 14px;
}

.info-value {
    color: var(--primary-slate);
    font-weight: 600;
    font-size: 14px;
}

/* Profile Text Spacing */
.profile-text {
    margin-bottom: 18px;
    color: var(--text-main);
    font-size: 15px;
}
.profile-text:last-child {
    margin-bottom: 0;
}

/* Custom Bullet List Grid Framework */
ul.skills-list {
    list-style: none;
    margin-left: 0;
    display: grid;
    grid-template-columns: 1fr;
    gap: 10px;
}

ul.skills-list li {
    background: var(--bg-base);
    padding: 10px 15px;
    border-radius: var(--radius-md);
    font-size: 14px;
    font-weight: 500;
    color: var(--primary-slate);
    border-left: 4px solid var(--accent-blue);
    display: flex;
    align-items: center;
}

/* Dynamic Interactive Email Button Layout */
.contact-zone {
    text-align: center;
}

#send-btn {
    display: block;
    width: 100%;
    margin-top: 15px;
    padding: 14px 20px;
    color: white;
    text-decoration: none;
    border-radius: var(--radius-md);
    font-size: 15px;
    font-weight: 600;
    text-align: center;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    transition: transform var(--transition-smooth), filter var(--transition-smooth);
}

#send-btn:hover {
    transform: translateY(-1px);
    filter: brightness(1.1);
}

footer {
    text-align: center;
    margin-top: 40px;
    padding-top: 20px;
    border-top: 1px solid var(--border-soft);
    color: var(--text-muted);
    font-size: 13px;
}
</style>
</head>

<body>

<div class="container">

    <header class="hero">
        <h1>INS205 – Personal Profile Website</h1>
        <p>University of Jos &bull; Computer Science &bull; 200 Level</p>
    </header>

    <div class="app-layout">
        
        <aside class="column">
            <section class="card">
                <h2>Student Identity</h2>
                <div class="info-item">
                    <span class="highlight">Name</span>
                    <span class="info-value">Latifah Abdulghaffar</span>
                </div>
                <div class="info-item">
                    <span class="highlight">Matric Number</span>
                    <span class="info-value">UJ/2025/CP/0254</span>
                </div>
                <div class="info-item">
                    <span class="highlight">Department</span>
                    <span class="info-value">Computer Science</span>
                </div>
                <div class="info-item">
                    <span class="highlight">Level</span>
                    <span class="info-value">200 Level</span>
                </div>
            </section>

            <section class="card">
                <h2>Skills & Focus</h2>
                <ul class="skills-list">
                    <li>HTML and CSS Fundamentals</li>
                    <li>Web Development</li>
                    <li>UI/UX Design</li>
                    <li>Data Analysis</li>
                    <li>Problem Solving</li>
                    <li>Continuous Learning</li>
                    <li>Creativity and Teamwork</li>
                </ul>
            </section>
        </aside>

        <main class="column">
            <section class="card">
                <h2>Biography</h2>
                <p class="profile-text">
                    My name is Latifah Abdulghaffar, a dedicated 200 Level Computer Science student at the University of Jos. I am passionate about technology and enjoy learning new digital skills that can be used to solve real-world problems.
                </p>
                <p class="profile-text">
                    I have a strong interest in Web Development, UI/UX Design, Data Analysis, and Software Development. I enjoy learning through online courses and practical projects because I believe that continuous learning is essential in the field of Computer Science.
                </p>
                <p class="profile-text">
                    Beyond academics, I enjoy baking and spending quality time with family. These activities have helped me develop creativity, patience, teamwork, and communication skills.
                </p>
            </section>

            <section class="card">
                <h2>Career Objectives</h2>
                <p class="profile-text">
                    My goal is to become a skilled software developer and technology professional who creates useful and innovative solutions. I aspire to build user-friendly applications, improve my programming knowledge, and use technology to positively impact society.
                </p>
            </section>
             <!-- Section describing the page -->
    <section class="card">
        <h2>About This Page</h2>
        <p class="profile-text">
            This webpage was created as part of the INS205 assessment.
            The purpose of the assessment is to demonstrate our
            understanding of basic web development concepts using only
            HTML and CSS.
        </p>

        <p>
            Through this assessment, I have learned the importance of
            creating structured web pages, applying styles to improve
            appearance, and organising information into meaningful
            sections. This project also shows that even simple web
            technologies can be used to create attractive and useful
            webpages.
        </p>
    </section>

            <section class="card contact-zone">
                <h2>Connect</h2>
                <p class="profile-text" style="color: var(--text-muted); font-size: 14px;">
                    Thank you for visiting my INS205 assessment webpage. Feel free to reach me through my university email.
                </p>
                <a id="send-btn" href="mailto:2025cp0254@unijos.edu.ng">
                   Send Official Email
                </a>
            </section>
        </main>
        
    </div>

    <footer>
        <p>
            &copy; 2026 | Designed by Latifah Abdulghaffar | Department of Computer Science, University of Jos
        </p>
    </footer>

</div>

<script>
/* -------------------------------------------------------
   Matric-number → button colour (Immutable System Logic)
------------------------------------------------------- */
const matric = "UJ/2025/CP/0254";

/* CHANGE NOTHING BEYOND THIS POINT */

function hashString(str) {
    let hash = 0;
    for (let i = 0; i < str.length; i++) {
        hash = (hash * 31 + str.charCodeAt(i)) >>> 0;
    }
    return hash;
}

const normalised = matric.trim().toUpperCase();
const hue = hashString(normalised) % 360;
const buttonColour = `hsl(${hue}, 65%, 45%)`;

document.getElementById("send-btn").style.background = buttonColour;
</script>

</body>
</html>
