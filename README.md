# LinkDesk

A single-page, browser-only tool for working with web links in spreadsheets and documents.

- **Make links:** upload an Excel or CSV file and download a copy where every plain-text address is clickable.
- **Open in batches:** load links and open them in batches of 10, 20, 30 or 50 tabs, with progress tracking.
- **Extract links:** paste text or add a Word, PDF, text or HTML file and pull out every web address, including links hidden behind clickable words.

Everything runs in the browser. Files are never uploaded anywhere.

## Run locally

Open `index.html` in a browser.

## Deploy

It is a static site with no build step. On Vercel, import this repository and deploy with the default settings.

## Notes

- Libraries load from cdnjs (SheetJS always; JSZip and PDF.js only when a Word or PDF file is added).
- Scanned PDFs have no selectable text, so no links can be read from them.
- Allow pop-ups for the page so a whole batch of tabs can open at once.
