# Render Deployment Guide for TzurGroup Website

## 🚀 Quick Deployment Steps

### 1. Create GitHub Repository
```bash
# If you haven't already, create a GitHub repository
# Go to github.com and create a new repository named "tzurgroup-website"
```

### 2. Push to GitHub
```bash
# Add your GitHub repository as remote origin
git remote add origin https://github.com/shofalitto/tzurgroup-website.git

# Push your code to GitHub
git branch -M main
git push -u origin main
```

### 3. Deploy to Render

1. **Go to [render.com](https://render.com)**
2. **Sign up/Login** with your GitHub account
3. **Click "New +"** → **"Static Site"**
4. **Connect your GitHub repository**
5. **Configure deployment:**
   - **Name**: `tzurgroup-website`
   - **Branch**: `main`
   - **Root Directory**: Leave empty (or `/`)
   - **Build Command**: Leave empty
   - **Publish Directory**: Leave empty
6. **Click "Create Static Site"**

### 4. Custom Domain (Optional)
- Go to your site settings
- Add your custom domain
- Update DNS records as instructed

---

## 📁 File Structure for Render

Your repository should have this structure:
```
tzurgroup-website/
├── index.html              # Main homepage
├── contact.html            # Contact page
├── README.md              # Project documentation
├── EMAIL_SETUP_GUIDE.md   # Email setup instructions
├── RENDER_DEPLOYMENT_GUIDE.md # This file
└── .gitignore             # Git ignore rules
```

---

## ⚙️ Render Configuration

### Static Site Settings
- **Build Command**: (leave empty)
- **Publish Directory**: (leave empty)
- **Environment**: Static Site
- **Auto-Deploy**: Yes (recommended)

### Environment Variables (if needed)
- No environment variables required for basic setup
- Add `FORMSPREE_ID` if you want to use environment variables for form IDs

---

## 🔧 Post-Deployment Setup

### 1. Set Up Contact Forms
1. **Go to [formspree.io](https://formspree.io)**
2. **Create account and new form**
3. **Get your form ID**
4. **Update HTML files:**
   ```html
   <!-- Replace YOUR_FORM_ID with your actual Formspree ID -->
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
5. **Commit and push changes:**
   ```bash
   git add .
   git commit -m "Add Formspree form ID"
   git push
   ```

### 2. Test Your Live Site
1. **Visit your Render URL** (e.g., `https://tzurgroup-website.onrender.com`)
2. **Test the contact form**
3. **Check that emails are received**

---

## 🎯 Render URL Structure

Your deployed site will be available at:
- **Main site**: `https://tzurgroup-website.onrender.com`
- **Contact page**: `https://tzurgroup-website.onrender.com/contact.html`

---

## 💰 Render Pricing

### Free Tier
- ✅ **Free static site hosting**
- ✅ **Custom domains**
- ✅ **Automatic deployments**
- ✅ **HTTPS included**
- ❌ **Sleeps after 15 minutes of inactivity** (wakes up on next visit)

### Paid Plans
- **Starter**: $7/month - Always awake, faster builds
- **Professional**: $25/month - Team features, priority support

---

## 🔄 Continuous Deployment

Once set up, any changes you push to GitHub will automatically deploy to Render:

```bash
# Make changes to your files
# Then commit and push
git add .
git commit -m "Update website content"
git push
# Render will automatically rebuild and deploy
```

---

## 🛠️ Troubleshooting

### Common Issues

1. **Site not loading**
   - Check that `index.html` is in the root directory
   - Verify the build completed successfully

2. **Contact form not working**
   - Ensure Formspree ID is correctly set
   - Check that form action URL is correct

3. **Styling issues**
   - Verify all CSS is embedded in HTML files
   - Check browser console for errors

### Support
- **Render Documentation**: [render.com/docs](https://render.com/docs)
- **Render Support**: Available in dashboard

---

## ✅ Deployment Checklist

- [ ] GitHub repository created
- [ ] Code pushed to GitHub
- [ ] Render account created
- [ ] Static site deployed on Render
- [ ] Custom domain configured (optional)
- [ ] Formspree account set up
- [ ] Contact forms tested
- [ ] Site tested on mobile devices

---

## 🎉 You're Live!

Once deployed, your TzurGroup website will be live and accessible worldwide. The contact forms will work (after Formspree setup), and you'll have a professional online presence for your global social risk protection services.

**Your live URL will be**: `https://tzurgroup-website.onrender.com`
