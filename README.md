<!--
  Overleaf-style project README
-->

# Academic CV / Resume

Modular **XeLaTeX** CV template: header with photo, profile, education, research, projects, experience, volunteering, languages, skills, and references. This CV is specifically designed in the **tabular Lebenslauf format** to apply for MSc programs in Germany (gap-free, reverse-chronological, and fact-oriented).

Sample content is **placeholder (mock) data**—replace it in `sections/` before use.

**Compiler:** [XeLaTeX](https://www.overleaf.com/learn/how-to/Choosing_a_LaTeX_Compiler) (required for `fontspec`).

---

## Screenshots

| CV — page 1 | CV — page 2 |
|-------------|-------------|
| ![First page of the CV PDF](screenshots/cv-page-1.png) | ![Second page of the CV PDF](screenshots/cv-page-2.png) |

| Overleaf: project files | Overleaf: set compiler to XeLaTeX |
|-------------------------|-------------------------------------|
| ![Project layout with main.tex and sections folder](screenshots/overleaf-project-files.png) | ![Menu showing XeLaTeX compiler selected](screenshots/overleaf-compiler-xelatex.png) |

> **Screenshots folder:** Place your images in [`screenshots/`](screenshots/) using the names above, or edit this README to point to your filenames (e.g. `screenshots/my-preview.png`).

---

## About LaTeX

[LaTeX](https://www.latex-project.org/) is a markup-based typesetting system: you write source (`.tex`) and compile to PDF. It keeps typography and spacing consistent, which is why many people use it for CVs, theses, and journal articles.

This template loads **fontspec** with **Arial** as the main font when the system (or project) provides it; otherwise it falls back to **TeX Gyre Heros** (bundled with TeX Live / Overleaf). To use true Arial on Overleaf, add the Arial `.ttf` files to your project and point `fontspec` at them (see comments in `main.tex`).

---

## About this template

- **Paper:** A4, 11pt `article`, custom navy styling and section rules.
- **Macros:** `\cvsection`, `\cvrow` (date column + body), `\cvlist` (compact bullets), `\stack` (tech stack line).
- **Photo:** `images.jpg` in the project root, included from `sections/header.tex` (change path or filename as needed).

| Path | Role |
|------|------|
| `main.tex` | Preamble, macro definitions, `\input{sections/...}`, signature block |
| `sections/header.tex` | Name, role, contact, photo, personal line |
| `sections/profile.tex` | Profile paragraph |
| `sections/education.tex` | Education |
| `sections/research.tex` | Research & publications |
| `sections/projects.tex` | Projects |
| `sections/experience.tex` | Professional experience |
| `sections/volunteering.tex` | Community & volunteering |
| `sections/languages.tex` | Languages |
| `sections/skills.tex` | Skills & competencies |
| `sections/references.tex` | References |
| `images.jpg` | Header photo |

---

## Open in Overleaf

1. Zip this project (**include** `main.tex`, the whole `sections/` folder, `images.jpg`, and optionally `screenshots/`).
2. In Overleaf: **New Project** → **Upload project**.
3. Click **Menu** (top left) → **Compiler** → **XeLaTeX**.
4. **Recompile** to build `main.pdf`.

See also: [Uploading a project](https://www.overleaf.com/learn/how-to/Uploading_a_project) and [Choosing a LaTeX compiler](https://www.overleaf.com/learn/how-to/Choosing_a_LaTeX_Compiler).

---

## Compile locally

Install a TeX distribution ([TeX Live](https://tug.org/texlive/), [MacTeX](https://tug.org/mactex/), or [MiKTeX](https://miktex.org/)), then:

```bash
cd "Sample Overleaf"
xelatex main.tex
```

Run twice if you add cross-references that need a second pass.

---

## Customize

- [ ] Edit each file under `sections/` with your real details.
- [ ] Set `pdfauthor` and `pdftitle` in `main.tex` (`\hypersetup`).
- [ ] Replace `images.jpg` or update `\includegraphics{...}` in `sections/header.tex`.
- [ ] Optional: uncomment the signature `\includegraphics` in `main.tex` and add your scan.

**Learn LaTeX:** [Overleaf Learn](https://www.overleaf.com/learn) · [LaTeX Wikibook](https://en.wikibooks.org/wiki/LaTeX)

---

## License

Template structure and content placeholders are provided as-is for personal use and adaptation. Replace mock data before publishing or sharing your CV.
