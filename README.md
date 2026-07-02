# Azure Static Portfolio Website with Azure Static Web Apps & GitHub CI/CD

## Project Overview

This project is a professional resume portfolio website customized from the **HTML5 UP Big Picture** template and deployed using **Azure Static Web Apps** with **GitHub-based CI/CD**.

The goal of this project was to build and document a real-world cloud portfolio that demonstrates front-end customization, GitHub version control, Azure deployment, CI/CD automation, responsive design updates, and troubleshooting skills.

The website presents my resume, certifications, hands-on cloud projects, GitHub repositories, and contact information in a clean recruiter-friendly format.

---

## Live Portfolio Features

The portfolio includes the following sections:

- **Home** — Intro section with professional headline, resume button, and quick portfolio overview.
- **What I Do** — Summary of IT support, cloud engineering, cybersecurity, troubleshooting, and documentation skills.
- **Who I Am** — Professional background, bilingual support, hands-on learning, and career direction.
- **Certifications & Training** — IT, cloud, cybersecurity, SOC, and Terraform-related training.
- **My Work** — Project gallery with clickable project cards that route to GitHub repositories.
- **Contact** — Email, resume download, GitHub link, and LinkedIn link.

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

## Template Customization Summary

This project started from the **Big Picture** template by HTML5 UP. The template was customized into a professional IT, cloud, and cybersecurity portfolio.

### Major HTML Changes

- Replaced default template content with custom resume portfolio content.
- Updated page navigation to include Home, What I Do, Who I Am, Certifications & Training, My Work, and Contact.
- Added a professional intro headline: `Hello, I'm Evelio.` and `IT Support • Cloud Engineering • Cybersecurity`.
- Added a **View Resume** button that opens `resume.pdf`.
- Added custom side panels to balance the blank visual space in the What I Do and Who I Am sections.
- Added highlight cards for quick recruiter scanning.
- Added a Certifications & Training section.
- Rebuilt the My Work section into project cards.
- Added project titles, descriptions, skills, and GitHub links.
- Added a direct Contact section with email, resume button, GitHub icon, and LinkedIn icon.
- Added footer attribution for HTML5 UP.

---

## Current Website Sections

### Home

The Home section introduces the portfolio, career focus, resume download, and project direction.

### What I Do

This section explains my focus on technical support, cloud engineering, cybersecurity, documentation, and hands-on project work.

### Who I Am

This section introduces my professional background as a bilingual IT professional focused on support, cloud, and cybersecurity.

### Certifications & Training

This section lists relevant certifications and training, including:

- CompTIA A+
- Microsoft Azure Fundamentals — AZ-900
- Google Cybersecurity Certificate
- SOC Analyst Training
- Terraform Hands-On Training

### My Work

The project gallery includes six portfolio projects:

1. **Azure Static Web Apps + GitHub CI/CD**
2. **AWS IAM Security + EC2 Segmentation**
3. **Azure Remote Development Environment**
4. **Static Website Hosting on Amazon S3**
5. **AWS Image Label Generator**
6. **Terraform AWS Multi-AZ VPC**

Each project card includes:

- Project image
- Project title
- Project summary
- Skills used
- Clickable image linking to GitHub
- Visible `View Project on GitHub` link

### Contact

The contact section includes:

- Email link
- Resume button
- GitHub profile link
- LinkedIn profile link

---

## Problems Encountered and Fixes

This project included several real troubleshooting steps that improved the final site.

### Issue 1: Project Images Did Not Redirect to GitHub

**Problem:**  
The original gallery images opened image files or did not redirect correctly when clicked.

**Cause:**  
The HTML5 UP template was originally designed as an image gallery/lightbox. The default gallery link structure pointed to full-size images instead of GitHub repositories.

**Fix:**  
Each image anchor tag was updated to point directly to the correct GitHub repository.

Example:

```html
<a href="https://github.com/EvelioMorales/example-project"
   class="project-link"
   target="_blank"
   rel="noopener noreferrer">
```

A custom `project-link` class was also added to support GitHub project navigation.

---

### Issue 2: Gallery Cards Looked Crowded After Adding Text

**Problem:**  
After adding project titles, descriptions, and skills, the project section became crowded and text overlapped.

**Cause:**  
The original gallery layout was designed for images only. Once project descriptions were added, the old spacing and fixed image layout no longer worked well.

**Fix:**  
The gallery CSS was updated to use a wider layout, better spacing, consistent image heights, and cleaner project-card formatting.

Key CSS updates included:

```css
.gallery {
	display: flex;
	flex-wrap: wrap;
	width: 65em;
	max-width: 100%;
	gap: 2em;
}

.gallery article {
	width: calc(50% - 1em);
	text-align: center;
	margin-bottom: 2em;
}
```

---

### Issue 3: Resume Button Needed a Valid File Path

**Problem:**  
The resume button needed to open the resume correctly from the website.

**Cause:**  
The site link used `resume.pdf`, so the PDF had to be placed in the same folder as `index.html`.

**Fix:**  
The resume file was saved as:

```text
html-web-portfolio/resume.pdf
```

The button uses:

```html
<a href="resume.pdf" class="button" target="_blank" rel="noopener noreferrer">View Resume</a>
```

---

### Issue 4: Contact Form Was Not Needed

**Problem:**  
The original template included a contact form, but the form did not send messages without a backend service.

**Cause:**  
The template used a placeholder form action.

**Fix:**  
The form was removed and replaced with a simple recruiter-friendly contact section containing email, resume, GitHub, and LinkedIn links.

---

### Issue 5: Footer Was Outside the HTML Body

**Problem:**  
The footer was accidentally placed after the closing `</html>` tag.

**Cause:**  
The footer was added after the scripts and closing document tags.

**Fix:**  
The footer was moved inside the `<body>` before the JavaScript scripts.

Correct structure:

```html
<footer id="footer">
	<ul class="menu">
		<li>&copy; Evelio Morales Jr.</li>
		<li>Design: <a href="https://html5up.net">HTML5 UP</a></li>
	</ul>
</footer>

<script src="assets/js/jquery.min.js"></script>
...
</body>
</html>
```

---

### Issue 6: Blank Space in What I Do and Who I Am Sections

**Problem:**  
The left and right sides of the template sections felt empty.

**Cause:**  
The original Big Picture template uses large fullscreen sections with content aligned to one side, leaving open visual space.

**Fix:**  
Side panels were added for quick-scan information such as tools, strengths, or career direction.

CSS was added for reusable side panels:

```css
.side-panel {
	position: absolute;
	top: 50%;
	transform: translateY(-50%);
	width: 22em;
	padding: 2em;
	background: rgba(255, 255, 255, 0.82);
	color: #39454b;
	border-radius: 0.5em;
	box-shadow: 0 0.25em 1em rgba(0, 0, 0, 0.12);
	z-index: 2;
}
```

---

### Issue 7: Repeated Information Between Panels and Highlight Cards

**Problem:**  
The side panels and highlight cards repeated similar information.

**Cause:**  
Both areas originally described the same skill categories.

**Fix:**  
The side panels were adjusted to show quick-scan categories such as tools, technologies, or career direction, while the main highlight cards explain strengths and practical skills.

This made each section serve a different purpose:

- **Side panel:** quick visual scan
- **Paragraph:** professional explanation
- **Highlight cards:** proof points and strengths

---

## Git and GitHub Issues Resolved

This project also included Git troubleshooting.

### Issue: Not a Git Repository

**Error:**

```bash
fatal: not a git repository (or any of the parent directories): .git
```

**Fix:**  
Navigated to the correct project folder containing the `.git` directory before running Git commands.

---

### Issue: Commit Attempt Before Staging Files

**Error:**

```bash
no changes added to commit
```

**Fix:**  
Staged files before committing:

```bash
git add .
git commit -m "Update portfolio website with project cards and resume"
```

---

### Issue: No Upstream Branch

**Error:**

```bash
fatal: The current branch main has no upstream branch
```

**Fix:**  
Connected the local branch to the remote GitHub branch:

```bash
git push --set-upstream origin main
```

---

### Issue: Non-Fast-Forward Push Rejection

**Error:**

```bash
! [rejected] main -> main (non-fast-forward)
```

**Fix:**  
Pulled remote changes using rebase before pushing:

```bash
git pull --rebase origin main
```

---

### Issue: Rebase Conflict with README.md

**Problem:**  
A conflict occurred because `README.md` was deleted remotely but modified locally.

**Fix:**  
Kept the updated README, staged the file, continued the rebase, and pushed again:

```bash
git add README.md
git rebase --continue
git push --set-upstream origin main
```

---

## Project Folder Structure

```text
azure-static-portfolio
│
├── README.md
├── html-web-portfolio
│   ├── index.html
│   ├── resume.pdf
│   ├── assets
│   │   ├── css
│   │   │   └── main.css
│   │   └── js
│   │       └── main.js
│   └── images
│       ├── thumbs
│       └── fulls
```

---

## Deployment Workflow

This project is designed to deploy through Azure Static Web Apps and GitHub Actions.

Typical workflow:

1. Update website files locally.
2. Test the website in the browser.
3. Stage changes with Git.
4. Commit changes.
5. Push changes to GitHub.
6. GitHub Actions triggers the Azure Static Web Apps deployment.
7. Azure hosts the updated website with managed HTTPS.

Example commands:

```bash
git status
git add .
git commit -m "Update portfolio website"
git push
```

---

## Skills Demonstrated

This project demonstrates:

- Static website customization
- HTML and CSS editing
- Responsive design troubleshooting
- Git and GitHub version control
- GitHub Actions deployment workflow
- Azure Static Web Apps hosting
- Resume portfolio development
- Documentation writing
- Troubleshooting and problem solving
- Recruiter-focused project presentation
- Cloud portfolio branding

---

## Lessons Learned

Through this project, I practiced more than just building a static website. I learned how to troubleshoot layout issues, fix Git workflow errors, improve recruiter-facing content, organize project documentation, and connect a local website project to a cloud deployment workflow.

This project helped strengthen my understanding of:

- How static websites are structured
- How portfolio content should be organized for employers
- How GitHub repositories should be documented
- How to resolve common Git errors
- How to customize a template without misrepresenting the original design
- How to use Azure Static Web Apps for simple cloud hosting

---

## Template Credit

This project uses the **Big Picture** template from [HTML5 UP](https://html5up.net).  
The template was customized for my personal resume portfolio and is used under the Creative Commons Attribution license.

---

## Author

**Evelio Morales Jr.**  
IT Support | Cloud Engineering | Cybersecurity  
GitHub: [EvelioMorales](https://github.com/EvelioMorales)  
LinkedIn: [Evelio Morales Jr.](https://www.linkedin.com/in/evelio-morales-jr101/)
