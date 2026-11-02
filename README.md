# Algoryx employee desk

Live internal dashboard for Algoryx: PIN login, marketing, sales (PDF lead parsing + cold call), and notifications.

## PIN access (change these after first login)

| Role | Name | PIN |
| --- | --- | --- |
| Super Admin | Riya Shah | 2401 |
| Admin | Arjun Mehta | 1204 |
| Employee | Maya Iyer | 1111 |

Super Admin manages people and PINs in Settings. Admin can enter marketing numbers, edit the call script, and post team notices. Everyone sees the same sections.

## Local

```bash
npm install
npm run dev
```

## Deploy on Vercel (free) via GitHub

1. Create a GitHub repo and push this folder.
2. Import the repo in [Vercel](https://vercel.com) (Hobby plan is enough).
3. Framework preset: Vite. Build command `npm run build`, output `dist`.
4. After deploy, open the URL, sign in with a PIN.

Data is stored in the browser on that device so the app can go live without a paid database. Use **Settings → Export backup** / **Import backup** to move the desk between machines. A shared database can be added later without changing the screens.

## Lead PDFs

Sales → Leads accepts a **text PDF** (exported contacts, not a photo scan). The parser looks for emails, phones, names, companies, titles, and addresses, then shows a review table before import.
