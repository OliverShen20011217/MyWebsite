# Oliver Shen — Personal Website  
# Description
A fast, data-driven personal site built with Middleman + ERB + vanilla CSS. Content lives in YAML for one-line updates; pages share a unified card UI (Education / Work Experience / Projects / Honors & Skills). Left profile panel collapses with pure CSS; top/left bars are sticky.  

Live: https://OliverShen20011217.github.io/  
 
Upload dates: Aug/12/2025

# Highlights
- Data-driven: All content sourced from data/*.yml; edit once, reflected site-wide.

- No-JS toggle: Left sidebar collapse via label + checkbox + CSS; no runtime JS.

- Consistent UI: Education/Work/Projects reuse one .we-* card stylesheet.

- Resume & downloads: Direct PDF download, JPG preview; per-project GitHub/ZIP links.

# Edit Content (YAML only)
- Top navigation: data/top_banner.yml

- Left profile: data/left_banner.yml (photo, contact, links)

- Education: data/education.yml (grouped by Title)

- Work experience: data/work_experience.yml (condition: still_working/passed, optional link: for company URL, descriptions: list)

- Projects: data/projects.yml (grouped by category; put About This Website first; supports Github_URL, download_URL)

- Honors & skills: data/honors_skills.yml (sections[].items[])

- **Assets**

	- Images → source/images/ (e.g., avatar, resume JPG)

	- Downloads → source/files/ (e.g., MyWebsite.zip, resume PDF) then reference as /files/…

# Deploy (GitHub Pages, automated)
Workflow: .github/workflows/deploy.yml

- Branch: push to main → auto build & publish

- Repo name: OliverShen20011217.github.io (user site root)

- Pages setting: Settings → Pages → Build and deployment: GitHub Actions  
 
  
# Notes
- Home highlight: only when URL is /index.html (intentional).

- Grid stability: grid-template-columns: minmax(0,1fr) minmax(0,3fr) + .maingrid > * { min-width: 0; }.

- Sticky left card: .leftBar { position: sticky; top: 60px; } (avoid overflow on ancestors).

- Download links: place ZIPs in source/files/, then set download_URL: /files/YourFile.zip.

- Company links: add link: in work_experience.yml to wrap the company name with <a>.


# Statement & Disclaimer
All content, text, images, and personal data in this repository are the intellectual property of **Oliver Shen** and are provided for portfolio purposes only. You’re welcome to reference the **layout/structure** (ERB/CSS/YAML patterns), but **do not copy** personal information, images, or unique wording without permission. If you adapt the templates, please give appropriate credit.