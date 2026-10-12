# How it works (technical notes)

These notes are for whoever maintains the site.

## Overview

`index.html` is a self-contained static page. It loads two things from the internet:

- **Fonts:** Archivo and Source Sans 3 from Google Fonts, used only for the website itself, not the resumes
- **jsPDF 2.5.1** from cdnjs (`https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js`), which builds the PDFs in the browser

There is no backend. All logic runs in one inline `<script>`.

## Data

- `TEMPLATES`: the five templates. Each is a list of blocks (heading, entry, bullet, paragraph, and so on). See [CUSTOMIZING.md](CUSTOMIZING.md) for the block codes.
- `LOOKS`: the layout settings for Traditional, Modern, and Compact.
- `COLORS`: the preset colorways.

## Layout engine

`layout(template, look, accentColor)` turns a template into a list of drawing operations measured in PDF points on a US Letter page (612 x 792 pt, 0.75 in margins):

- `text`: string, position, font, style, size, color, alignment, letter spacing
- `line`: rules under the header and section headings
- `rect`: the color band in the Modern look
- `dot`: bullet markers

Text wrapping and widths are measured with jsPDF's own font metrics (`splitTextToSize`, `getTextWidth`), so the layout matches the PDF.

The same operations are drawn twice:

- **Preview:** drawn on a `<canvas>` with matching system fonts (Helvetica/Arial or Times New Roman). The preview can differ from the PDF by a pixel or two, depending on the fonts installed on the device.
- **PDF:** drawn with jsPDF using its built-in standard fonts (Helvetica, Times). Text is real and selectable, which is what makes the resumes ATS-readable.

Bullets are drawn as small filled circles instead of a bullet character. Template text uses plain ASCII because the standard PDF fonts can't encode some Unicode characters.

## Downloads

When the page runs inside Claude's artifact viewer, it saves files through the viewer's `downloads` capability. Anywhere else, it falls back to a normal browser download, using a temporary `blob:` link with the `download` attribute.

## Saved preferences

The student's last template, look, and color are kept in `localStorage` under the key `resume-builder`. Nothing else is stored. Every read and write is wrapped in `try/catch`, so the page still works in private browsing.

## Testing a change

1. Open `index.html` in a browser.
2. Try every template with every look. Make sure nothing runs off the bottom of the preview.
3. Download a PDF, open it, select all the text, and paste it into a plain text editor. It should read top to bottom in the right order. That's roughly what an ATS sees.
