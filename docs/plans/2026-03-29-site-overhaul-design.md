# Site Overhaul Design — undamagedvirus.github.io

**Date:** 2026-03-29
**Approach:** Content-first (Option A) — fix all content systematically, leverage existing al-folio theme

---

## Goal

A complete personal showcase for Fraser Burns: professional CV for recruiters, hobby/project showcase, and blog for quality management learning and making interests.

---

## About Page (`_pages/about.md`)

- **Subtitle:** "Quality Team Leader | Quality Management Professional | Engineering Enthusiast"
- **Body:** Rewritten intro emphasising leadership trajectory — 13+ years QC background, Lab Engineer in Additive Manufacturing (90% productivity improvement), continuous improvement, HSE safety committee mentorship, current HNC upskilling
- **Profile photo:** `prof_pic.jpg` (already in place)
- **Location:** Arbroath, UK
- **Social links:** LinkedIn + GitHub only (remove dead/empty links)

---

## Resume (`assets/json/resume.json`)

### Work Experience — all summaries rewritten (remove Einstein placeholders)

| Role                      | Company                           | Dates        |
| ------------------------- | --------------------------------- | ------------ |
| Quality Team Leader       | Scott & Fyfe (Technical Textiles) | 2025–present |
| Goods In Inspector        | Sulzer GT Aero Services           | 2024–2025    |
| Lab Engineer              | Baker Hughes                      | 2022–2023    |
| Goods In QC Inspector     | Baker Hughes                      | 2018–2022    |
| NDE QC Inspector          | Pacson Valves                     | 2016–2018    |
| Quality Tester            | Bonar Yarns                       | 2016         |
| Quality Control Inspector | GA Engineering (Scotland)         | 2011–2015    |

- Scott & Fyfe summary: QMS maintenance/updates, quality assurance, team leadership in technical textiles manufacturing
- All summaries to emphasise upward progression toward quality management
- Fix location (remove San Francisco placeholder)

### Education

- HNC Mechanical Engineering, Edinburgh College — "In Progress" (not "Expected 2025")
- NC Practical Engineering, Perth College UHI — 2010

---

## CV Page (`_data/cv.yml`)

- Match updated work history from resume.json
- Remove placeholder "Nobel Prize" honors/awards section entirely
- Remove al-folio template Open Source Projects link
- **Interests:**
  - 3D Printing (functional parts, hobby models)
  - Mechanical Engineering projects
  - Quality Management, Lean, Continuous Improvement
  - Reading (quality/management/career development)

---

## Projects Page (`_pages/projects.md` + `_projects/`)

- **3D Printing** — functional parts and hobby model cards (placeholder cards ready to populate)
- **Baker Hughes Productivity Project** — additive manufacturing productivity improvement to 90%
- Structure set up to grow as new projects are added

---

## Blog (`_config.yml` + `_posts/`)

- Remove placeholder external sources (Medium/Google Blog feeds)
- Set up categories:
  - Quality & Management
  - 3D Printing
  - Engineering & Making
- Remove/replace placeholder posts

---

## Out of Scope (revisit later)

- Visual/design changes (custom colours, typography)
- New theme features or custom components
- Actual blog post content (structure only)
