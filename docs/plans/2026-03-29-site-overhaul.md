# Site Overhaul Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Replace all placeholder/template content with real, professional content for Fraser Burns — Quality Team Leader, QC professional, engineering enthusiast.

**Architecture:** Static Jekyll site using al-folio theme. Content lives in `_pages/about.md`, `assets/json/resume.json`, `_data/cv.yml`, `_projects/*.md`, `_posts/*.md`, `_news/*.md`, and `_config.yml`. No code changes — content edits only.

**Tech Stack:** Jekyll, al-folio theme, JSON (resume), YAML (cv/config), Markdown (pages/posts/projects)

---

### Task 1: Update About Page

**Files:**
- Modify: `_pages/about.md`

**Step 1: Replace the about page content**

Replace the entire file with:

```markdown
---
layout: about
title: about
permalink: /
subtitle: Quality Team Leader | Quality Management Professional | Engineering Enthusiast

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false
  more_info: >
    <p>Arbroath, United Kingdom</p>

news: true
selected_papers: false
social: true
---

I'm Fraser Burns, a Quality Team Leader with over 13 years of experience in quality control and inspection across Oil & Gas, aerospace, and technical textiles manufacturing. My career has taken me from hands-on inspection roles to leading quality teams, and I'm driven by a passion for continuous improvement and getting things right first time.

Most recently, I joined Scott & Fyfe as a Quality Team Leader, where I oversee the Quality Management System, ensure compliance with customer and regulatory requirements, and lead the team in maintaining and improving quality standards across technical textiles production.

Before that, I spent several years at Baker Hughes — first as a Goods In QC Inspector on subsea trees and assemblies, then as a Lab Engineer in their Additive Manufacturing division, where I helped increase productivity to 90% through process improvement and R&D. I'm also an active HSE advocate, having served on a safety committee and mentored colleagues on safe working practices.

Outside of work, I'm currently studying for an HNC in Mechanical Engineering and spend my time on 3D printing, engineering projects, and reading around quality management, lean thinking, and leadership.
```

**Step 2: Verify**

Open `_pages/about.md` and confirm no placeholder text remains.

**Step 3: Commit**

```bash
git add _pages/about.md
git commit -m "content: rewrite about page with real bio and correct subtitle"
```

---

### Task 2: Update resume.json — Basics & Location

**Files:**
- Modify: `assets/json/resume.json`

**Step 1: Update the basics section**

Replace the `"basics"` object (lines 2–24):

```json
"basics": {
  "name": "Fraser Burns",
  "label": "Quality Team Leader",
  "image": "",
  "email": "fraser.burns@hotmail.co.uk",
  "phone": "+44 7449829405",
  "url": "https://undamagedvirus.github.io",
  "summary": "Quality Team Leader with over 13 years of experience in quality control and inspection across Oil & Gas, aerospace, and technical textiles manufacturing. Skilled in QMS management, continuous improvement, dimensional inspection, and non-destructive testing. Currently leading the quality function at Scott & Fyfe while completing an HNC in Mechanical Engineering.",
  "location": {
    "address": "",
    "postalCode": "",
    "city": "Arbroath",
    "countryCode": "GB",
    "region": "Scotland"
  },
  "profiles": [
    {
      "network": "LinkedIn",
      "username": "fraser-burns-66a1857b",
      "url": "https://www.linkedin.com/in/fraser-burns-66a1857b"
    },
    {
      "network": "GitHub",
      "username": "UndamagedVirus",
      "url": "https://github.com/UndamagedVirus"
    }
  ]
},
```

**Step 2: Verify**

Confirm San Francisco and AlbertEinstein are gone.

**Step 3: Commit**

```bash
git add assets/json/resume.json
git commit -m "content: fix resume basics — correct label, location, and profiles"
```

---

### Task 3: Update resume.json — Work Experience

**Files:**
- Modify: `assets/json/resume.json`

**Step 1: Replace the entire `"work"` array**

```json
"work": [
  {
    "name": "Scott & Fyfe",
    "position": "Quality Team Leader",
    "url": "https://www.scottandfyfe.com/",
    "startDate": "2025-01-01",
    "endDate": "",
    "summary": "Leading the quality function at a technical textiles manufacturer. Responsible for maintaining and updating the Quality Management System, ensuring products meet customer and regulatory requirements, driving continuous improvement initiatives, and leading the quality team in day-to-day operations.",
    "highlights": ["QMS Management", "Quality Assurance", "Technical Textiles", "Team Leadership", "Continuous Improvement"]
  },
  {
    "name": "Sulzer GT Aero Services Ltd",
    "position": "Goods In Inspector",
    "url": "https://www.sulzer.com/",
    "startDate": "2024-01-01",
    "endDate": "2025-01-01",
    "summary": "Performed incoming inspection of gas turbine components and assemblies to ensure conformance with engineering drawings and quality standards. Supported the quality team in maintaining inspection records and non-conformance reporting.",
    "highlights": ["Gas Turbines", "Dimensional Inspection", "Non-Conformance Reporting"]
  },
  {
    "name": "Baker Hughes",
    "position": "Lab Engineer",
    "url": "https://www.bakerhughes.com/",
    "startDate": "2022-06-01",
    "endDate": "2023-10-01",
    "summary": "Worked within the Additive Manufacturing division supporting R&D, process improvement, and machine maintenance. Contributed to increasing lab productivity to 90% through workflow optimisation, CAD design support, and building strong customer and internal relationships.",
    "highlights": ["Additive Manufacturing", "Continuous Improvement", "CAD Design", "Research & Development", "Customer Relations"]
  },
  {
    "name": "Baker Hughes",
    "position": "Goods In Quality Control Inspector",
    "url": "https://www.bakerhughes.com/",
    "startDate": "2018-06-01",
    "endDate": "2022-06-01",
    "summary": "Carried out dimensional and visual inspection of subsea trees, sub-assemblies, and precision components to ensure conformance with drawings and specifications. Operated and programmed CMM, Laser Tracker, and Romer Arm equipment. Conducted MRB reviews, raised non-conformance reports, and supported investigations into quality escapes.",
    "highlights": ["Subsea Trees & Sub-Assemblies", "Dimensional Inspection", "MRB Review", "Non-Conformance Reporting & Investigations", "CMM / Laser Tracker / Romer Arm Operation & Programming"]
  },
  {
    "name": "Pacson Valves",
    "position": "NDE Quality Control Inspector",
    "url": "https://example.com",
    "startDate": "2016-06-01",
    "endDate": "2018-06-01",
    "summary": "Performed non-destructive testing and quality inspection on subsea valves and associated components. Ensured products met applicable codes, standards, and customer specifications throughout the manufacturing process.",
    "highlights": ["Subsea Valves", "Non-Destructive Testing", "Quality Inspection"]
  },
  {
    "name": "Bonar Yarns",
    "position": "Quality Tester",
    "url": "https://example.com",
    "startDate": "2016-01-01",
    "endDate": "2016-06-01",
    "summary": "Conducted quality testing on yarn and textile products to verify compliance with product specifications and customer requirements.",
    "highlights": ["Textile Quality Testing", "Product Compliance"]
  },
  {
    "name": "GA Engineering (Scotland)",
    "position": "Quality Control Inspector",
    "url": "https://example.com",
    "startDate": "2011-06-01",
    "endDate": "2015-10-01",
    "summary": "Inspected machined components produced under sub-contract to ensure dimensional accuracy and surface finish compliance with engineering drawings and customer requirements. Built a strong foundation in precision measurement and quality documentation over four years in the role.",
    "highlights": ["Sub-Contract Machining", "Dimensional Inspection", "Engineering Drawings", "Quality Documentation"]
  }
],
```

**Step 2: Verify**

Confirm all "Teaching at Palmer Physical Laboratory" placeholders are gone and Scott & Fyfe is the first entry.

**Step 3: Commit**

```bash
git add assets/json/resume.json
git commit -m "content: rewrite all work experience summaries, add Scott & Fyfe role"
```

---

### Task 4: Update resume.json — Skills & Interests

**Files:**
- Modify: `assets/json/resume.json`

**Step 1: Replace the `"skills"` array**

```json
"skills": [
  {
    "name": "Quality Management",
    "level": "Expert",
    "icon": "fa-solid fa-magnifying-glass",
    "keywords": [
      "Quality Management Systems (QMS)",
      "ISO 9001",
      "Non-Conformance Reporting",
      "MRB Review",
      "Continuous Improvement",
      "Root Cause Analysis"
    ]
  },
  {
    "name": "Inspection & Metrology",
    "level": "Expert",
    "icon": "fa-solid fa-ruler-combined",
    "keywords": [
      "Dimensional Inspection",
      "CMM Operation & Programming",
      "Laser Tracker",
      "Romer Arm",
      "GD&T",
      "Non-Destructive Testing"
    ]
  },
  {
    "name": "Engineering & Making",
    "level": "Intermediate",
    "icon": "fa-solid fa-gears",
    "keywords": [
      "3D Printing",
      "CAD Design",
      "Additive Manufacturing",
      "Mechanical Engineering"
    ]
  }
],
```

**Step 2: Replace the `"interests"` array**

```json
"interests": [
  {
    "name": "3D Printing",
    "icon": "fa-solid fa-print",
    "keywords": [
      "Functional Parts",
      "Hobby Models",
      "FDM Printing",
      "Design for Manufacture"
    ]
  },
  {
    "name": "Quality & Management",
    "icon": "fa-solid fa-book",
    "keywords": [
      "Quality Management",
      "Lean Thinking",
      "Continuous Improvement",
      "Leadership Development"
    ]
  },
  {
    "name": "Engineering",
    "icon": "fa-solid fa-wrench",
    "keywords": [
      "Mechanical Projects",
      "Problem Solving",
      "Making & Repair"
    ]
  }
],
```

**Step 3: Verify**

Confirm no "Quantum Mechanics" or "Physics" placeholder content remains in skills/interests.

**Step 4: Commit**

```bash
git add assets/json/resume.json
git commit -m "content: replace placeholder skills and interests with real content"
```

---

### Task 5: Update resume.json — Projects & Fix Certificates

**Files:**
- Modify: `assets/json/resume.json`

**Step 1: Replace the `"projects"` array**

```json
"projects": [
  {
    "name": "Additive Manufacturing Productivity Improvement",
    "summary": "Led process improvement initiatives within Baker Hughes' Additive Manufacturing lab, optimising workflows, machine utilisation, and material handling to increase overall lab productivity to 90%.",
    "highlights": ["Continuous Improvement", "Process Optimisation", "Additive Manufacturing"],
    "startDate": "2022-06-01",
    "endDate": "2023-10-01",
    "url": ""
  },
  {
    "name": "3D Printing Projects",
    "summary": "Ongoing personal 3D printing projects including functional replacement parts, tools, and hobby models. Focused on practical applications and learning design for manufacture principles.",
    "highlights": ["FDM Printing", "CAD Design", "Functional Parts"],
    "startDate": "2020-01-01",
    "endDate": "",
    "url": "https://undamagedvirus.github.io/projects"
  }
],
```

**Step 2: Fix the IOSH certificate issuer**

In the certificates array, find the IOSH Managing Safely entry and update the `"issuer"` field from `"Hexagon Metrology"` to `"IOSH"`. Also fix the XRF Safety Training issuer from `"Stanford University"` to `"Baker Hughes"` (or remove the issuer if unknown — set to `""`).

**Step 3: Verify**

Confirm no "Quantum Teleportation" or "Quantum Cryptography" remains in projects. Confirm IOSH issuer is correct.

**Step 4: Commit**

```bash
git add assets/json/resume.json
git commit -m "content: replace placeholder projects, fix certificate issuers"
```

---

### Task 6: Update cv.yml

**Files:**
- Modify: `_data/cv.yml`

**Step 1: Replace the entire file**

```yaml
- title: General Information
  type: map
  contents:
    - name: Full Name
      value: Fraser Burns
    - name: Location
      value: Arbroath, Scotland, UK
    - name: Languages
      value: English

- title: Education
  type: time_table
  contents:
    - title: HNC Mechanical Engineering
      institution: Edinburgh College
      year: In Progress
      description:
        - Part-time study alongside full-time employment.
        - Covering engineering principles, materials, and manufacturing processes.
    - title: NC Practical Engineering
      institution: Perth College UHI
      year: 2010
      description:
        - Foundation qualification in practical engineering skills.

- title: Experience
  type: time_table
  contents:
    - title: Quality Team Leader
      institution: Scott & Fyfe
      year: 2025 - Present
      description:
        - Maintaining and updating the Quality Management System.
        - Ensuring products meet customer and regulatory quality requirements.
        - Leading the quality team and driving continuous improvement.
        - title: Key Areas
          contents:
            - QMS Management
            - Quality Assurance
            - Team Leadership
    - title: Goods In Inspector
      institution: Sulzer GT Aero Services Ltd
      year: 2024 - 2025
      description:
        - Incoming inspection of gas turbine components.
        - Non-conformance reporting and quality documentation.
    - title: Lab Engineer
      institution: Baker Hughes
      year: 2022 - 2023
      description:
        - Additive Manufacturing lab support and process improvement.
        - Helped increase lab productivity to 90%.
        - title: Key Areas
          contents:
            - Additive Manufacturing
            - Continuous Improvement
            - CAD Design
    - title: Goods In Quality Control Inspector
      institution: Baker Hughes
      year: 2018 - 2022
      description:
        - Dimensional inspection of subsea trees and precision assemblies.
        - CMM, Laser Tracker, and Romer Arm operation and programming.
        - MRB review and non-conformance investigation.
    - title: NDE Quality Control Inspector
      institution: Pacson Valves
      year: 2016 - 2018
      description:
        - Non-destructive testing and inspection of subsea valves.
    - title: Quality Tester
      institution: Bonar Yarns
      year: 2016
    - title: Quality Control Inspector
      institution: GA Engineering (Scotland)
      year: 2011 - 2015
      description:
        - Inspection of sub-contract machined components.
        - Built foundation in dimensional measurement and quality documentation.

- title: Skills
  type: nested_list
  contents:
    - title: Quality Management
      items:
        - QMS (ISO 9001)
        - Non-Conformance Reporting
        - Root Cause Analysis
        - Continuous Improvement
    - title: Inspection & Metrology
      items:
        - Dimensional Inspection
        - CMM / Laser Tracker / Romer Arm
        - GD&T
        - Non-Destructive Testing
    - title: Engineering & Making
      items:
        - 3D Printing & Additive Manufacturing
        - CAD Design
        - Mechanical Engineering

- title: Interests
  type: list
  contents:
    - "<u>Making:</u> 3D Printing (functional parts & hobby models), mechanical engineering projects"
    - "<u>Learning:</u> Quality management, lean thinking, leadership & management development"
    - "<u>Reading:</u> Quality systems, continuous improvement, engineering"
```

**Step 2: Verify**

Confirm no "Nobel Prize", "Topic 1", "Description 1", or al-folio template links remain.

**Step 3: Commit**

```bash
git add _data/cv.yml
git commit -m "content: rewrite cv.yml with real experience, skills, and interests"
```

---

### Task 7: Replace Placeholder Projects

**Files:**
- Delete: `_projects/1_project.md` through `_projects/9_project.md`
- Create: `_projects/3d-printing.md`
- Create: `_projects/productivity-improvement.md`

**Step 1: Delete all placeholder project files**

```bash
rm _projects/1_project.md _projects/2_project.md _projects/3_project.md _projects/4_project.md _projects/5_project.md _projects/6_project.md _projects/7_project.md _projects/8_project.md _projects/9_project.md
```

**Step 2: Create `_projects/productivity-improvement.md`**

```markdown
---
layout: page
title: Additive Manufacturing Productivity Improvement
description: Process improvement initiative at Baker Hughes AM lab, achieving 90% productivity.
img: assets/img/1.jpg
importance: 1
category: work
---

During my time as a Lab Engineer in Baker Hughes' Additive Manufacturing division, I worked on a series of continuous improvement initiatives aimed at increasing the throughput and efficiency of the lab.

Through workflow analysis, machine utilisation improvements, material handling optimisation, and closer collaboration between the lab team and customers, we were able to increase overall lab productivity to **90%**.

**Key activities:**
- Mapping existing workflows and identifying bottlenecks
- Optimising build scheduling and machine downtime
- Supporting R&D projects and customer requirement management
- CAD design support for print preparation

This project reinforced my belief that sustainable improvement comes from understanding the process end-to-end and involving the people who do the work every day.
```

**Step 3: Create `_projects/3d-printing.md`**

```markdown
---
layout: page
title: 3D Printing Projects
description: Functional parts, tools, and hobby models printed on FDM printers.
img: assets/img/2.jpg
importance: 2
category: fun
---

3D printing is one of my main hobbies outside of work. I focus primarily on practical, functional prints — replacement parts, custom tools, and things that solve real problems — alongside hobby models for various projects.

**Areas of focus:**

- **Functional parts** — designing and printing replacement or custom components
- **Hobby models** — models related to other interests and projects
- **Learning design** — improving my CAD and design-for-manufacture skills through hands-on printing

I'll be adding specific project writeups here as I document them. Check the [blog](/blog) for related posts.
```

**Step 4: Verify**

Run `ls _projects/` and confirm only the two new files exist.

**Step 5: Commit**

```bash
git add _projects/
git commit -m "content: replace placeholder projects with real project pages"
```

---

### Task 8: Clean Up Blog Posts and Config

**Files:**
- Modify: `_config.yml`
- Delete all files in `_posts/`
- Delete placeholder news/announcements in `_news/`

**Step 1: Remove placeholder external blog sources from `_config.yml`**

Find the `external_sources` section and replace it:

```yaml
external_sources:
```

(Empty — remove the Medium and Google Blog entries.)

**Step 2: Update blog display categories in `_config.yml`**

Find:
```yaml
display_tags: ["formatting", "images", "links", "math", "code", "blockquotes"]
display_categories: ["external-services"]
```

Replace with:
```yaml
display_tags: ["quality", "3d-printing", "engineering", "lean", "management"]
display_categories: ["quality-management", "3d-printing", "engineering"]
```

**Step 3: Delete all placeholder posts**

```bash
rm _posts/*.md
```

**Step 4: Delete placeholder news items**

```bash
rm _news/announcement_1.md _news/announcement_2.md _news/announcement_3.md
```

**Step 5: Create a welcome news announcement**

Create `_news/2026-03-29-welcome.md`:

```markdown
---
layout: post
date: 2026-03-29 12:00:00
inline: true
related_posts: false
---

Welcome to my site — a space to share my work, projects, and learning in quality management and engineering.
```

**Step 6: Verify**

Confirm `_posts/` is empty, `_news/` has only the welcome announcement, and `_config.yml` has no Medium/Google external sources.

**Step 7: Commit**

```bash
git add _config.yml _posts/ _news/
git commit -m "content: remove placeholder blog posts, announcements, and external sources"
```

---

### Task 9: Final Config Cleanup

**Files:**
- Modify: `_config.yml`

**Step 1: Update site description and blog description**

Find:
```yaml
description: >
  A simple, whitespace theme for academics. Based on [*folio](https://github.com/bogoli/-folio) design.
```

Replace with:
```yaml
description: >
  Fraser Burns — Quality Team Leader, engineering enthusiast, and lifelong learner. This site showcases my professional experience, projects, and writing on quality management and making.
```

Find:
```yaml
blog_description: a simple whitespace theme for academics
```

Replace with:
```yaml
blog_description: Quality management, 3D printing, and engineering — one hobby at a time.
```

**Step 2: Fix the scholar section** (still references Einstein)

Find:
```yaml
scholar:
  last_name: [Einstein]
  first_name: [Albert, A.]
```

Replace with:
```yaml
scholar:
  last_name: [Burns]
  first_name: [Fraser, F.]
```

**Step 3: Verify**

Confirm no "academics" or "Einstein" references remain in config.

**Step 4: Commit**

```bash
git add _config.yml
git commit -m "content: update site and blog descriptions, fix scholar name config"
```

---

## Verification Checklist

After all tasks are complete, do a final sweep:

```bash
grep -r "Einstein\|Palmer Physical\|AlbertEinstein\|San Francisco\|CA 94115\|Quantum Mechanics\|Topic 1\|Description 1\|Nobel Prize\|al-folio\|example.com" --include="*.md" --include="*.yml" --include="*.json" _pages/ _data/ _projects/ _posts/ _news/ assets/json/
```

Any matches should be investigated and cleaned up before considering the overhaul complete.
