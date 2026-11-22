INSPECTION REPORT BUILDER - STAGE 1
==================================

FILES
Keep these files together in one folder:
  index.html, manifest.webmanifest, sw.js, icon-*.png

STAGE 1 FEATURES
- Company profile: company name, address, phone, license/certificate number.
- Company logo and brand color applied to the report and PDF.
- Invoice number, due date, and payment terms on reports and send drafts.
- Saved client directory (name, property address, email).
- Built-in roof, solar, and construction starter templates; save custom templates.
- Full JSON backup and restore for reports, photos, sent log, company profile,
  saved clients, and templates.
- Existing local report history, PDF export, and offline app behavior remain.

WHITE-LABEL A COPY FOR A CUSTOMER
1. Make a separate copy of this entire folder for each customer.
2. In that copy, edit manifest.webmanifest:
     "name": "CUSTOMER COMPANY Reports"
     "short_name": "CUSTOMER"
   Keep the JSON syntax valid and retain the existing icons.
3. Host that folder as its own static site (GitHub Pages, Netlify, or
   Cloudflare Pages). Do not reuse one customer's folder for another customer.
4. Open the customer's URL and save the company profile, logo, and brand color
   in the app. Each customer should use their own URL / browser profile.
5. To update a customer's app, replace index.html and sw.js together. The
   service-worker VERSION is currently irb-v2; bump it again for future updates.

FREE HOSTING WITH GITHUB PAGES
1. Create a repository for the customer copy (check GitHub's age rules; a parent
   may need to own the account).
2. Upload all files in the folder to the repository root.
3. Repository Settings > Pages > Deploy from a branch > main / root > Save.
4. After deployment, open the Pages URL and install it from the browser.

INSTALL
- iPhone/iPad: open the URL in Safari > Share > Add to Home Screen.
- Android: open in Chrome > menu > Install app / Add to Home screen.
- Computer: in Chrome or Edge, use the install icon in the address bar.

IMPORTANT DATA / LIMITATIONS
- Company profile, clients, templates, report history, and sent log stay in
  that browser's local storage / IndexedDB. They are not uploaded to a server.
- Browser storage is device- and browser-specific. It is not automatically
  shared between devices or users. Clearing site data can erase local records.
- Export a JSON backup regularly and keep a separate copy of important PDFs.
  Import merges records by ID; matching IDs are replaced.
- Logo and photos are stored locally in browser data and in exported backups.
- The app prepares email/text/WhatsApp drafts but cannot send messages or attach
  PDFs automatically. The user must attach and send the downloaded PDF.
- Payment terms and invoice details are informational; this app does not process
  payments, issue legally compliant invoices, or provide accounting/tax advice.
- The report disclaimer remains: aerial observations are not a structural
  engineering assessment. Have qualified professionals confirm findings.
- First open online is required to cache the PDF library for offline use.
