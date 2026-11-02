# LinkDesk

A single-page, browser-only tool for working with web links in spreadsheets and documents.

- **Make links:** upload an Excel or CSV file and download a copy where every plain-text address is clickable.
- **Open in batches:** load links and open them in batches of 10, 20, 30 or 50 tabs, with progress tracking.
- **Extract links:** paste text or add a Word, PDF, text or HTML file and pull out every web address, including links hidden behind clickable words.
- **Link Cleaner:** paste messy links or add a file. It removes everything after the `?` when a page does not need it (for example `x.com/user/status/123?a=abc` becomes `x.com/user/status/123`), removes tracking codes (`utm_`, `fbclid`, `gclid` and others), unwraps redirect links from Google, Facebook, Outlook and similar, fixes broken schemes and defanged links, drops invalid lines and duplicates, and can check that each site responds.

Everything runs in the browser. Files are never uploaded anywhere.

## Run locally

Open `index.html` in a browser.

## Deploy

It is a static site with no build step. On Vercel, import this repository and deploy with the default settings.

## Safety limits

- Files up to 100 MB.
- Spreadsheets up to 1,000,000 cells.
- Up to 5,000 links per list.
- Pasted text up to 2 million characters.
- PDFs read up to 300 pages.
- Word files that expand into very large content are refused.

## Notes

- Libraries load from cdnjs (SheetJS always; JSZip and PDF.js only when a Word or PDF file is added).
- The "Check they respond" button needs to reach other websites, so it works on your own site (for example on Vercel) but not inside claude.ai. It shows whether the site answers. It cannot tell whether one specific page exists, because browsers do not let a page read that.
- Scanned PDFs have no selectable text, so no links can be read from them.
- Allow pop-ups for the page so a whole batch of tabs can open at once.
