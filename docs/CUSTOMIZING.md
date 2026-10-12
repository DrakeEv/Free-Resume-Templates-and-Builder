# Customizing the site

Everything lives in `index.html`. Open it in a plain text editor, such as Notepad, TextEdit (in plain-text mode), or VS Code. Don't use Word, which adds formatting that breaks the file.

After any change, save the file, open it in your browser, and try a download to make sure everything still works.

## Change the office name or page wording

Search the file for the text you want to change and edit it directly. Common spots:

| What | Search for |
|---|---|
| Office name at the top | `Career Services` (appears in the header, the checklist, and the footer) |
| Page title | `Student Resume Templates` |
| Intro sentence | `Choose a template, pick a look` |
| Drive instructions | `How to edit and save your resume` |
| Checklist | `Before you send your resume` |
| Footer | `Questions? Stop by` |

## Change the website colors

The site's red, white, and blue colors are set in one place near the top of the file, in the `:root` block:

```css
--navy:#14284b; --red:#c8102e; --red-dark:#a30d25;
```

Replace the color codes (hex values) with your school's colors.

## Change the resume colorways

Search for `const COLORS`. Each entry is a name and a color code:

```js
const COLORS=[["Navy","#1f3a68"],["Crimson","#a6192e"],["Forest","#2f5d3a"], ...];
```

Add, remove, or rename entries. Use dark colors so text stays readable when printed.

## Edit the wording inside a resume template

Search for `const TEMPLATES`. Each template has an `id`, a `title`, a short `tag` and `desc` for its button, and a list of `blocks`. Each block is one piece of the resume, written with a short code:

| Code | Makes | Example |
|---|---|---|
| `H("...")` | A section heading | `H("Education")` |
| `E(left, right, sub)` | An entry: bold title on the left, date on the right, optional italic line below | `E("Job Title","Month Year - Present","Company Name, City, State")` |
| `L(left, right)` | A single bold line with a date on the right | `L("Certification Name - Issuer","Month Year")` |
| `B("...")` | A bullet point | `B("Trained 5 new hires.")` |
| `P("...")` | A paragraph | `P("Reliable, motivated student...")` |
| `K(label, text)` | A bold label followed by text | `K("Technical","Excel, Canva")` |
| `S("...")` | A small colored subheading (used in Skills-Based) | `S("Communication")` |
| `G` | A little extra space | `G` |

**Use plain characters only.** Type a regular hyphen (`-`), not an en dash or em dash, and straight quotes (`'`), not curly quotes. The built-in PDF fonts can't show some special characters.

## Add a new template

Copy an existing template block in `TEMPLATES`, from `{id:"..."` through its closing `]},`, paste it in, and change the `id`, `title`, `tag`, `desc`, and `blocks`. The `id` is used in the downloaded file's name, so keep it short with no spaces, for example `Nursing-Clinical`.

Keep each template to one page. If a preview runs past the bottom of the page, remove some blocks.

## Change or add a look

Search for `const LOOKS`. Each look sets the font (`helvetica` or `times`), body text size, name size, whether things are centered, and how section headings and lines are drawn. Copy a look, give it a new key and `name`, and adjust its numbers.

To keep a new look ATS-friendly, keep a single column and stick to `helvetica` or `times`.
