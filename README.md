# Student Resume Templates

A one-page website where students build an ATS-friendly resume template, preview it live, and download it as a Google Docs-ready Word file or a PDF. Made for Career Services.

**🔗 Live site: [drakeev.github.io/Free-Resume-Templates-and-Builder](https://drakeev.github.io/Free-Resume-Templates-and-Builder/)**

> **AI disclosure:** This project was created with the help of AI. The website code, resume templates, and documentation were written by Claude, an AI model made by Anthropic, working from instructions given by a Career Services advisor. A person reviewed the output and made the decisions about content, wording, and design. See [AI disclosure](#ai-disclosure) below for details.

---

## What students can do

1. **Pick a template**
   | Template | Best for | Section order |
   |---|---|---|
   | First Job | No work experience yet (including early college students) | Objective, Education, Skills, Activities & Leadership, Volunteer & Informal Work, Awards |
   | Classic | Most job applications | Summary, Experience, Education, Skills |
   | Internship | College students applying for internships | Education, Projects, Experience, Leadership & Involvement, Skills |
   | Graduating Student | Students about to graduate | Summary, Skills, Certifications & Certificates, Education, Work Experience |
   | Skills-Based | Career changers | Profile, Key Skills, Work History, Education & Training, Technical Skills |

2. **Pick a look:** Traditional (serif, centered), Modern (sans-serif, left-aligned, color band) or Compact (tight, minimal).
3. **Pick a color:** Navy, Crimson, Forest, Teal, Plum, Charcoal, or any custom color. The page warns students if a color is too light to read.
4. **Download** the template two ways:
   - **For Google Docs (.docx):** the version students edit. Google Docs opens it with its lines, bullets, and right-aligned dates intact.
   - **PDF:** a print-ready copy that matches the live preview.
5. **Edit it in Google Drive.** The page walks students through uploading the .docx file to Drive (school account or personal Gmail), opening it with Google Docs, filling it in, and downloading a PDF to apply with. Saving in Drive is required.

> **Why a .docx for editing?** Google Docs doesn't truly convert PDFs. It pulls out the text and drops anything drawn on the page, so a PDF opened in Docs loses its horizontal lines, bullets, and date alignment. A Word file opens in Docs as a real document, with its formatting kept.

The page also has a QR code so students can open it on their phones, and a short "Before you send your resume" checklist.

## Why the templates are ATS-friendly

Applicant tracking systems (ATS) read resumes as plain text. Every template and look is built to survive that:

- One column, with no tables, text boxes, icons, or photos
- Standard section names (Experience, Education, Skills)
- Standard fonts (Helvetica/Arial or Times) as real, selectable text
- Color only on the name, headings, and lines, so the resume also prints well in black and white
- Plain characters only (hyphens and vertical bars) so nothing turns into garbled symbols

Every template and look combination was generated and checked to make sure the text comes out cleanly in reading order and fits on one page.

## Privacy

- Nothing a student does on the page is uploaded anywhere. The PDF and .docx files are made inside the student's own browser.
- The page remembers each student's last template, look, and color on that device only (browser storage). No names, contact details, or resume content are stored.
- There is no sign-in, no tracking, and no analytics.

## Project files

| File | What it is |
|---|---|
| `index.html` | The whole website in one file: page layout, styles, template content, and the PDF and Word builders |
| `docs/HOSTING.md` | How to put the site online (GitHub Pages or a school website) and update the QR code |
| `docs/CUSTOMIZING.md` | How to change the school name, wording, colors, templates, and looks |
| `docs/STUDENT-GUIDE.md` | A plain-language guide you can share with students |
| `docs/HOW-IT-WORKS.md` | Technical notes for whoever maintains the site |

## Quick start

- **Try it on your computer:** download `index.html` and double-click it. It opens in your web browser. An internet connection is needed for the fonts and the PDF tool.
- **Put it online:** see [docs/HOSTING.md](docs/HOSTING.md). GitHub Pages is free and takes about five minutes.

## Requirements

- Any modern browser (Chrome, Edge, Safari, Firefox) on a computer or phone
- An internet connection (loads Google Fonts, the jsPDF library from cdnjs, and the docx library from jsDelivr)
- No server, database, or build step

## AI disclosure

This project was built with the help of generative AI.

- **Tool used:** Claude, an AI model made by Anthropic
- **What the AI did:** wrote the website code, the PDF layout engine, the text of the five resume templates, the student instructions on the page, and this documentation
- **What a person did:** a Career Services advisor described what students need, chose the colors, templates, and section order, requested changes, and reviewed the results
- **How it was checked:** each template and look combination was generated as both a PDF and a .docx file, checked to confirm it fits on one page, and checked to confirm its text reads cleanly in order (the way an ATS reads it)

AI can make mistakes. If you find wording that is unclear or advice that does not fit your students or local employers, please edit it. [docs/CUSTOMIZING.md](docs/CUSTOMIZING.md) shows where everything lives.

Commits written by the AI are marked with a `Co-Authored-By: Claude` line in the git history.

## Credits

- [jsPDF](https://github.com/parallax/jsPDF) (MIT License) for building PDFs in the browser
- [docx](https://github.com/dolanmiu/docx) (MIT License) for building Word files in the browser
- [Archivo](https://fonts.google.com/specimen/Archivo) and [Source Sans 3](https://fonts.google.com/specimen/Source+Sans+3) from Google Fonts (SIL Open Font License)

## License

No license has been chosen yet. Until one is added, the default copyright rules apply. If you want other schools to be able to reuse this, add a license such as MIT or Creative Commons BY.
