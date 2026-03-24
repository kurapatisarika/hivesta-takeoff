# Hivesta Takeoff Pro — Deployment Guide

## What's in this folder
- `src/HivestaApp.jsx` — the main app
- `src/main.jsx` — entry point
- `api/claude.js` — secure API proxy (hides your key)
- `index.html`, `vite.config.js`, `package.json`, `vercel.json` — project config

---

## STEP-BY-STEP: Deploy to Vercel

### 1. Create a GitHub account (if you don't have one)
Go to https://github.com and sign up for free.

### 2. Create a new GitHub repository
- Click the "+" icon → "New repository"
- Name it: hivesta-takeoff
- Set to Private
- Click "Create repository"

### 3. Upload these files to GitHub
- Click "uploading an existing file" link on the repo page
- Drag and drop ALL files from this folder (keep folder structure)
- Click "Commit changes"

### 4. Create a Vercel account
Go to https://vercel.com and sign up with your GitHub account.

### 5. Import your project in Vercel
- Click "Add New Project"
- Select your "hivesta-takeoff" repo
- Framework: Vite (auto-detected)
- Click "Deploy" — wait ~1 minute

### 6. Add your Anthropic API Key
- In Vercel dashboard → your project → Settings → Environment Variables
- Add:  Name: ANTHROPIC_API_KEY  |  Value: sk-ant-YOUR-KEY-HERE
- Click Save → then go to Deployments → click "Redeploy"

### 7. Your app is live!
You'll get a URL like: https://hivesta-takeoff.vercel.app

---

## STEP-BY-STEP: Embed on GoDaddy

### GoDaddy Website Builder
1. Open your GoDaddy site editor
2. Click "+" to add a section → choose "HTML" or "Embed Code"
3. Paste this code (replace the URL with your Vercel URL):

<iframe 
  src="https://hivesta-takeoff.vercel.app" 
  width="100%" 
  height="950px" 
  frameborder="0" 
  style="border-radius:8px; display:block;">
</iframe>

4. Save and publish

### WordPress on GoDaddy
1. Edit the page where you want the tool
2. Click "+" → search for "Custom HTML" block
3. Paste the same iframe code above
4. Update/Publish the page

---

## Get your Anthropic API Key
1. Go to https://console.anthropic.com
2. Sign up / log in
3. Go to API Keys → Create Key
4. Copy the key (starts with sk-ant-...)
5. Paste it in Vercel → Environment Variables

---
Questions? Contact Hivesta Construction
www.hivestaconstruction.com | (689) 254-3553
