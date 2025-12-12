# GitHub Pages Setup - Quick Guide

## Step-by-Step (5 Minutes)

### 1. Create GitHub Repository

- Go to github.com
- Click "New repository"
- Name: `fotscores-api-cache`
- **Make it PUBLIC** ✅
- Click "Create repository"

### 2. Upload Files

Upload these files from `github-repo-files/` folder:

- `.github/workflows/fetch-data.yml`
- `matches.json`
- `standings.json`
- `scorers.json`
- `README.md`

### 3. Add API Key Secret

- Settings → Secrets → Actions → New secret
- Name: `FOOTBALL_API_KEY`
- Value: `e8ad6894e465471cb9b31c30c8f6a400`

### 4. Enable GitHub Pages

- Settings → Pages
- Source: `main` branch, `/ (root)` folder
- Save

### 5. Get Your URL

After 2 minutes, you'll see:

```
https://YOUR_USERNAME.github.io/fotscores-api-cache/
```

### 6. Update Android App

Replace in `Constants.kt`:

```kotlin
const val BASE_URL = "https://YOUR_USERNAME.github.io/fotscores-api-cache/"
```

Remove API key requirement (no longer needed!)

---

## Files Location

All GitHub files are in:
`/Users/sohelkabir/Documents/app/Fotscores/github-repo-files/`

Upload these to your GitHub repository.
