# Business Card QR Maker

A single web page where each employee enters their contact details and downloads a QR code for the back of their business card. Scanning the code with an iPhone or Android camera offers to save the person as a contact.

The contact details are stored inside the QR code as a vCard 3.0, so the code works offline and never expires. Nothing anyone types leaves their browser.

## Files

- `index.html` is the complete page. Open it in a browser, or host it anywhere, including GitHub Pages.
- `squarespace-code-block.html` is the same tool packaged for a Squarespace Code Block. Its styles are scoped so they don't affect the rest of the site.

## Hosting on GitHub Pages

In the repository, go to **Settings → Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, and save. The page will be live at `https://<your-username>.github.io/<repo-name>/`.

## Printing

- Download the SVG for your printer when possible. It stays sharp at any size.
- The page shows the minimum print width for each code, usually about 1 inch (25 mm).
- Keep the white border around the code and print dark on a light background.
- Test a printed proof with both an iPhone and an Android phone.

## Updating details

The details are inside the code, so a change of phone number or title means generating a new code and reprinting.
