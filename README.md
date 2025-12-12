# Fotscores API Cache

This repository automatically fetches and caches Premier League data from Football-Data.org API every 5 minutes using GitHub Actions.

## 🚀 Setup Instructions

### 1. Create This Repository on GitHub

1. Go to [GitHub](https://github.com) and create a new **public** repository
2. Name it: `fotscores-api-cache` (or your preferred name)
3. **Important**: Make it PUBLIC (required for GitHub Pages)

### 2. Upload These Files

Upload all files from this folder to your new repository:

- `.github/workflows/fetch-data.yml`
- `matches.json`
- `standings.json`
- `scorers.json`
- `README.md`

### 3. Add Your API Key as a Secret

1. Go to your repository → **Settings**
2. Left sidebar → **Secrets and variables** → **Actions**
3. Click **New repository secret**
4. Name: `FOOTBALL_API_KEY`
5. Value: Your Football-Data.org API key (`e8ad6894e465471cb9b31c30c8f6a400`)
6. Click **Add secret**

### 4. Enable GitHub Pages

1. Go to **Settings** → **Pages**
2. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
3. Click **Save**
4. Wait 1-2 minutes for deployment

### 5. Get Your GitHub Pages URL

After enabling Pages, you'll see:

```
Your site is published at https://YOUR_USERNAME.github.io/fotscores-api-cache/
```

**Your API endpoints will be:**

- Matches: `https://YOUR_USERNAME.github.io/fotscores-api-cache/matches.json`
- Standings: `https://YOUR_USERNAME.github.io/fotscores-api-cache/standings.json`
- Top Scorers: `https://YOUR_USERNAME.github.io/fotscores-api-cache/scorers.json`

### 6. Test the GitHub Action

1. Go to **Actions** tab
2. Click on "Fetch Football Data" workflow
3. Click **Run workflow** → **Run workflow**
4. Wait ~30 seconds
5. Check if JSON files are updated in your repo

### 7. Update Your Android App

Replace `YOUR_USERNAME` in your Android app's `Constants.kt`:

```kotlin
const val BASE_URL = "https://YOUR_USERNAME.github.io/fotscores-api-cache/"
```

---

## 📊 How It Works

1. **GitHub Actions** runs every 5 minutes
2. Fetches fresh data from Football-Data.org API
3. Saves to `matches.json`, `standings.json`, `scorers.json`
4. Commits and pushes to repository
5. **GitHub Pages** serves the JSON files publicly
6. Your Android app fetches from GitHub Pages (unlimited users!)

---

## ✅ Benefits

- ✅ **Unlimited users** - No rate limits
- ✅ **Free forever** - No hosting costs
- ✅ **Auto-updates** - Every 5 minutes
- ✅ **No backend** - Pure GitHub solution
- ✅ **Public data** - No API key needed in app

---

## 🔧 Troubleshooting

**Action fails?**

- Check if `FOOTBALL_API_KEY` secret is set correctly
- Verify your API key is valid at football-data.org

**JSON files not updating?**

- Check Actions tab for error logs
- Make sure repository is public
- Verify GitHub Pages is enabled

**App can't fetch data?**

- Check GitHub Pages URL is correct
- Wait 2-3 minutes after first setup
- Test URLs in browser first

---

## 📝 Notes

- Data updates every 5 minutes (matches free tier delay)
- Free tier supports 12 competitions (we use only EPL)
- GitHub Actions has 2000 free minutes/month (plenty for this)
- JSON files are publicly accessible (no authentication needed)

---

## 🎯 Next Steps

After setup, update your Android app to use the GitHub Pages URL instead of the direct API.

See the Android app update instructions in your project.
