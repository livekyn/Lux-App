# Deployment Guide

Complete instructions for deploying KYN Lux to GitHub Pages or any static host.

## Table of Contents
1. [GitHub Pages (Recommended)](#github-pages-recommended)
2. [Alternative Hosts](#alternative-hosts)
3. [Custom Domain](#custom-domain)
4. [Security & Best Practices](#security--best-practices)

---

## GitHub Pages (Recommended)

### Step 1: Create a GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `kyn-lux` (or your preferred name)
3. Description: "Intelligent sun therapy tracking PWA"
4. Choose **Public** (to deploy with Pages)
5. Initialize with: ✓ Add a README file
6. Click **"Create repository"**

### Step 2: Upload Files

Choose one of these methods:

#### Method A: Web Upload (Easiest)
1. In your new repository, click **"Add file" → "Upload files"**
2. Drag and drop these files:
   - `index.html` (the main app)
   - `README.md`
   - `CHANGELOG.md`
   - `LICENSE`
   - `FEATURES.md`
   - `QUICKSTART.md`
   - `.gitignore`
3. Commit with message: "Initial commit: KYN Lux v4.5"

#### Method B: Git Command Line (If you have Git installed)
```bash
git clone https://github.com/YOUR_USERNAME/kyn-lux.git
cd kyn-lux

# Copy files into the directory
cp ~/Downloads/index.html .
cp ~/Downloads/README.md .
cp ~/Downloads/CHANGELOG.md .
# ... etc for other files

# Commit and push
git add .
git commit -m "Initial commit: KYN Lux v4.5"
git push origin main
```

### Step 3: Enable GitHub Pages

1. In your repository, go to **Settings** (top menu)
2. Scroll to **"Pages"** section (left sidebar)
3. Under **"Build and deployment"**:
   - **Source**: Select **"Deploy from a branch"**
   - **Branch**: Select **`main`** (or your branch)
   - **Folder**: Select **`/ (root)`**
4. Click **"Save"**

GitHub will take ~1 minute to build and deploy.

### Step 4: Verify Deployment

Your app is now live at:
```
https://YOUR_USERNAME.github.io/kyn-lux/
```

1. Visit that URL in your browser
2. You should see the KYN Lux home screen
3. Open on iPhone and add to home screen: **Share → Add to Home Screen**

✅ **Deployed!**

---

## Update Your App

Whenever you make changes (bug fixes, new features):

1. Update the files locally
2. Commit and push to `main` branch:
   ```bash
   git add .
   git commit -m "v4.5.1: Fix clothing icon colors"
   git push origin main
   ```
3. GitHub automatically re-deploys within 1 minute
4. Clear your browser cache (Cmd+Shift+Delete on desktop, or hard refresh with Cmd+Option+R on Safari iOS)

---

## Alternative Hosts

### Netlify (Drag & Drop)

1. Go to [netlify.com](https://netlify.com)
2. Sign in with GitHub account
3. Drag your `index.html` file into the deployment area
4. Your app is live at a Netlify URL (e.g., `https://wizardly-einstein-7d4c2c.netlify.app`)
5. To set a custom domain or enable auto-deployments from GitHub, connect your repository

**Advantages**: Easier initial setup, built-in preview deployments
**Disadvantages**: Requires account, slightly less customizable

### Vercel

1. Go to [vercel.com](https://vercel.com)
2. Sign in with GitHub
3. Click **"New Project"**
4. Import your `kyn-lux` repository
5. Click **"Deploy"**

Your app is live at `https://kyn-lux.vercel.app` (customizable).

**Advantages**: Very fast, great for SPAs, seamless GitHub integration
**Disadvantages**: May have build step (unnecessary for static files)

### AWS S3 + CloudFront

1. Create an S3 bucket
2. Upload `index.html` and all files
3. Enable static website hosting
4. (Optional) Use CloudFront for CDN/caching
5. Access your app at the S3 endpoint

**Advantages**: Highly scalable, excellent performance
**Disadvantages**: More complex, requires AWS account and setup knowledge

### Firebase Hosting

1. Install Firebase CLI: `npm install -g firebase-tools`
2. Run `firebase init` and select Hosting
3. Build folder: current directory (where `index.html` lives)
4. Deploy: `firebase deploy`

Your app is live at `https://YOUR_PROJECT.firebaseapp.com`

**Advantages**: Google's infrastructure, generous free tier
**Disadvantages**: Requires Google account and setup

---

## Custom Domain

### With GitHub Pages

1. Buy a domain from a registrar (GoDaddy, Namecheap, Google Domains, etc.)
2. In your repository **Settings → Pages**, under "Custom domain", enter your domain:
   - Example: `kyn-lux.com` or `health.yourdomain.com`
3. GitHub will create a `CNAME` file in your repository
4. In your domain registrar's DNS settings, add:
   - **CNAME record**: `your_username.github.io` → your custom domain
   - (Or follow your registrar's specific GitHub Pages instructions)
5. Wait 24 hours for DNS to propagate
6. Test: Visit `https://your-domain.com`

### With Netlify

1. In Netlify site settings, go to **Domain management**
2. Click **"Add custom domain"**
3. Enter your domain
4. Netlify generates a DNS setup instruction
5. Add the DNS records to your registrar
6. Wait for propagation (usually <1 hour)

### With Vercel

Same as Netlify — Vercel guides you through DNS setup after you add the domain.

---

## Security & Best Practices

### Enabling HTTPS
- ✅ **GitHub Pages**: Automatic (free SSL certificate included)
- ✅ **Netlify**: Automatic (free SSL certificate via Let's Encrypt)
- ✅ **Vercel**: Automatic (free SSL certificate)

All modern hosts provide HTTPS out of the box. No additional setup needed.

### Content Security Policy (CSP)

If you're concerned about security, you can add CSP headers. For static hosting:

**GitHub Pages**: Add this to your `index.html` `<head>`:
```html
<meta http-equiv="Content-Security-Policy" 
      content="default-src 'self'; 
               script-src 'self' 'unsafe-inline' https://fonts.googleapis.com; 
               style-src 'self' 'unsafe-inline' https://fonts.googleapis.com;
               font-src https://fonts.gstatic.com;
               img-src 'self' data:;">
```

This prevents:
- Inline script injection
- External script loading (except Google Fonts, which is required)
- Unsafe inline styles (except necessary ones)

### Subresource Integrity (SRI)

If loading external scripts, always use SRI hashes. Example:
```html
<link rel="stylesheet" href="https://fonts.googleapis.com/..."
      integrity="sha384-..." crossorigin="anonymous">
```

KYN Lux doesn't use external scripts (all embedded), so this isn't critical, but it's best practice.

### Data Privacy

- ✅ **No user tracking**: All metrics are local (localStorage)
- ✅ **No cookies**: Except those you explicitly set
- ✅ **Weather data only**: OpenMeteo API fetches cloud cover and UV (no personal data)
- ✅ **No third-party services**: No Google Analytics, Mixpanel, Sentry, etc.

If you ever add analytics, disclose it in your Privacy Policy.

### Backups

GitHub automatically backs up your code. For additional safety:
```bash
git clone --mirror https://github.com/YOUR_USERNAME/kyn-lux.git kyn-lux.backup.git
```

---

## Version Management

### Semantic Versioning

KYN Lux uses semantic versioning: **MAJOR.MINOR.PATCH**

- **Major** (4.x): Breaking UI changes, new features
- **Minor** (x.5): New features, improvements
- **Patch** (x.x.1): Bug fixes, minor tweaks

When deploying a new version:

1. Update version in top of `index.html`:
   ```html
   <!-- KYN Lux v4.5.1 -->
   ```

2. Update `CHANGELOG.md` with changes

3. Commit and push:
   ```bash
   git commit -m "Release: v4.5.1"
   git tag v4.5.1
   git push origin main
   git push origin v4.5.1
   ```

4. Create a GitHub Release:
   - Go to **Releases** tab
   - Click **"Create a new release"**
   - Tag: `v4.5.1`
   - Title: `KYN Lux v4.5.1`
   - Description: Summary from CHANGELOG

---

## Monitoring & Maintenance

### Check Deployment Status
- **GitHub Pages**: [github.com/YOUR_USERNAME/kyn-lux/deployments](https://github.com/YOUR_USERNAME/kyn-lux/deployments)
- **Netlify**: Dashboard shows deployment status and history
- **Vercel**: Dashboard shows build status and analytics

### Test on Real Devices

Always test on:
- ✅ iPhone (Safari, PWA installed)
- ✅ Android (Chrome, PWA installed)
- ✅ Desktop (Chrome, Safari, Firefox)

### Monitor Performance

- Use **WebPageTest** or **PageSpeed Insights** to check load times
- KYN Lux should load in <1 second (it's a single file)
- Monitor with: `curl -I https://your-domain.com/`

---

## Troubleshooting Deployment

### "404 Not Found"
- Check repository is **Public** (GitHub Pages requires this)
- Verify `index.html` is in the root of the repository (not in a subfolder)
- Check Pages settings point to `main` branch, `/ (root)` folder
- Wait 5–10 minutes after enabling Pages (first deploy is slow)

### "Site not updating"
- Clear browser cache (Cmd+Shift+Delete)
- Hard refresh on mobile (Cmd+Option+R on Safari)
- GitHub deploying? Check deployment status in Settings → Pages

### "HTTPS showing certificate error"
- GitHub Pages: Wait 24 hours after enabling custom domain
- Other hosts: Contact their support (usually <1 hour to resolve)

### "Custom domain not working"
- DNS propagation takes 1–48 hours (usually <1 hour)
- Check DNS records are correct: use `nslookup` or `dig`
  ```bash
  nslookup kyn-lux.com
  ```
- Verify CNAME record points to GitHub Pages server

---

## Next Steps

1. ✅ Create GitHub repo
2. ✅ Upload files
3. ✅ Enable GitHub Pages
4. ✅ Test on iPhone
5. 🔧 Add custom domain (optional)
6. 📢 Share your app!

---

**Version**: 4.5  
**Last Updated**: April 2026
