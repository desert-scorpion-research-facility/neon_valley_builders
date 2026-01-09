# GitHub Pages Deployment Checklist

Follow these steps to deploy your Neon Valley Builders website to GitHub Pages.

## ✅ Pre-Deployment Checklist

### 1. Add Your Real Images
- [ ] Replace placeholder images in `/public/images/` with your actual project photos
- [ ] Name them consistently (e.g., bbq1.jpg, bbq2.jpg, fireplace1.jpg, etc.)
- [ ] Optimize images for web (recommended: max 1200px wide, compressed)

### 2. Update Business Information
- [ ] Edit `/src/pages/contact.astro` with your real:
  - Phone number
  - Email address
  - Business hours
  - Service area

### 3. Configure for Your GitHub Account
- [ ] Open `astro.config.mjs`
- [ ] Replace `your-username` with YOUR GitHub username
- [ ] Replace `neon_valley_builders` with YOUR repository name (if different)

Example:
```js
export default defineConfig({
  site: 'https://john-doe.github.io',  // Your GitHub username
  base: '/my-construction-site',        // Your repo name
});
```

## 🚀 Deployment Steps

### Step 1: Create GitHub Repository
1. Go to https://github.com/new
2. Repository name: `neon_valley_builders` (or your choice)
3. Make it **Public**
4. **DO NOT** check "Add a README file"
5. Click "Create repository"

### Step 2: Initialize Git and Push
Open terminal in your project folder and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: Neon Valley Builders website"

# Rename branch to main
git branch -M main

# Add your GitHub repository as remote
# REPLACE with your actual GitHub username and repo name
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Push to GitHub
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Click **Pages** (left sidebar)
4. Under "Build and deployment":
   - **Source**: Select "GitHub Actions"
5. The deployment will start automatically!

### Step 4: Wait for Deployment
1. Go to the **Actions** tab in your repository
2. You'll see a workflow running called "Deploy to GitHub Pages"
3. Wait for it to complete (usually 2-3 minutes)
4. Once done, your site is live!

### Step 5: Access Your Site
Your website will be available at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

Example: `https://john-doe.github.io/neon_valley_builders/`

## 🔄 Making Updates

After your initial deployment, to update your site:

```bash
# Make your changes to files
# Then:

git add .
git commit -m "Description of your changes"
git push
```

GitHub Actions will automatically rebuild and redeploy your site!

## 🐛 Troubleshooting

### Site shows 404 error
- Check that GitHub Pages is enabled in Settings → Pages
- Verify the `site` and `base` in `astro.config.mjs` match your GitHub username and repo name
- Wait a few minutes after the first deployment

### Images not showing
- Ensure images are in `/public/images/` folder
- Check image file names match the paths in your `.astro` files
- Remember: image paths should start with `/images/...`

### Deployment fails
- Check the "Actions" tab for error messages
- Ensure your repository is public
- Verify Node.js and npm are working locally

## 📱 Testing Locally First

Before deploying, test your site locally:

```bash
# Start development server
npm run dev

# Build and preview production version
npm run build
npm run preview
```

Visit `http://localhost:4321/` to see your site.

## 💡 Tips

- **Custom Domain**: You can use a custom domain! See [GitHub Pages docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- **SSL/HTTPS**: GitHub Pages provides free SSL automatically
- **Analytics**: Consider adding Google Analytics or similar
- **SEO**: Each page has meta descriptions - customize them!

---

Need help? Check the main README.md file!
