# Smart Farm BD

A Bengali/English React + TypeScript starter for a mixed livestock and poultry farm.

## Current starter features
- Responsive dashboard and navigation
- Bengali/English language switch
- Add and search animal records
- Local demo persistence in browser storage
- Income/expense entry and summary
- QR code PNG download for animal records
- PWA manifest and basic static-shell service worker
- Firebase SDK initialization scaffold

## Important status
This is a **starter prototype**, not the completed production ERP. The visible demo currently stores animal and transaction entries in the browser. It does not yet implement Firebase phone OTP login, Firestore CRUD, secure QR profile routing, role management, breeding workflows, scheduled notifications, or production-grade accounting. Do not enter confidential or business-critical records until those modules are implemented and tested.

## Run locally
1. Install Node.js 20 or later.
2. Extract the ZIP.
3. Run `npm install`.
4. Copy `.env.example` to `.env`.
5. Fill in your Firebase Web App configuration.
6. Run `npm run dev`.

## Firebase setup still required
In Firebase Console:
- Create a project and register a Web App.
- Enable Phone Authentication and configure authorized domains / reCAPTCHA.
- Create Firestore database.
- Enable Storage.
- Review and test `firestore.rules` before deployment.
- Configure Storage Rules separately.
- Set up Cloud Functions for privileged workflows and scheduled reminders.

The current `firestore.rules` file is a starting point and requires refinement: sensitive collections should have collection-specific permission checks rather than a broad shared rule.

## Build
`npm run build`

## PWA icons
Add real PNG icons at `public/icon-192.png` and `public/icon-512.png` before publishing. The manifest references these files.
