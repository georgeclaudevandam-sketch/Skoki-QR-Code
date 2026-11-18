# Business Card QR Maker

A single web page where each employee enters their contact details and downloads a QR code for the back of their business card. Scanning the code with an iPhone or Android camera offers to save the person as a contact.

The contact details are stored inside the QR code as a vCard 3.0, so the code works offline and never expires. Nothing anyone types leaves their browser.

## Scanning a business card

The **Scan a card** tab reads someone else's card with a laptop webcam or a phone camera, or from a photo.

- If the card has a QR code with contact details, those are used directly.
- Otherwise the printed text is read on the device with [Tesseract.js](https://github.com/naptha/tesseract.js) and sorted into name, title, company, phones, email, website and address. The photo never leaves the browser. Check the details before saving, because printed text is read on a best-effort basis.
- **Save to contacts** downloads a `.vcf` file. Opening it on a phone or computer adds the contact.
- **Make a QR code from this** copies the details into the QR maker.
- The page also shows a QR code of the scanned contact, so someone at a laptop can scan it with their phone to add the contact there.

The camera needs the page to be served over `https://` (GitHub Pages and Squarespace both are). The first scan downloads the text reader, about 7 MB, and later scans reuse it.

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
