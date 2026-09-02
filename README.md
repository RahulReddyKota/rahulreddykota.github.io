# rahulreddykota.github.io

Personal portfolio site for **Rahul Reddy Kota** — MS Data Science @ UMBC, ML engineer, data analyst.

**Live:** https://rahulreddykota.github.io

---

## About

A single-page portfolio covering my background, work experience, projects, education, and contact details. Built as one self-contained HTML file with no framework, no build step, and no dependencies to install — the whole site is `index.html`, served directly by GitHub Pages.

## Stack

- HTML, CSS, and vanilla JavaScript, all inline in `index.html`
- [DM Sans](https://fonts.google.com/specimen/DM+Sans) and [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) via Google Fonts
- Images embedded as base64 data URIs (no external image requests)
- Hosted on GitHub Pages

## Features

- Dark/light theme toggle
- Responsive layout with a mobile nav drawer
- Scroll-triggered reveal animations via `IntersectionObserver`
- Tabbed project sections
- 3D-tilt hero photo with a click-to-upload fallback
- Contact form and quick links (email, LinkedIn, GitHub, phone)

## Sections

| Anchor | Contents |
| --- | --- |
| `#about` | Bio, education summary, current roles |
| `#experience` | UMBC Data Analytics Lab, Accenture |
| `#projects` | ARC AI (RAG), Big Data job market analysis, stock sentiment, skin cancer detection, cyberbullying detection |
| `#skills` | Languages, big data and cloud, databases, ETL/DevOps, ML/AI, BI tools |
| `#education` | UMBC MS, Sreenidhi B.Tech, certifications, awards |
| `#contact` | Contact form, direct links, resume download |

## Repository structure

```
.
├── index.html                      # the entire site
├── Rahul_Reddy_Kota_Resume.pdf     # linked from the hero and footer
└── README.md
```

## Running locally

Clone the repo and open the file — that's it:

```bash
git clone https://github.com/RahulReddyKota/rahulreddykota.github.io.git
cd rahulreddykota.github.io
open index.html          # macOS; use `start` on Windows or `xdg-open` on Linux
```

To serve it over HTTP instead (closer to how Pages serves it):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying

Any commit to `main` redeploys automatically through GitHub Pages, usually within a minute or two.

```bash
git add .
git commit -m "Update content"
git push
```

Hard-refresh (`Ctrl/Cmd + Shift + R`) after deploying — browsers cache the HTML.

## Editing notes

- **Replacing the headshot:** the hero image is a base64 data URI on the `#heroPhoto` `<img>` tag. Encode a new JPEG with `base64 -w0 photo.jpg` and swap the string. A 3:4 crop around 693×924 keeps the file near 55 KB.
- **Updating the resume:** replace `Rahul_Reddy_Kota_Resume.pdf` at the repo root, keeping the filename so the hero and footer links keep working.
- **Availability:** the "Open to Work" badge text lives in the `.hero-badge` div near the top of the hero section, and is echoed in the contact section blurb.

## Known limitations

- **The contact form does not send anything.** `handleContactSubmit()` only shows a "Message Sent ✓" confirmation and resets the fields — there is no backend. Anyone who uses it will believe they've reached me when they haven't. Wire it to [Formspree](https://formspree.io), [Getform](https://getform.io), or a similar service, or replace it with a plain `mailto:` link.
- Embedding images as base64 keeps the site dependency-free but inflates `index.html` to roughly 330 KB.

## Contact

- Email: kotarahulreddy@gmail.com
- LinkedIn: https://www.linkedin.com/in/rahul-reddy-kota-b55a3a251/
- GitHub: https://github.com/RahulReddyKota
