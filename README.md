[README.md](https://github.com/user-attachments/files/22687736/README.md)
# Tiny Wins

**Start tiny. Win daily.**  
A gentle, non‑judgmental micro‑habits app that helps people who feel excluded by traditional fitness advice make progress with **one movement nudge** and **one eating nudge** per day — especially those with **very limited mobility**.

- No diets. No gyms. No calorie counting.
- UK‑friendly language (e.g. *coke*, *chips*).
- Privacy‑first: no accounts; habits stored locally in the browser.

---

## ✨ Features

- **Daily challenges**: one *move a bit more* nudge + one *eat a bit less* nudge.
- **Level tailoring**: *Very limited mobility*, *Beginner*, *Moderate* challenge banks.
- **Progress & streaks**: confidence via simple check‑offs (no weight entry).
- **Accessibility**: **Large Text** and **High Contrast** modes.
- **For Clinicians**: printable one‑pager with safety and recommendation script.
- **About & Story**: founder note and programme principles.
- **Privacy by default**: uses `localStorage`; no personal data collected by the app.

Tech stack: **Next.js 14 (pages router)**, **React 18**, **Tailwind CSS**, **Framer Motion**, **lucide-react**.

---

## 🚀 Quick Start (Local Development)

**Requirements**
- Node.js **18+** and npm

**Install & run**
```bash
npm install
npm run dev
```

Open **http://localhost:3000**

**Build for production**
```bash
npm run build
npm start
```

---

## 🌐 Deploy

### Option A — Vercel (recommended)
1. Create a new repo on GitHub (e.g. `tiny-wins`) and push this project.
2. Go to **Vercel → Add New Project → Import from GitHub**.
3. Framework will auto‑detect **Next.js**. Click **Deploy**.
4. Add a custom domain (optional): *Project → Settings → Domains*.

### Option B — Vercel CLI (no GitHub)
```bash
npm install
npx vercel
# for a production URL:
npx vercel --prod
```

### Option C — Netlify
- New site → **Import from Git** → select your repo.  
- Use the Next.js preset (auto) or set:  
  - **Build command:** `npm run build`  
  - **Publish directory:** `.next` (Netlify plugin handles this for you).

> No environment variables are required for the starter.

---

## 📁 Project Structure

```
tiny-wins/
├─ pages/
│  ├─ _app.js          # Global styles import
│  └─ index.jsx        # Entire MVP (tabs + screens) in one file
├─ components/
│  └─ ui/              # Minimal Button, Card, Badge, Progress
├─ styles/
│  └─ globals.css      # Tailwind + a11y helpers
├─ public/
│  └─ favicon.ico
├─ tailwind.config.js
├─ postcss.config.js
├─ next.config.mjs
├─ package.json
└─ README.md
```

---

## 🧩 Key Files & How to Customise

- **Challenge banks**: in `pages/index.jsx` look for
  - `VERY_LIMITED_MOVE_CHALLENGES`, `BEGINNER_MOVE_CHALLENGES`, `MODERATE_MOVE_CHALLENGES`
  - `VERY_LIMITED_EAT_CHALLENGES`, `BEGINNER_EAT_CHALLENGES`, `MODERATE_EAT_CHALLENGES`
- **Branding & copy**: Home, About, Clinicians sections live in `pages/index.jsx`.
- **Accessibility controls**: `SettingsView` in `pages/index.jsx` (uses `localStorage` keys `tw-a11y-*`).
- **Icons**: from `lucide-react`. Swap or extend in the Header tab list.
- **Styling**: Tailwind utility classes throughout; tweak in `styles/globals.css` or inline.

---

## 🔒 Privacy & Data

- **No account / login.**  
- **No server data.** Streaks and preferences are stored in the user’s browser via `localStorage`.
- If you later add analytics or email, clearly update this section and the in‑app copy.

---

## 🩺 Safety Notice (Non‑medical)

This app provides **general wellbeing prompts** only. It isn’t a medical device or a substitute for professional care.  
Users should **start small**, **listen to their body**, and **speak to their GP** if they have concerns, pain, dizziness, chest discomfort, breathlessness beyond normal, or any uncertainty about what’s right for them.

Clinician tab includes a short **recommendation script** and a **print** button for an A4 one‑pager.

---

## 🔎 SEO & Discoverability (optional)

To reach people who avoid fitness sites:
- Add plain‑English content pages targeting searches like **“too tired to exercise”**, **“gentle ways to move at home”**, **“hate dieting but want to feel better”**.
- Add meta tags/OpenGraph in `pages/index.jsx` via `next/head` (title, description, social image).
- Share QR posters in **GP surgeries, pharmacies, libraries, community centres**.

Example `Head`:
```jsx
import Head from "next/head";
// inside the component render:
<Head>
  <title>Tiny Wins — start tiny, win daily</title>
  <meta name="description" content="A gentle micro‑habits app for people who hate diets and gyms. Very limited mobility options included." />
  <meta property="og:title" content="Tiny Wins" />
  <meta property="og:description" content="Move a little more. Eat a little less. No guilt. No numbers." />
</Head>
```

---

## 🗺️ Roadmap Ideas

- **PWA** (installable, offline) + subtle push reminders.
- **Printable A4 poster** with QR code for clinics and pharmacies.
- **Multi‑language** and culturally localised challenge banks.
- **Optional profiles** (with explicit consent) to sync streaks across devices.
- **Clinician referral pack** (PDF) and outcome measures (e.g. self‑reported energy/mood).

---

## 🤝 Contributing

PRs welcome. Please keep tone **non‑judgmental**, copy **plain English**, and protect **privacy by default**.

**Code style:** lightweight; Tailwind utilities; no CSS frameworks beyond Tailwind.  
**Testing:** manual for now; keep components small and accessible.

---

## 📄 License

MIT © You (the project owner).  
You can replace this with any licence you prefer for your business use.
