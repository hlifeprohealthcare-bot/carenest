# CareNest — Family Healthcare Demo (Updated)

This is a React + Vite frontend demonstration for CareNest by H Life Pro Healthcare. It uses an original healthcare design, service-specific detail pages, responsive desktop navigation and a four-item mobile bottom navigation. It is not a production healthcare platform.

## Run on Windows
1. Install Node.js LTS from https://nodejs.org/en/download/ and keep **Add to PATH** enabled.
2. Extract the ZIP to a normal folder (not inside the ZIP preview).
3. Open the **carenest-final-updated** folder in VS Code. Confirm `package.json` is directly inside this folder.
4. Open **Terminal → New Terminal**.
5. Run these commands one at a time:

   ```powershell
   npm install
   npm run dev
   ```

6. Open the localhost URL Vite prints (usually `http://localhost:5173`). Keep the terminal open while using the website.
7. To stop the local server, press `Ctrl + C` in the terminal.

## Production build
Run `npm run build`. Vite writes the build to `dist`. This should be run after `npm install` succeeds.

## What is included
- Booking form with “Book for Myself”, family-member selection and “Other” option.
- Four primary destinations: Home, Bookings, CareVault and Profile; on mobile they appear as a bottom navigation bar.
- Profile demo name **Bhargav Kotadiya**, family member add/edit/view/remove, and the required settings order: App Language, Medication Reminders, Text Size, Security Center.
- Searchable language list. The app loads Google Website Translator over the internet to translate the rendered page into a selected language where the Google widget supports it. Translation requires internet and a third-party service; it is not an offline or guaranteed professional medical translation. Dynamic page content may not always remain translated after every React update.
- Three separate valid demonstration PDFs: prescription, laboratory report and visit report.
- File picker for PDF, JPG/JPEG, PNG and DOCX with file-size/type checks. Files are listed in browser-local demo storage, not uploaded to a secure server.
- Medication reminders with add, edit and delete; notifications are not scheduled.
- Separate service-detail pages, multiple local booking requests, demo ambulance route details, clinician verification checklist and a press-and-hold plus swipe-to-acknowledge SOS demo.
- Responsive layout and reduced-motion preferences.

## Important limitations and safety
- Booking requests, profiles, reminders and records use browser-local demo storage only. No real provider is contacted and no appointment is confirmed.
- Ambulance route details are user-entered demo information; there is no GPS tracking or dispatch integration. In an immediate emergency in India, call 112 directly.
- SOS does not call emergency services, send messages or share location.
- Clinician verification is a checklist demonstration only. It does not verify real doctor/nurse credentials.
- Sample PDFs are fictional and clearly labelled not for clinical use.
- Do not enter real patient or sensitive health information.
- Healthcare images load from Unsplash and need internet. Replace with appropriately licensed local assets before production.
- Before production, add authentication, backend authorization, secure file storage, consent/audit logs, actual provider availability, notifications, and verified medical workflows.


## Latest fixes
- Removed the duplicate Medication Reminders panel from the Profile view; reminders are managed from the single Profile setting and reminder modal.
- Updated language switching so choosing English clears Google Translate's persistent translation cookie and reloads the original page, rather than leaving the app stuck in Gujarati. Other language selections set the selected translation cookie and apply the translator.
- Google Translate requires internet access and may translate some dynamically rendered labels imperfectly. This is not a professionally reviewed localization bundle.
- The website design uses original CareNest styling and healthcare patterns, not a pixel-for-pixel copy of Apollo HomeCare.
