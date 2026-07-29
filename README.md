# Defence Coaching - PWA

Static Progressive Web App for Defence Coaching LMS landing page.

Quick local testing

1. Serve the folder over HTTP so mobile browsers load local images properly:

```bash
# from project root
python -m http.server 8000
# open on your phone: http://YOUR_PC_IP:8000
```

2. Alternatively use Node http-server:

```bash
npm install -g http-server
http-server -p 8000
```

Deploy to GitHub and Vercel

Option A — Create a GitHub repo and push:

```bash
git init
git add .
git commit -m "Initial site"
# create repository on GitHub (via web) and add remote, or use GitHub CLI:
# gh repo create your-username/defence-pwa --public --source=. --remote=origin
git push -u origin main
```

Option B — Deploy with Vercel (recommended for static sites):

```bash
npm i -g vercel
vercel login
vercel --prod
```

Notes

- Test the PWA install flow on a real device (Chrome on Android, Safari on iOS has limited PWA support).
- If the hero image is still blank on mobile, open DevTools (remote debugging) and inspect network/console to see whether `1.jpg` or `1.b64` failed to load.
- After deploying to Vercel, open the Vercel-provided URL on your phone to validate visuals and PWA install behavior.
