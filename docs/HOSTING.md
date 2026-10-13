# Hosting the site

The site is a single file, `index.html`, with no server, database, or build step. Any web host that can serve one HTML file will work.

## Option 1: GitHub Pages (free)

1. In this repository on GitHub, go to **Settings** > **Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose the **main** branch and the **/ (root)** folder, then click **Save**.
4. Wait a minute or two, then refresh the page. GitHub shows your site's address, which looks like:
   `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`
5. Open that address on a computer and a phone to make sure it works, including **Download PDF**.

GitHub Pages is free for public repositories. A private repository needs a paid GitHub plan to use Pages.

## Option 2: Your school website

Send `index.html` to your web team or IT department. They can upload it as is, for example at `yourschool.edu/resumes`. Nothing else needs to be installed.

## Update the QR code after you host the site

The QR code on the page has to point to wherever the site lives. If you move the site, make a new QR code:

1. Go to any trusted QR code generator, or ask your IT team for one.
2. Make a QR code for your site's new address.
3. Download it as an **SVG** file.
4. Open `index.html` in a text editor and find the block that starts with `<svg viewBox=` inside `<div class="qr"`.
5. Replace that whole `<svg ...>...</svg>` block with the contents of your new SVG file.
6. Save the file, upload it again, and scan the code with your phone to test it.

**Tip:** Ask IT for a short link on your school's domain, like `yourschool.edu/resumes`, and put that in the QR code. If the site ever moves, IT can update where the short link points, and printed flyers keep working.

## Checklist before you share it

- [ ] The site opens on a phone and on a computer
- [ ] **Download for Google Docs (.docx)** and **Download PDF** both save a file
- [ ] The .docx opens in Google Docs with its lines and bullets
- [ ] The QR code opens the right address
- [ ] The school name and wording are correct (see [CUSTOMIZING.md](CUSTOMIZING.md))
