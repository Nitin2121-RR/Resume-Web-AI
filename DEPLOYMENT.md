# Deployment Guide for Vercel

## Method 1: Deploy via Vercel Dashboard (Easiest)

### Step 1: Prepare Your Files
Make sure you have these files in your project folder:
- index.html
- style.css
- script.js
- vercel.json
- .gitignore
- README.md

### Step 2: Create a GitHub Repository
1. Go to [GitHub](https://github.com)
2. Click "New Repository"
3. Name it: `portfolio` or `nitin-portfolio`
4. Make it Public
5. Don't initialize with README (we already have one)
6. Click "Create Repository"

### Step 3: Push Your Code to GitHub
Open your terminal in the project folder and run:

```bash
git init
git add .
git commit -m "Initial commit: Portfolio website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

### Step 4: Deploy on Vercel
1. Go to [Vercel](https://vercel.com)
2. Sign up/Login with GitHub
3. Click "Add New Project"
4. Import your GitHub repository
5. Configure:
   - Framework Preset: Other
   - Root Directory: ./
   - Build Command: (leave empty)
   - Output Directory: (leave empty)
6. Click "Deploy"
7. Wait 1-2 minutes for deployment
8. Your site will be live at: `your-project-name.vercel.app`

## Method 2: Deploy via Vercel CLI

### Step 1: Install Vercel CLI
```bash
npm install -g vercel
```

### Step 2: Login to Vercel
```bash
vercel login
```

### Step 3: Deploy
In your project folder, run:
```bash
vercel
```

Follow the prompts:
- Set up and deploy? Yes
- Which scope? (Select your account)
- Link to existing project? No
- Project name? (Press Enter for default)
- In which directory is your code? ./
- Want to override settings? No

### Step 4: Deploy to Production
```bash
vercel --prod
```

## Method 3: Drag and Drop (Quickest)

1. Go to [Vercel](https://vercel.com)
2. Sign up/Login
3. Click "Add New Project"
4. Click "Browse" or drag your project folder
5. Wait for upload and deployment
6. Done!

## Custom Domain (Optional)

1. Go to your project on Vercel
2. Click "Settings" → "Domains"
3. Add your custom domain
4. Follow DNS configuration instructions

## Updating Your Site

### Via GitHub:
```bash
git add .
git commit -m "Update portfolio"
git push
```
Vercel will automatically redeploy!

### Via CLI:
```bash
vercel --prod
```

## Troubleshooting

### Issue: Files not loading
- Check that all file paths are relative (no leading /)
- Verify vercel.json is in the root directory

### Issue: Styles not applying
- Clear browser cache (Ctrl + Shift + R)
- Check CSS file path in index.html

### Issue: Deployment failed
- Check .gitignore doesn't exclude necessary files
- Ensure all files are committed to Git

## Your Live URLs
After deployment, you'll get:
- Preview: `your-project-name-hash.vercel.app`
- Production: `your-project-name.vercel.app`

## Need Help?
- Vercel Docs: https://vercel.com/docs
- Vercel Support: https://vercel.com/support

---

Good luck with your deployment! 🚀
