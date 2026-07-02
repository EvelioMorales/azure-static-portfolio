# azure-static-portfolio

# Azure Static Portfolio Website with Azure Static Web Apps & GitHub CI/CD

## Project Summary

This project is a professional IT, cloud, and cybersecurity resume portfolio website customized from the **HTML5 UP Big Picture** template and deployed with **Azure Static Web Apps** using **GitHub-based CI/CD**.

The goal of this project was to turn a free responsive HTML template into a recruiter-ready personal portfolio that presents my resume, certifications, technical projects, GitHub repositories, and contact information in one place. The project also demonstrates practical skills in front-end customization, Git version control, cloud deployment, continuous deployment, troubleshooting, and technical documentation.

---

## Project Goals

- Build a professional resume portfolio for IT support, cloud support, cloud engineering, and cybersecurity roles.
- Customize an existing HTML5 UP template into a personal technical portfolio.
- Add a downloadable resume for employers and recruiters.
- Create a project gallery that links directly to GitHub repositories.
- Document certifications, technical skills, and hands-on cloud/security projects.
- Deploy the website using Azure Static Web Apps.
- Use GitHub and CI/CD to track changes and automate deployment.
- Document issues encountered and fixes applied to show problem-solving ability.

---

## Live Portfolio Features

The portfolio website includes the following sections:

### Home

The landing section introduces me as an IT support, cloud engineering, and cybersecurity-focused professional. It includes a professional headline, short portfolio summary, and a **View Resume** button.

### What I Do

This section summarizes my technical focus areas, including IT support, troubleshooting, documentation, cloud projects, and security-focused work. A side panel was added to make the section more visually balanced and easier for recruiters to scan.

### Who I Am

This section introduces my professional background, bilingual support experience, hands-on learning approach, and career direction. A matching side panel was added to highlight career strengths without repeating the same information from the main paragraph.

### Certifications & Training

This section lists certifications and training related to IT support, cloud computing, cybersecurity, SOC analysis, and Terraform.

### My Work

This section presents six project cards. Each card includes:

- A project image
- A visible project title
- A short project summary
- A skills line
- A clickable GitHub project link

### Contact

The contact section includes a clear call-to-action, email address, resume button, GitHub icon, and LinkedIn icon. The original form was removed so recruiters do not need to fill out a contact form.

---

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Git
- GitHub
- GitHub Actions
- Azure Static Web Apps
- Azure-managed HTTPS
- HTML5 UP Big Picture Template
- Font Awesome Icons

---

## Cloud and Deployment Services

### Azure Static Web Apps

Used to host and deploy the static portfolio website.

### GitHub Actions

Used for continuous integration and continuous deployment. Changes pushed to the GitHub repository can trigger the deployment workflow.

### GitHub Repository

Used for version control, project documentation, README updates, and source code management.

---

## Template Customization Work

This project started with the **Big Picture** template from HTML5 UP. The template was customized to fit a professional resume portfolio.

### Original Template Behavior

The original template included:

- Generic landing page text
- Placeholder sections
- Default gallery images
- A contact form placeholder
- Social media icons not specific to the portfolio
- Image lightbox behavior for gallery photos

### Custom Changes Made

- Replaced the default landing page with a professional portfolio introduction.
- Changed navigation from generic labels to recruiter-friendly sections.
- Added a focused headline: **IT Support • Cloud Engineering • Cybersecurity**.
- Added a **View Resume** button on the landing page.
- Added a **Certifications & Training** section.
- Replaced placeholder gallery items with real cloud and cybersecurity projects.
- Linked each project image to its GitHub repository.
- Added visible project titles, summaries, skills, and **View Project on GitHub** links.
- Removed the contact form and replaced it with direct contact options.
- Added GitHub and LinkedIn icons that route to the correct profiles.
- Added a footer with personal copyright and HTML5 UP attribution.
- Added side panels to balance the layout in the What I Do and Who I Am sections.
- Updated CSS for project cards, responsive gallery layout, highlight cards, and side panels.

---

## Project Gallery

The portfolio includes the following projects:

### 1. Azure Static Web Apps + GitHub CI/CD

Built and deployed a static portfolio website using Azure Static Web Apps with GitHub-based CI/CD automation.

**Skills:** Azure Static Web Apps, GitHub Actions, CI/CD, HTML, CSS

### 2. AWS IAM Security + EC2 Segmentation

Designed an AWS security lab using IAM access controls, EC2 resources, and segmented environments to demonstrate least privilege and secure cloud administration.

**Skills:** AWS IAM, EC2, Security Groups, Least Privilege, Cloud Security

### 3. Azure Remote Development Environment

Created a remote development environment using Azure infrastructure, Terraform, Docker, and VS Code SSH to support cloud-based development workflows.

**Skills:** Azure, Terraform, Docker, VS Code SSH, Linux

### 4. Static Website Hosting on Amazon S3

Hosted a static website on Amazon S3 to demonstrate cloud storage configuration, public website hosting, and basic AWS deployment practices.

**Skills:** Amazon S3, AWS, Static Hosting, Bucket Policy, HTML, CSS

### 5. AWS Image Label Generator

Built an image-labeling project using Amazon Rekognition and S3 to identify objects in uploaded images and demonstrate cloud-based AI services.

**Skills:** Amazon Rekognition, Amazon S3, AWS, Python, Cloud AI

### 6. Terraform AWS Multi-AZ VPC

Provisioned a multi-AZ AWS VPC proof of concept with Terraform to demonstrate infrastructure as code, networking, and scalable cloud architecture.

**Skills:** Terraform, AWS VPC, Subnets, Routing, Infrastructure as Code

---

## Problems Encountered and Fixes

This project involved several real troubleshooting issues. The fixes below show how I identified problems, researched the cause, and updated the code or Git workflow.

### Issue 1: Project Images Did Not Route to GitHub

**Problem:**  
After replacing the image links with GitHub repository URLs, clicking the project images did not always redirect to GitHub.

**Cause:**  
The original HTML5 UP Big Picture template uses a gallery/lightbox behavior. The gallery script can intercept clicks on images and open them as lightbox items instead of routing to external GitHub repositories.

**Fix:**

- Changed the anchor class from the original image/lightbox behavior to a custom class: `project-link`.
- Updated each project image link to use the GitHub repository URL.
- Added `target="_blank"` so the project opens in a new browser tab.
- Added `rel="noopener noreferrer"` for safer external linking.
- Added visible **View Project on GitHub** links under each project card so users clearly know the cards route to GitHub.

**Skill Demonstrated:** HTML troubleshooting, template behavior analysis, external linking, user experience improvement.

---

### Issue 2: Project Cards Looked Crowded

**Problem:**  
After adding project titles, descriptions, and skills under each image, the project section looked crowded and text overlapped visually.

**Cause:**  
The original gallery layout was designed mainly for images, not for full project cards with text content. Fixed image/card sizing caused the text to feel compressed.

**Fix:**

- Updated gallery CSS to use a wider layout.
- Added spacing with `gap` and `margin-bottom`.
- Set the image height on `.project-link` instead of forcing a fixed height on the entire article.
- Added text styling for project titles and project descriptions.
- Added responsive CSS so project cards stack cleanly on smaller screens.

**Skill Demonstrated:** CSS layout troubleshooting, responsive design, project-card UI improvement.

---

### Issue 3: Contact Form Was Not Useful for Recruiters

**Problem:**  
The original template included a contact form, but the form did not submit anywhere because the action was set to `#`.

**Cause:**  
Static websites do not process form submissions by default unless connected to a backend service or third-party form handler.

**Fix:**

- Removed the contact form.
- Replaced it with a direct email link using `mailto:`.
- Added a resume download button.
- Added clickable GitHub and LinkedIn icons.
- Wrote a stronger recruiter-focused call-to-action.

**Skill Demonstrated:** Static site limitation awareness, UX improvement, recruiter-focused design.

---

### Issue 4: Resume Link Needed Correct File Placement

**Problem:**  
The resume button required the PDF file to be saved in the correct location.

**Cause:**  
The HTML button used a relative path: `resume.pdf`. If the resume was placed inside the wrong folder, the link would not work.

**Fix:**

- Saved the resume PDF in the same folder as `index.html`.
- Used this link structure:

```html
<a href="resume.pdf" class="button" target="_blank" rel="noopener noreferrer">View Resume</a>
```

**Skill Demonstrated:** Relative path troubleshooting, static website file organization.

---

### Issue 5: HTML Structure Needed Cleanup

**Problem:**  
Some closing tags were misplaced while editing the gallery and footer sections.

**Cause:**  
The original template had nested section, content, gallery, and article elements. While adding new project cards, extra closing tags could break layout structure.

**Fix:**

- Corrected the gallery closing structure:

```html
</div>     <!-- closes .gallery -->
</div>     <!-- closes .content -->
</section> <!-- closes #work -->
```

- Moved the footer inside the `<body>` before the script tags.
- Confirmed each section closes before the next section starts.

**Skill Demonstrated:** HTML debugging, DOM structure cleanup, template editing.

---

### Issue 6: Side Panels Repeated Information

**Problem:**  
The What I Do and Who I Am side panels repeated information already listed in the highlight cards.

**Cause:**  
The first version of the side panels used similar wording to the main section cards.

**Fix:**

- Updated the side panels so they serve a different purpose.
- Used the side panels for quick-scan information.
- Used the highlight cards for strengths and proof points.

**Skill Demonstrated:** Content refinement, recruiter-focused UX, information architecture.

---

### Issue 7: Git Push Failed Because Branch Had No Upstream

**Problem:**  
Running `git push` produced this message:

```bash
fatal: The current branch main has no upstream branch.
```

**Cause:**  
The local `main` branch was not yet connected to the remote GitHub `main` branch.

**Fix:**

Used:

```bash
git push --set-upstream origin main
```

**Skill Demonstrated:** Git branch tracking, remote repository setup.

---

### Issue 8: Push Rejected Due to Remote Changes

**Problem:**  
Git rejected the push because the local branch was behind the remote branch.

**Cause:**  
The GitHub repository had changes that were not yet in the local repository.

**Fix:**

- Pulled remote changes with rebase.
- Resolved README conflict.
- Staged the resolved README file.
- Continued the rebase.
- Pushed successfully to GitHub.

Commands used during the process included:

```bash
git pull --rebase origin main
git add README.md
git rebase --continue
git push --set-upstream origin main
```

**Skill Demonstrated:** Git conflict resolution, rebase workflow, version control troubleshooting.

---

## Final Website Structure

```text
azure-static-portfolio/
│
├── README.md
├── html-web-portfolio/
│   ├── index.html
│   ├── resume.pdf
│   ├── assets/
│   │   ├── css/
│   │   │   └── main.css
│   │   └── js/
│   │       └── main.js
│   └── images/
│       ├── thumbs/
│       └── fulls/
```

---

## Key Skills Demonstrated

- Static website development
- HTML and CSS customization
- Responsive design troubleshooting
- Git and GitHub version control
- GitHub Actions deployment workflow
- Azure Static Web Apps hosting
- Resume portfolio design
- Technical documentation
- Cloud project presentation
- Problem-solving and debugging
- Recruiter-focused project organization

---

## How to Run Locally

1. Clone the repository:

```bash
git clone https://github.com/EvelioMorales/azure-static-portfolio.git
```

2. Open the project folder:

```bash
cd azure-static-portfolio/html-web-portfolio
```

3. Open `index.html` in a browser.

---

## How to Update the Website

1. Make changes to the website files.
2. Stage the changes:

```bash
git add .
```

3. Commit the changes:

```bash
git commit -m "Update portfolio website"
```

4. Push to GitHub:

```bash
git push
```

5. Azure Static Web Apps will redeploy the site through the GitHub workflow.

---

## Future Improvements

- Add a live website URL once deployment is complete.
- Add project screenshots or architecture diagrams for each project.
- Add badges for Azure, AWS, Terraform, GitHub Actions, and CompTIA A+.
- Add a dedicated skills section with categorized tools.
- Add accessibility testing and performance optimization.
- Add custom domain support.

---

## Template Credit

This project uses the **Big Picture** template from **HTML5 UP**. The template was customized for my personal resume portfolio and is used under the Creative Commons Attribution license.

Template: https://html5up.net/big-picture

---

## About Me

I am Evelio Morales Jr., a bilingual IT professional focused on technical support, cloud engineering, and cybersecurity. This portfolio was built to demonstrate hands-on technical growth, cloud project experience, documentation skills, and readiness for IT support, cloud support, and cybersecurity-related roles.
