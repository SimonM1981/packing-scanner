# MG Packing System - Barcode & QR Scanner

Mobile-friendly web app for warehouse packing staff to scan barcodes/QR codes and record packing data directly into a Google Sheet.

## Features
- Live camera barcode/QR scanning (using html5-qrcode)
- Fallback: take photo of barcode if live scan fails
- Capture photos of inner box and carton label
- Submit data to private Google Apps Script backend → saves to Google Sheet + Drive
- Mobile optimized (works best on Android Chrome)

## Live Demo
https://simonm1981.github.io/packing-scanner/

## How to use
1. Open the link above on a mobile phone
2. Allow camera access when prompted
3. Fill in worker names, carton ID, customer (optional)
4. Scan **inner** and **outer** barcode using "SCAN LIVE" buttons
5. Take photos of labels if needed
6. Enter quantity
7. Tap **SUBMIT PACKING DATA**

Data is saved to a private Google Sheet (not visible publicly).

## Tech stack
- Frontend: HTML + CSS + JavaScript + [html5-qrcode](https://github.com/mebjas/html5-qrcode)
- Backend: Google Apps Script (receives POST requests)
- Hosting: GitHub Pages

## Setup (for developers)
1. Fork or clone this repo
2. Create Google Apps Script project with `doPost` endpoint (see `Code.gs` in related project)
3. Update `SCRIPT_URL` in `index.html` to your own Apps Script web app URL
4. Deploy → enable GitHub Pages on main branch

## License
MIT (or whatever you prefer – add if needed)
