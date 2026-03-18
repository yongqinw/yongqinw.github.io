# Website Update Skill

You are helping Yongqin Wang update his personal academic research website at https://yongqinw.github.io/.
This is a Jekyll-based site (Minimal Mistakes theme) hosted on GitHub Pages.

## Site Architecture

| Section | Content Location | Archive Page |
|---------|-----------------|--------------|
| Home/Bio | `_pages/about.md` | `/` |
| Publications | `_publications/*.md` | `_pages/publications.md` |
| Talks | `_talks/*.md` | `_pages/talks.html` |
| Teaching | `_teaching/*.md` | `_pages/teaching.html` |
| CV (online) | `_pages/cv.md` | `/cv/` |
| CV (PDF) | `files/yongqin_wang_cv.pdf` | — |
| Author sidebar | `_config.yml` (author section) | — |
| Navigation menu | `_data/navigation.yml` | — |

---

## How to Update Each Section

### Adding a Publication

Create `_publications/YYYY-MM-DD-<slug>.md`:

```yaml
---
title: "Full Publication Title"
collection: publications
permalink: /publications/YYYY-MM-DD-<slug>
date: YYYY-MM-DD
venue: 'Conference or Journal Name (e.g., ASPLOS, MICRO, PETS)'
paperurl: 'https://link-to-paper-or-preprint'
citation: 'Yongqin Wang, Coauthor Name, ... "Title." <i>Venue</i>. Year.'
excerpt: 'Optional one-sentence summary shown in the list view.'
---

Optional longer abstract or description in markdown.
```

**Key rules:**
- Use `date:` in `YYYY-MM-DD` format (used for sort order)
- `citation:` supports HTML like `<i>italic</i>` for venue name
- `paperurl:` should link to arXiv, ACM DL, or author's copy
- Slug should be short and descriptive, e.g., `2025-01-15-mypaper`

---

### Adding a Talk

Create `_talks/YYYY-MM-DD-<slug>.md`:

```yaml
---
title: "Talk Title"
collection: talks
type: "Talk"
permalink: /talks/YYYY-MM-DD-<slug>
venue: "Conference or Institution Name"
date: YYYY-MM-DD
location: "City, State/Country"
---

Optional description, slides link, or recording link.
```

---

### Adding a Teaching Entry

Create `_teaching/YYYY-MM-DD-<slug>.md`:

```yaml
---
title: "Role - Course Name"
collection: teaching
type: "Course code or type (e.g., CSCI 567, Graduate Course)"
permalink: /teaching/YYYY-MM-DD-<slug>
venue: "University of Southern California"
date: YYYY-MM-DD
location: "Los Angeles, California"
---

Brief description of the role (TA, co-instructor, guest lecturer, etc.)
```

---

### Updating the Home/Bio Page

Edit `_pages/about.md`. This is the homepage (`permalink: /`).

- The author sidebar (photo, bio, links) is controlled by `_config.yml` under the `author:` key
- The main content area is free Markdown — write bio, research summary, news, etc.
- Keep an updated list of selected publications or research highlights here

---

### Updating the CV

Two components:
1. **Online CV page** — edit `_pages/cv.md` (use Markdown or HTML tables/lists)
2. **Downloadable PDF** — replace `files/yongqin_wang_cv.pdf` with the updated file

---

### Updating Author Profile (Sidebar)

Edit `_config.yml`, find the `author:` section:

```yaml
author:
  name: "Yongqin Wang"
  avatar: "images/selfie.jpeg"
  bio: "PhD candidate @ University of Southern California"
  location: "Los Angeles, CA"
  email: your@email.com
  links:
    - label: "Google Scholar"
      icon: "fas fa-fw fa-graduation-cap"
      url: "https://scholar.google.com/..."
    - label: "LinkedIn"
      icon: "fab fa-fw fa-linkedin"
      url: "https://linkedin.com/in/..."
```

To change the profile photo, put the new image in `images/` and update `avatar:`.

---

### Updating Navigation Menu

Edit `_data/navigation.yml`:

```yaml
main:
  - title: "Publications"
    url: /publications/
  - title: "Teaching"
    url: /teaching/
  - title: "Talks"
    url: /talks/
  - title: "CV"
    url: /cv/
```

---

## Deployment

Changes go live automatically when pushed to GitHub:

```bash
git add <changed files>
git commit -m "Add/Update <description>"
git push
```

GitHub Pages rebuilds the site within ~1-2 minutes.

---

## Local Preview (optional)

```bash
bundle exec jekyll serve
# Open http://localhost:4000
```

---

## Checklist for Common Updates

### New Publication
- [ ] Create `_publications/YYYY-MM-DD-slug.md` with all front matter fields
- [ ] Include `paperurl:` linking to the paper
- [ ] Update `files/yongqin_wang_cv.pdf` if needed
- [ ] Optionally update `_pages/about.md` if it's a notable paper

### New Talk
- [ ] Create `_talks/YYYY-MM-DD-slug.md`
- [ ] Include venue, location, date

### New Teaching
- [ ] Create `_teaching/YYYY-MM-DD-slug.md`
- [ ] Specify role (TA / Co-instructor / Guest Lecturer)

### General Profile Update
- [ ] Edit `_pages/about.md` for bio changes
- [ ] Edit `_config.yml` author section for sidebar changes
- [ ] Replace `files/yongqin_wang_cv.pdf` with new CV

---

## Current Site Content Summary

- **Publications**: 10 papers (2019–2025), venues include ASPLOS, MICRO, ISCA, PETS, CLOUD, ICLR
- **Talks**: 3 talks (2023–2024)
- **Teaching**: 5 entries (2021–2024), USC — TA and Co-instructor roles for Computer Architecture/Microarchitecture
- **Research focus**: Privacy-preserving computation (MPC, TEE, ORAM, PPML)
- **Current status**: PhD Candidate at USC

---

## File Naming Conventions

| Content Type | Pattern | Example |
|---|---|---|
| Publications | `YYYY-MM-DD-shortname.md` | `2025-03-15-newpaper.md` |
| Talks | `YYYY-MM-DD-talk.md` | `2025-02-10-talk.md` |
| Teaching | `YYYY-season-role.md` | `2025-spring-ta.md` |

Always use lowercase, hyphens (no spaces or underscores) in slugs.
