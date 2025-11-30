# MOCVIEW Legal Documents - GitHub Pages Site

**Domain:** https://legal.mocview.com  
**Repository:** https://github.com/mocview-app/mocview-legal  
**Status:** Ready for deployment

---

## 🚀 Quick Start (30 Minutes to Live Site)

### Step 1: Create GitHub Repository (5 minutes)

1. Go to: https://github.com/organizations/mocview-app/repositories/new
2. Repository name: `mocview-legal`
3. Visibility: **Public** (required for free GitHub Pages)
4. **DO NOT** initialize with README (you'll upload these files)
5. Click **Create repository**

### Step 2: Upload These Files (2 minutes)

**Option A: Web Upload (Easier)**
1. On the new repository page, click **uploading an existing file**
2. Drag ALL files and folders from this directory
3. Commit message: "Initial commit - Legal documents"
4. Click **Commit changes**

**Option B: Git Command Line**
```bash
cd mocview-legal
git init
git add .
git commit -m "Initial commit - Legal documents"
git branch -M main
git remote add origin https://github.com/mocview-app/mocview-legal.git
git push -u origin main
```

### Step 3: Enable GitHub Pages (1 minute)

1. Go to repository **Settings**
2. Scroll to **Pages** (in left sidebar)
3. Under **Source**, select:
   - Branch: **main**
   - Folder: **/ (root)**
4. Click **Save**
5. ✅ You'll see: "Your site is ready to be published at https://mocview-app.github.io/mocview-legal/"

### Step 4: Configure Custom Domain (5 minutes)

Still in Settings > Pages:

1. Under **Custom domain**, enter: `legal.mocview.com`
2. Click **Save**
3. ✅ GitHub will verify the CNAME file
4. Wait 1-2 minutes, then check **Enforce HTTPS** (enables free SSL certificate)

### Step 5: Configure Namecheap DNS (5 minutes)

1. Log in to Namecheap: https://www.namecheap.com/myaccount/login/
2. Go to **Domain List** > click **Manage** next to mocview.com
3. Go to **Advanced DNS** tab
4. Click **Add New Record**
5. Configure:
   - **Type:** CNAME Record
   - **Host:** legal
   - **Value:** mocview-app.github.io.
   - **TTL:** Automatic
6. Click **Save All Changes** (green checkmark)

### Step 6: Wait for DNS Propagation (5-30 minutes)

**Check progress:**
```bash
# Mac/Linux Terminal
dig legal.mocview.com

# Or use online tool
https://dnschecker.org/#CNAME/legal.mocview.com
```

**Expected result:**
```
legal.mocview.com. 300 IN CNAME mocview-app.github.io.
```

### Step 7: Verify SSL Certificate (5 minutes)

1. Go back to GitHub: Settings > Pages
2. Wait until you see: ✅ **"Your site is published at https://legal.mocview.com"**
3. Check **Enforce HTTPS** is enabled
4. Visit: https://legal.mocview.com
5. Verify green padlock 🔒 in browser

---

## ✅ Success Checklist

After deployment, verify these URLs work:

- [ ] https://legal.mocview.com (Home page with gradient)
- [ ] https://legal.mocview.com/privacy (Privacy Policy)
- [ ] https://legal.mocview.com/terms (Terms of Service)
- [ ] Green padlock 🔒 on all pages (HTTPS enabled)
- [ ] Mobile responsive (test on phone)
- [ ] Print functionality works

---

## 📁 Site Structure

```
mocview-legal/
├── CNAME                        # Custom domain configuration
├── README.md                    # This file
├── index.html                   # Home page (gradient design)
│
├── privacy/
│   └── index.html              # Privacy Policy
│
├── terms/
│   └── index.html              # Terms of Service (to be created)
│
└── assets/
    ├── css/
    │   └── style.css           # Gradient styling
    └── images/
        └── (future logo files)
```

---

## 🎨 Design Features

**Matching your existing site aesthetic:**
- Gradient background: Red → Orange → Yellow-Orange → Pink
- MOCVIEW logo with spaced letters (M O C  V I E W)
- White text on gradient
- Clean, modern card design
- Mobile responsive
- Print-friendly legal documents

**Colors Used:**
- Primary Red: #D32F2F (brand color from logo)
- Orange: #FF6B35
- Yellow-Orange: #FFB347
- Pink: #FF1493

---

## 🔗 URLs for LinkedIn OAuth App

**Once site is live, use these URLs:**

**Privacy Policy:**
```
https://legal.mocview.com/privacy
```

**Terms of Service:**
```
https://legal.mocview.com/terms
```

---

## 🔧 Updating Legal Documents

### Option 1: GitHub Web Interface (Easier)

1. Go to: https://github.com/mocview-app/mocview-legal
2. Navigate to file (e.g., `privacy/index.html`)
3. Click **Edit** (pencil icon)
4. Make changes
5. Scroll down, add commit message
6. Click **Commit changes**
7. Changes live in ~30 seconds

### Option 2: Git Command Line

```bash
cd mocview-legal
# Edit files locally
git add .
git commit -m "Update privacy policy"
git push
# Changes live in ~30 seconds
```

---

## 📊 GitHub Pages Features

**What you get for FREE:**
- Unlimited bandwidth
- Free SSL certificate (HTTPS)
- Automatic deployment (push to deploy)
- Custom domain support
- 99.9% uptime (GitHub infrastructure)
- Global CDN (fast worldwide)

**Limitations:**
- Must be public repository
- 1GB repository size limit (plenty for documents)
- 100GB bandwidth/month (more than enough)
- 10 builds/hour (you won't hit this)

---

## 🆘 Troubleshooting

### Issue: Custom domain not working

**Check:**
1. CNAME file contains exactly: `legal.mocview.com`
2. Namecheap DNS has CNAME record: `legal` → `mocview-app.github.io.`
3. Wait 30 minutes for DNS propagation
4. Try incognito/private browsing (cache issue)

**Test DNS:**
```bash
dig legal.mocview.com
# Should show CNAME pointing to mocview-app.github.io
```

### Issue: SSL certificate not provisioning

**Check:**
1. DNS propagation complete (use dnschecker.org)
2. "Enforce HTTPS" enabled in Settings > Pages
3. Wait 5-10 minutes after DNS propagation
4. Try disabling and re-enabling "Enforce HTTPS"

### Issue: 404 errors on subpages

**Check:**
1. Folder structure is correct (`privacy/index.html` not `privacy.html`)
2. Files uploaded correctly
3. Clear browser cache
4. Use trailing slash: `legal.mocview.com/privacy/`

---

## 🔄 Future Migration to Next.js

**This is a temporary solution** (perfect for now).

**Migration plan (Sprint 2-3):**
1. Build full marketing site in Next.js
2. Deploy to Vercel (like existing site)
3. Move legal docs to Next.js routes
4. Update DNS: `legal.mocview.com` → redirect to `mocview.com/privacy`
5. Keep this GitHub Pages as backup/archive

**Until then:** This GitHub Pages site is:
- ✅ Production-ready
- ✅ Zero cost
- ✅ Zero maintenance
- ✅ Perfect for LinkedIn OAuth

---

## 📞 Support

**Questions about deployment?**

**GitHub Pages Documentation:**
- https://docs.github.com/pages

**DNS Help:**
- Namecheap: https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages

**MOCVIEW Internal:**
- Scrum Master: Claude.ai Desktop
- Legal: legal@mocview.com

---

## 📝 Maintenance

**No regular maintenance required!**

**When to update:**
- Legal document changes (annual review)
- Contact information changes
- Adding new documents
- Branding updates

**How to update:**
1. Edit HTML files directly in GitHub
2. Commit changes
3. Live in 30 seconds

---

## ✅ Post-Deployment Tasks

Once site is live:

1. **Test all URLs** (home, privacy, terms)
2. **Test on mobile** (iOS and Android)
3. **Test print functionality**
4. **Verify SSL certificate** (green padlock)
5. **Update LinkedIn OAuth app** with legal URLs
6. **Inform team** that legal docs are live
7. **Add to Sprint 1 completion checklist** ✅

---

## 🎉 You're Done!

**Your legal documents are now live at:**
- https://legal.mocview.com

**Total deployment time:** ~30 minutes  
**Total cost:** $0 (FREE forever)  
**Maintenance:** Zero

**Ready for LinkedIn OAuth app creation!** 🚀

---

**Created:** November 30, 2025  
**For:** MOCVIEW Sprint 1  
**Status:** Production-ready
