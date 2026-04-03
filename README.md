🌡️ Temp Advisor
AI-powered temperature & humidity storage guide for fruits, vegetables, dairy, and more.
> Built with vanilla HTML/CSS/JS + Claude AI + Open-Meteo weather API. Deployable in minutes on Vercel — free forever.
---
✨ Features
📍 Live weather detection — auto-fetches your location's outdoor temperature and humidity
📷 AI photo scanning — upload a photo of your fridge or shelf and Claude identifies the items
🧊 4 storage types — Refrigerator, Freezer, Pantry, Cold Warehouse
💧 Humidity recommendations — ideal humidity range per item with visual bar indicator
✅ Compatibility check — flags items stored in the wrong environment
🌙 Dark mode — automatic, follows system preference
📱 Mobile-friendly — works on any device
---
🚀 Deploy in 5 minutes (Vercel)
Step 1 — Get your Anthropic API key
Go to console.anthropic.com
Create an account and go to API Keys
Click Create Key and copy it
Step 2 — Push to GitHub
```bash
git clone https://github.com/YOUR_USERNAME/temp-advisor
cd temp-advisor
git add .
git commit -m "initial commit"
git push
```
Step 3 — Deploy to Vercel
Go to vercel.com and sign in with GitHub
Click Add New Project → select your `temp-advisor` repo
Click Deploy (Vercel will auto-detect the config)
Step 4 — Add your API key (keeps it secret!)
In your Vercel project, go to Settings → Environment Variables
Add a new variable:
Name: `ANTHROPIC_API_KEY`
Value: your API key from Step 1
Click Save, then go to Deployments and click Redeploy
That's it — your app is live at `https://your-project.vercel.app` 🎉
---
📁 Project structure
```
temp-advisor/
├── api/
│   └── scan.js          # Vercel serverless function (keeps API key secret)
├── public/
│   └── index.html       # Full frontend app
├── vercel.json          # Vercel routing config
└── README.md
```
---
🔒 Security
Your Anthropic API key is stored as a Vercel environment variable — it is never exposed to the browser. All AI calls are proxied through the `/api/scan` serverless function.
---
🛠️ Local development
```bash
npm install -g vercel
vercel dev
```
Then open `http://localhost:3000`.
Set your API key locally:
```bash
export ANTHROPIC_API_KEY=your_key_here
```
---
📊 Tech stack
Layer	Technology
Frontend	HTML, CSS, Vanilla JS
AI vision & recommendations	Claude claude-sonnet-4-20250514 (Anthropic)
Weather & humidity data	Open-Meteo API (free, no key needed)
Geocoding	Nominatim / OpenStreetMap
Hosting & backend	Vercel (free tier)
---
📝 LinkedIn post template
> 🌡️ I built **Temp Advisor** — an AI-powered app that recommends the ideal temperature and humidity to store your food.
>
> You upload a photo of your fridge or pantry → the AI identifies your items → it gives you precise storage conditions for each one, based on your live local weather.
>
> Built with: Claude AI · Open-Meteo · Vercel · vanilla HTML/JS
>
> 🔗 Live demo: https://your-project.vercel.app
> 📂 GitHub: https://github.com/YOUR_USERNAME/temp-advisor
>
> #buildinpublic #AI #webdev #project
---
📄 License
MIT — free to use, modify, and share.
