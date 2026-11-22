# Premium Due Reminder

A phone-friendly web app for customer service teams: on every **5th and 25th** it lists customers whose insurance premium is due before the next check-in, flags who to remind **3 days before** the due date, and opens **WhatsApp** with a ready-made **English + Chinese** reminder. It also exports a PDF list with each customer's ePartner screenshot.

**Open the app:** `index.html` (or the GitHub Pages link, if enabled).

## Features
- Import the customer list from Excel (.xlsx/.xls) or CSV; column names are matched automatically
- Check-in cycles on the 5th and 25th, plus 3 days' overlap so nobody falls in the gap
- Monthly / quarterly / half-yearly / yearly premiums roll forward automatically
- Messy data is never guessed: impossible dates, missing phones and duplicates go to a "To check" tab
- WhatsApp-styled bilingual message with a chat preview; you always press Send yourself
- PDF export: a summary page, then one page per customer with both messages and the ePartner screenshot
- Every save, delete and import asks for confirmation

## Privacy
There is no server. Customer data, screenshots and "reminded" marks are stored only in the browser of the device that imports them (localStorage / IndexedDB). **Never commit real customer files to this repository.** The files in `docs/` use made-up customers.

## Files
- `index.html`: the whole app (one file; libraries load from cdnjs: SheetJS, html2canvas, jsPDF)
- `docs/HOW-TO-USE.md`: plain-English user guide
- `docs/sample-customers.csv`: made-up test list (includes deliberately messy rows)
- `docs/sample-output.pdf`: a test-run PDF for the 25 Nov 2026 check-in
