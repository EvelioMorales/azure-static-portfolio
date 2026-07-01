# Azure Static Portfolio Website with HTML5 UP Template Customization and GitHub CI/CD

## Project Description

This project demonstrates how I customized and deployed a professional IT, cloud, and cybersecurity portfolio website using the **HTML5 UP Big Picture** template, **Azure Static Web Apps**, **GitHub**, and **GitHub Actions CI/CD**.

The goal of this project was to turn a general-purpose website template into a resume-ready portfolio that presents my technical skills, certifications, downloadable resume, cloud projects, GitHub repositories, and contact information in a clean, recruiter-friendly format.

This project demonstrates beginner-to-intermediate skills in front-end customization, cloud hosting, source control, CI/CD deployment, technical documentation, and professional portfolio development.

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Architecture](#2-architecture)
3. [Technologies Used](#3-technologies-used)
4. [Template Credit](#4-template-credit)
5. [Website Customizations](#5-website-customizations)
6. [Project Folder Structure](#6-project-folder-structure)
7. [Step-by-Step Deployment](#7-step-by-step-deployment)
8. [GitHub CI/CD Workflow](#8-github-cicd-workflow)
9. [Security Features](#9-security-features)
10. [Troubleshooting and Fixes](#10-troubleshooting-and-fixes)
11. [Lessons Learned](#11-lessons-learned)
12. [Future Improvements](#12-future-improvements)
13. [Resume Project Description](#13-resume-project-description)
14. [Author](#14-author)

---

# 1. Project Overview

## Goal

The goal of this project was to build and deploy a professional resume portfolio website using Azure Static Web Apps and GitHub CI/CD while documenting the process as a cloud engineering portfolio project.

The website includes:

- Home section
- What I Do section
- Who I Am section
- Certifications section
- My Work / Projects section
- Downloadable resume button
- GitHub and LinkedIn contact icons
- Clickable project images that route to GitHub repositories
- Responsive design based on the HTML5 UP Big Picture template

## What This Project Demonstrates

- Azure Static Web Apps deployment
- GitHub source control
- GitHub Actions CI/CD
- Static website hosting
- HTML and CSS customization
- Template modification and attribution
- Project documentation
- Recruiter-focused portfolio design
- Cloud and cybersecurity project presentation

---

# 2. Architecture

## Architecture Diagram

```text
User / Recruiter
      |
      v
Browser over HTTPS
      |
      v
Azure Static Web Apps
      |
      v
Deployed HTML / CSS / JavaScript Portfolio
      |
      v
GitHub Repository + GitHub Actions CI/CD
```

## Architecture Explanation

The portfolio website is hosted using Azure Static Web Apps. The project files are stored in GitHub, and Azure creates a GitHub Actions workflow that automatically deploys updates when changes are pushed to the main branch.

When a recruiter visits the website, they can review my resume, certifications, technical skills, cloud projects, and contact information. Each project image links directly to its related GitHub repository.

---

# 3. Technologies Used

| Technology | Purpose |
|---|---|
| Azure Static Web Apps | Hosts the static portfolio website |
| GitHub | Stores project source code |
| GitHub Actions | Automates CI/CD deployment |
| HTML | Structures the website content |
| CSS | Styles the website layout and project cards |
| JavaScript | Supports template interactivity |
| VS Code | Code editor used for customization |
| Git | Version control |
| HTML5 UP Big Picture | Base website template |

---

# 4. Template Credit

This project uses the **Big Picture** template from **HTML5 UP**.

The template was customized for my personal IT, cloud, and cybersecurity resume portfolio. The original template credit is kept in the footer to comply with the Creative Commons Attribution license.

Template source: [HTML5 UP](https://html5up.net)

---

# 5. Website Customizations

The original HTML5 UP Big Picture template was modified to create a professional resume portfolio.

## Navigation Updates

The navigation was updated from the default template links to portfolio-specific sections:

```html
<li><a href="#intro">Home</a></li>
<li><a href="#one">What I Do</a></li>
<li><a href="#two">Who I Am</a></li>
<li><a href="#certifications">Certifications</a></li>
<li><a href="#work">My Work</a></li>
<li><a href="#contact">Contact</a></li>
```

## Home Section Update

The default template intro text was replaced with a professional landing page message focused on IT support, cloud engineering, cybersecurity, and technical projects.

Example headline:

```html
<h2>Hello, I'm Evelio.</h2>
```

## What I Do Section

The section was customized to explain my focus areas:

- IT support
- Cloud engineering
- Cybersecurity
- Technical troubleshooting
- Documentation
- Hands-on cloud projects

## Who I Am Section

The section was rewritten to introduce me as a bilingual IT professional from Houston, Texas, with a background in customer service, troubleshooting, computer repair, scheduling, and hands-on technical projects.

## Certifications Section Added

A new Certifications section was added to highlight relevant IT, cloud, and cybersecurity training.

Example certifications included:

- CompTIA A+
- Microsoft Azure Fundamentals — AZ-900
- Google Cybersecurity Certificate
- SOC Analyst Training
- Terraform Hands-On Training

## My Work Section Improved

The original image gallery was converted into a project portfolio section.

Each project now includes:

- Clickable project image
- GitHub repository link
- Visible project title
- Short project description
- Skills used

Example project card structure:

```html
<article class="from-left">
    <a href="https://github.com/EvelioMorales/Azure-Static-Portfolio-Website-with-Azure-Static-Web-App-GitHub-CI-CD"
       class="project-link"
       target="_blank"
       rel="noopener noreferrer">
        <img src="images/thumbs/01.jpg"
             title="Azure Static Web Apps and GitHub Actions"
             alt="Azure Static Web Apps and GitHub Actions project" />
    </a>

    <h3>Azure Static Web Apps + GitHub CI/CD</h3>
    <p>Deployed a static portfolio website using Azure Static Web Apps and GitHub Actions for automated CI/CD.</p>
    <p><strong>Skills:</strong> Azure Static Web Apps, GitHub Actions, HTML, CSS, CI/CD</p>
</article>
```

## Project Image Links Updated

The original template opened full-size images when clicked. This was changed so each project image routes to a GitHub repository instead.

Original template behavior:

```html
<a href="images/fulls/01.jpg" class="image fit">
```

Updated project behavior:

```html
<a href="https://github.com/EvelioMorales/example-project"
   class="project-link"
   target="_blank"
   rel="noopener noreferrer">
```

## Gallery CSS Updated

The gallery CSS was updated so project cards have enough space for images, descriptions, and skills.

Key update:

```css
.gallery article {
    width: calc(50% - 1em);
    position: relative;
    text-align: center;
    margin-bottom: 2em;
}

.gallery .project-link {
    display: block;
    width: 100%;
    height: 18em;
    overflow: hidden;
    border-radius: 0.35em;
    margin-bottom: 1em;
}

.gallery .project-link img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
```

## Contact Section Rebuilt

The original contact form was removed because it did not send messages without backend configuration.

The replacement contact section includes:

- Strong call-to-action
- Email link
- Resume download button
- GitHub icon
- LinkedIn icon

Example contact call-to-action:

```html
<h2>Let’s Connect</h2>
<p>
    I am actively pursuing opportunities in IT support, cloud engineering, cybersecurity, and technical support.
    If you are looking for someone who is motivated, bilingual, hands-on, and committed to solving technical problems,
    I would be glad to connect. View my resume, explore my GitHub projects, or contact me directly by email.
</p>
```

## Resume Download Added

A downloadable resume button was added:

```html
<a href="resume.pdf" class="button" target="_blank" rel="noopener noreferrer">View Resume</a>
```

The resume file should be saved in the same folder as `index.html`:

```text
html-web-portfolio/
├── index.html
├── resume.pdf
├── assets/
└── images/
```

---

# 6. Project Folder Structure

```text
azure-static-portfolio/
├── index.html
├── resume.pdf
├── README.md
├── assets/
│   ├── css/
│   │   └── main.css
│   ├── js/
│   │   └── main.js
│   └── sass/
├── images/
│   ├── thumbs/
│   │   ├── 01.jpg
│   │   ├── 02.jpg
│   │   ├── 03.jpg
│   │   ├── 04.jpg
│   │   ├── 05.jpg
│   │   └── 06.jpg
│   └── fulls/
├── screenshots/
│   ├── 01-live-homepage.png
│   ├── 02-project-gallery.png
│   ├── 03-contact-section.png
│   ├── 04-github-actions-success.png
│   └── 05-azure-static-web-app-overview.png
└── architecture/
    └── azure-static-portfolio-architecture.png
```

---

# 7. Step-by-Step Deployment

## Step 1 — Download the HTML5 UP Template

The Big Picture template was downloaded from HTML5 UP and extracted locally.

## Step 2 — Open the Project in VS Code

The project folder was opened in Visual Studio Code to edit the HTML, CSS, images, and project content.

## Step 3 — Customize the Template

The default template content was replaced with resume portfolio content.

Main updates included:

- Replaced the default intro text
- Updated navigation labels
- Added professional portfolio copy
- Added certifications
- Added project cards
- Added clickable GitHub project images
- Added downloadable resume
- Replaced the form with direct contact links
- Kept HTML5 UP design credit

## Step 4 — Add Project Images

Architecture diagrams and project images were added to the `images/thumbs/` folder and used in the My Work section.

## Step 5 — Add Resume PDF

The resume file was saved as:

```text
resume.pdf
```

and placed in the same folder as `index.html`.

## Step 6 — Initialize Git

```bash
git init
git add .
git commit -m "Customize HTML5 UP portfolio template"
```

## Step 7 — Connect to GitHub

```bash
git branch -M main
git remote add origin https://github.com/EvelioMorales/Azure-Static-Portfolio-Website-with-Azure-Static-Web-App-GitHub-CI-CD.git
git push -u origin main
```

## Step 8 — Create Azure Static Web App

In the Azure Portal, create a new Static Web App.

Recommended settings:

```text
Resource Group: rg-portfolio-dev
Name: azure-static-portfolio
Plan: Free
Source: GitHub
Branch: main
Build Preset: Custom
App Location: /
Output Location: leave blank
```

## Step 9 — Verify GitHub Actions Deployment

After Azure Static Web Apps connects to the GitHub repository, it creates a GitHub Actions workflow.

When code is pushed to the main branch, GitHub Actions deploys the latest version of the website to Azure.

## Step 10 — Test the Live Website

Verify that:

- The site loads over HTTPS
- Navigation links work
- Project images open GitHub repositories
- Resume button opens `resume.pdf`
- Email link opens the correct email address
- GitHub and LinkedIn icons work
- Website works on desktop and mobile

---

# 8. GitHub CI/CD Workflow

Azure Static Web Apps automatically creates a GitHub Actions workflow for deployment.

The deployment process works like this:

```text
Edit website files locally
        |
        v
Commit changes with Git
        |
        v
Push code to GitHub main branch
        |
        v
GitHub Actions workflow starts
        |
        v
Azure Static Web Apps deploys updated website
        |
        v
Live portfolio updates automatically
```

---

# 9. Security Features

This project includes several security and best-practice features:

- HTTPS enabled through Azure Static Web Apps
- Azure-managed SSL/TLS certificate
- Static website architecture with no exposed server backend
- GitHub version control for change history
- GitHub Actions deployment logs
- External links use `target="_blank"` and `rel="noopener noreferrer"`
- No contact form collecting user data
- No database or sensitive backend services exposed

---

# 10. Troubleshooting and Fixes

## Challenge 1 — Project Images Opened the Lightbox Instead of GitHub

The original template used an image gallery/lightbox behavior. This caused images to open full-size images instead of routing users to GitHub project repositories.

### Fix

The project links were changed from:

```html
<a href="images/fulls/01.jpg" class="image fit">
```

To:

```html
<a href="https://github.com/EvelioMorales/example-project"
   class="project-link"
   target="_blank"
   rel="noopener noreferrer">
```

The gallery JavaScript behavior may also need to be adjusted in `assets/js/main.js` if the lightbox still intercepts clicks.

## Challenge 2 — Project Cards Looked Crowded

After adding project titles, descriptions, and skills, the project cards became crowded because the CSS was originally designed for image-only gallery items.

### Fix

The gallery CSS was updated to allow project cards to expand vertically. A fixed height was applied only to the image link, not to the entire article card.

## Challenge 3 — Contact Form Did Not Send Messages

The original template used a form with this placeholder action:

```html
<form method="post" action="#">
```

This does not send messages without a backend or form service.

### Fix

The form was removed and replaced with:

- Email link
- Resume button
- GitHub icon
- LinkedIn icon

## Challenge 4 — Resume Link Needed Correct File Location

The resume button links to:

```html
<a href="resume.pdf">View Resume</a>
```

### Fix

The `resume.pdf` file was saved in the same folder as `index.html`.

---

# 11. Lessons Learned

Through this project, I learned how to:

- Customize an existing HTML/CSS template for a professional use case
- Structure a portfolio for recruiters and hiring managers
- Use Git and GitHub for source control
- Deploy a static website with Azure Static Web Apps
- Use GitHub Actions for automated CI/CD deployment
- Replace template placeholder content with professional resume content
- Link project images directly to GitHub repositories
- Add a downloadable resume to a static website
- Troubleshoot CSS layout issues
- Document changes clearly in a technical README

---

# 12. Future Improvements

Planned improvements:

- Add a custom domain
- Add security headers documentation
- Add a Terraform deployment version
- Add Azure Monitor or Application Insights documentation
- Add screenshots of the live website and deployment workflow
- Add a project walkthrough video
- Add better mobile spacing for project cards
- Add accessibility improvements for images and buttons

---

# 13. Resume Project Description

**Azure Static Portfolio Website with GitHub CI/CD**  
Customized and deployed a professional resume portfolio website using the HTML5 UP Big Picture template, Azure Static Web Apps, GitHub, and GitHub Actions. Updated the template with resume content, certifications, project cards, clickable GitHub project images, a downloadable resume, and direct contact links. Implemented automated CI/CD deployment from GitHub to Azure Static Web Apps and documented the full deployment process.

**Skills Used:** Azure Static Web Apps, GitHub, GitHub Actions, HTML, CSS, JavaScript, CI/CD, Static Website Hosting, Technical Documentation

---

# 14. Author

**Evelio Morales Jr.**  
Bilingual IT Professional focused on IT support, cloud engineering, cybersecurity, and technical support.

- GitHub: [https://github.com/EvelioMorales](https://github.com/EvelioMorales)
- LinkedIn: Replace with your LinkedIn URL
- Portfolio: Replace with your live Azure Static Web Apps URL
