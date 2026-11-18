# العربي (Al-Arabi) — 3D Arabic Heritage Registration & Live Program Management App

**مسابقة لاكتشاف البطل في اللغة العربية — قسم اللغة العربية وآدابها، جامعة دار الهدى الإسلامية**

## Features
- **3D Heritage UI**: Royal Mahogany & Burnished Gold aesthetic with 3D tilt prize medallions (`4444` / `3333` / `2222`), Mashrabiya geometric lattice borders, and RTL Arabic typography (`Amiri` & `Cairo`).
- **Live Registration & UPI Payment**: Collects `اسم المشارك`, `عمر المشارك`, `كلية`, and `رقم الهاتف`, generates a scannable ₹50 UPI QR code for `+91 90725 84470`, and compresses uploaded payment screenshots.
- **Instant 3D Entry Pass**: Generates a printable/downloadable 3D participant pass upon registration.
- **Zero-Refresh Live Program Manager (`لوحة الإدارة`)**:
  - Default Admin PIN: `2026`
  - Streams registrations in real time across all devices using Firebase Firestore `onSnapshot` (also works offline/locally via `BroadcastChannel` + `localStorage` fallback if Firebase keys are not yet added).
  - Verify/reject payments, inspect payment screenshots, assign chest numbers, broadcast live stage announcements, and export participant lists to CSV.

## Quick Setup & Deployment (Vercel + Firebase)

### 1. Install Dependencies Locally
```bash
npm install
npm run dev
```

### 2. Connect Firebase Firestore (For Multi-Device Live Sync)
1. Go to [Firebase Console](https://console.firebase.google.com/) and create a new project.
2. Enable **Cloud Firestore** (Start in test mode or allow read/write on `registrations` and `settings`).
3. Copy your Web App credentials into a `.env` file (see `.env.example`).

### 3. Deploy to Vercel
1. Push this folder to GitHub or run `npx vercel` in the project directory.
2. Add the `VITE_FIREBASE_*` environment variables in your Vercel Project Settings.
3. Deploy!
