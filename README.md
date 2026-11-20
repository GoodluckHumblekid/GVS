# GUDDITHEKING VICOBA Management System

Responsive static web application based on the supplied VICOBA.xlsx workbook.

## Included
- Dashboard: members, share capital, loans and outstanding balances
- Member registration, editing, deletion and search
- Bulk Excel import (`.xls`, `.xlsx`, `.csv`) from the first worksheet
- Downloadable Excel import template
- Shares and savings deposit/withdrawal tracking
- Loan application, approval/rejection and balance tracking
- Loan repayments with overpayment validation
- Excel exports for members, loans, transactions and full records
- Print-friendly reports / Save as PDF
- JSON backup and restore
- Configurable share price and loan eligibility
- Responsive mobile and desktop layout

## Run and publish
Open `index.html` in a modern browser. For GitHub Pages, upload `index.html`, `style.css`, `app.js`, and this README to a repository. Then go to **Settings → Pages**, select the `main` branch and root folder, and save.

The SheetJS library is loaded from jsDelivr CDN for Excel import/export, so an internet connection is needed for those functions.

## Imported workbook data
The app starts with the 97 member IDs from the workbook (`GTK2026/0001` to `GTK2026/0097`). The first member is Ngasa Shadrack. Share value is TZS 2,500. Four member rows have populated share counts (1, 2, 4 and 10); remaining blank share counts are initialized as zero. Empty names are left blank for completion.

**Loan percentage conflict:** Sheet2's written instructions say 70% loan eligibility, while Sheet1 formulas calculate 80%. The app defaults to 70% based on the written instruction. This can be changed in Settings.

## Data and security limitation
This is a GitHub Pages/browser-only version. Data is stored in local storage on the current browser/device and is not synchronized across users or devices. It has no server authentication, role-based permissions or central database. For live VICOBA financial operations involving multiple users, implement a secure backend, database, authentication, authorization, audit trail and automated backups.
