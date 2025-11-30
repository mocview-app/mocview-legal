# MOCVIEW Legal Site - Deployment Checklist

**Target Completion:** 30-60 minutes  
**Domain:** https://legal.mocview.com  
**Status:** ⬜ Not Started

---

## ✅ Pre-Deployment (Already Complete)

- [x] Legal documents finalized
- [x] HTML files created with gradient design
- [x] CSS styling matching main site
- [x] CNAME file configured
- [x] README with instructions
- [x] All files ready in `/mnt/user-data/outputs/mocview-legal/`

---

## 📦 Step 1: Create GitHub Repository (5 min)

- [ ] Go to https://github.com/organizations/mocview-app/repositories/new
- [ ] Repository name: `mocview-legal`
- [ ] Visibility: **Public** ✅
- [ ] Do NOT initialize with README
- [ ] Click **Create repository**
- [ ] Copy repository URL: `https://github.com/mocview-app/mocview-legal.git`

**Estimated time:** 5 minutes  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## 📤 Step 2: Upload Files to GitHub (2 min)

**Method chosen:** 
- [ ] Web Upload (easier) 
- [ ] Git Command Line

### If using Web Upload:
- [ ] Click "uploading an existing file"
- [ ] Drag all files from `mocview-legal/` folder
- [ ] Commit message: "Initial commit - Legal documents"
- [ ] Click **Commit changes**
- [ ] Verify all files uploaded (check file tree)

### If using Git Command Line:
```bash
cd /path/to/mocview-legal
git init
git add .
git commit -m "Initial commit - Legal documents"
git branch -M main
git remote add origin https://github.com/mocview-app/mocview-legal.git
git push -u origin main
```

**Files to verify uploaded:**
- [ ] CNAME
- [ ] README.md
- [ ] index.html
- [ ] privacy/index.html
- [ ] assets/css/style.css

**Estimated time:** 2 minutes  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## 🌐 Step 3: Enable GitHub Pages (1 min)

- [ ] Go to repository **Settings**
- [ ] Click **Pages** in left sidebar
- [ ] Under **Source**:
  - [ ] Branch: **main**
  - [ ] Folder: **/ (root)**
- [ ] Click **Save**
- [ ] Wait for confirmation message
- [ ] Note the temporary URL: `https://mocview-app.github.io/mocview-legal/`

**Estimated time:** 1 minute  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## 🔧 Step 4: Configure Custom Domain (5 min)

**In GitHub (Settings > Pages):**
- [ ] Under **Custom domain**, enter: `legal.mocview.com`
- [ ] Click **Save**
- [ ] Wait for DNS check (1-2 minutes)
- [ ] Verify CNAME file was recognized
- [ ] Check **Enforce HTTPS** (wait if grayed out)

**Estimated time:** 5 minutes  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## 🌍 Step 5: Configure Namecheap DNS (5 min)

- [ ] Log in to Namecheap: https://www.namecheap.com/myaccount/login/
- [ ] Dashboard → **Domain List**
- [ ] Find **mocview.com** → Click **Manage**
- [ ] Go to **Advanced DNS** tab
- [ ] Click **Add New Record**

**New Record Settings:**
- [ ] Type: **CNAME Record**
- [ ] Host: `legal`
- [ ] Value: `mocview-app.github.io.`
- [ ] TTL: **Automatic**

- [ ] Click **Save All Changes** (green checkmark)
- [ ] Verify record appears in list

**Estimated time:** 5 minutes  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## ⏱️ Step 6: Wait for DNS Propagation (5-30 min)

**Start time:** __________  
**Check every:** 5 minutes

**Test DNS propagation:**
- [ ] Use online tool: https://dnschecker.org/#CNAME/legal.mocview.com
- [ ] Or terminal: `dig legal.mocview.com`

**Expected result:**
```
legal.mocview.com. 300 IN CNAME mocview-app.github.io.
```

**Progress:**
- [ ] 5 min - Check 1: ⬜ Propagated | ⬜ Not yet
- [ ] 10 min - Check 2: ⬜ Propagated | ⬜ Not yet
- [ ] 15 min - Check 3: ⬜ Propagated | ⬜ Not yet
- [ ] 20 min - Check 4: ⬜ Propagated | ⬜ Not yet
- [ ] 30 min - Check 5: ⬜ Propagated | ⬜ Not yet

**Estimated time:** 5-30 minutes (usually 5-10)  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## 🔒 Step 7: Verify SSL Certificate (5 min)

- [ ] Go to GitHub: Settings > Pages
- [ ] Verify message: ✅ "Your site is published at https://legal.mocview.com"
- [ ] Verify **Enforce HTTPS** is checked
- [ ] Visit https://legal.mocview.com
- [ ] Verify green padlock 🔒 in browser
- [ ] Click padlock → Verify certificate is valid

**If HTTPS not enabled:**
- [ ] Wait 5 more minutes (certificate provisioning)
- [ ] Try unchecking and rechecking "Enforce HTTPS"
- [ ] Clear browser cache and retry

**Estimated time:** 5 minutes  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## ✅ Step 8: Final Verification (10 min)

**Test all URLs work:**
- [ ] https://legal.mocview.com (Home page)
- [ ] https://legal.mocview.com/privacy (Privacy Policy)
- [ ] https://legal.mocview.com/terms (Terms of Service - when created)

**Test functionality:**
- [ ] Navigation links work (home ↔ privacy ↔ terms)
- [ ] Gradient background displays correctly
- [ ] MOCVIEW logo displays correctly
- [ ] Document cards are clickable
- [ ] Footer information is correct
- [ ] Email links work (privacy@mocview.com, legal@mocview.com)

**Test responsive design:**
- [ ] Desktop view (Chrome)
- [ ] Desktop view (Safari)
- [ ] Desktop view (Firefox)
- [ ] Mobile view (iPhone/iOS)
- [ ] Mobile view (Android)
- [ ] Tablet view (iPad)

**Test print functionality:**
- [ ] Privacy Policy prints correctly
- [ ] Terms prints correctly
- [ ] Print styles applied (no gradient, black text)

**Test SSL/Security:**
- [ ] Green padlock on all pages
- [ ] Certificate valid (not expired)
- [ ] No mixed content warnings
- [ ] HTTPS redirects work

**Estimated time:** 10 minutes  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## 📋 Step 9: Update LinkedIn OAuth App (5 min)

**Now that legal docs are live, update LinkedIn app:**

- [ ] Go to LinkedIn Developer Portal
- [ ] Open MOCVIEW app settings
- [ ] Update **Privacy Policy URL**: `https://legal.mocview.com/privacy`
- [ ] Update **Terms of Service URL**: `https://legal.mocview.com/terms`
- [ ] Save changes
- [ ] Test OAuth flow

**Estimated time:** 5 minutes  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## 📢 Step 10: Announce & Document (5 min)

- [ ] Notify team legal docs are live
- [ ] Update Sprint 1 checklist: ✅ Legal documents hosted
- [ ] Add URLs to project documentation
- [ ] Take screenshots for records
- [ ] Update Scrum Master on completion

**Announcement template:**
```
✅ MOCVIEW Legal Documents Now Live!

Privacy Policy: https://legal.mocview.com/privacy
Terms of Service: https://legal.mocview.com/terms

Ready for LinkedIn OAuth integration.
```

**Estimated time:** 5 minutes  
**Status:** ⬜ Not Started | ⬜ In Progress | ⬜ Complete

---

## 📊 Deployment Summary

**Total estimated time:** 30-60 minutes  
**Actual time taken:** __________ minutes

**Date started:** __________  
**Date completed:** __________

**Final URLs:**
- Home: https://legal.mocview.com
- Privacy: https://legal.mocview.com/privacy
- Terms: https://legal.mocview.com/terms

**GitHub Repository:** https://github.com/mocview-app/mocview-legal

**Status:** 
- ⬜ Not Started
- ⬜ In Progress
- ⬜ Completed Successfully
- ⬜ Issues Encountered (document below)

---

## ⚠️ Issues & Resolutions

**If any issues occurred, document here:**

| Issue | Solution | Time Lost |
|-------|----------|-----------|
|       |          |           |
|       |          |           |

---

## 🎉 Success Criteria (All must be ✅)

- [ ] GitHub repository created
- [ ] All files uploaded successfully
- [ ] GitHub Pages enabled
- [ ] Custom domain configured
- [ ] Namecheap DNS updated
- [ ] DNS propagated successfully
- [ ] SSL certificate provisioned
- [ ] HTTPS enforced on all pages
- [ ] All URLs work correctly
- [ ] Mobile responsive verified
- [ ] Print functionality works
- [ ] LinkedIn OAuth URLs updated
- [ ] Team notified

---

## 🔄 Next Steps After Deployment

- [ ] Monitor DNS for 24 hours (ensure stability)
- [ ] Test OAuth flow with LinkedIn
- [ ] Continue Sprint 1 authentication implementation
- [ ] Plan Next.js migration for Sprint 2-3

---

**Deployment Status:** ⬜ Ready to Deploy

**Deployed by:** __________  
**Verified by:** __________  
**Date:** __________

---

**✅ DEPLOYMENT COMPLETE!**

Legal documents live at: https://legal.mocview.com
