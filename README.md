# Academic CV / Resume (LaTeX)

This folder is a modular LaTeX resume template you can upload to [Overleaf](https://www.overleaf.com/) or compile on your own machine.

---

## About LaTeX

[LaTeX](https://www.latex-project.org/) is a document preparation system. You write plain text with markup (commands like `\section{}`, `\textbf{}`), and a compiler produces a polished PDF with consistent typography, spacing, and structure. It is widely used for theses, papers, and CVs because layout stays stable when you edit content.

This project uses **XeLaTeX** (or LuaLaTeX) so we can load modern fonts with **fontspec** (e.g. Calibri on systems that have it, or TeX Gyre Heros as a fallback).

---

## About this resume

- **Purpose:** Academic-style CV suitable for university or job applications (education first, then research, projects, experience, etc.).
- **Content:** The sample uses **mock data** (placeholder name, employers, schools). Replace text in the `sections/` files with your real information.
- **Layout:** A4, 11pt, navy accent color, header with contact block and photo, timeline-style `\cvrow` entries, and section rules.
- **Structure:**

| File | Contents |
|------|----------|
| `main.tex` | Preamble, custom commands (`\cvsection`, `\cvrow`, `\cvlist`, `\stack`), document shell |
| `sections/header.tex` | Name, title, address, phone, email, GitHub, LinkedIn, photo, personal line |
| `sections/profile.tex` | Short profile paragraph |
| `sections/education.tex` | Degrees and schooling |
| `sections/research.tex` | Research and publications |
| `sections/projects.tex` | Academic / personal projects |
| `sections/experience.tex` | Professional experience |
| `sections/volunteering.tex` | Community and volunteering |
| `sections/languages.tex` | Languages |
| `sections/skills.tex` | Skills matrix |
| `sections/references.tex` | References |
| `images.jpg` | Header photo (replace with your own, same filename or update `header.tex`) |

**Signature:** At the bottom of `main.tex` you can uncomment the line that includes a scanned signature image and add your `signature.png` (or similar).

---

## Installation and compilation

### Option A — Overleaf (no local install)

1. Zip this entire folder (`main.tex`, `sections/`, `images.jpg`, etc.).
2. In Overleaf: **New Project → Upload Project** and select the zip.
3. Open **Menu** (top left) → **Compiler** → choose **XeLaTeX**.
4. Click **Recompile**. The PDF should build; if Calibri is missing on Overleaf, the template falls back to TeX Gyre Heros automatically.

Ensure `images.jpg` (or whatever filename you use in `header.tex`) is in the project root.

### Option B — Local TeX distribution

Install a full TeX system so `xelatex` and the required packages are available:

| OS | Common install |
|----|----------------|
| **Windows** | [MiKTeX](https://miktex.org/) or [TeX Live](https://tug.org/texlive/) |
| **macOS** | [MacTeX](https://tug.org/mactex/) (or TeX Live) |
| **Linux** | `sudo apt install texlive-full` (Debian/Ubuntu) or your distro’s TeX Live package |

Then from this directory:

```bash
cd "Sample Overleaf"
xelatex main.tex
```

Run **twice** if you change cross-references or the table of contents (not heavily used here, but harmless). For a clean build you can delete auxiliary files (`*.aux`, `*.log`, `*.out`) when sharing only sources.

### Optional: Calibri

If **Calibri** is installed (e.g. with Microsoft Office), XeLaTeX will use it. Otherwise the template uses **TeX Gyre Heros** from TeX Live—no extra step required.

---

## Quick customization checklist

- [ ] Replace mock data in each file under `sections/`.
- [ ] Update `pdfauthor` and `pdftitle` in `main.tex` (`\hypersetup{...}`).
- [ ] Swap `images.jpg` or change the path in `sections/header.tex`.
- [ ] Add a real signature image if needed (`main.tex`).

For questions about LaTeX syntax, see [Overleaf Learn](https://www.overleaf.com/learn) or [LaTeX Wikibook](https://en.wikibooks.org/wiki/LaTeX).
